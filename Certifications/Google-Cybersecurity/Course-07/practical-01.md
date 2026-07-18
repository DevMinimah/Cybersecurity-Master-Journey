# Technical Exercise: Python Conditional Statements for Security Automation

**Activity:** Create a Conditional Statement  
**Environment:** Jupyter Notebook (Python)  
**Role Assumed:** Security Analyst  
**Tools Utilized:** Python, Conditional Logic (`if`, `elif`, `else`), Logical Operators (`and`, `or`), Membership Operator (`in`)  

## Scenario
As a security analyst, I automated the process of checking whether a user's operating system requires an update and investigated login attempts to a specific device. The automation verifies if login attempts were made by approved users and if they occurred during designated organization hours.

---

## Task 1: Basic `if` Statement for OS Updates
*   **Action:** I wrote a conditional statement to check if a specific operating system requires an update.
*   **Code:**
    ```python
    # Assign a variable named `system` to a specific operating system, represented as a string
    # This variable indicates which operating system is running
    # Feel free to run this cell multiple times; each time try assigning `system` to different values ("OS 1", "OS 2", "OS 3") and observe the result
    system = "OS 2"

    # If OS 2 is running, then display a "no update needed" message
    if system == "OS 2":
        print("no update needed")
    ```
*   **Output:** 
    ```text
    no update needed
    ```
*   **Observation:** The code correctly evaluated the condition and printed the expected message when the `system` variable matched "OS 2".

---

## Task 2: Testing Variable Assignments
*   **Action:** I modified the `system` variable to "OS 3" and updated the condition to observe the behavior.
*   **Code:**
    ```python
    # Assign `system` to a specific operating system
    # This variable represents which operating system is running
    # Feel free to run this cell multiple times; each time try assigning `system` to different values ("OS 1", "OS 2", "OS 3") and observe the result
    system = "OS 3"

    # If OS 3 is running, then display a "no update needed" message
    if system == "OS 3":
        print("no update needed")
    ```
*   **Output:** 
    ```text
    no update needed
    ```
*   **Observation:** When the condition matched the variable ("OS 3"), it printed "no update needed". If the condition did not match the variable (e.g., checking for "OS 1" or "OS 2" while the variable was "OS 3"), there was no output, demonstrating that `if` statements only execute when the condition evaluates to `True`.

---

## Task 3: Implementing `else` for Fallback Logic
*   **Action:** I added an `else` block to provide a message when updates are needed.
*   **Code:**
    ```python
    # Assign `system` to a specific operating system
    # This variable represents which operating system is running
    system = "OS 2"

    # If OS 2 is running, then display a "no update needed" message
    # Otherwise, display a "update needed" message
    if system == "OS 2":
        print("no update needed")
    else:
        print("update needed")
    ```
*   **Output:** 
    ```text
    no update needed
    ```
    *(Note: When testing with `system = "OS 1"`, the output was `update needed`)*
*   **Observation:** The script outputs "no update needed" only when the system variable is exactly "OS 2". For any other OS value, it correctly defaults to the `else` block and outputs "update needed".

---

## Task 4: Adding `elif` for Multiple Conditions
*   **Action:** I expanded the logic to handle "OS 1" and "OS 3" specifically using `elif` statements.
*   **Code:**
    ```python
    # Assign `system` to a specific operating system
    # This variable represents which operating system is running
    system = "OS 2"

    # If OS 2 is running, then display a "no update needed" message
    # Otherwise if OS 1 is running, display a "update needed" message
    # Otherwise if OS 3 is running, display a "update needed" message
    if system == "OS 2":
        print("no update needed")
    elif system == "OS 1":
        print("update needed")
    elif system == "OS 3":
        print("update needed")
    ```
*   **Output:** 
    ```text
    no update needed
    ```
*   **Observation:** Outputs "no update needed" only for "OS 2", and "update needed" for "OS 1" or "OS 3". If an unhandled value (like "OS 4") is assigned, nothing is printed, highlighting the limitation of not having a catch-all `else` statement.

---

## Task 5: Consolidating Logic with the `or` Operator
*   **Action:** I combined the two `elif` statements into a single, more concise statement using the `or` logical operator.
*   **Code:**
    ```python
    # Assign `system` to a specific operating system
    # This variable represents which operating system is running
    system = "OS 2"

    # If OS 2 is running, then display a "no update needed" message
    # Otherwise if either OS 1 or OS 3 is running, display a "update needed" message
    if system == "OS 2":
        print("no update needed")
    elif system == "OS 1" or system == "OS 3":
        print("update needed")
    ```
*   **Output:** 
    ```text
    no update needed
    ```
*   **Observation:** This consolidates the logic efficiently. It outputs "no update needed" for "OS 2", and correctly triggers the "update needed" message for either "OS 1" or "OS 3" using a single `elif` block, improving code readability.

---

## Task 6: Hardcoded User Verification
*   **Action:** I wrote a conditional to check if a specific username matches an approved user variable.
*   **Code:**
    ```python
    # Assign `approved_user1` and `approved_user2` to usernames of approved users
    approved_user1 = "elarson"
    approved_user2 = "bmoreno"

    # Assign `username` to the username of a specific user trying to log in
    username = "bmoreno"

    # If the user trying to log in is among the approved users, then display a message that they are approved to access this device
    # Otherwise, display a message that they do not have access to this device
    if username == approved_user2:
        print("This user has access to this device.")
    else:
        print("This user does not have access to this device.")
    ```
