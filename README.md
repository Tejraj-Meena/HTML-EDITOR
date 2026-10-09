# Code Editor - Android App

A full-featured HTML/CSS/JS code editor for Android with file import, undo/redo, image support, and live preview.

## Features
- **Multi-file support** - Create and edit multiple HTML, CSS, and JS files
- **File import** - Pick `.html`, `.css`, `.js` files directly from your device
- **Image support** - Import images and use them in your HTML
- **Undo/Redo** - Full undo/redo history for all changes
- **Auto-closing tags** - HTML tags close automatically
- **Live preview** - See your code run in real-time
- **Dark mode** - Toggle between light and dark themes
- **Download project** - Export entire project as `.zip`

## Build for Android

### Option 1: Build on GitHub (Automatic)

1. Create a GitHub repository and push all files from this folder
2. Go to your repo's **Actions** tab
3. Click **Build APK** and select **Run workflow**
4. Wait 5-10 minutes for the build to complete
5. Download **code-editor-apk** from Artifacts
6. Extract the APK and install on your Android device

### Option 2: Build Locally

**Requirements:**
- Node.js 16+ 
- Java 17+
- Android SDK

**Steps:**
```bash
npm install
npx capacitor add android
npx capacitor sync android
cd android
./gradlew assembleDebug
```

APK will be at: `android/app/build/outputs/apk/debug/app-debug.apk`

## Installation

1. Download `app-debug.apk`
2. Transfer to your Android phone (email, cloud storage, USB, etc.)
3. Open the file in Files app or browser
4. Tap **Install** and allow "Unknown Apps" if prompted
5. Launch from your app drawer

## Usage

- **Import files:** Click ðŸ“„ HTML, ðŸŽ¨ CSS, âš™ï¸ JS, or ðŸ–¼ï¸ Image buttons
- **Edit:** Click any tab to switch files
- **Undo/Redo:** Use â†¶ and â†· buttons or Ctrl+Z / Ctrl+Y
- **New files:** Click **+** tab to create new files
- **Preview:** Select which page to view from the dropdown
- **Download:** Click **Download** to save project as `.zip`

## Permissions

The app requests:
- **Read/Write Storage** - To import files and save projects
- **Share** - To share downloaded files

## Notes

- Code is auto-saved to your phone's storage
- Images are embedded in the preview (not in exported ZIP)
- Works fully offline once installed
- Supports file names with any extension

## Development

To modify the editor, edit `www/index.html` and run:
```bash
npx capacitor sync android
```

Then rebuild the APK.