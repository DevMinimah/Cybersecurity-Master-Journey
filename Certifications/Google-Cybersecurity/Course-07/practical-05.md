# Technical Exercise: Python Algorithm Development for Security Automation

**Activity:** Develop an Algorithm  
**Environment:** Jupyter Notebook (Python)  
**Role Assumed:** Security Analyst  
**Tools Utilized:** Python, List Methods (`.append()`, `.remove()`, `.index()`), Conditional Logic (`if`, `elif`, `else`, `and`), Nested Functions  

## Scenario
As a security analyst, I developed a Python algorithm to automate the verification process for users and their assigned devices. This involved managing synchronized lists of approved users and devices, validating credentials, and implementing a nested conditional function to handle login authentication securely and efficiently.

---

## Task 1: Exploring Synchronized List Indexing
*   **Action:** I explored how indices work across two synchronized lists containing approved usernames and their corresponding device IDs.
*   **Code:**
    ```python
    # Assign `approved_users` to a list of approved usernames
    approved_users = ["elarson", "bmoreno", "tshah", "sgilmore", "eraab"]

    # Assign `approved_devices` to a list of device IDs that correspond to the usernames in `approved_users`
    approved_devices = ["8rp2k75", "hl0s5o1", "2ye3lzg", "4n482ts", "a307vir"]

    # Display the element at the specified index in `approved_users`
    print(approved_users[4])

    # Display the element at the specified index in `approved_devices`
    print(approved_devices[4])
    ```
*   **Output:** 
    ```text
    eraab
    a307vir
    ```
*   **Observation:** Using the same index (`4`) on both lists successfully retrieved the corresponding approved user and their assigned device. This demonstrates that maintaining synchronized lists allows for reliable parallel data retrieval.

---

## Task 2: Adding New Entries with `.append()`
*   **Action:** I used the `.append()` method to add a new user and their device ID to the respective synchronized lists.
*   **Code:**
    ```python
    # Assign `approved_users` to a list of approved usernames
    approved_users = ["elarson", "bmoreno", "tshah", "sgilmore", "eraab"]

    # Assign `approved_devices` to a list of device IDs that correspond to the usernames in `approved_users`
    approved_devices = ["8rp2k75", "hl0s5o1", "2ye3lzg", "4n482ts", "a307vir"]

    # Assign `new_user` to the username of a new approved user
    new_user = "gesparza"

    # Assign `new_device` to the device ID of the new approved user
    new_device = "3rcv4w6"

    # Add that user's username and device ID to `approved_users` and `approved_devices` respectively
    approved_users.append(new_user)
    approved_devices.append(new_device)

    # Display the contents of `approved_users`
    print(approved_users)

    # Display the contents of `approved_devices`
    print(approved_devices)
    ```
*   **Output:** 
    ```text
    ['elarson', 'bmoreno', 'tshah', 'sgilmore', 'eraab', 'gesparza']
    ['8rp2k75', 'hl0s5o1', '2ye3lzg', '4n482ts', 'a307vir', '3rcv4w6']
    ```
*   **Observation:** The `.append()` method successfully added the new approved user and device to the end of their respective lists, maintaining the synchronized structure while keeping all existing entries intact.

---

## Task 3: Revoking Access with `.remove()`
*   **Action:** I used the `.remove()` method to delete a departed employee and their device from the synchronized lists.
*   **Code:**
    ```python
    # Assign `approved_users` to a list of approved usernames
    approved_users = ["elarson", "bmoreno", "tshah", "sgilmore", "eraab", "gesparza"]

    # Assign `approved_devices` to a list of device IDs that correspond to the usernames in `approved_users`
    approved_devices = ["8rp2k75", "hl0s5o1", "2ye3lzg", "4n482ts", "a307vir", "3rcv4w6"]

    # Assign `removed_user` to the username of the employee who has left the team
    removed_user = "tshah"

    # Assign `removed_device` to the device ID of the employee who has left the team
    removed_device = "2ye3lzg"

    # Remove that employee's username and device ID from `approved_users` and `approved_devices` respectively
    approved_users.remove(removed_user)
    approved_devices.remove(removed_device)

    # Display `approved_users`
    print(approved_users)

    # Display `approved_devices`
    print(approved_devices)
    ```
*   **Output:** 
    ```text
    ['elarson', 'bmoreno', 'sgilmore', 'eraab', 'gesparza']
    ['8rp2k75', 'hl0s5o1', '4n482ts', 'a307vir', '3rcv4w6']
    ```
*   **Observation:** Using `.remove()` successfully deleted the departed employee and their device from the lists while keeping everyone else in order. This demonstrates an efficient way to revoke access programmatically when personnel changes occur.

---

