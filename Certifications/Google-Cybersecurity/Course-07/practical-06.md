# Technical Exercise: Python Regular Expressions for Log Analysis and Threat Triage

**Activity:** Use Regular Expressions to Find Patterns  
**Environment:** Jupyter Notebook (Python)  
**Role Assumed:** Security Analyst  
**Tools Utilized:** Python, `re` module, Regular Expressions (`\w`, `+`, `\d`, `\.`, `{1,3}`), `re.findall()`, Iterative Statements  

## Scenario
As a security analyst, I automated log analysis tasks using regular expressions to extract specific device IDs requiring OS updates and to identify valid IP addresses from a security log. I then cross-referenced the extracted valid IPs against a threat intelligence list of flagged addresses to prioritize incident investigation.

---

## Task 1: Importing the Regular Expression Module
*   **Action:** I imported the built-in `re` module to enable regular expression operations in Python.
*   **Code:**
    ```python
    # Import the `re` module in Python
    import re
    ```
*   **Output:** 
    ```text
    (No output; module imported successfully)
    ```
*   **Observation:** The `re` module is now available in the environment, providing access to functions like `re.findall()` for pattern matching.

---

## Task 2: Inspecting Raw Device Log Data
*   **Action:** I displayed the contents of a string containing a log of device IDs to understand the data structure.
*   **Code:**
    ```python
    # Assign `devices` to a string containing device IDs, each device ID represented by alphanumeric characters
    devices = "r262c36 67bv8fy 41j1u2e r151dm4 1270t3o 42dr56i r15xk9h 2j33krk 253be78 ac742a1 r15u9q5 zh86b2l ii286fq 9x482kt 6oa6m6u x3463ac i4l56nq g07h55q 081qc9t r159r1u"

    # Display the contents of `devices`
    print(devices)
    ```
*   **Output:** 
    ```text
    r262c36 67bv8fy 41j1u2e r151dm4 1270t3o 42dr56i r15xk9h 2j33krk 253be78 ac742a1 r15u9q5 zh86b2l ii286fq 9x482kt 6oa6m6u x3463ac i4l56nq g07h55q 081qc9t r159r1u
    ```
*   **Observation:** The raw log data is a single string containing mixed valid and invalid device IDs, requiring pattern matching to isolate the targets.

---

## Task 3: Defining the Target Regex Pattern
*   **Action:** I created a regular expression pattern to identify device IDs that start with "r15", indicating a specific operating system requiring an update.
*   **Code:**
    ```python
    # Assign `devices` to a string containing device IDs, each device ID represented by alphanumeric characters
    devices = "r262c36 67bv8fy 41j1u2e r151dm4 1270t3o 42dr56i r15xk9h 2j33krk 253be78 ac742a1 r15u9q5 zh86b2l ii286fq 9x482kt 6oa6m6u x3463ac i4l56nq g07h55q 081qc9t r159r1u"

    # Assign `target_pattern` to a regular expression pattern for finding device IDs that start with "r15"
    target_pattern = "r15\w+"
    ```
*   **Output:** 
    ```text
    (No output; variable assigned)
    ```
*   **Observation:** The pattern `"r15\w+"` specifically targets device IDs starting with "r15" followed by one or more alphanumeric characters. Without `r15`, it would match any alphanumeric string; without `\w+`, it would only match the first character after "r15".

---

## Task 4: Extracting Target Device IDs
*   **Action:** I used the `re.findall()` function to extract all device IDs matching the target pattern from the log string.
*   **Code:**
    ```python
    # Assign `devices` to a string containing device IDs, each device ID represented by alphanumeric characters
    devices = "r262c36 67bv8fy 41j1u2e r151dm4 1270t3o 42dr56i r15xk9h 2j33krk 253be78 ac742a1 r15u9q5 zh86b2l ii286fq 9x482kt 6oa6m6u x3463ac i4l56nq g07h55q 081qc9t r159r1u"

    # Assign `target_pattern` to a regular expression pattern for finding device IDs that start with "r15"
    target_pattern = "r15\w+"

    # Use `re.findall()` to find the device IDs that start with "r15" and display the results
    print(re.findall(target_pattern, devices))
    ```
