# Technical Exercise: Python Algorithm Development for Access Control Automation

**Activity:** Create Another Algorithm  
**Environment:** Jupyter Notebook (Python)  
**Role Assumed:** Security Analyst  
**Tools Utilized:** Python, File I/O (`open()`, `.read()`, `.write()`, `.split()`, `.join()`), Iterative Statements (`for`), Conditional Logic (`if`, `in`), Custom Functions (`def`)  

## Scenario
As a security analyst, I developed an algorithm to parse a text file containing an IP address allow list and automatically remove IP addresses that no longer have access to restricted content. This automated the process of updating access control lists, ensuring that only authorized IP addresses remain in the configuration file.

---

## Task 1: Initializing Variables
*   **Action:** I defined the target filename and the list of IP addresses to be removed from the allow list.
*   **Code:**
    ```python
    # Assign `import_file` to the name of the file 
    import_file = "allow_list.txt"

    # Assign `remove_list` to a list of IP addresses that are no longer allowed to access restricted information. 
    remove_list = ["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"]

    # Display `import_file`
    print(import_file)

    # Display `remove_list`
    print(remove_list)
    ```
*   **Output:** 
    ```text
    allow_list.txt
    ['192.168.97.225', '192.168.158.170', '192.168.201.40', '192.168.58.57']
    ```
*   **Observation:** Both variables displayed their respective contents, confirming the successful initialization of the target file path and the exclusion list.

---

## Task 2: Opening the File (Incomplete Block)
*   **Action:** I wrote the first line of the `with` statement to open the file in read mode to observe the behavior of an incomplete context manager.
*   **Code:**
    ```python
    # Assign `import_file` to the name of the file 
    import_file = "allow_list.txt"

    # Assign `remove_list` to a list of IP addresses that are no longer allowed to access restricted information. 
    remove_list = ["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"]

    # First line of `with` statement
    with open(import_file, "r") as file:
    ```
*   **Output:** 
    ```text
    File "<ipython-input-2-b925af1022fc>", line 11
        with open(import_file, "r") as file:
                                            ^
    SyntaxError: unexpected EOF while parsing
    ```
*   **Observation:** Running an incomplete `with` block throws a syntax error, confirming that the context manager requires an indented body to execute properly.

---

## Task 3: Reading the File Contents
*   **Action:** I completed the `with` statement to read the file into a string variable and displayed the raw data.
*   **Code:**
    ```python
    # Assign `import_file` to the name of the file 
    import_file = "allow_list.txt"

    # Assign `remove_list` to a list of IP addresses that are no longer allowed to access restricted information. 
    remove_list = ["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"]

    # Build `with` statement to read in the initial contents of the file
    with open(import_file, "r") as file:

      # Use `.read()` to read the imported file and store it in a variable named `ip_addresses`
      ip_addresses = file.read()

    # Display `ip_addresses`
    print(ip_addresses)
    ```
*   **Output:** 
    ```text
    ip_address
    192.168.25.60
    192.168.205.12
    --------------
    192.168.6.9
    192.168.52.90
    --------------
    192.168.156.224
    192.168.60.153
    192.168.58.57
    192.168.69.116
    ```
*   **Observation:** Reading the file shows each IP on a separate line, which means the file uses newline characters for organization. This vertical format is more structured than a space-separated string, making it easier to parse and manipulate individual IP addresses when removing entries from the allow list.

---

## Task 4: Converting String to List
*   **Action:** I used the `.split()` method to convert the raw string into an iterable list of individual IP addresses.
*   **Code:**
    ```python
    # Assign `import_file` to the name of the file 
    import_file = "allow_list.txt"

    # Assign `remove_list` to a list of IP addresses that are no longer allowed to access restricted information. 
    remove_list = ["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"]

    # Build `with` statement to read in the initial contents of the file
    with open(import_file, "r") as file:

      # Use `.read()` to read the imported file and store it in a variable named `ip_addresses`
      ip_addresses = file.read()

    # Use `.split()` to convert `ip_addresses` from a string to a list
    ip_addresses = ip_addresses.split()

    # Display `ip_addresses`
    print(ip_addresses)
    ```
