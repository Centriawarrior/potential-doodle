# Logbook

| Date       | Used hours |                       Subject(s)                        |                                     output                                      |
| :--------- | :--------: | :-----------------------------------------------------: | :-----------------------------------------------------------------------------: |
| 30.10.2024 |     2      |              lecture 1 → Kick-off lecture               |               Watched lecture and explored Itslearning materials                |
| 31.10.2024 |     1      |        Exercise: Link to the Git repo + Logbook         |                            Added link to Itslearning                            |
| 31.10.2024 |     1      | My knowledge check and cisco course navigation tutorial |                              Passed test with 79%                               |
| 1.11.2024  |     1      |         Module 1: Introduction to Cybersecurity         |                               Passed Module quiz                                |
| 4.11.2024  |     2      | lecture 2 → Introduction to the PortSwigger environment |              Watched lecture and registered account to Portswigger              |
| 6.11.2024  |     1      |         Module 2: Introduction to Cybersecurity         |                               Passed Module quiz                                |
| 6.11.2024  |     1      |         Module 3: Introduction to Cybersecurity         |                               Passed Module quiz                                |
| 7.11.2024  |     1      |         Module 4: Introduction to Cybersecurity         |                               Passed Module quiz                                |
| 7.11.2024  |     1      |         Module 5: Introduction to Cybersecurity         |                               Passed Module quiz                                |
| 7.11.2024  |     2      |                    Course Final Exam                    |                           Passed Final Exam with 97%                            |
| 10.11.2024 |     2      |                       Portswigger                       |        Explored the environment and got motivated to study and pass labs        |
| 11.11.2024 |     2      |            lecture 3 → Starting the project             |               Watched lecture and brainstormed ideas for project                |
| 12.11.2024 |     1      |                 Portswigger first labs                  |                      Solved first 3 APPRENTICE level labs                       |
| 16.11.2024 |     3      |                 Booking system phase 1                  |            Downloaded Docker and Deno. Created structure for phase 1            |
| 18.11.2024 |     2      |            lecture 4 → The project continues            |                   Watched lecture and went through assignment                   |
| 24.11.2024 |     2      |              Booking system phase 1 final               |     Fixed issues with zap and registrations with the help of lecture videos     |
| 25.11.2024 |     4      |                        lecture 5                        |    Watched lecture and brainstormed ideas for index and login pages with AI     |
| 26.11.2024 |     2      |                    Continued project                    |                  Ran first tests with Zap and analyzed alerts                   |
| 26.11.2024 |     2      |                  more Portswigger labs                  |                              Completed 3 more labs                              |
| 01.12.2024 |     3      |                     week 4 homework                     |    Modified booking system until passed without errors and returned logbook     |
| 03.12.2024 |     4      |          week 5 homework and more portswigger           |        Performed wider report of system and did more labs in portswigger        |
| 08.12.2024 |     2      |                         week 5                          | Wrote whats wrong based on zap report with system and pushed code to the github |

# Weekly breakdown about project

## Week 3:

Link to first report: https://github.com/Centriawarrior/potential-doodle/blob/main/Registration_page_first_test.md

Eliminated input handling vulnerabilities like Path Traversal and SQL Injection etc.

Link to the second report: https://github.com/Centriawarrior/potential-doodle/blob/main/Registration_page_second_test.md

## Week 4:

Link to the first report before knowing about potential errors:
https://github.com/Centriawarrior/potential-doodle/blob/main/index-login-registration-first-test.md

What has been done between reports:
Enhanced Security:

- Added implements like `Content-Security-Policy`, `X-Frame-Options`, and `X-Content-Type-Options` to protect against clickjacking and MIME sniffing.
  Better Routing:
- Explicit routing logic for `GET` and `POST` requests across multiple endpoints (`/`, `/register`, `/login`), enhancing readability and scalability.
  Middleware Introduction:
- Global middleware (`addSecurityHeaders`) centralizes security measures, ensuring all responses are protected.

Link to the second report after fixing errors:
https://github.com/Centriawarrior/potential-doodle/blob/main/index-login-registration-second-test.md)

## Week 5:

Performed a security check of the booking system using ZAPs manual Explore.
Link to the report:
https://github.com/Centriawarrior/potential-doodle/blob/main/tests/fullsystemfirsttest.md

Based on the ZAP report, five most critical points to address in booking system:

---

### 1. **Format String Error**

- **What is wrong?**
  - A format string error was identified in the `POST` request to `http://localhost:8000/resources`. The parameter `resource_name` was found vulnerable to a format string attack.
- **How did I find it?**
  - ZAP flagged this issue as a `Medium` risk. The parameter accepts unsanitized user input, which could be evaluated as a command.
- **How should it work/What should be fixed?**
  - Validate and sanitize all user inputs to ensure they are free from format string tokens. Avoid using user inputs directly in string formatting functions. Use libraries or methods designed to safely handle string inputs.

---

### 2. **Cross-Site Scripting (XSS) - Persistent in JSON Responses**

- **What is wrong?**
  - Two instances of XSS vulnerabilities were found in `GET` requests to `http://localhost:8000/resourcesList`. Parameters `resource_description` and `resource_name` allow script injection, e.g., `<script>alert(1);</script>`.
- **How did I find it?**
  - ZAP flagged these as `Low` risk but with significant potential for exploitation if developers or other components do not handle the JSON response safely.
- **How should it work/What should be fixed?**
  - Escape all output in JSON responses. Use libraries like OWASP's ESAPI Encoding module. Apply input validation and sanitation to ensure only expected characters are accepted. Ensure server-side validation mirrors client-side checks.

---

### 3. **Loosely Scoped Cookies**

- **What is wrong?**
  - Cookies were not scoped to a Fully Qualified Domain Name (FQDN), potentially allowing unintended access by subdomains.
- **How did I find it?**
  - ZAP flagged this in both `POST` (`http://localhost:8000/login`) and `GET` (`http://localhost:8000/logout`) requests.
- **How should it work/What should be fixed?**
  - Always set cookies with a `Path` and `Domain` attribute that limits their scope to specific subdomains. Add `HttpOnly` and `Secure` flags to cookies where applicable to prevent JavaScript access and ensure secure transmission.

---

### 4. **Suspicious Comments in the Code**

- **What is wrong?**
  - Comments in the HTML of `http://localhost:8000/reservation` exposed sensitive information, such as `<!-- Reserver username (pre-filled) -->`.
- **How did I find it?**
  - ZAP identified this as an `Informational` risk, but the exposed information could aid attackers in understanding application logic.
- **How should it work/What should be fixed?**
  - Remove all comments containing sensitive information or references to sensitive data structures. Use secure logging methods for debugging and ensure no sensitive details are present in production code.

---

### 5. **Session Management Tokens in Responses**

- **What is wrong?**
  - Session management tokens, such as `session_id`, were exposed in HTTP headers during `POST` and `GET` requests (`http://localhost:8000/login`).
- **How did I find it?**
  - ZAP highlighted this in `Session Management Response Identified` as an `Informational` alert. Exposing session identifiers increases the risk of session hijacking.
- **How should it work/What should be fixed?**
  - Tokens should only be transmitted in secure, encrypted cookies. Avoid exposing session identifiers in URLs or headers. Implement secure session management practices, such as using short-lived tokens and enforcing secure connections (`HTTPS`).

---

### Next Steps to the week 6:

1. Prioritize addressing the **Format String Error** and **XSS vulnerabilities**, as these could directly enable attacks.
2. Implement proper cookie management and session token handling to mitigate data leakage risks.
3. Conduct a review of the codebase to remove sensitive comments and improve adherence to secure coding standards.
