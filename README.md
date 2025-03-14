# 👉 AeronauticaHelper Setup 👈
This is an application that watches your AFK boat in Aeronautica! You will get a notification via the webhook if the game crashes, if you disconnect, or if your boat suddenly stops (island collision, out of fuel, etc), accompanied by a screenshot. Though possible, errors occur minimally when the camera is positioned properly. **Version 2 introduces AutoSteer** and built-in Anti-AFK.

---

## 🧾 Functionality

As previously stated, the application will recognize the following and send alerts via the designated webhook with a screenshot to better assess the issue:
- Disconnect from game
- Boat stops (island collision, out of fuel, etc)
- Game crashes
- When you approach the destination (the ship will stop too)

Major alerts, such as the cases above, will include an @everyone ping, while non-major alerts will not receive a ping.

**AutoSteer** gets the current bearing and matches it to the destination. Automated keystrokes are then performed to adjust accordingly.⭐**Essentially, assuming everything works properly, you will pull out your ship to open sea and come back when you get a notification.**

---

## 🪟 Windows Installation:

### 1. **Python Environment**

- **Python Version:** 
  Make sure you have Python 3.7 or higher installed. You can download it from [python.org](https://www.python.org/downloads/).

### 2. **Setup**

- **Webhook URL:**  
  The code sends alerts to a Discord channel using a webhook. Replace the `WEBHOOK_URL` constant in the code with your actual Discord webhook URL:
  ```python
  WEBHOOK_URL = "https://discord.com/api/webhooks/your_webhook_id/your_webhook_token"
  ```
  Replace `SHIP_TOP_SPEED` and `MULTIPLIER` with the corresponding speed and turning strength. Customize `CYCLE_INTERVAL` and `LEEWAY` to your desire.

### 3. **Project Structure**

Your project might look like this:
```
/AeronauticaHelper
├── AeroHelperMain.py    # Contains the application code
├── log_data.txt         # Log file created by the application
└── README.md            # (Optional) Documentation for your project
```

- **AeroHelperMain.py:**  
  This file will contain the complete Python code provided. It includes:
  - Configuration constants.
  - Functions to capture screenshots, perform OCR, extract the distance, and send alerts (with an attached screenshot when needed).
  - The main loop that ties everything together, running at a fixed interval (or dynamically based on elapsed time).

- **log_data.txt:**  
  This log file will be created by the application to store timestamps, OCR output, and any alerts sent.


### 4. **Running the Application**

**Run the Script:**  
   In your terminal or command prompt, navigate to your project directory and run:
   ```bash
   python AeroHelperMain.py
   ```

  ---

## ☝️ Please Note:

- If you enjoy our script, please ⭐ and 👁️ the repo!

- For enhanced results, if you are NOT using AutoSteer, consider positioning your camera below the ship (for more OCR clarity).

- **If you ARE using AutoSteer, consider turning ROBLOX's Graphics Quality to the LOWEST option, as this makes the water's color more consistent (for whatever reason), leading to enhanced OCR clarity.**

- It is generally best practice to AFK in a server in which there are few people and the server's age is minimal.

- Setup your webhook in a channel/server with only you, as there will be various @everyone pings when major alerts are sent!

- Close the chat/player list so others can't mess up your mission!

- Some boats turn quicker than others (though it may take longer); they will all reach the target. Customize the `MULTIPLIER` to your ship's liking, just make sure it doesnt auscultate.

---

## 🗣️ Latest Version: 2.1

This version includes a UI, and various QoL improvements. Enjoy!

---

## 📈 Upcoming Features:

- Full AutoPilot (v3)?

- AI Pathfinding (v4)

---

### Questions or concerns? [DM me on Discord!](https://discord.gg/3adphMca)

---

# THIS SCRIPT HAS BEEN CLEARED WITH AERONAUTICA STAFF. THIS IS 100% SAFE TO USE.
![AeroHelperV2Approved](https://github.com/user-attachments/assets/0778f8ec-c958-479e-938d-5bea5166b56b)