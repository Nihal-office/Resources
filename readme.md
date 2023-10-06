# Website Security Headers Retrieval Script

This script allows you to retrieve specific security response headers from a list of website URLs and save the results to a CSV or JSON file. It is useful for analyzing the security headers of various websites.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Usage](#usage)
- [Optional](#optional)
- [Output](#output)
- [Examples](#examples)

## Prerequisites

Before using this script, make sure you have the following prerequisites installed:

- Python 3.x
- Required Python packages
  - requests
  - pandas

## Usage

To use the script, follow these steps:

1. Create a text file (`input.txt`) containing one website URL per line.
2. Run the script.py with the following command:

python Script.py input.txt output.csv

## Optional

These are the options available in the script

- For JSON Output
python Script.py input.txt output.json --format json  (--format is an optional flag which you can use to save the output in JSON format)

- For sites which have SSL ISSUES
  
python script.py input.txt output.csv --disable-ssl-verify  (--disable-ssl-verify will disable SSL verification and ignore any SSL issues)

- `input.txt`: Path to the input file with the list of website URLs.
- `output.csv`: Path to the output file where headers will be saved. You can change the format to JSON by specifying `--format json`.
- The default format is CSV.

## Output

The script retrieves the following security response headers for each website:

- strict-transport-security
- x-frame-options
- x-content-type-options
- content-security-policy
- referrer-policy
- permissions-policy

The headers are saved in the specified output file in CSV or JSON format.

## Examples

- For CSV File:
  
python script.py input.txt output.csv --format csv

- For JSON file:
  
python script.py input.txt output.json --format json

- For Default Format (CSV) :

python script.py input.txt output.csv

- For Websites with SSL ISSUES:

python script.py input.txt output.csv --disable--ssl-verify
