# Technical Exercise: Python Iterative Statements for Security Automation

**Activity:** Create Loops  
**Environment:** Jupyter Notebook (Python)  
**Role Assumed:** Security Analyst  
**Tools Utilized:** Python, `for` loops, `while` loops, `range()`, `break` statement, Conditional Logic  

## Scenario
As a security analyst, I automated repetitive security tasks using Python iterative statements. This included automating network connection attempt messages, detecting unauthorized IP addresses attempting to access restricted data, and generating unique employee ID numbers for the Sales department.

---

## Task 1: Basic `for` Loop with `range()`
*   **Action:** I wrote an iterative statement to display a network connection message a specific number of times.
*   **Code:**
    ```python
    # Iterative statement using `for`, `range()`, and a loop variable of `i`
    # Display "Connection could not be established." three times

    for i in range(0, 3):
        print("Connection could not be established.")
    ```
*   **Output:** 
    ```text
    Connection could not be established.
    Connection could not be established.
    Connection could not be established.
    ```
*   **Observation:** The `for` loop successfully executed the print statement exactly three times, demonstrating basic iteration control using the `range()` function.

---

## Task 2: Using a Variable in `range()`
*   **Action:** I incorporated a variable (`connection_attempts`) into the `range()` function to make the loop dynamic.
*   **Code:**
    ```python
    # Create a variable called `connection_attempts` that stores the number of times the user has tried to connect to the network
    connection_attempts = 5

    # Iterative statement using `for`, `range()`, a loop variable of `i`, and `connection_attempts`
    # Display "Connection could not be established." as many times as specified by `connection_attempts`

    for i in range(0, connection_attempts):
        print("Connection could not be established")
    ```
*   **Output:** 
    ```text
    Connection could not be established
    Connection could not be established
    Connection could not be established
    Connection could not be established
    Connection could not be established
    ```
*   **Observation:** By passing the `connection_attempts` variable into `range()`, the loop dynamically adjusted its iterations. Changing the variable value directly controls the number of executions, improving code flexibility.

---

## Task 3: Implementing a `while` Loop
*   **Action:** I replicated the connection attempt logic using a `while` loop, which relies on a condition rather than a fixed iteration count.
*   **Code:**
    ```python
    # Assign `connection_attempts` to an initial value of 0, to keep track of how many times the user has tried to connect to the network
    connection_attempts = 0

    # Iterative statement using `while` and `connection_attempts`
    # Display "Connection could not be established." every iteration, until connection_attempts reaches a specified number

    while connection_attempts < 5:
        print("Connection could not be established")

        # Update `connection_attempts` (increment it by 1 at the end of each iteration) 
        connection_attempts = connection_attempts + 1
    ```
*   **Output:** 
    ```text
    Connection could not be established
    Connection could not be established
    Connection could not be established
    Connection could not be established
    Connection could not be established
    ```
*   **Observation:** The iteration message prints continuously until the `while` condition (`connection_attempts < 5`) evaluates to False. Unlike a `for` loop, the `while` loop requires manual incrementing of the counter variable to prevent infinite loops.

---

## Task 4: Iterating Through a List of IP Addresses
*   **Action:** I used a `for` loop to iterate through and display elements of a list containing IP addresses.
*   **Code:**
    ```python
    # Assign `ip_addresses` to a list of IP addresses from which users have tried to log in
    ip_addresses = ["192.168.142.245", "192.168.109.50", "192.168.86.232", "192.168.131.147",
                    "192.168.205.12", "192.168.200.48"]

    # For loop that displays the elements of `ip_addresses` one at a time
    for i in ip_addresses:
        print(i)
    ```
*   **Output:** 
    ```text
    192.168.142.245
    192.168.109.50
    192.168.86.232
    192.168.131.147
    192.168.205.12
    192.168.200.48
    ```
*   **Observation:** The `for` loop efficiently traversed the entire list, assigning each IP address to the loop variable `i` sequentially and printing it. This is the standard method for iterating over collections in Python.

---

## Task 5: Combining Loops with Conditional Logic (Allow List Check)
*   **Action:** I nested an `if/else` statement inside the `for` loop to check each IP address against an authorized allow list.
*   **Code:**
    ```python
    # Assign `allow_list` to a list of IP addresses that are allowed to log in
    allow_list = ["192.168.243.140", "192.168.205.12", "192.168.151.162", "192.168.178.71", 
                  "192.168.86.232", "192.168.3.24", "192.168.170.243", "192.168.119.173"]

    # Assign `ip_addresses` to a list of IP addresses from which users have tried to log in
    ip_addresses = ["192.168.142.245", "192.168.109.50", "192.168.86.232", "192.168.131.147",
                    "192.168.205.12", "192.168.200.48"]

    # For each IP address in the list of IP addresses from which users have tried to log in, 
    # If it is among the allowed addresses, then display “IP address is allowed”
    # Otherwise, display “IP address is not allowed”

    for i in ip_addresses:
        if i in allow_list:
            print("IP address is allowed")
        else:
            print("IP address is not allowed")
    ```
