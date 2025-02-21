# Smart Gmail Bot

This Smart Gmail Bot automatically replies to emails based on sentiment analysis, urgency detection, and email type classification. It also organizes emails into labels based on these criteria.

## Features

- Sentiment Analysis
- Urgency Detection
- Email Type Classification
- Smart Template Selection
- Automatic Email Organization

## Requirements

- Python 3.6+
- Required Python libraries:
  - `imaplib`
  - `email`
  - `pandas`
  - `smtplib`
  - `textblob`

## Installation

1. Clone the repository or download the script.

2. Install the required Python libraries:
   ```sh
   pip install pandas textblob
   Enable "Less secure app access" in your Gmail account settings:

Go to your Google Account. <vscode_annotation details='%5B%7B%22title%22%3A%22hardcoded-credentials%22%2C%22description%22%3A%22Embedding%20credentials%20in%20source%20code%20risks%20unauthorized%20access%22%7D%5D'> </vscode_annotation> - Select Security.
Under "Less secure app access," turn on "Allow less secure apps."
Enable IMAP in your Gmail account settings:

Go to your Gmail account.
Select Settings (gear icon) > See all settings.
Go to the "Forwarding and POP/IMAP" tab.
In the "IMAP access" section, select "Enable IMAP."
Configuration
Replace the placeholders in the script with your actual email credentials. You can use environment variables for better security.
 Email credentials
EMAIL_ADDRESS = "your_email@gmail.com"
EMAIL_PASSWORD = "your_password"


Run the script:
The bot will start and continuously check for new unread emails. It will process each email based on sentiment, urgency, and type, send auto-replies if necessary, and organize emails into labels.

To stop the bot, press Ctrl+C.

Example
Here is an example of how to set up and run the bot:


Install the required libraries:
pip install pandas textblob (and the others listed on top)
Configure your email credentials in the script or using environment variables.

Run the bot:
python (gmail_bot.py)

