# Moodle Lecture Monitor

This script automates the monitoring, downloading, and summarizing of course materials from a Moodle e-learning portal.

## Features

* Continually monitors Moodle for new lecture files (PDF/PPTX).
* Bypasses Moodle iframe plugins (e.g., Amanote) to extract direct file download links.
* Extracts raw text from downloaded presentations.
* Uses the OpenRouter API (Trinity model) to generate a brief summary of the lecture content.
* Sends the lecture title and AI summary as a notification to a Telegram bot.
* Maintains a local log (`processed_lectures.txt`) to prevent duplicate processing.

## Setup & Run

1. Install required dependencies: 
   `pip install -r requirements.txt`
2. Update the `CONFIGURATION` block inside `moodle_parser.py` with your Moodle credentials, OpenRouter API key, and Telegram bot tokens.
3. Execute the script: 
   `python moodle_parser.py`