*   **Output:** 
    ```text
    ['ip_address', '192.168.25.60', '192.168.205.12', '192.168.97.225', '192.168.6.9', '192.168.52.90', '192.168.158.170', '192.168.90.124', '192.168.186.176', '192.168.133.188', '192.168.203.198', '192.168.201.40', '192.168.218.219', '192.168.52.37', '192.168.156.224', '192.168.60.153', '192.168.58.57', '192.168.69.116']
    ```
*   **Observation:** The `.split()` method successfully transformed the single string into an iterable list, allowing for programmatic access to each individual IP address for conditional checking.

---

## Task 5: Iterating Through the List
*   **Action:** I built a `for` loop to iterate through the `ip_addresses` list and display each element.
*   **Code:**
    ```python
    # Assign `import_file` to the name of the file 
    import_file = "allow_list.txt"

    # Assign `remove_list` to a list of IP addresses that are no longer allowed to access restricted information. 
    remove_list = ["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"]

    # Build `with` statement to read in the initial contents of the file
    with open(import_file, "r") as file:

      # Use `.read()` to read the imported file and store it in a variable named `ip_addresses`
      ip_addresses = file.read()

    # Use `.split()` to convert `ip_addresses` from a string to a list
    ip_addresses = ip_addresses.split()

    # Build iterative statement
    # Name loop variable `element`
    # Loop through `ip_addresses`
    for element in ip_addresses:

        # Display `element` in every iteration
        print(element)
    ```
*   **Output:** 
    ```text
    ip_address
    192.168.25.60
    192.168.205.12
    192.168.52.90
    --------------
    192.168.90.124
    192.168.186.176
    192.168.133.188
    --------------
    192.168.156.224
    
    ```
*   **Observation:** The iterative statement successfully traversed the list, verifying that each IP address could be accessed individually and sequentially.

---

## Task 6: Removing Unauthorized IPs
*   **Action:** I nested an `if` conditional inside the `for` loop to check if the current IP was in the `remove_list` and used `.remove()` to delete it.
*   **Code:**
    ```python
    # Assign `import_file` to the name of the file 
    import_file = "allow_list.txt"

    # Assign `remove_list` to a list of IP addresses that are no longer allowed to access restricted information. 
    remove_list = ["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"]

    # Build `with` statement to read in the initial contents of the file
    with open(import_file, "r") as file:

      # Use `.read()` to read the imported file and store it in a variable named `ip_addresses`
      ip_addresses = file.read()

    # Use `.split()` to convert `ip_addresses` from a string to a list
    ip_addresses = ip_addresses.split()

    # Build iterative statement
    # Name loop variable `element`
    # Loop through `ip_addresses`
    for element in ip_addresses:
      
      # Build conditional statement
      # If current element is in `remove_list`,
        if element in remove_list:

            # then current element should be removed from `ip_addresses`
            ip_addresses.remove(element)

    # Display `ip_addresses` 
    print(ip_addresses)
    ```
*   **Output:** 
    ```text
    ['ip_address', '192.168.25.60', '192.168.205.12', '192.168.6.9', '192.168.52.90', '192.168.90.124', '192.168.186.176', '192.168.133.188', '192.168.203.198', '192.168.218.219', '192.168.52.37', '192.168.156.224', '192.168.60.153', '192.168.69.116']
    ```
*   **Observation:** The combination of the `for` loop and the `if element in remove_list` condition successfully identified and removed the unauthorized IP addresses from the active list in memory.

---

