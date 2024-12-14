# VULNER

This project involves creating a script for comprehensive network device mapping, identifying ports, services, and vulnerabilities. The user defines the network range, after which the program deploys tools like nmap and masscan for scanning and mapping purposes, storing the data in a newly created directory. The script also probes for network vulnerabilities, employing nmap, searchsploit, hydra,  to identify security gaps, such as weak passwords. Finally, the scan summary and findings are presented to the user.

## Automation Script Overview and Explanation

### 1. Script Execution

- The script must be run as a **ROOT** user. If not, execution cannot proceed.
- If the user is correctly identified as **ROOT**, the process continues.

### 2. Scan Options

- The user must choose between a **New Scan** or reviewing a **Previous Scan**.

#### a. New Scan

- If selected, the user must choose between:
  - **Basic Scan:**

    - The user inputs IP addresses.
    - The addresses' validity is checked before scanning.
    - The scan uses **Masscan** for IP address scanning and **Nmap** for port scanning (both TCP and UDP).
    - Results are saved in **TXT** and **XML** formats.
    - The user may use **Hydra** for brute-forcing services like SSH, FTP, RDP, and Telnet, using specified user and password files.
    - Results are saved as a text file.
    - The system can compress results into a **ZIP** file.

  - **Full Scan:**

    - Similar to the basic scan but utilizes **Nmap Scripting Engine (NSE)** for deeper vulnerability detection.
    - Results are saved in **XML** format and converted to an easily readable **HTML** file.

#### b. Previous Scan

- The user inputs an IP address to check if a scan was previously conducted.
- The system verifies and displays prior scan results.

### 3. Additional Notes

- Address validation and file integrity checks occur throughout the process.
- The script indicates the current stage of execution.
- All results are saved in **XML** format and converted into a readable **HTML** file.
- The system compresses results, including all relevant folders and files, into a **ZIP** file.

