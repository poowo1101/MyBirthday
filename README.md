# 🎂 Birthday Reminder

A simple and lightweight Python script for Windows that automatically starts with your system, counts down the days until your birthday, and brings a festive mood on your special day!

## ✨ Features
* ⚙️ **Windows Startup Integration:** Automatically adds itself to the Windows Registry (`CurrentVersion\Run`) to run in the background upon system boot.
* 📅 **Smart Countdown:** Accurately calculates days until your next birthday, handling leap years seamlessly (even if you were born on February 29th!).
* 🔔 **Native Notifications:** Utilizes the `plyer` library to display beautiful Windows desktop notifications.
* 🎉 **Celebration Mode:** When the big day arrives, it flashes a celebration notice and automatically opens a birthday cake image alongside your festive music.

## 📁 Project Structure
For the script to work properly, make sure your project directory is structured as follows:
```text
MyBirthday/
│
├── birthday.py       # Main Python script
├── cake.png          # Birthday cake image
└── music.mid         # Festive melody (MIDI or MP3 format)
```

## 🚀 Setup & Installation

### 1. Clone the Repository
```bash
git clone https://github.com
cd MyBirthday
```

### 2. Install Dependencies
The script relies on the `plyer` package for system notifications. Install it via pip:
```bash
pip install plyer
```

### 3. Configure Your Birthday
The script reads your birthday configuration from the Windows `AppData` directory. Create a configuration file at the following path:
`C:\Users\<YOUR_USERNAME>\AppData\Roaming\birthday_config.json`

Add your birthday inside the JSON file using the `YYYY-MM-DD` format:
```json
{
  "birthday": "2005-08-15"
}
```

## 🛠️ Usage

Simply run the script via your terminal. The initial run will automatically register the program into your Windows Startup:
```bash
python birthday.py
```

### 🥷 Running Silently (Background Mode)
To prevent the black console window from popping up every time Windows boots, you can change the file extension from `.py` to `.pyw` (e.g., `birthday.pyw`), or compile it into a standalone executable using PyInstaller:
```bash
pip install pyinstaller
pyinstaller --noconsole --onefile birthday.py
```

## 📝 License
This project is open-source and free to use. Media assets used within this project (such as audio) are sourced from the Public Domain.
