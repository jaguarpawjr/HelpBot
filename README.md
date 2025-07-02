

🤖 KS Help Bot

KS Help Bot is a Telegram bot designed to assist students, particularly those in Computer Engineering, Mechanical Engineering, and Electrical Engineering programs. The bot provides useful links, responds to user inputs, and integrates with Google Drive to allow file listing and download.

---

## ✨ Features

* Personalized user onboarding: greets users by name and asks for their program.
* Program-based resource sharing via inline buttons.
* Access to helpful external resources and websites.
* Google Drive integration: lists files from a specified folder and enables file downloads.
* Telegram group message interaction (fetches last message from a group - WIP).
* Modular command handlers for easy extension.

---

## 🧠 Technologies Used

* Python 3
* `python-telegram-bot`
* Google Drive API (`google-api-python-client`)
* `google-auth`

---

## 🔧 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/kshelpbot.git
cd kshelpbot
```

### 2. Install Dependencies

Make sure you have Python 3 installed. Then install the required libraries:

```bash
pip install python-telegram-bot google-api-python-client google-auth
```

### 3. Google Drive API Setup

* Go to the [Google Cloud Console](https://console.cloud.google.com/).
* Create a new project or select an existing one.
* Enable the **Google Drive API**.
* Create a **Service Account** and download the JSON credentials file.
* Rename it to `sfn.json` and place it in the project root.
* Share your target Google Drive folder with the service account email (found in the JSON file).

### 4. Bot Token Setup

Replace the token in `main.py` with your Telegram Bot token:

```python
token = "YOUR_TELEGRAM_BOT_TOKEN"
```

Alternatively, keep the `main.py` file with the token defined like:

```python
# main.py
token = "your_bot_token_here"
```

### 5. Run the Bot

```bash
python your_script_name.py
```

Replace `your_script_name.py` with the actual name of your bot file.

---

## 📋 Available Commands

| Command     | Description                                                           |
| ----------- | --------------------------------------------------------------------- |
| `/start`    | Begins user conversation and onboarding.                              |
| `/command1` | Provides a link to a support website.                                 |
| `/command2` | Provides program-specific resource links.                             |
| `/command3` | Fetches the last message from a Telegram group (WIP).                 |
| `/command4` | Lists and allows file downloads from a connected Google Drive folder. |

---

## 📁 Project Structure

```
├── main.py              # Contains your bot token
├── sfn.json             # Google Service Account credentials
├── bot_script.py        # Main bot logic (this script)
├── README.md            # Project documentation
```

---

## 🔒 Security Note

* Keep your `sfn.json` and `main.py` files private.
* Do not commit them to public repositories.
* Use `.gitignore` to exclude them:

```
sfn.json
main.py
```

---

## 📌 To-Do / Improvements

* Improve error handling and edge cases (e.g. file download by name).
* Store user inputs and track sessions.
* Add file upload support to Google Drive.
* Make the command3 group message fetching fully functional.

---

## 🙌 Contribution

Pull requests are welcome! If you have ideas for improving the bot or new features to add, feel free to fork the project and submit a PR.

---

## 📝 License

This project is licensed under the MIT License. See `LICENSE` for more details.

