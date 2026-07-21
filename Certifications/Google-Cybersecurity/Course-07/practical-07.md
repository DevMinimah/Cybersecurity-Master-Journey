# Technical Exercise: Python File I/O and Log Parsing for Security Analysis

**Activity:** Import and Parse a Text File  
**Environment:** Jupyter Notebook (Python)  
**Role Assumed:** Security Analyst  
**Tools Utilized:** Python, File I/O (`open()`, `.read()`, `.write()`, `.split()`), Context Managers (`with` statement)  

## Scenario
As a security analyst, I automated the ingestion and parsing of security log files for analysis. This included reading raw log data, structuring it into lists, appending missing log entries to maintain chronological integrity, and generating a formatted text file documenting approved IP addresses for restricted access.

---

## Task 1: Opening the Log File
*   **Action:** I opened the security log file in read mode using a context manager to prepare it for ingestion.
*   **Code:**
    ```python
    # Assign `import_file` to the name of the text file that contains the security log file
    import_file = "login.txt"

    # First line of the `with` statement
    # Use `open()` to import security log file and store it as a string
    with open(import_file, "r") as file:
    ```
*   **Output:** 
    ```text
    (No output; file is opened in context)
    ```
*   **Observation:** The `with` statement safely opens the file and ensures it is automatically closed after the block executes, preventing resource leaks and file lock issues.

---

## Task 2: Reading the Raw Log Data
*   **Action:** I used the `.read()` method to ingest the entire file into a single string variable and displayed the raw data.
*   **Code:**
    ```python
    # Assign `import_file` to the name of the text file that contains the security log file
    import_file = "login.txt"

    # The `with` statement
    # Use `open()` to import security log file and store it as a string
    with open(import_file, "r") as file:

      # Use `.read()` to read the imported file and store the result in a variable named `text`
      text = file.read()

    # Display the contents of `text`
    print(text)
    ```
*   **Output:** 
    ```text
    username,ip_address,time,date
    tshah,192.168.92.147,15:26:08,2022-05-10
    dtanaka,192.168.98.221,9:45:18,2022-05-09
    ... (truncated for brevity) ...
    eraab,192.168.24.12,11:29:27,2022-05-11
    jsoto,192.168.25.60,5:09:21,2022-05-09
    ```
*   **Observation:** The `.read()` method successfully ingested the entire file into a single continuous string, preserving the original comma-separated values and newline characters for further processing.

---

## Task 3: Structuring Data with `.split()`
*   **Action:** I split the raw log string into a list of individual line strings to make the data iterable.
*   **Code:**
    ```python
    # Assign `import_file` to the name of the text file that contains the security log file
    import_file = "login.txt"

    # The `with` statement
    # Use `open()` to import security log file and store it as a string
    with open(import_file, "r") as file:

      # Use `.read()` to read the imported file and store the result in a variable named `text`
      text = file.read()

    # Display the contents of `text` split into separate lines 
    print(text.split())
    ```
*   **Output:** 
    ```text
    ['username,ip_address,time,date', 'tshah,192.168.92.147,15:26:08,2022-05-10', 'dtanaka,192.168.98.221,9:45:18,2022-05-09', 'tmitchel,192.168.110.131,14:13:41,2022-05-11', 'daquino,192.168.168.144,7:02:35,2022-05-08', 'eraab,192.168.170.243,1:45:14,2022-05-11', 'jlansky,192.168.238.42,1:07:11,2022-05-11', 'acook,192.168.52.90,9:56:48,2022-05-10', 'asundara,192.168.58.217,23:17:52,2022-05-12', 'jclark,192.168.214.49,20:49:00,2022-05-10', 'cjackson,192.168.247.153,19:36:42,]
    ```
*   **Observation:** Using `.split()` breaks the entire log file into individual words and tokens by whitespace, transforming one continuous string into a structured list.

---

## Task 4: Appending Missing Log Entries
*   **Action:** I appended a missing log entry to the file using append mode and verified the update by reading the file again.
*   **Code:**
    ```python
    # Assign `import_file` to the name of the text file that contains the security log file
    import_file = "login.txt"

    # Assign `missing entry` to a log that was not recorded in the log file
    missing_entry = "jrafael,192.168.243.140,4:56:27,2022-05-09"

    # Use `open()` to import security log file and store it as a string
    # Pass in "a" as the second parameter to indicate that the file is being opened for appending purposes
    with open(import_file, "a") as file:

        # Use `.write()` to append `missing_entry` to the log file
        file.write(missing_entry)

    # Use `open()` with the parameter "r" to open the security log file for reading purposes
    with open(import_file, "r") as file:

        # Use `.read()` to read in the contents of the log file and store in a variable named `text`
        text = file.read()

    # Display the contents of `text`
    print(text)
    ```
