# QUESTION 2: TEST CASE DESIGN

## Application: Login System

### Objective
To test the Login System by checking valid inputs, invalid inputs, empty fields, password length and account locking functionality.

### Test Case Table

| Test Case ID | Test Scenario | Input Data | Expected Output |
|---|---|---|---|
| TC_01 | Valid login | Username: user1, Password: pass123 | Login successful. User is redirected to the home page. |
| TC_02 | Empty username | Username: Empty, Password: pass123 | Display "Username is required." Login should not proceed. |
| TC_03 | Empty password | Username: user1, Password: Empty | Display "Password is required." Login should not proceed. |
| TC_04 | Password less than 6 characters | Username: user1, Password: pass1 | Display "Password must be at least 6 characters." |
| TC_05 | Password exactly 6 characters | Username: user2, Password: pass12 (valid registered credentials) | Login successful because the password meets the minimum length. |
| TC_06 | Invalid username | Username: wronguser, Password: pass123 | Display "Invalid username or password." |
| TC_07 | Invalid password | Username: user1, Password: wrong123 | Display "Invalid username or password." |
| TC_08 | Three consecutive failed login attempts | Enter incorrect credentials three consecutive times. | Display "Account locked due to 3 failed login attempts." Further login attempts are blocked. |

### Test Case Coverage

| Functional Requirement | Test Case ID |
|---|---|
| Username must not be empty | TC_02 |
| Password must not be empty | TC_03 |
| Password must contain at least 6 characters | TC_04, TC_05 |
| Valid credentials allow successful login | TC_01, TC_05 |
| Invalid credentials display an error | TC_06, TC_07 |
| Account locks after 3 failed attempts | TC_08 |

### Conclusion

The above test cases cover the major functional requirements of the Login System. Both valid and invalid inputs, boundary conditions and account locking scenarios are included to verify the expected behaviour of the application.