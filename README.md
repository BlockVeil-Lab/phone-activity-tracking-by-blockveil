# phone-activity-tracking-by-blockveil

Track Android device activity using MacroDroid and log events to Google Sheets via Google Apps Script.

## Features
- Logs device activity (screen, connectivity, etc.)
- Uses MacroDroid (no custom APK)
- Stores data in user-owned Google Sheets
- No third-party servers

## Requirements
- Android device
- MacroDroid app
- Google account (for Sheets + Apps Script)

## How It Works
1. MacroDroid macro captures device events
2. Macro sends data via HTTP POST
3. Google Apps Script receives data
4. Data is appended to Google Sheets

## Setup

### 1. Import Macro
- Open MacroDroid
- Import `macro/Phone_Activity_Tracking_by_BlockVeil.macro`

### 2. Google Apps Script
- Open Google Sheets
- Extensions → Apps Script
- Paste code from `apps-script/google_apps_script.js`
- Deploy as Web App
- Copy Web App URL

### 3. Configure Macro
- Paste Web App URL into Macro HTTP Request action
- Set Content-Type to `application/json`

## Privacy
- All data stays in your own Google Sheet
- No external servers
- No tracking, no analytics, no uploads by BlockVeil

## License
MIT
