Follow these steps to set up the Gmail Bulk Email Bot on your computer. This bot will help you send bulk emails, auto-reply to unread emails, and schedule emails to be sent later.

Step 1: Download & Install Python

1.1 Download Python
	•	Go to Python’s official website.
	•	Download the latest version of Python 3 (make sure you download Python 3, not Python 2).
	•	Install it by running the downloaded file and follow the installation steps.
	•	During installation, check the box that says “Add Python to PATH”.

1.2 Check Python Installation
	•	After installing Python, open the command prompt (Windows) or terminal (Mac/Linux).
	•	Type the following command and hit enter:

python --version


	•	If it shows a version number (e.g., Python 3.x.x), Python is installed correctly!

Step 2: Install Required Libraries

You need to install a few Python libraries for the bot to work. Follow these steps:

2.1 Install Libraries
	•	Open your command prompt (Windows) or terminal (Mac/Linux).
	•	Run the following command to install the required libraries:

pip install pandas smtplib imaplib email deep-translator schedule



This will install everything the script needs to send emails and interact with Gmail.

Step 3: Download the Gmail Bulk Email Bot Script

3.1 Get the Bot Script
	•	Download the bot script from this repository or file (wherever you have it hosted or stored).
	•	Save it on your computer. For example, save it in a folder called “GmailBulkEmailBot”.

3.2 Open the Script
	•	Use any text editor (like Notepad or VS Code) to open the bot script (e.g., gmail_bulk_email_bot.py).

Step 4: Set Up Your Gmail Account

4.1 Use an App Password (Not Your Gmail Password)
	•	Important: Don’t use your regular Gmail password. You must create an App Password. Here’s how:
	1.	Go to your Google Account.
	2.	In the “Security” section, turn on 2-step verification (if you haven’t already).
	3.	Once 2-step verification is enabled, scroll down and click on App Passwords.
	4.	Generate an App Password (choose “Mail” and “Windows Computer” or “Other” if you prefer).
	5.	Copy the password shown—this will be used in the script.

4.2 Edit Gmail Credentials in the Script
	•	In the script, find this section:

EMAIL_ADDRESS = 'your_email@gmail.com'  # Replace with your Gmail address
EMAIL_PASSWORD = 'your_app_password'   # Replace with your Gmail App Password


	•	Replace 'your_email@gmail.com' with your Gmail address.
	•	Replace 'your_app_password' with the App Password you just generated.

Step 5: Set Up Email Templates (Optional)

You can customize the email templates that the bot will use to send emails. Here’s how:

5.1 Find Templates in the Script
	•	In the script, there’s a section with pre-made templates:

TEMPLATES = {
    "welcome": "Welcome to our service!",
    "thank_you": "Thank you for your order! We appreciate your support.",
    "follow_up": "Just following up on your recent inquiry.",
    "custom": "Custom message for special cases.",
    # etc...
}


	•	Feel free to change any text inside the quotation marks to your custom message. For example:

"thank_you": "Thanks for choosing our service, we appreciate you!"

Step 6: Prepare the CSV File for Bulk Emails

The bot needs a CSV file with contact details for sending bulk emails.

6.1 Create the CSV File
	•	Open a spreadsheet program like Excel or Google Sheets.
	•	Create columns for email, name, subject, and attachment (optional).
	•	Example CSV file (contacts.csv):

email,name,subject,attachment
recipient1@example.com,John Doe,Welcome to our service!,path/to/file1.pdf
recipient2@example.com,Jane Smith,Thank you for your order!,path/to/file2.jpg


	•	Save this file as contacts.csv.

Step 7: Run the Bot

7.1 Start the Script
	•	Go back to your command prompt or terminal.
	•	Navigate to the folder where you saved the script (use cd path/to/folder to change directories).
	•	Run the script using the following command:

python gmail_bulk_email_bot.py



7.2 Using the Bot
	•	The bot will show a menu with options. For example:

1. Send Bulk Emails
2. Auto-Reply to Unread Emails
3. Schedule Emails
4. Edit or Add Custom Templates
5. Exit


	•	Select the option you want by typing the number and hitting Enter.

Troubleshooting
	•	“SMTP Error or Connection Error”
	•	Make sure you’re connected to the internet and check Gmail’s SMTP settings (the script uses smtp.gmail.com on port 465).
	•	“Invalid Template”
	•	Make sure you’re using a template name that exists in the script (like "thank_you", "welcome", etc.). You can add your own templates in the script.

License

This project is licensed under the MIT License - see the LICENSE file for details.

Let me know if anything is unclear or if you need more help!