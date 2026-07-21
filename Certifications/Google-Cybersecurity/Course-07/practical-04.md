# Technical Exercise: Python String Manipulation for Security Automation

**Activity:** Work with Strings in Python  
**Environment:** Jupyter Notebook (Python)  
**Role Assumed:** Security Analyst  
**Tools Utilized:** Python, String Methods (`str()`, `.index()`), String Slicing, String Concatenation, Conditional Logic  

## Scenario
As a security analyst, I automated the processing of string data by updating employee IDs to meet standardized formats, extracting specific characters from device IDs, and parsing URL components for network analysis and reporting.

---

## Task 1: Converting Data Types to Strings
*   **Action:** I converted a numeric employee ID into a string format to prepare it for standardized formatting.
*   **Code:**
    ```python
    # Assign `employee_id` to a four digit number as an initial value
    employee_id = 4186

    # Display the data type of `employee_id`
    print(type(employee_id))

    # Reassign `employee_id` to the same value but in the form of a string
    employee_id = "4186"

    # Display the data type of `employee_id` now
    print(type(employee_id))
    ```
*   **Output:** 
    ```text
    <class 'int'>
    <class 'str'>
    ```
*   **Observation:** The data type of `employee_id` changed upon reassignment. It initially displayed as an integer class, and after reassignment, it correctly displayed as a string class (`<class 'str'>`), which is required for string manipulation operations.

---

## Task 2: Validating String Length
*   **Action:** I implemented a conditional statement to check if the employee ID meets the new five-digit standardization criteria.
*   **Code:**
    ```python
    # Assign `employee_id` to a four digit number as an initial value
    employee_id = 4186

    # Reassign `employee_id` to the same value but in the form of a string
    employee_id = str(employee_id)

    # Conditional statement that displays a message if the length of `employee_id` is less than five digits
    if len(employee_id) < 5:
        print("This employee ID has less than five digits. It does not meet length requirements.")
    ```
*   **Output:** 
    ```text
    This employee ID has less than five digits. It does not meet length requirements.
    ```
*   **Observation:** The `len()` function accurately evaluated the string length. Since the ID was four characters long, the condition evaluated to `True`, triggering the compliance warning message.

---

## Task 3: String Concatenation for ID Standardization
*   **Action:** I used string concatenation to automatically prefix a non-compliant four-digit ID with an "E" to meet the five-character requirement.
*   **Code:**
    ```python
    # Assign `employee_id` to a four digit number as an initial value
    employee_id = 4186

    # Reassign `employee_id` to the same value but in the form of a string
    employee_id = str(employee_id)

    # Display the `employee_id` as it currently stands
    print(employee_id)

    # Conditional statement that updates the `employee_id` if its length is less than 5 digits
    if len(employee_id) < 5:
        employee_id = "E" + employee_id
        
    # Display the `employee_id` after the update
    print(employee_id)
    ```
*   **Output:** 
    ```text
    4186
    E4186
    ```
*   **Observation:** The script successfully identified the length deficiency and used the `+` operator to concatenate "E" with the original string, dynamically updating the variable to a compliant five-character format.

---

## Task 4: Extracting Specific Characters via Indexing
*   **Action:** I extracted a specific character from a device ID string using zero-based indexing.
*   **Code:**
    ```python
    # Assign `device_id` to a string that contains alphanumeric characters
    device_id = "r262c36"

    # Extract the fourth character in `device_id` and display it
    print(device_id[3])
    ```
*   **Output:** 
    ```text
    2
    ```
*   **Observation:** Using bracket notation with index `3` successfully retrieved the fourth character ("2") from the string, demonstrating Python's zero-based indexing system.

---

## Task 5: Extracting Substrings via Slicing
*   **Action:** I extracted a sequence of characters (the first through third characters) from the device ID using string slicing.
*   **Code:**
    ```python
    # Assign `device_id` to a string that contains alphanumeric characters
    device_id = "r262c36"

    # Extract the first through the third characters in `device_id` and display the result
    print(device_id[0:3])
    ```
*   **Output:** 
    ```text
    r26
    ```
*   **Observation:** The slice `[0:3]` correctly captured characters at indices 0, 1, and 2, stopping before index 3. This is a fundamental technique for isolating specific segments of structured identifier strings.

