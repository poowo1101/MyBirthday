# 🎂 Birthday Reminder

A simple and lightweight Python script for Windows that automatically starts with your system, counts down the days until your birthday, and brings a festive mood on your special day!

## ✨ Features
* ⚙️ **Windows Startup Integration:** Automatically registers itself into the Windows Registry (`CurrentVersion\Run`) to run silently in the background upon system boot.
* 📅 **Smart Countdown:** Accurately calculates days until your next birthday, handling leap years seamlessly (even if you were born on February 29th!).
* 🔔 **Native Notifications:** Utilizes the `plyer` library to display beautiful Windows desktop notifications.
* 🎉 **Celebration Mode:** When the big day arrives, it flashes a celebration notice and automatically opens your birthday image alongside your festive music track.

## 📁 Project Structure
Based on your local workspace, the project directory is structured as follows:
```text
My birthday/
│
├── birthday.pyw      # Main Python script (runs silently without console window)
├── image.png         # Birthday celebratory image
├── music.mp3         # Festive background music track
├── requirements.txt  # Project dependencies
└── setup.py          # Setup script for initialization
```

## 🚀 Setup & Installation

### 1. Clone the Repository
```bash
git clone https://github.com
cd "My birthday"
```

### 2. Install Dependencies
Install all required packages (like `plyer`) listed in your configuration using pip:
```bash
pip install -r requirements.txt
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

## 🛠️ Usage & Testing

To initialize the script and automatically add it to the Windows Startup registry, run the following command in your terminal:
```bash
python birthday.pyw
```

### 🥷 How It Works in the Background
* Because the script uses the `.pyw` extension, it will run completely invisibly without opening a black command prompt window.
* You can verify that it is active and scheduled to run on boot by opening **Task Manager** (`Ctrl + Shift + Esc`) and checking the **Startup apps** tab for the entry.

## 📝 License
This project is open-source and free to use. Media assets used within this project are sourced from the Public Domain.
