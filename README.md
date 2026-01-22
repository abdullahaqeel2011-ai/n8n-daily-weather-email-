# n8n-daily-weather-email-
# 🌤️ Morning Weather Report – n8n Workflow

This n8n workflow automatically sends a **personalized daily weather report** to your Gmail inbox every morning at **7 AM**.  
It uses the free [Open-Meteo API](https://open-meteo.com/) to fetch real-time weather data — no API key required!

## ⚙️ Workflow Overview

**Goal:** Automate your morning routine by getting a weather update via email.  
**Trigger:** Every day at 7:00 AM.  
**Output:** A friendly Gmail message showing today’s temperature and weather emoji (☀️🌧️❄️⛈️).

## 🧩 Nodes Breakdown

### 1️⃣ Schedule Trigger
Starts the workflow automatically every day at **7 AM**, no manual action needed.

### 2️⃣ HTTP Request
Fetches current weather data from the Open-Meteo API:  

https://api.open-meteo.com/v1/forecast?latitude=24.86&longitude=67.01&current_weather=true

### 3️⃣ Code Node (JavaScript)
Processes the data and assigns the correct emoji based on weather code:
- ☀️ Clear sky  
- 🌧️ Rainy  
- ❄️ Snowy  
- ⛈️ Thunderstorm  

It also builds a clean subject and message for the email body.

### 4️⃣ Set Node
Formats a friendly weather message:

Good morning! 🌅
Here’s today’s weather:
☀️ Current temperature: 27°C
Have a great day! 🌞

### 5️⃣ Gmail Node
Sends the formatted message to your Gmail inbox using Gmail OAuth2 credentials.  
No API key or server setup required!

## 🧠 Example Output

**Subject:** ☀️ Today’s Weather Report  
**Body:**

Good morning! 🌅  
Here’s today’s weather:  
☀️ Current temperature: 27°C  
Have a great day! 🌞

## 🚀 Features

✅ 100% No-Code (only one short JS function)  
✅ Uses free public API (no API key)  
✅ Fully automated and beginner-friendly  
✅ Customizable time, location, and message format  
✅ Sends through Gmail automatically  

## 🛠️ Setup Instructions

1. Import the `.json` workflow into your **n8n editor**.  
2. Connect your **Gmail OAuth2 credentials** in the Gmail node.  
3. (Optional) Change latitude & longitude in the HTTP Request node to your location.  
4. Activate the workflow — and enjoy daily weather updates in your inbox! 💌  

## 🌈 Tech Stack

- **n8n.io** – Workflow Automation Platform  
- **Open-Meteo API** – Free weather data  
- **Gmail Node** – Email integration  

## 📄 License

Licensed for educational and commercial use.

👤 **Author**

**Abdullah Aqeel**  

AI Automation Engineer | Software Quality Assurance Engineer (SQAE)