## Task 7: Rewriting the File
*   **Action:** I converted the updated list back to a string using `.join()` and overwrote the original file using write mode ("w").
*   **Code:**
    ```python
    # Assign `import_file` to the name of the file 
    import_file = "allow_list.txt"

    # Assign `remove_list` to a list of IP addresses that are no longer allowed to access restricted information. 
    remove_list = ["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"]

    # Build `with` statement to read in the initial contents of the file
    with open(import_file, "r") as file:

      # Use `.read()` to read the imported file and store it in a variable named `ip_addresses`
      ip_addresses = file.read()

    # Use `.split()` to convert `ip_addresses` from a string to a list
    ip_addresses = ip_addresses.split()

    # Build iterative statement
    # Name loop variable `element`
    # Loop through `ip_addresses`
    for element in ip_addresses:
      
      # Build conditional statement
      # If current element is in `remove_list`,
        if element in remove_list:

            # then current element should be removed from `ip_addresses`
            ip_addresses.remove(element)

    # Convert `ip_addresses` back to a string so that it can be written into the text file 
    ip_addresses = " ".join(ip_addresses)       

    # Build `with` statement to rewrite the original file
    with open(import_file, "w") as file:

      # Rewrite the file, replacing its contents with `ip_addresses`
      file.write(ip_addresses)
    ```
*   **Output:** 
    ```text
    (No output; file is written to disk)
    ```
*   **Observation:** Using `.join()` converted the list back to a string format required for file writing, and opening the file with the "w" parameter successfully overwrote the old allow list with the updated, sanitized list.

---

## Task 8: Verifying the Updated File
*   **Action:** I opened the file again in read mode to verify that the unauthorized IPs were permanently removed from the disk.
*   **Code:**
    ```python
    # Assign `import_file` to the name of the file 
    import_file = "allow_list.txt"

    # Assign `remove_list` to a list of IP addresses that are no longer allowed to access restricted information. 
    remove_list = ["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"]

    # Build `with` statement to read in the initial contents of the file
    with open(import_file, "r") as file:

      # Use `.read()` to read the imported file and store it in a variable named `ip_addresses`
      ip_addresses = file.read()

    # Use `.split()` to convert `ip_addresses` from a string to a list
    ip_addresses = ip_addresses.split()

    # Build iterative statement
    # Name loop variable `element`
    # Loop through `ip_addresses`
    for element in ip_addresses:
      
      # Build conditional statement
      # If current element is in `remove_list`,
        if element in remove_list:

            # then current element should be removed from `ip_addresses`
            ip_addresses.remove(element)

    # Convert `ip_addresses` back to a string so that it can be written into the text file 
    ip_addresses = " ".join(ip_addresses)       

    # Build `with` statement to rewrite the original file
    with open(import_file, "w") as file:

      # Rewrite the file, replacing its contents with `ip_addresses`
      file.write(ip_addresses)

    # Build `with` statement to read in the updated file
    with open(import_file, "r") as file:

        # Read in the updated file and store the contents in `text`
        text = file.read()

    # Display the contents of `text`
    print(text)
    ```
*   **Output:** 
    ```text
    ip_address 192.168.25.60 192.168.205.12 192.168.6.9 192.168.52.90 192.168.90.124 192.168.186.176 192.168.133.188 192.168.203.198 192.168.218.219 192.168.52.37 192.168.156.224 192.168.60.153 192.168.69.116
    ```
*   **Observation:** Reading the file confirmed that the unauthorized IP addresses were successfully purged from the disk file, completing the automated update process.

---