*   **Output:** 
    ```text
    ['r151dm4', 'r15xk9h', 'r15u9q5', 'r159r1u']
    ```
*   **Observation:** The function successfully isolated and returned a list of all device IDs requiring updates, filtering out the irrelevant data in a single operation.

---

## Task 5: Inspecting Raw Network Log Data
*   **Action:** I displayed the contents of a network security log file to examine its structure and identify data quality issues.
*   **Code:**
    ```python
    # Assign `log_file` to a string containing username, date, login time, and IP address for a series of login attempts 
    log_file = "eraab 2022-05-10 6:03:41 192.168.152.148 \niuduike 2022-05-09 6:46:40 192.168.22.115 \nsmartell 2022-05-09 19:30:32 192.168.190.178 \narutley 2022-05-12 17:00:59 1923.1689.3.24 \nrjensen 2022-05-11 0:59:26 192.168.213.128 \naestrada 2022-05-09 19:28:12 1924.1680.27.57 \nasundara 2022-05-11 18:38:07 192.168.96.200 \ndkot 2022-05-12 10:52:00 1921.168.1283.75 \nabernard 2022-05-12 23:38:46 19245.168.2345.49 \ncjackson 2022-05-12 19:36:42 192.168.247.153 \njclark 2022-05-10 10:48:02 192.168.174.117 \nalevitsk 2022-05-08 12:09:10 192.16874.1390.176 \njrafael 2022-05-10 22:40:01 192.168.148.115 \nyappiah 2022-05-12 10:37:22 192.168.103.10654 \ndaquino 2022-05-08 7:02:35 192.168.168.144"

    # Display contents of `log_file`
    print(log_file)
    ```
*   **Output:** 
    ```text
    eraab 2022-05-10 6:03:41 192.168.152.148 
    iuduike 2022-05-09 6:46:40 192.168.22.115 
    ... (truncated for brevity) ...
    daquino 2022-05-08 7:02:35 192.168.168.144
    ```
*   **Observation:** The log file contains usernames, timestamps, and IP addresses, but also includes malformed/invalid IP addresses (e.g., `1923.1689.3.24`) due to data collection errors.

---

## Task 6: Defining a Strict IP Regex Pattern
*   **Action:** I created a regular expression pattern designed to match IP addresses with exactly three digits per segment.
*   **Code:**
    ```python
    # Assign `log_file` to a string containing username, date, login time, and IP address for a series of login attempts 
    log_file = "eraab 2022-05-10 6:03:41 192.168.152.148 \niuduike 2022-05-09 6:46:40 192.168.22.115 \nsmartell 2022-05-09 19:30:32 192.168.190.178 \narutley 2022-05-12 17:00:59 1923.1689.3.24 \nrjensen 2022-05-11 0:59:26 192.168.213.128 \naestrada 2022-05-09 19:28:12 1924.1680.27.57 \nasundara 2022-05-11 18:38:07 192.168.96.200 \ndkot 2022-05-12 10:52:00 1921.168.1283.75 \nabernard 2022-05-12 23:38:46 19245.168.2345.49 \ncjackson 2022-05-12 19:36:42 192.168.247.153 \njclark 2022-05-10 10:48:02 192.168.174.117 \nalevitsk 2022-05-08 12:09:10 192.16874.1390.176 \njrafael 2022-05-10 22:40:01 192.168.148.115 \nyappiah 2022-05-12 10:37:22 192.168.103.10654 \ndaquino 2022-05-08 7:02:35 192.168.168.144"

    # Assign `pattern` to a regular expression pattern that will match with IP addresses of the form xxx.xxx.xxx.xxx
    pattern = "\d\d\d\.\d\d\d\.\d\d\d\.\d\d\d"
    ```
