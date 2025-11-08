````
# Laravel .env Scanner

`env-scanner.py` is a Python tool that scans multiple subdomains for exposed `.env` files. It automates checks by appending `/.env` to each target from a provided list (e.g., `subdomains.txt`). Discovered files are recorded to an output file (default: `hasil.txt`; override with `-o`). Ideal for security research, penetration testing, and bug bounty reconnaissance.

## Features

- Fast multi-threaded scanning
- Customizable thread count and request timeout
- Saves valid `.env` URLs to a specified output file
- Lightweight and easy to integrate into recon pipelines

## Installation

1. Clone this repository:
   git clone https://github.com/username/Laravel-env-scanner.git
   cd Laravel-env-scanner

2. Install the required dependencies:
   bash : pip3 install -r requirements.txt

3. Example Running tools : python3 env-scanner.py -o results.txt


This command:

* Scans all subdomains in subdomains.txt

* Uses 50 threads

* Saves exposed .env URLs to results.txt

Output
Each line in the output file contains a full URL where a .env file was found and accessible (HTTP 200).

Disclaimer !!!
{ WARNING: FOR LEGAL AND ETHICAL USE ONLY }

This tool is exclusively intended for authorized security testing on systems you own or have explicit written permission to test (e.g., bug bounty programs, penetration testing contracts, internal red teaming).
````
