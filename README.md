# letschecksmb


# Let's Check SMB

It is a tool that can scan for and exploit vulnerabilities in the Server Message Block (SMB) protocol, which is used for file sharing and remote access in Windows networks. SMB vulnerabilities can allow attackers to execute arbitrary code, access sensitive data, or spread malware across the network.

## Features

- Scans for SMB vulnerabilities using nmap scripts
- Exploits SMB vulnerabilities using Metasploit modules
- Supports ms17-010 (EternalBlue), ms08-067 (NetAPI), and ms09-050 (SMBv2) vulnerabilities
- Provides a meterpreter shell for post-exploitation actions
- Generates reports in HTML, XML, or CSV formats

## Requirements

- Python 3.x
- Nmap
- Metasploit Framework
- Impacket

## Installation

Clone the repository using the following command:

`git clone https://github.com/user/SMB-Vuln-Scan-Exploit.git`

Change the directory to the cloned repository:

`cd SMB-Vuln-Scan-Exploit`

Install the required Python packages:

`pip install -r requirements.txt`

## Usage

Run the tool using the following command:

`python smb-vuln-scan-exploit.py -t target -p port -v vuln -e exploit -o output`

The arguments are as follows:

- `-t target`: The IP address or range of the target SMB host(s)
- `-p port`: The port number of the SMB service (default: 445)
- `-v vuln`: The vulnerability to scan for (ms17-010, ms08-067, or ms09-050)
- `-e exploit`: The exploit to use (eternalblue, netapi, or smb2)
- `-o output`: The output format (html, xml, or csv)

For example, to scan for and exploit ms17-010 vulnerability on host 192.168.1.10 using eternalblue exploit and generate an HTML report, use the following command:

`python smb-vuln-scan-exploit.py -t 192.168.1.10 -v ms17-010 -e eternalblue -o html`

The tool will first scan the target host using nmap scripts and check if it is vulnerable to ms17-010. If it is, it will launch the Metasploit module for eternalblue and try to get a meterpreter shell on the target system. If successful, it will display the shell prompt and allow you to perform post-exploitation actions. It will also save the scan and exploit results in an HTML file in the output folder.

## Disclaimer

This tool is for educational and research purposes only. Do not use it on any system without permission. I am not responsible for any damage or legal consequences caused by this tool. Use it at your own risk.