## Task 4: Validating User Approval
*   **Action:** I wrote a conditional statement using the `in` operator to verify if a given username exists in the approved users list.
*   **Code:**
    ```python
    # Assign `approved_users` to a list of approved usernames
    approved_users = ["elarson", "bmoreno", "sgilmore", "eraab", "gesparza"]

    # Assign `approved_devices` to a list of device IDs that correspond to the usernames in `approved_users`
    approved_devices = ["8rp2k75", "hl0s5o1", "4n482ts", "a307vir", "3rcv4w6"]

    # Assign `username` to a username
    username = "sgilmore"

    # Conditional statement
    # If `username` belongs to `approved_users`, then display "The user ______ is approved to access the system."
    # Otherwise display "The user ______ is not approved to access the system."
    if username in approved_users:
        print("The username", username, "is approved to access the system.")
    else:
        print("The user ______ is not approved to access the system.")
    ```
*   **Output:** 
    ```text
    The username sgilmore is approved to access the system.
    ```
*   **Observation:** The `in` operator efficiently evaluated the condition, confirming that "sgilmore" is present in the allow list and triggering the appropriate approval message.

---

## Task 5: Finding the User Index
*   **Action:** I used the `.index()` method to find the numerical position of the approved username within the list.
*   **Code:**
    ```python
    # Assign `approved_users` to a list of approved usernames
    approved_users = ["elarson", "bmoreno", "sgilmore", "eraab", "gesparza"]

    # Assign `approved_devices` to a list of device IDs that correspond to the usernames in `approved_users`
    approved_devices = ["8rp2k75", "hl0s5o1", "4n482ts", "a307vir", "3rcv4w6"]

    # Assign `username` to a username
    username = "sgilmore"

    # Assign `ind` to the index of `username` in `approved_users`
    ind = approved_users.index(username)

    # Display the value of `ind`
    print(ind)
    ```
*   **Output:** 
    ```text
    2
    ```
*   **Observation:** The `.index()` method accurately returned `2`, which is the zero-based position of "sgilmore". This index is crucial for cross-referencing the synchronized device list.

---

## Task 6: Cross-Referencing Lists via Index
*   **Action:** I used the index obtained from the user list to retrieve the corresponding assigned device ID from the device list.
*   **Code:**
    ```python
    # Assign `approved_users` to a list of approved usernames
    approved_users = ["elarson", "bmoreno", "sgilmore", "eraab", "gesparza"]

    # Assign `approved_devices` to a list of device IDs that correspond to the usernames in `approved_users`
    approved_devices = ["8rp2k75", "hl0s5o1", "4n482ts", "a307vir", "3rcv4w6"]

    # Assign `username` to a username
    username = "sgilmore"

    # Assign `ind` to the index of `username` in `approved_users`
    ind = approved_users.index(username)

    # Display the device ID at the index that matches the value of `ind` in `approved_devices`
    print(approved_devices[ind])
    ```
*   **Output:** 
    ```text
    4n482ts
    ```
*   **Observation:** By connecting the `ind` variable to the `approved_devices` list, the output accurately returned "4n482ts", proving that synchronized lists can be reliably queried using a shared index.

---

## Task 7: Verifying User and Device Match
*   **Action:** I combined conditions using the logical `and` operator to verify both user approval and device assignment simultaneously.
*   **Code:**
    ```python
    # Assign `approved_users` to a list of approved usernames
    approved_users = ["elarson", "bmoreno", "sgilmore", "eraab", "gesparza"]

    # Assign `approved_devices` to a list of device IDs that correspond to the usernames in `approved_users`
    approved_devices = ["8rp2k75", "hl0s5o1", "4n482ts", "a307vir", "3rcv4w6"]

    # Assign `username` to a username
    username = "sgilmore"

    # Assign `device_id` to a device ID
    device_id = "4n482ts"

    # Assign `ind` to the index of `username` in `approved_users`
    ind = approved_users.index(username)

    # Conditional statement
    # If `username` belongs to `approved_users`, and if the device ID at `ind` in `approved_devices` matches `device_id`,
    # then display a message that the username is approved,
    # followed by a message that the user has the correct device
    if username in approved_users and device_id == approved_devices[ind]:
        print("The user", username, "is approved to access the system.")
        print(device_id, "is the assigned device for", username)
    ```
*   **Output:** 
    ```text
    The user sgilmore is approved to access the system.
    4n482ts is the assigned device for sgilmore
    ```
*   **Observation:** The compound condition successfully confirmed that "sgilmore" is in the approved users list and that "4n482ts" is their registered device, triggering the dual success messages.

---

