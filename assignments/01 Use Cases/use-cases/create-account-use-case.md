### Use Case: Customer Creating an Account

**Change Log:**

| Revision | Date              | Person       | Reason for Change |
| -------- | ----------------- | ------------ | ----------------- |
| New      | 25 September 2024 | Nathan Roark | Initial release   |

---

**Primary Actor:** Customer

**Goal in Context:**  
The customer creates a new bank account they can use for accessing the system.

---

**Preconditions:**

1. The banking system is accessible and functioning without technical issues.
2. The customer must have internet access and a device with a web browser.
3. The customer must have a valid SSN.
4. The customer has not previously registered for an account in the system.

---

**Trigger:**  
The future customer navigates to the account registration page on the bank's website (accessible via the homepage or a dedicated "Create Account" link).

---

**Scenario:**

1. **Customer** navigates to the bank's homepage and clicks on "Create an Account."
2. **System** displays the registration form requesting the customer's personal details: name, address, phone number, email, social security number (SSN), etc.
3. **Customer** fills out the registration form with the required details and clicks **Submit**.
4. **Customer** sets their username and password for future logins.
5. **System** validates the entered information:
   - Ensures the username is unique by checking against existing records.
   - Ensures the personal details are complete and correctly formatted.
   - Ensures the password meets security requirements (e.g., length, complexity).
   - Checks that the SSN format is valid.
6. **System** prompts the customer to review and agree to the terms and conditions.
7. **Customer** reviews and accepts the terms and conditions.
8. **System** verifies the customer information, and if valid, creates a new customer profile.
9. **System** sends a confirmation email to the customer with account details and a link for verification.
10. **Customer** verifies their email by clicking the link provided in the confirmation email.
    - If the link fails, the **Customer** has an option to request a new verification email.
11. **System** confirms account creation and allows the customer to log in using the newly created credentials.

---

**Exceptions:**

1. **Username Not Unique**:  
   If the username is already taken, the **System** prompts the customer to choose a different username by displaying an appropriate error message.
2. **Incomplete Form**:  
   If any required field is left blank, the **System** prompts the customer to complete the form before proceeding.

3. **Password Requirement Failure**:  
   If the password does not meet security requirements, the **System** informs the customer and provides the necessary password criteria.

4. **Invalid SSN Format**:  
   If the SSN format is invalid, the **System** alerts the customer to enter a valid SSN, providing guidelines on the correct format.

5. **Email Verification Timeout**:  
   If the email verification link is not clicked within a specified time (e.g., 24 hours), the **System** disables the account creation, and the **Customer** must restart the process. A reminder email may be sent before this action occurs.

---

**Priority:**  
High. This feature is critical for the success of the project and must be implemented in the first release.

---

**When Available:**  
Planned for initial release.

---

**Frequency of Use:**  
This feature will be used whenever a new customer registers with the bank, potentially multiple times a day.

---

**Channel to Actor:**  
The customer accesses this feature via the web interface on the bank's website.

---

**Secondary Actors:**  
None.

---

**Channels to Secondary Actors:**  
Not applicable.

---

**Open Issues:**

1. Will the system require additional identity verification, such as a government-issued ID, to complete the registration process?
2. What is the timeout period for completing the account creation process (e.g., due to session expiration)?
3. Is there a need for CAPTCHA or another tool for mitigating automated account creation during the registration process?
4. How should the system handle duplicate account creation attempts if a customer starts the process but does not complete verification?
