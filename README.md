Snapchat Mass Report Tool

A Python-based script to automate mass reporting of Snapchat accounts via the Snapchat support API.

--------------------------------------------------

⚠️ Disclaimer

This tool is intended for educational purposes only. Misuse to harass, spam, or harm others is strictly prohibited and may violate Snapchat's Terms of Service and applicable laws. Use responsibly and ethically.

--------------------------------------------------

Features

- Automatically solves Google reCAPTCHA v2 challenges via 2Captcha API
- Generates random email addresses to simulate distinct reports
- Sends repeated report requests targeting a specified Snapchat user
- Colored terminal output using Colorama for clear status updates

--------------------------------------------------

Requirements

- Python 3.6+
- requests library
- colorama library

Install dependencies via:

pip install requests colorama

--------------------------------------------------

Configuration

Create a config.json file in the same directory with the following structure:

{
  "api_key": "YOUR_2CAPTCHA_API_KEY",
  "user": "TARGET_SNAPCHAT_USERNAME",
  "message": "REASON_FOR_REPORTING_MESSAGE"
}

- api_key: Your 2Captcha API key for solving captchas
- user: Snapchat username you want to report
- message: Reason/message explaining the report

--------------------------------------------------

Usage

Run the script:

python snapchat_mass_report.py

The script will continuously generate new reports until stopped manually.

--------------------------------------------------

How It Works

1. Generates a random email for each report.
2. Requests 2Captcha to solve the Google reCAPTCHA on Snapchat support.
3. Sends a POST request to Snapchat's report endpoint with the generated data.
4. Prints success or error messages in the console.

--------------------------------------------------

Code Overview

- Uses requests.Session() for HTTP session persistence.
- Handles CAPTCHA solving asynchronously by polling 2Captcha service.
- Builds multipart form-data to mimic a genuine report submission.
- Uses colorama for colored output to differentiate status messages.

--------------------------------------------------

Warning

Excessive or abusive use of mass reporting can lead to account suspension or legal issues. Always comply with platform rules and local laws.

--------------------------------------------------

License

This project is provided as-is for educational and testing purposes.

--------------------------------------------------

Developed by [Your Name or GitHub handle]
Feel free to contribute or raise issues!
