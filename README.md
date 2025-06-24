# Directory Traversal Attack & Wireshark Analysis

I built this lab as part of CodePath’s CYB102 cybersecurity course to learn how attackers can exploit vulnerable file paths on FTP servers. The goal was to launch a Directory Traversal attack, extract sensitive files, and use a packet capture tool (PCAP) to determine what data was accessed.

## Scenario
You have been hired by the IRS to investigate the Fairly Oddparents Corp. They are suspected of some shady business and are withholding vital information about the company; we have been granted access to the company server and permission to access their files. The Fairly Oddparents Corp. has only publicly released what is found in the general folder, and announced their earnings in general/reports.txt... but Timmy, Wanda, and Cosmo are suspected to be hiding the original reports in their personal folders...

## Objective
Launch a Directory Traversal attack! Run attack.js on directories to see what's inside -- see if you can reveal the contents of an alternative version of the general/reports.txt!

## Tools & Technologies Used
- Ubuntu 22.04 LTS VM (Azure Lab or local VirtualBox)
- Bash scripting
- Node.js (for FTP server)
- Vim (for editing attack.sh)
- Wireshark (for PCAP analysis)

## What This Lab Does
- Spins up a vulnerable FTP server using a Node.js script
- Creates and executes a bash script (attack.sh) to launch a Directory Traversal attack
- Explores hidden or private folders (e.g., /timmy/, /wanda/, /cosmo/) to find restricted files
- Analyzes server.pcapng to identify which files were improperly accessed
- Reveals the truth behind misleading reports published by the Fairly Oddparents Corp

## Screenshots
### "attack.sh" - Traversal script built to probe hidden directories:
<img src="https://github.com/user-attachments/assets/0ac4509d-5db8-4589-85b0-b1f6bafec5a1" width="600"/>

### "server.pcapng" analysis - Viewing file access through Wireshark:
<img src="https://github.com/user-attachments/assets/c1a05b17-d3e0-4472-a98d-132397ac8eb5" width="600"/>

## Lessons Learned
This project helped me understand how insecure directory structures can be exploited using simple bash scripts and traversal techniques. I practiced scripting in Bash, navigating with Vim, and reviewing packet captures to trace unauthorized access. By identifying which internal reports were leaked, I saw how forensic analysis is critical in post-breach investigations and how important secure server configurations are in defending sensitive data.
