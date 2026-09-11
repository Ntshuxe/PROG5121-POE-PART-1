# PROG5121 POE Part 1 - User Registration and Login

**Student:** [Maluleke Ntshuxeko Valentia] - [ST10493052]  
**Module:** PROG5121 - Programming 1A

## Project Overview
Console-based Java application that handles user registration and login using decisions only (if-else). No GUI, loops or JOptionPane.

## How to Run
1. Open NetBeans
2. Run `UserRegistration.java`
3. Follow prompts for First Name, Last Name, Username, Password, Cell Number

## Validation Logic (Decisions Only)
- **First/Last Name:** `.trim().isEmpty()` check. If first name empty, stop and ask again.
- **Username:** Must contain `_` and length <=5 - `checkUserName()`
- **Password:** Min 8 chars, capital letter, number, special char - `checkPasswordComplexity()` using regex.
- **Cell Number:** International format +27 + 9 digits. Regex implemented - `checkCellPhoneNumber()`
- **Login:** Checks username and password match stored values.

## JUnit Testing
6 tests implemented in `LoginTest.java` - all passing 100% (Username, Password, Cell, Registration, Login success/fail).

## Links
- **GitHub Repository:** [https://github.com/Ntshuxe/PROG5121-POE-PART-1]
- **Video Presentation (Unlisted YouTube):** [Paste your YouTube link here]

## References
The following source was used to develop the cell phone regex validation:

GeeksforGeeks, 2023. *How to validate a phone number using regex - Java source code* (Version 1.0) [Source code]. Available at: <https://www.geeksforgeeks.org/how-to-validate-a-phone-number-using-regex/> [Accessed 11 May 2026].

### In-Code Attribution
Regex logic in `Login.java` -> `checkCellPhoneNumber()` method adapted from GeeksforGeeks (2023).