## Task 8: Handling Device Mismatches with `elif`
*   **Action:** I added an `elif` statement to handle the specific scenario where a user is approved, but the provided device ID does not match their assigned device.
*   **Code:**
    ```python
    # Assign `approved_users` to a list of approved usernames
    approved_users = ["elarson", "bmoreno", "sgilmore", "eraab", "gesparza"]

    # Assign `approved_devices` to a list of device IDs that correspond to the usernames in `approved_users`
    approved_devices = ["8rp2k75", "hl0s5o1", "4n482ts", "a307vir", "3rcv4w6"]

    # Assign `username` to a username
    username = "sgilmore"

    # Assign `device_id` to a device ID
    device_id = "4n482ts"

    # Assign `ind` to the index of `username` in `approved_users`
    ind = approved_users.index(username)

    # If statement
    if username in approved_users and device_id == approved_devices[ind]:
        print("The user", username, "is approved to access the system.")
        print(device_id, "is the assigned device for", username)

    # Elif statement
    # Handles the case when `username` belongs to `approved_users` but element at `ind` in `approved_devices` does not match `device_id`
    elif username in approved_users and device_id != approved_devices[ind]:
        print("The user", username, "is approved to access the system, but", device_id, "is not their assigned device.")
    ```
*   **Output:** 
    ```text
    The user sgilmore is approved to access the system.
    4n482ts is the assigned device for sgilmore
    ```
*   **Observation:** While the current test variables triggered the initial `if` block, the `elif` structure is now in place to gracefully catch and alert on hardware mismatches for valid users, preventing silent failures.

---

## Task 9: Automating Login with a Nested Conditional Function
*   **Action:** I encapsulated the verification logic into a reusable `login()` function using nested conditionals to handle multiple authentication outcomes.
*   **Code:**
    ```python
    # Assign `approved_users` to a list of approved usernames
    approved_users = ["elarson", "bmoreno", "sgilmore", "eraab", "gesparza"]

    # Assign `approved_devices` to a list of device IDs that correspond to the usernames in `approved_users`
    approved_devices = ["8rp2k75", "hl0s5o1", "4n482ts", "a307vir", "3rcv4w6"]

    # Define a function named `login` that takes in two parameters, `username` and `device_id`
    def login(username, device_id):

        # If `username` belongs to `approved_users`, 
        if username in approved_users:

            # then display "The user ______ is approved to access the system.",
            print("The user", username, "is approved to access the system.")

            # assign `ind` to the index of `username` in `approved_users`,
            ind = approved_users.index(username)

            # and execute the following conditional
            # If `device_id` matches the element at the index `ind` in `approved_devices`,
            if device_id == approved_devices[ind]:

              # then display "______ is the assigned device for ______" 
              print(device_id, "is the assigned device for", username)

            # Otherwise,
            else:

              # display "______ is not their assigned device"
              print(device_id, "is not their assigned device.")
      
        # Otherwise (part of the outer conditional and handles the case when `username` does not belong to `approved_users`),
        else:

            # Display "The user ______ is not approved to access the system."
            print("The username", username, "is not approved to access the")

    # Call the function you just defined to experiment with different username and device_id combinations
    login("elarson", "8rp2k75")      
    login("bmoreno", "h10s501")      
    login("sgilmore", "4n482ts")     
    login("eraab", "a307vir")        
    login("gesparza", "3rcv4w6")
    ```
*   **Output:** 
    ```text
    The user elarson is approved to access the system.
    8rp2k75 is the assigned device for elarson
    The user bmoreno is approved to access the system.
    h10s501 is not their assigned device.
    The user sgilmore is approved to access the system.
    4n482ts is the assigned device for sgilmore
    The user eraab is approved to access the system.
    a307vir is the assigned device for eraab
    The user gesparza is approved to access the system.
    3rcv4w6 is the assigned device for gesparza
    ```
*   **Observation:** Once the program confirms the user is approved and enters the inner conditional, it checks the specific device. If the device_id matches, it prints a success message. If it doesn't match (as seen with "bmoreno"), it triggers the `else` block to flag the mismatch. This demonstrates how nested conditionals allow for structured, multi-step security verifications.

---

## Technical Takeaways
1. **Synchronized Data Structures:** Maintaining parallel lists with matching indices is a foundational technique for mapping related data (like users to devices) without requiring complex dictionary structures.
 are critical for dynamic list management, allowing security scripts to scale as personnel join or leave the organization.
2. **Cross-Referencing via Index:** Using `.index()` to find a user's position and then querying a second list with that same index is a highly efficient way to validate paired credentials.
3. **Compound Conditions:** The logical `and` operator ensures that multiple security criteria (identity + hardware) must be met simultaneously before granting access.
4. **Nested Conditionals for Authentication:** Structuring login logic with outer conditionals (user validation) and inner conditionals (device validation) creates clean, readable, and secure authentication flows.

---
*Note: This document outlines my hands-on practice and learning proficiency in Python algorithm development, list manipulation, and nested conditional logic for automated user and device authentication required for cybersecurity operations.*