Ultimate Customizable Gmail Bot

This Python script allows you to send bulk emails, set up auto-replies, schedule emails, and manage custom email templates using your Gmail account.

Step 1: Install Python

If you don’t have Python installed, follow these instructions:

For Windows:
	1.	Download Python from the official website: Python Downloads
	2.	Run the installer and make sure to check the box “Add Python to PATH” during the installation.
	3.	Verify the installation by opening a Command Prompt and typing:

python --version

It should show the installed Python version.

For macOS:
	1.	Open the terminal and install Python using Homebrew (if you don’t have Homebrew, install it from here):

brew install python


	2.	Verify the installation by typing:

python3 --version



For Linux:
	1.	Open the terminal and use the following command to install Python:

sudo apt-get install python3


	2.	Verify the installation by typing:

python3 --version

Step 2: Install Dependencies

The script requires a few external libraries. To install them, open your terminal (or Command Prompt on Windows) and run the following command:

pip install pandas deep-translator schedule

This will install the following dependencies:
	•	pandas: For reading and processing CSV files.
	•	deep-translator: For translation support.
	•	schedule: For scheduling emails.

Note:

smtplib, imaplib, and email are built-in libraries in Python, so you don’t need to install them separately.

Step 3: Update Your Script

Before running the script, you’ll need to update some details:

1. Gmail Credentials

In the script, find the following lines and replace them with your Gmail account details:

EMAIL_ADDRESS = "your_email@gmail.com"  # Replace with your Gmail address
EMAIL_PASSWORD = "your_app_password"  # Replace with your Gmail App Password

Important:
Use your Gmail App Password instead of your regular Gmail password. If you don’t have an app password, follow these steps to create one:
	1.	Go to Google Account Security.
	2.	Under “Signing in to Google,” click App Passwords.
	3.	Generate a new app password and use that instead of your regular Gmail password.

2. Customize Your Email Templates

You can customize the default email templates directly in the script. Find the TEMPLATES dictionary in the script:

TEMPLATES = {
    "welcome": "Welcome to our service! We are excited to have you!",
    "thank_you": "Thank you for your order! We appreciate your support.",
    "follow_up": "Just following up to ensure everything went well.",
    "custom": "Enter your custom message here.",
    "reminder": "Don't forget to check our latest products!",
    "promo": "Special promo just for you! Check it out!",
    "feedback": "We'd love to hear your feedback!",
    "thank_you_order": "Thank you for your order, we're preparing it for you!",
}

You can change the content of each template as needed.

3. Prepare Your CSV File

The script requires a CSV file with contact information to send bulk emails. Make sure your CSV file has the following columns:
	•	email: Recipient email address
	•	name: Recipient’s name
	•	subject: Subject of the email (optional)
	•	attachment: Path to the attachment (optional)

Example CSV format:

email,name,subject,attachment
example@email.com,John,Welcome Email,/path/to/file.jpg
another@email.com,Alice,Thank You Email,/path/to/file.pdf

Step 4: Run the Script

Once you have updated the script with your Gmail credentials, templates, and prepared your CSV file, you’re ready to run the script!
	1.	Save the script to a file, for example, gmail_bot.py.
	2.	Open your terminal (or Command Prompt on Windows) and navigate to the folder where the script is saved.
	3.	Run the script by typing:

python gmail_bot.py

The script will prompt you to choose an option to send bulk emails, set up auto-replies, or schedule emails.

Step 5: Optional - Running the Script in Google Colab

If you prefer to run the script in Google Colab:
	1.	Go to Google Colab.
	2.	Create a new notebook.
	3.	Copy the entire script into a cell in the notebook.
	4.	Run the script by pressing Shift + Enter.

Important Notes for Google Colab:
	•	Make sure to upload the CSV file to your Google Colab environment by clicking on the file icon on the left sidebar and then uploading your file.
	•	You may need to change how you handle file paths in the script since Google Colab runs in a cloud environment.

Step 6: Troubleshooting

If you encounter any issues, here are a few things to check:
	1.	Invalid Gmail App Password: Make sure you’ve generated and used the correct Gmail App Password (not your regular Gmail password).
	2.	CSV Formatting: Ensure that your CSV file is properly formatted (with the correct column headers).
	3.	Missing Libraries: Ensure you’ve installed all the required libraries by running pip install pandas deep-translator schedule.

Enjoy using your Ultimate Customizable Gmail Bot!

Let me know if this works for you, and if anything else needs to be changed!