*   **Output:** 
    ```text
    (No output; variable assigned)
    ```
*   **Observation:** This pattern is highly rigid. It will only match IPs with exactly three digits per segment, which will inevitably miss valid IPs that have 1 or 2 digits in a segment (e.g., `192.168.22.115`).

---

## Task 7: Extracting IPs with Strict Pattern
*   **Action:** I applied the strict pattern using `re.findall()` to observe its limitations.
*   **Code:**
    ```python
    # Assign `log_file` to a string containing username, date, login time, and IP address for a series of login attempts 
    log_file = "eraab 2022-05-10 6:03:41 192.168.152.148 \niuduike 2022-05-09 6:46:40 192.168.22.115 \nsmartell 2022-05-09 19:30:32 192.168.190.178 \narutley 2022-05-12 17:00:59 1923.1689.3.24 \nrjensen 2022-05-11 0:59:26 192.168.213.128 \naestrada 2022-05-09 19:28:12 1924.1680.27.57 \nasundara 2022-05-11 18:38:07 192.168.96.200 \ndkot 2022-05-12 10:52:00 1921.168.1283.75 \nabernard 2022-05-12 23:38:46 19245.168.2345.49 \ncjackson 2022-05-12 19:36:42 192.168.247.153 \njclark 2022-05-10 10:48:02 192.168.174.117 \nalevitsk 2022-05-08 12:09:10 192.16874.1390.176 \njrafael 2022-05-10 22:40:01 192.168.148.115 \nyappiah 2022-05-12 10:37:22 192.168.103.10654 \ndaquino 2022-05-08 7:02:35 192.168.168.144"

    # Assign `pattern` to a regular expression pattern that will match with IP addresses of the form xxx.xxx.xxx.xxx
    pattern = "\d\d\d\.\d\d\d\.\d\d\d\.\d\d\d"

    # Use the `re.findall()` function on `pattern` and `log_file` to extract the IP addresses of the form xxx.xxx.xxx.xxx and display the results
    print(re.findall(pattern, log_file))
    ```
*   **Output:** 
    ```text
    ['192.168.152.148', '192.168.190.178', '192.168.213.128', '192.168.247.153', '192.168.174.117', '192.168.148.115', '192.168.103.106', '192.168.168.144']
    ```
*   **Observation:** As predicted, valid IPs like `192.168.22.115` were missed because they do not have exactly three digits in every segment, demonstrating the need for a more flexible pattern.

---

## Task 8: Extracting IPs with Flexible Pattern (`+`)
*   **Action:** I updated the pattern to use the `+` quantifier, allowing one or more digits per segment.
*   **Code:**
    ```python
    # Assign `log_file` to a string containing username, date, login time, and IP address for a series of login attempts 
    log_file = "eraab 2022-05-10 6:03:41 192.168.152.148 \niuduike 2022-05-09 6:46:40 192.168.22.115 \nsmartell 2022-05-09 19:30:32 192.168.190.178 \narutley 2022-05-12 17:00:59 1923.1689.3.24 \nrjensen 2022-05-11 0:59:26 192.168.213.128 \naestrada 2022-05-09 19:28:12 1924.1680.27.57 \nasundara 2022-05-11 18:38:07 192.168.96.200 \ndkot 2022-05-12 10:52:00 1921.168.1283.75 \nabernard 2022-05-12 23:38:46 19245.168.2345.49 \ncjackson 2022-05-12 19:36:42 192.168.247.153 \njclark 2022-05-10 10:48:02 192.168.174.117 \nalevitsk 2022-05-08 12:09:10 192.16874.1390.176 \njrafael 2022-05-10 22:40:01 192.168.148.115 \nyappiah 2022-05-12 10:37:22 192.168.103.10654 \ndaquino 2022-05-08 7:02:35 192.168.168.144"

    # Update `pattern` to a regular expression pattern that will match with IP addresses with any variation in the number of digits per segment
    pattern = "\d+\.\d+\.\d+\.\d+"

    # Use the `re.findall()` function on `pattern` and `log_file` to extract the IP addresses of the updated form specifed above and display the results
    print(re.findall(pattern, log_file))
    ```
