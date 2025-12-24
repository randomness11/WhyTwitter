# Why Twitter?

A Chrome extension that adds psychological friction to Twitter/X by requiring you to state your intention before accessing it.

![Chrome Extension](https://img.shields.io/badge/Chrome-Extension-green) ![Manifest V3](https://img.shields.io/badge/Manifest-V3-blue)

## How It Works

1. Navigate to `twitter.com` or `x.com` → **Blocked**
2. Type why you're opening Twitter (5+ characters)
3. Access granted for **5 minutes** in **that tab only**
4. After 5 minutes → automatically blocked again
5. New tab = new reason required

## Features

- 🚫 Blocks Twitter/X until you state your reason
- ⏱️ 5-minute per-tab access limit (enforced)
- 📝 Logs all your reasons locally
- 🔒 No data collected, no external requests
- 🎨 Matches X's official design language

## Installation

### Step 1: Download the Extension
```bash
git clone https://github.com/randomness11/whytwitter.git
```
Or click **Code → Download ZIP** and extract it.

#### Step 2: Open Chrome Extensions Page
- Open Chrome and navigate to:
  ```
  chrome://extensions
  ```
- Or go to **⋮ Menu → Extensions → Manage Extensions**

#### Step 3: Enable Developer Mode
- Toggle the **Developer mode** switch in the top-right corner

![Developer Mode Toggle](https://developer.chrome.com/static/docs/extensions/get-started/tutorial/hello-world/image/extensions-page-e702dd4555c1c.png)

#### Step 4: Load the Extension
1. Click **Load unpacked**
2. Navigate to the downloaded/cloned folder
3. Select the folder containing `manifest.json`
4. Click **Select Folder**

#### Step 5: Verify Installation
- You should see **"Why Twitter?"** in your extensions list
- The extension icon will appear in your toolbar
- Try visiting `twitter.com` — you'll be blocked! 🎉

---

### Updating the Extension
If you installed manually:
1. Pull the latest changes or re-download
2. Go to `chrome://extensions`
3. Click the **↻ refresh** icon on the extension card

## Files

| File | Purpose |
|------|---------|
| `manifest.json` | Extension config (Manifest V3) |
| `background.js` | Service worker — intercepts navigation, manages timers |
| `block.html` | Block page UI |
| `block.js` | Input validation and messaging |
| `icon.svg` | Source icon |
| `icon128.png` | Extension icon (128x128) |

## Privacy

- All data stored locally via `chrome.storage.local`
- Reasons never leave your browser
- No analytics, no tracking, no external requests

## License

MIT
