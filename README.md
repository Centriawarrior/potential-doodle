# Logbook

| Date       | Used hours |                             Subject(s)                             |                                                                output                                                                |
| :--------- | :--------: | :----------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------------------------------: |
| 30.10.2024 |     2      |                    lecture 1 → Kick-off lecture                    |                                          Watched lecture and explored Itslearning materials                                          |
| 31.10.2024 |     2      |              Exercise: Link to the Git repo + Logbook              |                                                      Added link to Itslearning                                                       |
| 1.11.2024  |     2      |              Module 1: Introduction to Cybersecurity               |                                                          Passed Module quiz                                                          |
| 4.11.2024  |     2      |               Lecture 2: Introduction to PortSwigger               |                                          Watched lecture, registered account on PortSwigger                                          |
| 6.11.2024  |     2      |              Module 2: Introduction to Cybersecurity               |                                                          Passed Module quiz                                                          |
| 6.11.2024  |     1      |              Module 3: Introduction to Cybersecurity               |                                                          Passed Module quiz                                                          |
| 7.11.2024  |     4      |            Module 4 & 5: Introduction to Cybersecurity             |                                                   Passed Module quizzes for 4 & 5                                                    |
| 7.11.2024  |     2      |                         Course Final Exam                          |                                                      Passed Final Exam with 97%                                                      |
| 10.11.2024 |     2      |                            PortSwigger                             |                                        Explored environment, motivated to study and pass labs                                        |
| 11.11.2024 |     3      |                  Lecture 3: Starting the Project                   |                                             Watched lecture, brainstormed project ideas                                              |
| 12.11.2024 |     1      |                       PortSwigger First Labs                       |                                                 Solved first 3 APPRENTICE level labs                                                 |
| 15.11.2024 |     1      |                    Study: Cybersecurity Basics                     |                                        Reviewed fundamental cybersecurity concepts and tools                                         |
| 16.11.2024 |     5      |                 Booking System Phase 1 & Lecture 4                 |                 Downloaded Docker and Deno, created structure for Phase 1; watched lecture, went through assignment                  |
| 17.11.2024 |     1      |                 Study: PortSwigger Lab Techniques                  |                                   Studied techniques for solving PortSwigger labs more efficiently                                   |
| 18.11.2024 |     2      |                  Lecture 4: The Project Continues                  |                                               Watched lecture, went through assignment                                               |
| 19.11.2024 |     1      |                Study: Vulnerability Scanning Tools                 |                                     Learned more about vulnerability scanning and best practices                                     |
| 21.11.2024 |     1      |                    Study: Web Security Overview                    |                                   Went over common web security vulnerabilities (SQLi, XSS, etc.)                                    |
| 23.11.2024 |     1      |                 Study: Ethical Hacking Strategies                  |                                       Focused on ethical hacking methodologies and tool usage                                        |
| 24.11.2024 |     2      |                    Booking System Phase 1 Final                    |                                       Fixed issues with zap, registrations with lecture videos                                       |
| 25.11.2024 |     5      |       Lecture and Study: Exploitation Techniques & Lecture 5       | Reviewed exploitation techniques using Metasploit and other tools; watched lecture, brainstormed ideas for index/login pages with AI |
| 26.11.2024 |     4      |             Continued Project & More PortSwigger Labs              |                                   Ran first tests with Zap, analyzed alerts; completed 3 more labs                                   |
| 27.11.2024 |     1      |                      Study: Threat Modelling                       |                                      Studied techniques for threat modelling and risk analysis                                       |
| 29.11.2024 |     1      |              Study: Web Application Firewalls (WAFs)               |                                           Focused on the purpose and functionality of WAFs                                           |
| 1.12.2024  |     4      |             Study: Network Security & Week 4 Homework              |  Reviewed basic network security concepts (firewalls, encryption); modified booking system, passed without errors, returned logbook  |
| 4.12.2024  |     5      |       Lecture and Study: Incident Response & Week 5 Homework       |        Learned about steps in incident response and handling breaches; performed system report, did more labs in PortSwigger         |
| 5.12.2024  |     1      |                  Study: Penetration Testing Tools                  |                                    Studied tools like Burp Suite and Nmap for penetration testing                                    |
| 7.12.2024  |     1      |                    Study: Cybersecurity Ethics                     |                                  Reviewed ethical considerations and legal aspects in cybersecurity                                  |
| 8.12.2024  |     2      |                               Week 5                               |                                       Wrote issues based on Zap report, pushed code to GitHub                                        |
| 9.12.2024  |     4      | Study: Advanced Web Security Techniques & Debugging Booking System |                 Studied advanced techniques for securing web applications; debugged errors, improved error handling                  |
| 10.12.2024 |     4      |        PortSwigger Labs - Advanced & Booking System Phase 2        |                        Solved more advanced PortSwigger labs; implemented user authentication and login flow                         |
| 11.12.2024 |     5      |            Study: SIEM Systems & Booking System Phase 2            |          Reviewed Security Information and Event Management (SIEM) systems; implemented user authentication and login flow           |
| 12.12.2024 |     4      |               Study: Cryptography Basics & Lecture 6               |                    Studied basic encryption and decryption methods; watched lecture on advanced security concepts                    |
| 13.12.2024 |     3      |                               Study                                |                                    Focused on handling incidents with formal protocols for errors                                    |
| 14.12.2024 |     3      |                  Project Review and Documentation                  |                                                Reviewed project, wrote documentation                                                 |
| 15.12.2024 |     3      |                    Study & Project Adjustments                     |                                                       preparing for submission                                                       |
| 16.12.2024 |     2      |                     Final Project Adjustments                      |                                      Final adjustments to project and preparing for submission                                       |

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

## Week 6:

Our system does not use consent (except for accepting the terms of service, but this is a slightly different matter).
Is this good?
Not using user consent can raise ethical and legal concerns, depending on the nature of the data collected or processed. Consent ensures transparency, user control, and compliance with privacy laws like GDPR or CCPA. Without consent, users may not feel confident about how their information is used, potentially undermining trust. However, if the system does not collect personal data beyond what is essential (e.g., terms of service acceptance), omitting additional consent might simplify user experience. Balancing compliance, transparency, and usability is key.

Choose an example page where consent is required. Tell us which one you chose. Tell us why consent is required?
The registration page requires consent because users must agree to the terms of service before creating an account. Consent is required here because the terms outline the rules for using the system, responsibilities, and rights of both the user and provider. Accepting the terms ensures users are aware of what they are agreeing to before proceeding. This helps prevent misuse and legal disputes, ensuring users actively acknowledge and agree to the conditions for accessing the system.
