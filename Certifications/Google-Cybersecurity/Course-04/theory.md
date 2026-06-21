# Course 04: Tools of The Trade: Linux and SQL

## 📅 Date Started: 2026-06-12
## 📅 Date Completed: 2026-06-22

## 🎯 What I Learned:

- Operating Systems & Virtualization: 
  - Explored OS types (Windows, macOS, Linux, ChromeOS, Android, iOS) and OS vulnerabilities, including legacy systems.
  - Learned the four-part interaction process: User → Application → Operating System → Hardware.
  - Understood firmware basics (BIOS and UEFI) and how Virtualization Technology allows OS environments to run on Virtual Machines (VMs) for safe, isolated testing.

- Linux Architecture & Distributions: 
  - Studied Linux components: User, Applications, Shell, Filesystem Hierarchy Standard (FHS), Kernel, and Hardware.
  - Mapped distribution lineages: Red Hat (parent of CentOS), Slackware (parent of SUSE), and Debian (parent of Ubuntu and Kali Linux).
  - Utilized security-focused distros (Kali Linux, Parrot, AlmaLinux, Ubuntu, CentOS) and industry tools (Metasploit, Burp Suite, John the Ripper, Autopsy, tcpdump, Wireshark).

- Linux Command Line (CLI) & Shells: 
  - Differentiated between Graphical User Interface (GUI) and Command-Line Interface (CLI).
  - Explored shell types: Bourne-Again Shell (bash), C Shell (csh), Korn Shell (ksh), Enhanced C shell (tcsh), and Z Shell (zsh).
  - Understood Input/Output streams: Standard input (stdin), standard output (stdout), and standard error (stderr).

- Linux Filesystem & Navigation: 
  - Navigated the Filesystem Hierarchy Standard (FHS): Root (/), /home (user directories), /bin (binaries), /etc (configurations), /tmp (temporary files), and /mnt (mounts).
  - Executed navigation commands: pwd, cd, and ls.

- Linux File Operations & Searching: 
  - Read file contents using cat, head, tail, and less (with navigation keys: Space, b, Up/Down arrows, q).
  - Managed files using mkdir, rmdir, touch, rm, mv (move/rename), cp (copy), and nano (text editor).
  - Searched and filtered data using grep, piping (|), and find (with options like -name, -iname, -mtime, -mmin).

- Linux Permissions & User Management: 
  - Modified file permissions using chmod.
  - Analyzed the risks of logging in as the root (superuser): security vulnerabilities, irreversible mistakes, and lack of accountability.
  - Managed users and privileges using sudo, useradd, userdel, usermod, and chown.
  - Utilized built-in Linux documentation commands for troubleshooting and learning, including help (shell built-ins), man (full manual pages), whatis (one-line descriptions), and apropos (keyword searching for manual pages).

- SQL Fundamentals & Query Structure: 
  - Explored relational databases and the role of SQL in analyzing large security datasets.
  - Constructed basic queries using SELECT (columns) and FROM (tables).
  - Organized query output using ORDER BY for ascending (default) and descending (DESC) sorting.

- SQL Filtering & Joins: 
  - Refined searches using the WHERE clause and operators: =, <, >, <=, >=, <>, AND, OR, NOT, and BETWEEN.
  - Used pattern matching with the LIKE operator and wildcards: % (percentage sign for multiple characters) and _ (underscore for a single character).
  - Combined data from multiple tables using various join types:
    - INNER JOIN: Returns only the rows where there is a match in a specified common column between the two tables.
    - LEFT JOIN: Returns all rows from the left table, and the matched rows from the right table (returns NULL if no match is found).
    - RIGHT JOIN: Returns all rows from the right table, and the matched rows from the left table (returns NULL if no match is found).
    - FULL JOIN: Returns all rows when there is a match in either the left or right table.

- SQL Aggregate Functions & Core Terminology: 
  - Applied aggregate functions for data analysis: COUNT (number of rows), AVG (average of numerical data), and SUM (total of numerical data).
  - Mastered core database terms: Primary keys (unique row identifiers), Foreign keys (links to primary keys in other tables), Relational databases, Queries, Syntax, and Data types (String, Numeric, Date/Time).

## 💡 Key Takeaways:
- Linux is the industry standard for cybersecurity professionals due to its powerful CLI, open-source transparency, and granular system control.
- Mastering the Filesystem Hierarchy Standard (FHS) and basic CLI navigation is critical for operating efficiently in environments without a GUI.
- Root access is powerful but dangerous; relying on sudo and standard user accounts enforces accountability and prevents catastrophic system errors.
- Knowing how to use built-in help tools (man, apropos, whatis) is a vital survival skill in Linux, allowing you to learn and troubleshoot directly from the terminal without relying on external search engines.
- SQL is an essential analytical tool for security analysts, enabling the rapid querying, filtering, and correlation of massive datasets (like system logs).
- Understanding relational database structures and the different types of SQL joins allows analysts to perform comprehensive data correlation and uncover hidden patterns across multiple tables.

## 🔗 Links/Resources:
- [Google Cybersecurity Professional Certificate](https://www.coursera.org/professional-certificates/google-cybersecurity)
- [Linux Command Cheat Sheet](https://www.guru99.com/linux-commands-cheat-sheet.html)
- [SQL Tutorial - W3Schools](https://www.w3schools.com/sql/)
- [Unix and Linux Stack Exchange](https://unix.stackexchange.com)


---

🎓 Google Cybersecurity Professional Certificate | Course 4 of 8    