# ScoreBug Project

## Overview
This project consists of two HTML pages that work together to display and control a live scorebug for a sports match. The scorebug updates in real-time using Firebase Realtime Database.

### Components:
1. **Score Control Page (score_control.html)**
   - Provides an interface to update the score, set wins, and opponent name.
   - Updates the Firebase Realtime Database with these values.
   
2. **Live Score Display (score_display.html)**
   - Retrieves data from Firebase and displays it as a scorebug overlay.
   - Updates dynamically as data changes.

---

## Features
### Score Control Page
- **Add/Remove Points:** Buttons to increase or decrease the score for both teams.
- **Add/Remove Set Wins:** Buttons to update the number of sets won.
- **Opponent Name Input:** Allows setting the opponent’s name.
- **Reset Score:** Resets only the current score.
- **Reset All:** Resets score, sets, and opponent name.
- **Firebase Integration:** Updates are stored in Firebase and automatically reflected in the display page.

### Live Score Display
- **Real-time Updates:** Fetches and displays score and set data from Firebase.
- **Scorebug UI:** Displays team names, current set number, scores, and set wins.
- **Name Formatting:** Ensures opponent names are limited to 4 characters for better display.
- **Set Number Display:** Automatically updates the current set number based on the number of sets won.
- **Minimal UI:** Transparent background for overlay compatibility.

---

## Setup Instructions
### 1. Firebase Setup
Before using the scorebug, set up Firebase:
1. Go to [Firebase Console](https://console.firebase.google.com/).
2. Create a new project.
3. Navigate to **Realtime Database** and create a new database.
4. Copy the configuration details (API key, database URL, etc.).
5. Replace the placeholder Firebase configuration in both `score_control.html` and `score_display.html` with your own.

### 2. Running the Score Control Page
1. Open `score_control.html` in a web browser.
2. Use the interface to update the scores and opponent name.
3. Changes are automatically pushed to Firebase.

### 3. Running the Live Score Display
1. Open `score_display.html` in a browser.
2. The scorebug will update in real-time based on Firebase data.

---

## Firebase Database Structure
```json
{
  "score": {
    "teamA": 0,
    "teamB": 0,
    "teamSetA": 0,
    "teamSetB": 0,
    "opponentName": "Opponent"
  }
}
```

---

## Customization
- **Styling:** Modify CSS in both files to adjust the appearance.
- **Positioning:** Change `.score-bug` styles in `score_display.html` for custom placement.
- **Team Names:** Modify `teamNameA` in Firebase to customize the home team name.

---

## Dependencies
- [Firebase JavaScript SDK](https://firebase.google.com/docs/web/setup)

---

## License
This project is open-source. Modify and use it as needed.

---

## Author
Zach Ehlers

