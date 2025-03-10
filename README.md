# ShieldX-Defender

![GitHub Workflow Status](https://img.shields.io/github/workflow/status/the0ffs3c/ShieldX-Defender/CI)

## Overview

**ShieldX-Defender** is a Python-based antivirus scanner that integrates real-time file monitoring with YARA rule-based scanning and known malware hash detection. The software provides effective protection against malicious files by scanning files for known malware signatures, suspicious behaviors, and file types. 

This project allows users to easily integrate a local antivirus scanner into their systems with minimal configuration and offers a web dashboard to view scan results.

## Features

- **Real-time File Monitoring**: Automatically scans files when they're added or modified.
- **YARA Rule Integration**: Uses YARA rules for enhanced malware detection.
- **Known Malware Hash Checking**: Compares file hashes against a database of known malware hashes.
- **Web Dashboard**: View scan results through a real-time web interface (Flask-based).
- **Customizable Alerts**: Sends alerts for suspicious or malicious files.
- **Cross-Platform**: Works on Linux, Windows, and macOS.

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/the0ffs3c/ShieldX-Defender.git
   cd ShieldX-Defender
2. Set up the environment:
It's recommended to create a virtual environment to manage dependencies:
   ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
3. Install dependencies:
Run the following command to install the necessary dependencies:
    ```bash 
     pip install -r requirements.txt

4. Configure YARA Rules:
Ensure that your YARA rules are correctly placed in the data/yara_rules/ directory. You can find example rules in the data/yara_rules/ folder. You can add custom rules as well. To add your own YARA rules, just place them in the data/yara_rules/ folder and ensure they have the .yar extension.

5. Run the application:
Once the setup is complete, start the application by running:
   ```bash
   python antivirus.py
6. Access the dashboard:
Open your web browser and go to http://localhost:6969 to view the real-time web dashboard of scan results.
Usage
After successfully installing ShieldX-Defender, you can use it to scan files, monitor directories, and access results on the web dashboard.

Scanning Files
You can run the scanner on any file by calling the scan_file() method in the scanner.py module. For example:
   ```bash
scanner = AntiVirusScanner()
scanner.scan_file('/path/to/file')




