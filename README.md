Email Spam Classifier using Trie and IMAP
This project is a Python-based spam email classifier that connects to a Gmail inbox using IMAP and classifies emails as Spam or Ham (not spam) using a Trie data structure for keyword detection.

Features
Connects to Gmail using IMAP and App Passwords

Fetches emails from the inbox

Uses a Trie-based keyword matcher to detect spam content

Detects spam through:

Common spam keywords (e.g., "free", "win", "offer")

Presence of suspicious links (http://, https://)

Classifies and prints each email as Spam or Ham

Technologies Used
Python 3

imaplib and email for email handling

Regular Expressions (re) for detecting links

Custom implementation of Trie Data Structure

Project Structure
bash
Copy code
spam_classifier.py       # Main script
How It Works
Logs into Gmail using IMAP and an App Password

Fetches all emails from the inbox

Scans the body of each email for:

Spam keywords (e.g., "free", "click here", "limited offer")

Suspicious links using pattern matching (http[s]?://...)

Uses a Trie for efficient keyword matching

Prints the classification result: Spam or Ham

Setup Instructions
1. Enable IMAP on Gmail
Go to Gmail Settings → Forwarding and POP/IMAP

Enable IMAP

2. Create a Google App Password
Go to your Google Account → Security → App Passwords

Generate a new password for "Mail"

Replace it in the script:

python
Copy code
username = "your-email@gmail.com"
app_password = "your-app-password"
How to Run
bash
Copy code
python spam_classifier.py
Example Output
pgsql
Copy code
Total emails: 25
Email from: Netflix <no-reply@netflix.com> - Subject: Payment Failed - Classified as: Ham
Email from: "Prize Dept" <lottery@randommail.com> - Subject: You won $1000! - Classified as: Spam
Limitations and Notes
Only checks emails in the inbox (not spam, promotions, etc.)

No machine learning is used — classification is based on keywords and links

Works best in trusted environments (your own Gmail account with App Passwords)

License
MIT License — Free to use, modify, and distribute.