*   **Output:** 
    ```text
    ['192.168.152.148', '192.168.22.115', '192.168.190.178', '1923.1689.3.24', '192.168.213.128', '1924.1680.27.57', '192.168.96.200', '1921.168.1283.75', '19245.168.2345.49', '192.168.247.153', '192.168.174.117', '192.16874.1390.176', '192.168.148.115', '192.168.103.10654', '192.168.168.144']
    ```
*   **Observation:** While this captured the previously missed valid IPs, it also incorrectly extracted malformed, invalid IPs with more than three digits per segment (e.g., `1923.1689.3.24`), proving that `+` is too permissive.

---

## Task 9: Extracting Valid IPs with Bounded Quantifiers (`{1,3}`)
*   **Action:** I refined the pattern using curly brackets `{1,3}` to strictly match 1 to 3 digits per segment, filtering out invalid entries.
*   **Code:**
    ```python
    # Assign `log_file` to a string containing username, date, login time, and IP address for a series of login attempts 
    log_file = "eraab 2022-05-10 6:03:41 192.168.152.148 \niuduike 2022-05-09 6:46:40 192.168.22.115 \nsmartell 2022-05-09 19:30:32 192.168.190.178 \narutley 2022-05-12 17:00:59 1923.1689.3.24 \nrjensen 2022-05-11 0:59:26 192.168.213.128 \naestrada 2022-05-09 19:28:12 1924.1680.27.57 \nasundara 2022-05-11 18:38:07 192.168.96.200 \ndkot 2022-05-12 10:52:00 1921.168.1283.75 \nabernard 2022-05-12 23:38:46 19245.168.2345.49 \ncjackson 2022-05-12 19:36:42 192.168.247.153 \njclark 2022-05-10 10:48:02 192.168.174.117 \nalevitsk 2022-05-08 12:09:10 192.16874.1390.176 \njrafael 2022-05-10 22:40:01 192.168.148.115 \nyappiah 2022-05-12 10:37:22 192.168.103.10654 \ndaquino 2022-05-08 7:02:35 192.168.168.144"

    # Assign `pattern` to a regular expression that matches with all valid IP addresses and only those 
    pattern = "\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}"

    # Use `re.findall()` on `pattern` and `log_file` and assign `valid_ip_addresses` to the output 
    valid_ip_addresses = re.findall(pattern, log_file)

    # Display the contents of `valid_ip_addresses`
    print(valid_ip_addresses)
    ```
*   **Output:** 
    ```text
    ['192.168.152.148', '192.168.22.115', '192.168.190.178', '192.168.213.128', '192.168.96.200', '192.168.247.153', '192.168.174.117', '192.168.148.115', '192.168.103.106', '192.168.168.144']
    ```
*   **Observation:** The `{1,3}` quantifier perfectly balanced flexibility and validation. It successfully extracted all valid IPs while automatically filtering out the malformed entries with >3 digits per segment.

---

## Task 10: Loading Threat Intelligence Data
*   **Action:** I defined and displayed a list of known flagged IP addresses for cross-referencing.
*   **Code:**
    ```python
    # Assign `flagged_addresses` to a list of IP addresses that have been previously flagged for unusual activity
    flagged_addresses = ["192.168.190.178", "192.168.96.200", "192.168.174.117", "192.168.168.144"]

    # Display the contents of `flagged_addresses`
    print(flagged_addresses)
    ```
*   **Output:** 
    ```text
    ['192.168.190.178', '192.168.96.200', '192.168.174.117', '192.168.168.144']
    ```
*   **Observation:** The threat intelligence list is loaded and ready to be used as a reference for automated triage.

---

