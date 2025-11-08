````
# Laravel .env Scanner

`env-scanner.py` is a Python tool that scans multiple subdomains for exposed `.env` files. It automates checks by appending `/.env` to each target from a provided list (e.g., `subdomains.txt`). Discovered files are recorded to an output file (default: `hasil.txt`; override with `-o`). Ideal for security research, penetration testing, and bug bounty reconnaissance.

---

## Features

- Fast multi-threaded scanning
- Customizable thread count and request timeout
- Saves valid `.env` URLs to a specified output file
- Lightweight and easy to integrate into recon pipelines

---

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/username/Laravel-env-scanner.git
   cd Laravel-env-scanner

2. Install the required dependencies:
   bash : pip3 install -r requirements.txt

```
python3 env-scanner.py [file] [-t THREADS] [--timeout TIMEOUT] [-o OUTPUT]
```

Arguments
ArgumentDescriptionfilePath to the subdomain list file (e.g., subdomains.txt)
Options
OptionDescriptionDefault-h, --helpShow help message and exit--t THREADS, --threads THREADSNumber of concurrent threads50--timeout TIMEOUTRequest timeout in seconds5-o OUTPUT, --output OUTPUTOutput file to save resultshasil.txt
Example
bash

```
python3 env-scanner.py subdomains.txt -t 100 --timeout 10 -o env-results.txt
```

This command:

* Scans all subdomains in subdomains.txt

* Uses 100 threads

* Sets a 10-second timeout per request

* Saves exposed .env URLs to env-results.txt

Output
Each line in the output file contains a full URL where a .env file was found and accessible (HTTP 200).
Disclaimer
This tool is intended for authorized security testing only. Do not use it on systems you do not own or have explicit permission to test. The author is not responsible for misuse.
License
MIT License
text

````