---

## Task 6: Parsing URL Protocols
*   **Action:** I extracted the protocol and syntax (`https://`) from a URL string using fixed-index slicing.
*   **Code:**
    ```python
    # Assign `url` to a specific URL
    url = "https://exampleURL1.com"

    # Extract the protocol of `url` along with the syntax following it, display the result
    print(url[0:8])
    ```
*   **Output:** 
    ```text
    https://
    ```
*   **Observation:** Slicing from index 0 to 8 cleanly isolated the secure protocol prefix, which is a common first step in URL parsing and validation scripts.

---

## Task 7: Locating Substrings with `.index()`
*   **Action:** I used the `.index()` string method to find the starting position of the domain extension within the URL.
*   **Code:**
    ```python
    # Assign `url` to a specific URL
    url = "https://exampleURL1.com"

    # Display the index where the domain extension ".com" is located in `url`
    print(url.index(".com"))
    ```
*   **Output:** 
    ```text
    19
    ```
*   **Observation:** The `.index()` method accurately returned `19`, which is the zero-based index where the substring ".com" begins in the URL string.

---

## Task 8: Storing Index Values in Variables
*   **Action:** I stored the output of the `.index()` method in a variable named `ind` for reuse in subsequent operations.
*   **Code:**
    ```python
    # Assign `url` to a specific URL
    url = "https://exampleURL1.com"

    # Assign `ind` to the output of applying `.index()` to `url` in order to extract the starting index of ".com" in `url` 
    ind = url.index(".com")
    ```
*   **Output:** 
    ```text
    (No output; value is stored in variable)
    ```
*   **Observation:** Storing the index position in a variable prevents redundant method calls and allows for dynamic, reusable string manipulation logic.

---

## Task 9: Dynamic String Slicing
*   **Action:** I used the stored `ind` variable to dynamically slice and extract the exact domain extension from the URL.
*   **Code:**
    ```python
    # Assign `url` to a specific URL
    url = "https://exampleURL1.com"

    # Assign `ind` to the output of applying `.index()` to `url` in order to extract the starting index of ".com" in `url` 
    ind = url.index(".com")

    # Extract the domain extension in `url` and display it
    print(url[ind:ind+4])
    ```
*   **Output:** 
    ```text
    .com
    ```
*   **Observation:** By storing the index position in the variable `ind`, I could reuse it to dynamically slice out the exact domain extension (`.com`). This makes the code adaptable to URLs of varying lengths, as the slice adjusts relative to the found index.

---

## Task 10: Extracting the Domain Name
*   **Action:** I combined fixed and dynamic indexing to extract the core website name from the URL, isolating it between the protocol and the domain extension.
*   **Code:**
    ```python
    # Assign `url` to a specific URL
    url = "https://exampleURL1.com"

    # Assign `ind` to the output of applying `.index()` to `url` in order to extract the starting index of ".com" in `url` 
    ind = url.index(".com")

    # Extract the website name in `url` and display it
    print(url[8:ind])
    ```
*   **Output:** 
    ```text
    exampleURL1
    ```
*   **Observation:** Slicing from index `8` (the end of `https://`) to the dynamically determined `ind` variable cleanly isolated the core domain name, demonstrating precise control over string segmentation.

---

## Technical Takeaways
1. **Data Type Conversion:** Explicitly converting integers to strings using `str()` is a prerequisite for applying string-specific methods and concatenation operations.
2. **Dynamic Slicing:** Combining the `.index()` method with slice notation (e.g., `[ind:ind+4]`) creates robust, adaptable code that can parse strings of varying lengths without hardcoding absolute end indices.
3. **String Concatenation:** The `+` operator provides a simple, effective way to merge strings dynamically, which is highly useful for standardizing identifiers like employee or device IDs.
4. **Zero-Based Indexing:** Understanding Python's zero-based indexing and exclusive upper bounds in slicing (e.g., `[0:3]` gets indices 0, 1, 2) is critical for accurately extracting substrings.

---
*Note: This document outlines my hands-on practice and learning proficiency in Python string manipulation, data type conversion, dynamic string slicing, and automated data parsing required for cybersecurity operations.*