# Bitinning Post Creator — Android App

A native Android app for creating professional crypto news post cards.

---

## 🚀 EASIEST WAY: Auto-build APK via GitHub (FREE, no setup needed)

### Steps:
1. Create a free account at [github.com](https://github.com)
2. Create a **new repository** (any name, e.g. `bitinning-app`)
3. Upload all files from this folder to the repository
4. Go to **Actions** tab → you'll see "Build Bitinning APK" running automatically
5. Wait ~3 minutes → go to **Releases** or click the workflow run → **Artifacts**
6. Download `Bitinning-debug.apk`
7. Install on your Android phone:
   - Settings → Security (or Privacy) → **Enable "Install unknown apps"**
   - Open the APK file → Install

> **That's it!** Every time you push changes, a new APK is built automatically.

---

## 💻 Build Locally with Android Studio

### Requirements:
- Android Studio (free): https://developer.android.com/studio
- Java 17+

### Steps:
1. Open Android Studio
2. **File → Open** → select this folder (`BitinningApp`)
3. Wait for Gradle sync to complete (~2 min first time)
4. Click **Build → Build Bundle(s)/APK(s) → Build APK(s)**
5. APK saved to: `app/build/outputs/apk/debug/app-debug.apk`
6. Transfer to phone and install

---

## 📱 Install APK on Android Phone

### Method 1 — USB:
1. Connect phone via USB
2. Enable USB Debugging (Settings → Developer Options)
3. Run: `adb install app/build/outputs/apk/debug/app-debug.apk`

### Method 2 — File Transfer:
1. Copy APK to phone storage
2. Open file manager → tap the APK
3. Allow "Install from unknown sources" when prompted
4. Tap Install

### Method 3 — Send via WhatsApp/Telegram:
Send the APK file to yourself on WhatsApp/Telegram → tap to download → tap to install

---

## 📁 Project Structure

```
BitinningApp/
├── app/
│   └── src/main/
│       ├── AndroidManifest.xml        ← App config, permissions
│       ├── assets/www/
│       │   ├── index.html             ← THE APP (full editor)
│       │   ├── html2canvas.min.js     ← Offline image export
│       │   ├── manifest.json          ← PWA manifest
│       │   └── icons/                 ← App icons
│       ├── java/com/bitinning/postcreator/
│       │   └── MainActivity.java      ← Android WebView wrapper
│       └── res/
│           ├── layout/activity_main.xml
│           ├── values/colors.xml
│           ├── values/strings.xml
│           ├── values/themes.xml
│           ├── xml/file_paths.xml
│           └── mipmap-*/ic_launcher.png
├── .github/workflows/
│   └── build-apk.yml                 ← Auto-build on GitHub
├── build.gradle
├── settings.gradle
└── gradlew
```

---

## ✨ App Features

- **Card 1** — Headline post with Bebas Neue font, gold/white word color toggle
- **Card 2** — Details card with bullet points editor
- **4K Export** — Downloads at 2160×2700px
- **Font Size Controls** — Heading (16–80px) and Body (8–24px)
- **Image Upload** — Background + Logo PNG
- **Fully Offline** — No internet needed after install
- **Portrait locked** — Optimized for mobile creation

---

## 🛠 Troubleshooting

**"App not installed" error:**
→ Uninstall previous version first, then reinstall

**White screen on launch:**
→ Force close app → reopen

**Image upload not working:**
→ Grant storage permission: Settings → Apps → Bitinning → Permissions → Storage → Allow

**Download button not working:**
→ Grant storage permission as above

---

## 📝 Version

- **Version:** 1.0.0
- **Min Android:** 5.0 (API 21)
- **Target Android:** 14 (API 34)
- **Package:** com.bitinning.postcreator