*   **Output:** 
    ```text
    This user has access to this device.
    ```
*   **Observation:** Successfully validated the hardcoded username and granted access.

---

## Task 7: Using the `in` Operator for Allow Lists
*   **Action:** I replaced individual variables with an `approved_list` and used the `in` operator to check for membership.
*   **Code:**
    ```python
    # Assign `approved_list` to a list of approved usernames
    approved_list = ["elarson", "bmoreno", "tshah", "sgilmore", "eraab"]

    # Assign `username` to the username of a specific user trying to log in
    username = "misha"

    # If the user trying to log in is among the approved users, then display a message that they are approved to access this device
    # Otherwise, display a message that they do not have access to this device
    if username in approved_list:
        print("This user has access to this device.")
    else:
        print("This user does not have access to this device.")
    ```
*   **Output:** 
    ```text
    This user does not have access to this device.
    ```
*   **Observation:** Correctly grants access to usernames present in the `approved_list`. Assigning a random username (e.g., "misha") triggers the `else` block, confirming the user is not on the allow list. This is a scalable approach for access control.

---

## Task 8: Evaluating Boolean Variables
*   **Action:** I used a conditional statement to check a Boolean variable representing organization hours.
*   **Code:**
    ```python
    # Assign `organization_hours` to a Boolean value that represents whether the user is trying to log in during organization hours
    organization_hours = True

    # If the entered `organization_hours` has a value of True, then display "Login attempt made during organization hours."
    # Otherwise, display "Login attempt made outside of organization hours."
    if organization_hours:
        print("Login attempt made during organization hours.")
    else:
        print("Login attempt made outside of organization hours.")
    ```
*   **Output:** 
    ```text
    Login attempt made during organization hours.
    ```
*   **Observation:** When `organization_hours` is assigned the Boolean `True`, the condition evaluates successfully and outputs that the login attempt was made during organization hours.

---

## Task 9: Assembling Independent Conditions
*   **Action:** I combined the access check and the time check into the same script as two separate `if` statements.
*   **Code:**
    ```python
    # Assign `approved_list` to a list of approved usernames
    approved_list = ["elarson", "bmoreno", "tshah", "sgilmore", "eraab"]

    # Assign `username` to the username of a specific user trying to log in
    username = "bmoreno"

    # If the user trying to log in is among the approved users, then display a message that they are approved to access this device
    # Otherwise, display a message that they do not have access to this device
    if username in approved_list:
        print("This user has access to this device.")
    else:
        print("This user does not have access to this device.")

    # Assign `organization_hours` to a Boolean value that represents whether the user is trying to log in during organization hours
    organization_hours = True

    # If the entered `organization_hours` has a value of True, then display "Login attempt made during organization hours."
    # Otherwise, display "Login attempt made outside of organization hours."
    if organization_hours == True:
        print("Login attempt made during organization hours.")
    else:
        print("Login attempt made outside of organization hours.")
    ```
*   **Output:** 
    ```text
    This user has access to this device.
    Login attempt made during organization hours.
    ```
*   **Observation:** The script evaluates both conditions independently, printing separate, distinct messages for access approval and login time. 

---

## Task 10: Consolidating Conditions with the `and` Operator
*   **Action:** I merged both security checks into a single, concise conditional statement using the `and` logical operator.
*   **Code:**
    ```python
    # Assign `approved_list` to a list of approved usernames
    approved_list = ["elarson", "bmoreno", "tshah", "sgilmore", "eraab"]

    # Assign `username` to the username of a specific user trying to log in
    username = "bmoreno"

    # Assign `organization_hours` to a Boolean value that represents whether the user is trying to log in during organization hours
    organization_hours = True

    # If the user is among the approved users and they are logging in during organization hours, then convey that the user is logged in
    # Otherwise, convey that either the username is not approved or the login attempt was made outside of organization hours
    if username in approved_list and organization_hours == True:
        print("Login attempt made by an approved user during organization hours.")
    else:
        print("Username not approved or login attempt made outside of organization hours.")
    ```
*   **Output:** 
    ```text
    Login attempt made by an approved user during organization hours.
    ```
*   **Observation:** Combines both checks efficiently. Outputs a unified success message *only* if both conditions are met simultaneously. If either condition fails, it defaults to a single, unified failure message, reducing code redundancy.

---

## Technical Takeaways
1. **Control Flow:** `if`, `elif`, and `else` statements are foundational for automating security validations, such as OS patching status and access control.
2. **Code Conciseness:** Logical operators (`or`, `and`) and membership operators (`in`) significantly reduce code length and improve readability compared to multiple nested or sequential `if` statements.
3. **Scalability:** Using lists with the `in` operator is far more scalable and maintainable for access control than hardcoding individual variables for each approved user.
4. **Boolean Evaluation:** Python allows direct evaluation of Boolean variables in `if` statements (e.g., `if organization_hours:`), eliminating the need for redundant `== True` comparisons.


---
*Note: This document outlines my hands-on practice and learning proficiency in Python conditional logic, automated security validations (such as OS patching status and access control), and scalable identity verification techniques required for cybersecurity operations.*