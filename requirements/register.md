# Feature :: register a new user for admission

## Mock user interface with HTML
- File: register_mock_ui.html

## User flow 1
1. User navigates to the registration page.
2. User fills out the registration form with required information from input validation rules.
3. User submits the registration form
4. Save draft data into database

## User flow 2
1. User navigates to the registration page.
2. User fills out the registration form with required information from input validation rules.
3. User submits the registration form
4. User confirms the submission of the registration form.

## Input Validation Rules in table format
| Field | id | Input type | test_id | Validation Rule | Error message |
|-------|----|------------|---------|----------------|---------------|
| Gender | gender | radio button | input-gender | Required, must be either 'Male' or 'Female' | Please select a valid gender |
| Prefix | prefix | Select | input-prefix | Required, must be one of 'Mr.', 'Mrs.', 'Ms.' | Please select a valid prefix |
| First Name | first_name | textfield | input-first-name | Required, must be a non-empty string | Please enter a valid first name |
| Last Name | last_name | textfield | input-last-name | Required, must be a non-empty string | Please enter a valid last name |
| ID Card | id_card | textfield | input-id-card | Required, must be a valid Thai ID card number (13 digits) | Please enter a valid ID card number |
| Education level | education_level | Select | input-education-level | Required, must be one of 'High School', 'Bachelor', 'Master', 'Doctorate' | Please select a valid education level |
| School name | school_name | textfield | input-school-name | Required, must be a non-empty string | Please enter a valid school name |
| GPAX | gpax | textfield | input-gpax | Required, must be a number between 0.00 and 4.00 | Please enter a valid GPAX |
| Mobile Number | mobile_number | textfield | input-mobile-number | Required, must be a valid Thai mobile number (10 digits) | Please enter a valid mobile number |
| Confirm mobile number | confirm_mobile_number | textfield | input-confirm-mobile-number | Required, must match the mobile number | Please enter a valid mobile number |
| Email | email | textfield | input-email | Required, must be a valid email address | Please enter a valid email address |
| Confirm email | confirm_email | textfield | input-confirm-email | Required, must match the email address | Please enter a valid email address |
| Enrollment type | enrollment_type | radio button | input-enrollment-type | Required, must be one of 'Regular', 'Credit Bank' | Please select a valid enrollment type |

## Test Cases

### Test Case 1: Successful Registration
**Precondition:** User is on the registration page.
**Steps:**
1. Fill out the registration form with valid information.
2. Submit the registration form.

Example Input Data
| Field | Value |
|-------|-------|
| Gender | Male |
| Prefix | Mr. |
| First Name | John |
| Last Name | Doe |
| ID Card | 1234567890123 |
| Education level | Bachelor |
| School name | ABC University |
| GPAX | 3.50 |
| Mobile Number | 0812345678 |
| Confirm mobile number | 0812345678 |
| Email | john.doe@example.com |
| Confirm email | john.doe@example.com |
| Enrollment type | Regular |

**Expected Result:** Draft data is saved into the database.

### Test Case 2: Confirm Submission
**Precondition:** User has submitted the registration form.
**Steps:**
1. Fill out the registration form with valid information.
2. Confirm the submission of the registration form.

Example Input Data
| Field | Value |
|-------|-------|
| Gender | Male |
| Prefix | Mr. |
| First Name | John |
| Last Name | Doe |
| ID Card | 1234567890123 |
| Education level | Bachelor |
| School name | ABC University |
| GPAX | 3.50 |
| Mobile Number | 0812345678 |
| Confirm mobile number | 0812345678 |
| Email | john.doe@example.com |
| Confirm email | john.doe@example.com |
| Enrollment type | Regular |

**Expected Result:** Registration is successfully completed.

### Test Case 3: Input Validation
**Precondition:** User is on the registration page.
**Steps:**
1. Fill out the registration form with invalid information.
2. Submit the registration form.

Example with invalid input data
| Field | Value |
|-------|-------|
| Gender | InvalidGender |
| Prefix | Mr. |
| First Name | John123 |
| Last Name | Doe! |
| ID Card | 123 |
| Education level | Unknown |
| School name |  |
| GPAX | 5.00 |
| Mobile Number | 08123 |
| Confirm mobile number | 08123 |
| Email | john.doe@ |
| Confirm email | john.doe@ |
| Enrollment type | InvalidType |

**Expected Result:** Appropriate error messages are displayed for each invalid field.