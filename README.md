# 🚀 Ajodownloader

**Ajodownloader** is a feature-rich Telegram bot that downloads files from URLs and uploads them to Telegram or a Nextcloud server. It supports asynchronous transfers, real-time progress tracking, and auto-deletion from Nextcloud. Perfect for seamless file management!

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![GitHub Issues](https://img.shields.io/github/issues/izzathnisfer/ajodownloader_testing)](https://github.com/izzathnisfer/ajodownloader_testing/issues)

---

## ✨ Features

- 📥 **File Downloads**: Download files from any HTTP/HTTPS URL with live progress.
- 📤 **Upload Options**:
  - To **Telegram** (up to 2 GB).
  - To your home **Nextcloud** via WebDAV with public share links.
- ☁️ **Nextcloud Integration**:
  - Configure using `/setnc`.
  - Optional auto-deletion with a user-defined timer.
- 📊 **Progress Tracking**: Shows speed, percentage, and ETA.
- 🖥️ **System Monitoring**: Displays CPU, RAM, disk usage, and uptime.
- 🔒 **User Management**:
  - Restricted to authorized users.
  - Limit of 3 concurrent tasks per user (default).

---

## 🛠️ Installation

### Prerequisites

- Python 3.8 or higher (3.10+ recommended)
- Telegram Bot Token from [@BotFather](https://t.me/BotFather)
- (Optional) Nextcloud account for cloud uploads

### Steps

```bash
# Clone the repository
git clone https://github.com/izzathnisfer/ajodownloader.git
cd ajodownloader

# Create a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

### Configure the Bot Using `.env`

Create a `.env` file in the project root with the following:

```env
API_ID=<your-api-id>
API_HASH=<your-api-hash>
BOT_TOKEN=<bot-token>
AUTHORIZED_USERS=<admin-ids>  # Comma-separated list if multiple
```

> You can obtain `API_ID` and `API_HASH` from [my.telegram.org](https://my.telegram.org).

### Run the Bot

```bash
python ajodownloader.py
```

---

## 📖 Usage

Start the bot on Telegram and use these commands:

| Command     | Description                            | Example                                |
|-------------|----------------------------------------|----------------------------------------|
| `/start`    | Check if the bot is running            | `/start`                               |
| `/help`     | List all commands                      | `/help`                                |
| `/l <url>`  | Download & upload to Telegram          | `/l https://example.com/file.zip`      |
| `/ld <url>` | Download & upload to Nextcloud         | `/ld https://example.com/file.zip`     |
| `/setnc`    | Configure Nextcloud settings           | `/setnc`                               |

---

## ⚙️ Configuring Nextcloud

1. Send `/setnc` to open the settings menu.
2. Use inline buttons to configure:
   - **URL**: e.g., `https://cloud.example.com`
   - **Username**
   - **Password**
   - **Auto-Delete**: Toggle on/off
   - **Delete Timer**: In minutes

Click **"Close"** to save and exit.

---

## 🔁 Example Workflows

### Upload to Telegram

```text
/l https://example.com/sample.pdf
```

The bot downloads `sample.pdf` and uploads it to your Telegram chat.

### Upload to Nextcloud

```text
/ld https://example.com/sample.pdf
```

The bot downloads `sample.pdf`, uploads it to Nextcloud, and provides a public share link.

---

## 📋 Requirements

The `requirements.txt` includes:

```
pyrogram==2.0.106
tgcrypto==1.2.5
httpx==0.27.0
requests==2.31.0
psutil==5.9.8
aiofiles==23.2.1
```

Install with:

```bash
pip install -r requirements.txt
```

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repo.
2. Create a new branch:
   ```bash
   git checkout -b feature/YourFeature
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add YourFeature"
   ```
4. Push to GitHub:
   ```bash
   git push origin feature/YourFeature
   ```
5. Open a Pull Request.

> Follow the existing style and include tests where needed.

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).

---

## 📬 Contact

- Open an issue on GitHub.
- Contact the maintainer: **izzathnisfer**

---

**Happy downloading with Ajodownloader! 🎉**