*   **Output:** 
    ```text
    username,ip_address,time,date
    tshah,192.168.92.147,15:26:08,2022-05-10
    ... (truncated for brevity) ...
    jsoto,192.168.25.60,5:09:21,2022-05-09
    jrafael,192.168.243.140,4:56:27,2022-05-09
    ```
*   **Observation:** Using 'a' mode with `.write()` adds the missing entry to the end of the log file without erasing existing data, unlike 'w' mode which would overwrite everything. This is critical for security logs because maintaining a complete, chronological record is essential for audits and investigations.

---

## Task 5: Defining the Allow List Variables
*   **Action:** I defined the filename and the string of approved IP addresses for the new allow list file.
*   **Code:**
    ```python
    # Assign `import_file` to the name of the text file that you want to create
    import_file = "allow_list.txt"

    # Assign `ip_addresses` to a list of IP addresses that are allowed to access the restricted information
    ip_addresses = "192.168.218.160 192.168.97.225 192.168.145.158 192.168.108.13 192.168.60.153 192.168.96.200 192.168.247.153 192.168.3.252 192.168.116.187 192.168.15.110 192.168.39.246"

    # Display `import_file`
    print(import_file)

    # Display `ip_addresses`
    print(ip_addresses)
    ```
*   **Output:** 
    ```text
    allow_list.txt
    192.168.218.160 192.168.97.225 192.168.145.158 192.168.108.13 192.168.60.153 192.168.96.200 192.168.247.153 192.168.3.252 192.168.116.187 192.168.15.110 192.168.39.246
    ```
*   **Observation:** Variables were successfully initialized to hold the target filename and the space-separated IP addresses, preparing the data for file creation.

---

## Task 6: Writing the Allow List to Disk
*   **Action:** I created the new text file and wrote the approved IP addresses to it using write mode.
*   **Code:**
    ```python
    # Assign `import_file` to the name of the text file that you want to create
    import_file = "allow_list.txt"

    # Assign `ip_addresses` to a list of IP addresses that are allowed to access the restricted information
    ip_addresses = "192.168.218.160 192.168.97.225 192.168.145.158 192.168.108.13 192.168.60.153 192.168.96.200 192.168.247.153 192.168.3.252 192.168.116.187 192.168.15.110 192.168.39.246"

    # Create a `with` statement to write to the text file 
    with open(import_file, "w") as file:

      # Write `ip_addresses` to the text file
       file.write(ip_addresses)
    ```
*   **Output:** 
    ```text
    (No output; file is written to disk)
    ```
*   **Observation:** The "w" parameter in `open()` created the `allow_list.txt` file and wrote the IP string to it. This mode overwrites any existing file with the same name, ensuring the allow list is exactly as specified.

---

## Task 7: Verifying the Written Allow List
*   **Action:** I read and displayed the contents of the newly created allow list file to verify the write operation.
*   **Code:**
    ```python
    # Assign `import_file` to the name of the text file that you want to create
    import_file = "allow_list.txt"

    # Assign `ip_addresses` to a list of IP addresses that are allowed to access the restricted information
    ip_addresses = "192.168.218.160 192.168.97.225 192.168.145.158 192.168.108.13 192.168.60.153 192.168.96.200 192.168.247.153 192.168.3.252 192.168.116.187 192.168.15.110 192.168.39.246"

    # Create a `with` statement to write to the text file 
    with open(import_file, "w") as file:

        # Write `ip_addresses` to the text file
        file.write(ip_addresses)

    # Create a `with` statement to read in the text file 
    with open(import_file, "r") as file:

        # Read the file and store the result in a variable named `text`
        text = file.read()

    # Display the contents of `text`
    print(text)
    ```
*   **Output:** 
    ```text
    192.168.218.160 192.168.97.225 192.168.145.158 192.168.108.13 192.168.60.153 192.168.96.200 192.168.247.153 192.168.3.252 192.168.116.187 192.168.15.110 192.168.39.246
    ```
*   **Observation:** Reading the file in "r" mode confirmed that the IP addresses were successfully persisted to disk, completing the automated generation of the approved IP documentation.

---

## Technical Takeaways
1. **Context Managers:** The `with` statement is the Pythonic standard for file I/O, ensuring files are properly closed and system resources are released even if exceptions occur during processing.
2. **File Modes:** Understanding the distinction between "r" (read), "w" (write/overwrite), and "a" (append) is critical for security log management; using "w" on a log file would destroy historical data, whereas "a" preserves it.
3. **Data Structuring:** Combining `.read()` with `.split()` allows analysts to quickly convert raw, unstructured text files into Python lists, making the data iterable and ready for programmatic analysis.
4. **Automated Reporting:** Using `.write()` to generate text files enables the automated creation of compliance documents, such as approved IP allow lists, directly from security scripts.

---
*Note: This document outlines my hands-on practice and learning proficiency in Python file I/O operations, log parsing, data structuring, and automated security reporting required for cybersecurity operations.*