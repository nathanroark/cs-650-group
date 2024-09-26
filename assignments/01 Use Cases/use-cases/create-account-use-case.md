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

1. The banking system must be operational.
2. The customer must have internet access and a device with a web browser.
3. The customer must have a valid SSN.
4. The customer has not previously registered for an account in the system.

---

**Trigger:**  
The future customer navigates to the account registration page on the bank's website.

---

**Scenario:**

1. **Customer** navigates to the bank's homepage and clicks on "Create an Account."
2. **System** displays the registration form requesting the customer's personal details: name, address, phone number, email, social security number, etc.
3. **Customer** fills out the registration form with the required details.
4. **Customer** sets their username and password for future logins.
5. **System** validates the entered information:
   - Ensures the username is unique.
   - Ensures the personal details are valid.
   - Ensures the password meets security requirements (e.g., length, complexity).
   - Checks that the social security number (SSN) format is valid.
6. **System** prompts the customer to review and agree to the terms and conditions.
7. **Customer** reviews and accepts the terms and conditions.
8. **System** verifies the customer information, and if valid, creates a new customer profile.
9. **System** sends a confirmation email to the customer with account details and a link for verification.
10. **Customer** verifies their email by clicking the link.
11. **System** confirms account creation and allows the customer to log in using the newly created credentials.

---

**Exceptions:**

1. If the username is not unique, the **System** prompts the customer to choose a different username.
2. If any required field is left blank, the **System** prompts the customer to complete the form.
3. If the password does not meet security requirements, the **System** informs the customer and provides the necessary password criteria.
4. If the social security number format is invalid, the **System** alerts the customer to enter a valid SSN.
5. If the email verification link is not clicked within a specified time (e.g., 24 hours), the **System** disables the account creation, and the customer must start the process again.

---

**Priority:**  
High. This feature is critical for the success of the project and must be implemented in the first release.

---

**When Available:**  
Planned for inital release.

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

1. Will the system require additional identity verification, (e.g., government-issued ID), to complete the registration process?
2. What is the timeout period for completing the account creation process (e.g., due to session expiration)?
3. Is there a need for CAPTCHA or another tool for threat actor mitigation during the registration process?
