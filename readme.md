
# User Management Project

There are 31 extra test cases compare to the basecode.  Each branch has test cases to test the necessary changes. Can verified through in commits. 



## Issue resolved:

1. **exceptions logs are missing**: Addressed the absence of exception logs in user routes by integrating logging functionality. This ensures that all exceptions are captured and logged, improving traceability, debugging, and monitoring of user-related operations.

link to the issue: https://github.com/MohammedAhmeduddin/user_management/tree/11-exceptions-logs-are-missing-in-user-routes


2. **remove duplicate login endpoint**: Simplified the user route by removing the redundant login endpoint, ensuring there is only a single login route. This change reduces redundancy, improves maintainability, and prevents potential inconsistencies in login logic.

link to the issue: https://github.com/MohammedAhmeduddin/user_management/tree/9-duplicate-login-endpoint


3. **Added logging Functionality and improved error handling in email service**: The refactored code enhances the original by incorporating detailed logging and robust error handling to improve monitoring and debugging. Logging is added at key stages, such as service initialization, email template rendering, and sending, providing visibility into operations. It logs specific details like email type and recipient, making it easier to track actions and diagnose issues. Error handling is strengthened with `try-except` blocks to catch and log failures during template rendering or email sending, ensuring clear error messages with contextual information. These changes make the service more reliable, maintainable, and transparent for developers.

link to the issue: https://github.com/MohammedAhmeduddin/user_management/tree/3-lack-of-error-handling-and-no-logging-in-email-service


4. **password validation contraints**: The refactored code adds **password validation** to enforce strong security requirements, ensuring passwords contain uppercase, lowercase, special characters, and numbers with min password length 8 characters. It also includes detailed logging for monitoring key operations and robust error handling to log and manage failures during email rendering or sending. These updates enhance security, reliability, and maintainability.

link to the issue: https://github.com/MohammedAhmeduddin/user_management/tree/5-password-validation-constraints

5. **Verify Email missing UUID**
Cause: Email was being sent before the user got added to the DB. Fix: Mail was made to sent after the user was added to the DB.

link to the issue: https://github.com/MohammedAhmeduddin/user_management/tree/7-email-missing-uuid


6. **GitHub and linkedin url are null in create user** : rCause: GitHub URL and LinkedIn URL are null in the response of the create user. Fix: Values are being correctly mapped to response object.
link to the issue: https://github.com/MohammedAhmeduddin/user_management/tree/13-github-and-linked-url-are-null-in-create-user



7. **Refactored jwt Service**: The code was refactored to improve **readability**, **functionality**, and **maintainability**. Detailed **docstrings** were added for better documentation. The `decode_token` function now includes error handling to safely manage invalid tokens. Logic was simplified for clarity, and explicit algorithm specifications enhance security. These changes make the code more robust, user-friendly, and easier to maintain or extend.
link to the issue: https://github.com/MohammedAhmeduddin/user_management/tree/1-lack-of-error-handling-in-token-decoding-no-token-refresh-mechanism-no-expiration-check-in-jwt-service



# Added feature User Profile Management:
Enhance user profile management by enabling users to update profile fields such as name, bio, and location, and allowing managers or admins to upgrade users to professional status. This involves creating API endpoints for profile updates and professional status upgrades, updating the profile page to display professional status and editable fields, and sending notifications upon status upgrades. Optional improvements include field validation, dynamic field addition, and a user-friendly interface for managers/admins. The implementation requires reviewing the existing codebase, designing APIs, updating the database schema, developing the necessary functionality, refining the UI, and writing unit tests to ensure reliability.


link of the commit: https://github.com/kaw393939/user_management/commit/ccf4947d8f2df8d6784ef6b313ddc1061bf30a32


Here’s a combined version of both pieces of content, integrating all the insights cohesively:

---

**What I Learned**

This assignment provided a substantial opportunity to enhance my technical expertise in secure software development and system reliability. Implementing features such as enforcing password complexity requirements (e.g., minimum length, special characters, and case sensitivity) demonstrated the importance of adhering to security best practices in user authentication. Refactoring the JWT service to include structured error handling and explicit algorithm specifications improved the system's robustness and security, ensuring secure and reliable token management. Addressing issues like duplicate login routes and nickname mismatches in user creation highlighted the value of database integrity and efficient query design to maintain consistency and scalability in multi-user environments.

The integration of detailed logging across various services, including user routes and email services, underscored the importance of observability in modern applications. By adding logging at critical execution points and during exception handling, the system now offers better traceability, simplifies debugging processes, and improves monitoring. Refactoring and modularizing these components reinforced the importance of maintainable and extensible code, which is essential for managing large, collaborative codebases effectively. Additionally, working with unique constraints in the database, especially for nicknames, emphasized the necessity of dynamically validating inputs to avoid runtime conflicts.

Through this project, I also gained hands-on experience in collaborative development workflows, including issue tracking, branching strategies, and version control best practices. Isolating changes for each task and maintaining comprehensive documentation helped achieve consistency and scalability while adhering to software development standards. Adding 31 extra test cases strengthened my understanding of comprehensive testing, ensuring the reliability and accuracy of the newly implemented features and bug fixes.

Ultimately, this project deepened my knowledge of designing secure, maintainable, and reliable systems while addressing practical challenges in real-world development scenarios. It reinforced critical lessons in debugging, implementing robust logging and error-handling mechanisms, and enhancing application security. This experience also showcased the value of clean, maintainable code, dynamic validation, and thoughtful system architecture in building scalable, production-grade software.




