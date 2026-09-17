# PROG5121 POE Part 1 - User Registration and Login

**Student:** Maluleke Ntshuxeko Valentia  
**Student Number:** ST10493052  
**Module:** PROG5121 - Programming 1A  
**Assessment:** POE Part 1 - Registration and Login Feature

---

## Project Overview

A console-based Java application that allows a user to register an account and then log in. The program validates the username, password, and South African cell phone number, stores the details after a successful registration, and then verifies the user's login credentials. The application uses decisions, loops, and a regular expression for the cell phone check, as required by Part 1 of the brief.

---

## Project Structure

| File | Purpose |
|------|---------|
| `UserRegistration.java` | The main class. Handles user input and the program flow. |
| `Login.java` | Contains all the validation methods and the login logic. |
| `LoginTest.java` | JUnit 4 unit tests for the Login class. |

---

## How to Run

1. Open the project in NetBeans.
2. Right-click on `UserRegistration.java` and select **Run File**.
3. Follow the prompts to enter the first name, last name, username, password, and cell phone number.
4. Once registration succeeds, enter the same username and password to log in.

---

## Validation Rules

| Field | Rule |
|-------|------|
| First Name | Must not be empty. |
| Last Name | Must not be empty. |
| Username | Must contain an underscore (`_`) and be no longer than five characters. |
| Password | At least 8 characters, must contain a capital letter, a number, and a special character. |
| Cell Phone Number | Must include the international country code (for example, `+27`) followed by the number. |

---

## Class Details

### `UserRegistration.java`
The main class. It:
- Reads input from the user using `Scanner`.
- Re-prompts if the first name, last name, username, password, or cell number is not valid.
- Creates a `Login` object and calls `registerUser()`.
- If registration succeeds, it allows the user to log in.

### `Login.java`
Holds all the validation and login logic:
- `checkUserName()` — checks the underscore and length rule.
- `checkPasswordComplexity()` — checks length, capital letter, number, and special character.
- `checkCellPhoneNumber()` — uses a regular expression to check the international format.
- `registerUser()` — runs all three checks and stores the user details.
- `loginUser()` — compares entered details to the stored ones.
- `returnLoginStatus()` — returns the correct login message.

### `LoginTest.java`
Six JUnit 4 tests that verify:
- Username validation (correct and incorrect).
- Password validation (correct and incorrect).
- Cell phone validation (correct and incorrect).
- Registration success and failure messages.
- Login success and failure.
- Return login status message.

---

## Unit Tests

All six tests pass. They use the test data from the brief:
- Username: `kyl_1` (valid), `kyle!!!!!!!` (invalid)
- Password: `Ch&&sec@ke99!` (valid), `password` (invalid)
- Cell number: `+27838968976` (valid), `08966553` (invalid)

---

## Links

- **GitHub Repository:** https://github.com/Ntshuxe/PROG5121-POE-PART-1

---

## References

The following source was used to develop the cell phone regular expression:

GeeksforGeeks, 2023. *How to validate a phone number using regex – Java source code* (Version 1.0) [Source code]. Available at: <https://www.geeksforgeeks.org/how-to-validate-a-phone-number-using-regex/> [Accessed 11 May 2026].

### In-Code Attribution
The regex logic in `Login.java` inside `checkCellPhoneNumber()` was adapted from GeeksforGeeks (2023).
