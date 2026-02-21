# Python Event Driven Keylogger

##Project Overview
This project is a Proof-of-Concept (POC) implementation of a software-based keylogger. It uses an event-driven architecture to intercept and log keyboard interrupts into a raw text file. This tool was developed to study OS-level hooks, asynchronous event handling, and system resource management.

##Technical ImplementationLanguage:
Python 3.12+
Core Library: pynput for global keyboard event interception.
Architecture: Event-driven (asynchronous) to ensure near-zero CPU overhead.
Storage Module: Sequential file I/O using UTF-8 encoding.
Error Handling: Implemented try-except blocks to handle non-alphanumeric "Special Keys."

##Getting Started
Prerequisites:
Python 3.12 or higher
pip (Python package manager).

Installation
Clone the repository:
//Bash
git clone https://github.com/yourusername/keylogger-poc.git
//

Install dependencies:
//Bash
pip install pynput
//

Running the Tool
//Bash
python keylogger.py
//

Note: On macOS, you must grant Accessibility permissions to your terminal. On Windows, run as Administrator for full system-wide logging.

##Complexity Analysis
Time Complexity: $O(n)$ — The processing time scales linearly with the number of keystrokes.
Space Complexity: $O(n)$ — The log file grows incrementally based on user input.
Performance: Designed to operate at <1% CPU usage to avoid system detection.

##Limitations & Ethical DisclaimerThis project is for EDUCATIONAL PURPOSES ONLY. * Stealth: This script is easily detectable by modern Antivirus heuristic engines.
Security: Logs are stored in Plain Text. This implementation does not include encryption or network exfiltration.
Ethics: Unauthorized use of this tool on a device you do not own is illegal. Always obtain explicit, written consent before monitoring any system.

## Future Improvements:
Implement AES-256 Encryption for log files.
Add a GUI Dashboard using CustomTkinter.
Integrate Email/Cloud Exfiltration modules.
Add Anomaly Detection based on typing rhythm (Dwell Time).