## Task 9: Encapsulating Logic in a Function
*   **Action:** I wrapped the entire parsing and updating logic into a reusable `update_file()` function.
*   **Code:**
    ```python
    # Define a function named `update_file` that takes in two parameters: `import_file` and `remove_list`
    # and combines the steps you've written in this lab leading up to this
    def update_file(import_file, remove_list):

        # Build `with` statement to read in the initial contents of the file
        with open(import_file, "r") as file:

            # Use `.read()` to read the imported file and store it in a variable named `ip_addresses`
            ip_addresses = file.read()

        # Use `.split()` to convert `ip_addresses` from a string to a list
        ip_addresses = ip_addresses.split()

        # Build iterative statement
        # Name loop variable `element`
        # Loop through `ip_addresses`
        for element in ip_addresses:

            # Build conditional statement
            # If current element is in `remove_list`,
            if element in remove_list:

                # then current element should be removed from `ip_addresses`
                ip_addresses.remove(element)

        # Convert `ip_addresses` back to a string so that it can be written into the text file 
        ip_addresses = " ".join(ip_addresses)       

        # Build `with` statement to rewrite the original file
        with open(import_file, "w") as file:

            # Rewrite the file, replacing its contents with `ip_addresses`
            file.write(ip_addresses)
    ```
*   **Output:** 
    ```text
    (No output; function is defined)
    ```
*   **Observation:** Encapsulating the algorithm into a single function makes the code modular, reusable, and easier to maintain. It allows the security analyst to update any allow list file with any removal list by simply passing the arguments, rather than rewriting the logic.

---

## Task 10: Executing the Function
*   **Action:** I called the `update_file()` function with a new removal list and verified the final file state.
*   **Code:**
    ```python
    # Define a function named `update_file` that takes in two parameters: `import_file` and `remove_list`
    # and combines the steps you've written in this lab leading up to this
    def update_file(import_file, remove_list):

      # Build `with` statement to read in the initial contents of the file
      with open(import_file, "r") as file:

        # Use `.read()` to read the imported file and store it in a variable named `ip_addresses`
        ip_addresses = file.read()

      # Use `.split()` to convert `ip_addresses` from a string to a list
      ip_addresses = ip_addresses.split()

      # Build iterative statement
      # Name loop variable `element`
      # Loop through `ip_addresses`
      for element in ip_addresses:
        
        # Build conditional statement
        # If current element is in `remove_list`,
        if element in remove_list:

          # then current element should be removed from `ip_addresses`
          ip_addresses.remove(element)

      # Convert `ip_addresses` back to a string so that it can be written into the text file 
      ip_addresses = " ".join(ip_addresses)       

      # Build `with` statement to rewrite the original file
      with open(import_file, "w") as file:

        # Rewrite the file, replacing its contents with `ip_addresses`
        file.write(ip_addresses)

    # Call `update_file()` and pass in "allow_list.txt" and a list of IP addresses to be removed
    update_file("allow_list.txt", ["192.168.25.60", "192.168.140.81", "192.168.203.198"])

    # Build `with` statement to read in the updated file
    with open("allow_list.txt", "r") as file:

      # Read in the updated file and store the contents in `text`
      text = file.read()

    # Display the contents of `text`
    print(text)
    ```
*   **Output:** 
    ```text
    ip_address 192.168.205.12 192.168.6.9 192.168.52.90 192.168.90.124 192.168.186.176 192.168.133.188 192.168.218.219 192.168.52.37 192.168.156.224 192.168.60.153 192.168.69.116
    ```
*   **Observation:** The function executed flawlessly, removing the newly specified IPs and updating the file. This demonstrates the power of automating routine access control maintenance through custom Python functions.

---

## Technical Takeaways
1. **File Parsing Pipeline:** Combining `.read()`, `.split()`, and `.join()` provides a robust pipeline for reading structured text files, modifying the data in memory, and writing it back to disk.
2. **Iterative Filtering:** Using a `for` loop combined with the `in` operator and `.remove()` is an effective method for sanitizing lists based on a secondary exclusion list.
3. **Function Encapsulation:** Wrapping file I/O and data manipulation logic into a custom function promotes the DRY (Don't Repeat Yourself) principle, making security automation scripts highly reusable and scalable.

---
*Note: This document outlines my hands-on practice and learning proficiency in Python file parsing, iterative data filtering, and automated access control list management required for cybersecurity operations.*