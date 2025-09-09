# TourTracker🎸
Web scraping application for concerts with automatic email notifications.

## 📌 Description
TourTracker is a Python project that performs web scraping on a tours page using Selectorlib.

The extracted data is stored in a SQLite database, and whenever a new event is detected, the system sends a notification via email.

The email is sent using SMTP, with environment variables protected by dotenv.

## Features
- Extract concerts from a tours page
- Store data in a SQLite database
- Prevent duplicates by checking if the event already exists
- Notify new concerts found via email

## 🛠️ Technologies Used
- **Python** – main language
- **Requests** – page content fetching
- **Selectorlib** – data extraction via YAML
- **SQLite** – local database
- **smtplib + ssl** – email sending
- **dotenv** – environment variable management

## 📚 Learnings
The development of TourTracker was of great importance for me to practice:

- Web scraping with requests and Selectorlib
- Integration with SQLite database
- Sending emails with SMTP
- Using dotenv to protect credentials
- Structuring reusable Python projects

## ▶️ How to Run Locally
Clone the repository:

``` bash
git clone https://github.com/gabriel-oligom/tour-tracker-scraping
cd tour-tracker-scraping
```

Create and activate a virtual environment:
``` bash
python -m venv venv
source venv/bin/activate   # Linux / Mac
venv\Scripts\activate      # Windows
```

Install dependencies:
``` bash
pip install -r requirements.txt
```

Set up environment variables in the .env file:
``` bash
EMAIL_USER=your_email@gmail.com
EMAIL_PASSWORD=your_password
EMAIL_RECEIVER=receiver@gmail.com
```

Execute a aplicação:
``` bash
# Windows
py main.py
# or 
python main.py

# Linux / Mac
python main.py
```