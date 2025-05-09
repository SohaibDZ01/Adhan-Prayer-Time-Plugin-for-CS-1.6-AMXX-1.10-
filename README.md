# 📿 Adhan & Prayer Time Plugin for CS 1.6 (AMXX 1.10)

DOWNLOAD  HERE: https://github.com/SohaibDZ01/Adhan-Prayer-Time-Plugin-for-CS-1.6-AMXX-1.10-/releases/tag/cs1.6

## 🔧 Overview

This plugin is developed by me with the aim of encouraging players in **Algeria** to pray on time. When it's time for **Adhan (Islamic call to prayer)**, the plugin plays the Adhan sound for players located in Algeria and automatically moves them to **Spectator mode for 15 minutes**, allowing them to take a break from the game and perform their prayer.

This way, everyone shares in the **Ajar (reward) and Hassanat (good deeds)**.

## ⚙️ How It Works

- The plugin checks the player's **location using GeoIP2 City**.
- It reads the **prayer times** from a **JSON file**, which is updated **daily** for all **Algerian provinces**.
- The JSON file is placed in the `addons/amxmodx/configs/adhan` directory and contains accurate prayer times for each day and each Wilaya (province).
- The **json.inc** library is used to parse the JSON data.
- Adhan sounds are downloaded from the internet and played automatically during prayer time.
- Built for **AMX Mod X version 1.10**.
- The plugin is **still in development**.

## 📦 Installation Instructions

### 1. Configure the JSON Generator Script
- Copy the `generate_adhan_time.py` script to your game server.
- Edit this line in the script:
  ```python
  /home/cs_server/cstrike/addons/amxmodx/configs/adhan
  ```
  Change it to match the full path where you want the daily `adhan-YYYY-MM-DD.json` file to be saved.

### 2. Edit the Cron Setup Script
- Open `setup-cron.sh` and change this line:
  ```bash
  SCRIPT_PATH="/home/cs_server/scripts/generate_adhan_time.py"
  ```
  Replace it with the actual path to your `generate_adhan_time.py`.

### 3. Activate the Cron Job
- Give execute permission and run the script:
  ```bash
  chmod +x setup-cron.sh
  ./setup-cron.sh
  ```
- This will schedule the script to run **automatically every night at midnight** to generate the updated prayer times.

### 4. Install the Plugin
- Copy the `cstrike` folder into your server directory.
- Add `adhan_prayer_time.amxx` to this file:
  ```
  addons/amxmodx/configs/plugins.ini
  ```

### 5. Restart Your Server

## 🕌 Final Note

The plugin is still under development. Your feedback and suggestions are welcome!

DOWNLOAD  HERE: https://github.com/SohaibDZ01/Adhan-Prayer-Time-Plugin-for-CS-1.6-AMXX-1.10-/releases/tag/cs1.6

**Baraka Allahou Fikom – May Allah bless you all.**
