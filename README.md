📧 Email Spam Classifier using Trie and IMAP

This project is a Python-based spam email classifier that connects to a Gmail inbox using IMAP and classifies emails as Spam or Ham (not spam) using a Trie data structure for keyword detection.

🚀 Features
✅ Connects to Gmail using IMAP and App Passwords.

✅ Fetches emails from the inbox.

✅ Uses a Trie-based keyword matcher to detect spam content.

✅ Detects spam via:

Common spam keywords (like "free", "win", "offer").

Presence of suspicious links (http://, https://).

✅ Classifies and prints each email as Spam or Ham.

🧰 Technologies Used
Python 3

imaplib and email for email handling

Regular Expressions (re) for link detection

Custom implementation of Trie Data Structure

📁 Project Structure
bash
Copy code
spam_classifier.py        # Main script
🧠 How It Works
Login to Gmail using IMAP and an App Password.

Fetch all emails from the inbox.

Scan the body of each email for:

Spam keywords (e.g., "free", "click here", "limited offer").

Suspicious links using re.findall(r'http[s]?://\S+', ...).

Trie is used for efficient keyword matching.

Prints the classification of each email: Spam or Ham.

🔐 Setup Instructions
1. Enable IMAP on Gmail
Go to Gmail Settings → Forwarding and POP/IMAP

Enable IMAP

2. Create a Google App Password
Go to Google App Passwords

Generate a new password for "Mail"

Replace it in the script:

python
Copy code
username = "your-email@gmail.com"
app_password = "your-app-password"
▶️ How to Run
bash
Copy code
python spam_classifier.py
📌 Example Output
pgsql
Copy code
Total emails: 25
Email from: Netflix <no-reply@netflix.com> - Subject: Payment Failed - Classified as: Ham
Email from: "Prize Dept" <lottery@randommail.com> - Subject: You won $1000! - Classified as: Spam
📌 Limitations & Notes
Only checks inbox emails, not other folders.

Doesn't use ML — only keyword and link-based rules.

Works best in trusted environments (Gmail + App Passwords).

📜 License
MIT License — free to use, modify, and distribute.