## Task 11: Automated Threat Triage Loop
*   **Action:** I wrote an iterative statement with a conditional to loop through the extracted valid IPs and check them against the flagged list.
*   **Code:**
    ```python
    # Assign `log_file` to a string containing username, date, login time, and IP address for a series of login attempts 
    log_file = "eraab 2022-05-10 6:03:41 192.168.152.148 \niuduike 2022-05-09 6:46:40 192.168.22.115 \nsmartell 2022-05-09 19:30:32 192.168.190.178 \narutley 2022-05-12 17:00:59 1923.1689.3.24 \nrjensen 2022-05-11 0:59:26 192.168.213.128 \naestrada 2022-05-09 19:28:12 1924.1680.27.57 \nasundara 2022-05-11 18:38:07 192.168.96.200 \ndkot 2022-05-12 10:52:00 1921.168.1283.75 \nabernard 2022-05-12 23:38:46 19245.168.2345.49 \ncjackson 2022-05-12 19:36:42 192.168.247.153 \njclark 2022-05-10 10:48:02 192.168.174.117 \nalevitsk 2022-05-08 12:09:10 192.16874.1390.176 \njrafael 2022-05-10 22:40:01 192.168.148.115 \nyappiah 2022-05-12 10:37:22 192.168.103.10654 \ndaquino 2022-05-08 7:02:35 192.168.168.144"

    # Assign `pattern` to a regular expression that matches with all valid IP addresses and only those 
    pattern = "\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}"

    # Use `re.findall()` on `pattern` and `log_file` and assign `valid_ip_addresses` to the output 
    valid_ip_addresses = re.findall(pattern, log_file)

    # Assign `flagged_addresses` to a list of IP addresses that have been previously flagged for unusual activity
    flagged_addresses = ["192.168.190.178", "192.168.96.200", "192.168.174.117", "192.168.168.144"]

    # Iterative statement begins here
    # Loop through `valid_ip_addresses` with `address` as the loop variable
    for address in valid_ip_addresses:

        # Conditional begins here
        # If `address` belongs to `flagged_addresses`, display "The IP address ______ has been flagged for further analysis."
        if address in flagged_addresses:
            print("The IP address", address, "has been flagged for further analysis.")

        # Otherwise, display "The IP address ______ does not require further analysis."
        else:
            print("The IP address", address, "does not require further analysis.")
    ```
*   **Output:** 
    ```text
    The IP address 192.168.152.148 does not require further analysis.
    The IP address 192.168.22.115 does not require further analysis.
    The IP address 192.168.190.178 has been flagged for further analysis.
    The IP address 192.168.213.128 does not require further analysis.
    The IP address 192.168.96.200 has been flagged for further analysis.
    The IP address 192.168.247.153 does not require further analysis.
    The IP address 192.168.174.117 has been flagged for further analysis.
    The IP address 192.168.148.115 does not require further analysis.
    The IP address 192.168.103.106 does not require further analysis.
    The IP address 192.168.168.144 has been flagged for further analysis.
    ```
*   **Observation:** The script successfully automated the triage process. It iterated through the cleaned list of valid IPs and instantly identified which ones matched the threat intelligence list, prioritizing them for immediate security investigation.

---

## Technical Takeaways
1. **Regex Quantifier Precision:** Choosing the right quantifier is critical. While `+` is flexible, it can over-match invalid data. Bounded quantifiers like `{1,3}` provide the exact validation needed for structured data like IP addresses.
2. **Automated Data Extraction:** The `re.findall()` function is a powerful tool for parsing unstructured or semi-structured log files, instantly converting raw text into actionable lists of indicators.
3. **Iterative Threat Triage:** Combining regex extraction with iterative `for` loops and `in` conditionals allows security analysts to automate the cross-referencing of log data against threat intelligence feeds, drastically reducing manual review time.

---
*Note: This document outlines my hands-on practice and learning proficiency in Python regular expressions, log parsing, data validation, and automated threat triage required for cybersecurity operations.*