*   **Output:** 
    ```text
    IP address is not allowed
    IP address is not allowed
    IP address is allowed
    IP address is not allowed
    IP address is allowed
    IP address is not allowed
    ```
*   **Observation:** The script successfully evaluated each IP address individually against the `allow_list`, providing immediate, granular feedback on access status for every entry in the log.

---

## Task 6: Terminating Loops Early with `break`
*   **Action:** I added the `break` keyword to immediately halt the loop if an unauthorized IP address was detected, simulating a security triage response.
*   **Code:**
    ```python
    # Assign `allow_list` to a list of IP addresses that are allowed to log in
    allow_list = ["192.168.243.140", "192.168.205.12", "192.168.151.162", "192.168.178.71", 
                  "192.168.86.232", "192.168.3.24", "192.168.170.243", "192.168.119.173"]

    # Assign `ip_addresses` to a list of IP addresses from which users have tried to log in
    ip_addresses = ["192.168.142.245", "192.168.109.50", "192.168.86.232", "192.168.131.147",
                    "192.168.205.12", "192.168.200.48"]

    # For each IP address in the list of IP addresses from which users have tried to log in, 
    # If it is among the allowed addresses, then display “IP address is allowed”
    # Otherwise, display “IP address is not allowed. Further investigation of login activity required”

    for i in ip_addresses:
        if i in allow_list:
            print("IP address is allowed")
        else:
            print("IP address is not allowed. Further investigation of login activity required")
            break
    ```
*   **Output:** 
    ```text
    IP address is not allowed. Further investigation of login activity required
    ```
*   **Observation:** The loop evaluated the first IP address, found it was not in the `allow_list`, printed the escalation message, and immediately executed `break`, terminating the loop. This prevents unnecessary processing once a critical security threshold is breached.

---

## Task 7: Generating Sequential IDs with a `while` Loop
*   **Action:** I used a `while` loop to generate unique employee IDs for the Sales department, ensuring they are divisible by 5 and fall within a specific range.
*   **Code:**
    ```python
    # Assign the loop variable `i` to an initial value of 5000
    i = 5000

    # While loop that generates unique employee IDs for the Sales department by iterating through numbers
    # and displays each ID created

    while i <= 5150:
        print(i)
        i = i + 5
    ```
*   **Output:** 
    ```text
    5000
    5005
    5010
    ... (continues in increments of 5) ...
    5145
    5150
    ```
*   **Observation:** The `while` loop successfully generated the sequence by checking the upper bound (`<= 5150`) and incrementing the counter by 5 on each iteration, perfectly matching the business logic requirements.

---

## Task 8: Injecting Conditional Alerts within a Loop
*   **Action:** I embedded an `if` statement inside the `while` loop to trigger a specific alert when the ID generation reached a predefined threshold (5100).
*   **Code:**
    ```python
    # Assign the loop variable `i` to an initial value of 5000
    i = 5000

    # While loop that generates unique employee IDs for the Sales department by iterating through numbers
    # and displays each ID created
    # This loop displays "Only 10 valid employee ids remaining" once `i` reaches 5100

    while i <= 5150: 
        print(i)
        if i == 5100:
            print("Only 10 valid employee ids remaining")
        i = i + 5
    ```
*   **Output:** 
    ```text
    5000
    5005
    ...
    5095
    5100
    Only 10 valid employee ids remaining
    5105
    ...
    5150
    ```
*   **Observation:** The `print(i)` statement is placed before the conditional to ensure the current ID is always printed. The conditional check simply injects the alert message when the specific threshold (5100) is reached, without interrupting the primary loop flow or skipping the ID print.

---

## Technical Takeaways
1. **Loop Selection:** `for` loops are optimal for iterating over known collections (like lists) or fixed ranges, while `while` loops are best for condition-based iteration where the number of executions is not predetermined.
 is critical to manually update the loop variable in a `while` loop to prevent infinite execution.
2. **Early Termination:** The `break` statement is a powerful tool for security automation, allowing scripts to halt processing immediately when a critical anomaly (like an unauthorized IP) is detected, saving computational resources and triggering immediate escalation.
3. **Nested Logic:** Combining iterative statements with conditional logic (`if/else` inside loops) enables dynamic, real-time decision-making, such as validating each item in a log against an allow list or triggering threshold-based alerts.
4. **Dynamic Iteration:** Using variables within the `range()` function makes loops adaptable to changing environmental states, such as a dynamically updating count of failed connection attempts.

---
*Note: This document outlines my hands-on practice and learning proficiency in Python iterative logic, automated security validations (such as IP allow-list checking and loop termination), and scalable identity generation techniques required for cybersecurity operations.*