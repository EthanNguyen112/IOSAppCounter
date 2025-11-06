# IOSAppCounter
An automation for the IOS shortcut app to show how many times an application has been open and how long it's been used. Purpose the actively keep the user aware of their screen time, productivity tracking, and app usage awareness.

## Features
- Tracks how many times selected apps are opened each day
- Creates and stores data persistently in `/Shortcuts/AppCounter.txt`
- Prompts the user the amount of time spent and opened for today
- If the selected app is opened and has an hour or more of screen time, a 5 min timer is set
- Reset the count every day
- Easy to extend for multiple apps

## Installation
Download here: https://www.icloud.com/shortcuts/a5027a7ac7ac441d8c899c20e8e6436a

1. **Download the `AppCounter.shortcut' file** from this repository.
2. Open it on your iPhone → it’ll open in the **Shortcuts app**.
3. Tap **Add Shortcut**.
4. Go to **Shortcuts → Automation → + → Create Personal Automation**.
5. Choose **App → [Select the app you want to track] → Is Opened → Next.**
6. Add **Run Shortcut → [Choose “App Open Counter”] → Next.**
7. Turn off **Ask Before Running** → **Done.**

## How It Works
Each time your chosen app opens:
1. The automation triggers.
2. The shortcut creates and writes to `AppCounter.txt` from Shortcuts folder.
3. It appends the current app and the date to the `AppCounter.txt`.
4. It looks for and counts the amount of time and displays the information when the selected apps are open.
5. When the screen time of the selected app is more than an hour, it sets a timer for X amount of time (Currently set for 5 minutes).
6. it sends an alert:  
  EX: “Opened Instagram (1h 15mins) 10 time(s)”
7. when the dates in AppCounter.txt do not match, it resets the information to the current date

## File Storage
All data is stored in:
iCloud Drive → Shortcuts → AppCounter.txt


