# 💼 LinkedIn Easy Apply Bot

A Python automation script that searches LinkedIn for jobs matching a custom query and automatically submits applications to every listing with **Easy Apply** enabled. Built with **Selenium** as a hands-on browser automation exercise.

## ✨ Features

- Logs in to LinkedIn automatically
- Runs a job search using your keywords, location, and filters
- Detects listings with the **Easy Apply** option
- Fills in basic application fields (such as phone number) and submits
- Skips complex multi-step applications to avoid incomplete submissions
- Loops through all results on the search page

## 🛠️ Tech Stack

- **Python 3.x**
- **Selenium**: automates browser navigation, clicks, and form input
- **ChromeDriver**: drives the Chrome browser

## 📦 Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/linkedin-easy-apply-bot.git
   cd linkedin-easy-apply-bot
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Make sure Google Chrome is installed (recent Selenium versions manage ChromeDriver automatically).

## ⚙️ Configuration

Set your credentials as environment variables and define your search URL:

```python
LINKEDIN_EMAIL = os.environ["LINKEDIN_EMAIL"]
LINKEDIN_PASSWORD = os.environ["LINKEDIN_PASSWORD"]
PHONE_NUMBER = os.environ["PHONE_NUMBER"]
SEARCH_URL = "https://www.linkedin.com/jobs/search/?f_AL=true&keywords=data%20analyst&location=Mexico"
```

The `f_AL=true` parameter filters results to Easy Apply jobs only.

## ▶️ Usage

```bash
python main.py
```

A Chrome window will open and the bot will work through the listings. Keep an eye on it during the first runs.

## ⚠️ Disclaimer

This project is for **educational purposes only**. Automating activity on LinkedIn goes against its User Agreement and may lead to account restrictions. LinkedIn also updates its page structure often, so element selectors may need updating. Use responsibly, ideally with a test account.

## 📚 What I Learned

- Automating browser interactions with Selenium
- Locating elements with XPath and CSS selectors
- Handling dynamic pages, waits, and pop-ups
- Managing exceptions when page elements are missing
- Keeping credentials secure with environment variables

## 📄 License

MIT License
