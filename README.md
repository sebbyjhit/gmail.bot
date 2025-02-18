Ultimate Customizable Gmail Bot: README.md

Introduction

This bot enables you to send bulk emails, automatically reply to unread emails, and schedule emails using customizable email templates. You can interact with the script through a simple text interface.

Key Features
	•	Send Bulk Emails: Send emails to a list of contacts stored in a CSV file.
	•	Auto-reply to Unread Emails: Automatically reply to unread emails with pre-set templates.
	•	Schedule Emails: Schedule emails to be sent at a specific time each day.

Requirements

Before running the bot, make sure you have the following:
	1.	Python 3.x installed.
	2.	Required Python Libraries:
	•	smtplib (for sending emails)
	•	imaplib (for reading incoming emails)
	•	email (for composing email messages)
	•	time (for pauses between emails)
	•	pandas (for handling CSV files)
	•	os (for interacting with the file system)
	•	schedule (for scheduling emails)

You can install the required Python libraries by running:

pip install pandas schedule

How to Set Up and Run the Bot

Step 1: Setting Up Your Gmail Account

Before using this bot, ensure that you’ve set up an App Password for your Gmail account, as Gmail no longer allows direct login with your regular Gmail password when using third-party apps like this one.
	1.	Go to your Google account: https://myaccount.google.com
	2.	Under Security, enable 2-Step Verification if it’s not already enabled.
	3.	Create an App Password by selecting “App passwords” under the Security settings.
	4.	Generate a new password for the “Mail” app (you can name it anything, like “email-bot”).
	5.	Use the App Password generated instead of your regular Gmail password when prompted by the script.

Step 2: Running the Script
	1.	Save the script as a Python file (e.g., email_bot.py).
	2.	Open a terminal and navigate to the folder where your script is saved.
	3.	Run the script with the command:

python email_bot.py

Step 3: Input User Information

Upon running the script, you’ll be prompted to input the following:
	•	Gmail Address: Your Gmail address for sending emails.
	•	App Password: The Gmail App Password you created.
	•	Email Templates: Custom email templates for different email types, such as “Welcome”, “Thank You”, “Follow-Up”, and a custom one for special cases.

How to Use the Features

1. Send Bulk Emails (CSV)

This feature allows you to send emails to multiple recipients stored in a CSV file. The CSV file should have the following columns:
	•	email: The recipient’s email address.
	•	subject: The subject of the email.
	•	name: The recipient’s name.
	•	attachment (optional): The file path of an attachment, if any.

How to Use
	1.	Prepare your CSV file in the format mentioned above.
	2.	When prompted, provide the path to your CSV file (e.g., C:/path/to/your/contacts.csv).
	3.	Select the template you want to use (e.g., “welcome”, “thank_you”).
	4.	The bot will send the emails and display a success message for each one.

2. Auto-Reply to Unread Emails

This function reads unread emails from your inbox and sends a reply using one of your pre-configured templates.

How to Use
	1.	Make sure your Gmail inbox has unread emails.
	2.	Choose a response template for each incoming email.
	3.	The bot will fetch unread emails and send the reply accordingly.

3. Schedule Emails

This feature allows you to schedule an email to be sent at a specific time.

How to Use
	1.	Input the recipient’s email, subject, and choose the email template.
	2.	Set the time (in HH:MM format, 24-hour clock) for when you want the email to be sent.
	3.	The email will be sent at the scheduled time, and the bot will repeat this every day.

What Each Part of the Code Does

User Inputs Section

EMAIL_ADDRESS = input("Enter your Gmail address: ")
EMAIL_PASSWORD = input("Enter your Gmail App Password: ")

	•	EMAIL_ADDRESS: Your Gmail address.
	•	EMAIL_PASSWORD: The Gmail App password for authentication.

Custom Email Templates

TEMPLATES = {
    "welcome": input("Enter your 'Welcome' email message: "),
    "thank_you": input("Enter your 'Thank You' email message: "),
    "follow_up": input("Enter your 'Follow-Up' email message: "),
    "custom": input("Enter a custom email message for special cases: ")
}

	•	You will be prompted to enter the content for 4 different email templates: Welcome, Thank You, Follow-Up, and Custom. These templates can be used when sending bulk emails or auto-replies.

send_bulk_emails() Function

def send_bulk_emails():
    file_path = input("Enter the path to your CSV file (e.g., contacts.csv): ")
    ...

	•	This function reads the contacts from the provided CSV file and sends the selected email template to each recipient.

auto_reply() Function

def auto_reply():
    ...

	•	This function checks for unread emails in your inbox and sends an auto-reply based on the chosen template.

schedule_email() Function

def schedule_email():
    ...

	•	This function allows you to schedule emails to be sent at a specific time each day.

Error Handling

The script contains basic error handling to ensure smooth operation. For example, if an invalid template is selected, it defaults to the custom template. It also provides error messages if there’s a problem with sending emails or accessing the CSV file.

Conclusion

This bot allows you to automate email processes with Gmail using templates and CSV files. By following the setup instructions and understanding the functionality, you can make your email communication more efficient.

Make sure to test the bot with a few test emails before sending bulk emails to ensure everything is working properly.

Let me know if you need further clarification or adjustments to this guide!
