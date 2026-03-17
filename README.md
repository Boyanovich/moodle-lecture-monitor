# Moodle lecture monitor

I wrote this script because checking the university e-learning portal for new files every day was driving me crazy. It uses Selenium to check for new course materials, bypasses the annoying Amanote iframe popups, downloads the latest PDF/PPTX, and uses OpenRouter's API (Trinity model) to summarize the text and ping a Telegram bot.

## Setup & Run

Make sure you have Google Chrome installed on your system.

1. `pip install -r requirements.txt`
2. Put your Moodle credentials, OpenRouter API key, and Telegram bot tokens inside the `CONFIGURATION` block in `moodle_parser.py`.
3. Run `python moodle_parser.py`. 

The script runs in a continuous loop (checks every 15 minutes by default). It saves the URLs of processed lectures locally in `processed_lectures.txt` so it won't spam you with the same summary twice.