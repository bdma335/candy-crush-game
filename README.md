# 🍬 Candy Crush Game

A fun and addictive match-3 puzzle game built with HTML5 Canvas, featuring smooth drag-and-drop mechanics, particle effects, and AdSense integration.

## 🎮 Play Now

**Game URL:** https://bdma335.github.io/candy-crush-game/

**Admin Panel:** https://bdma335.github.io/candy-crush-game/admin.html

## ✨ Features

- 🎯 **Smooth Drag & Drop** - Intuitive candy swapping mechanics
- 💥 **Particle Effects** - Beautiful bubble burst animations
- 📱 **Mobile Responsive** - Works perfectly on all devices
- ⚙️ **Admin Panel** - Control game settings and ads
- 📢 **AdSense Ready** - Multiple ad slots integrated
- 💾 **LocalStorage** - Settings persist across sessions
- 🎨 **Customizable** - Adjust grid size, moves, and candy types

## 🎮 How to Play

1. **Drag** a candy to an adjacent position (up, down, left, or right)
2. **Match** 3 or more candies of the same type
3. **Score** points and watch the bubble burst animation
4. **Complete** the level before running out of moves

## ⚙️ Admin Panel

### Access Admin Panel
- **URL:** https://bdma335.github.io/candy-crush-game/admin.html
- **Default Password:** `admin123`

### Admin Features

#### 🎮 Game Settings
- **Initial Moves** - Set starting moves (1-100)
- **Grid Size** - Change board size (6x6 to 10x10)
- **Candy Types** - Adjust difficulty (4-8 types)

#### 📢 AdSense Configuration
- **Top Ad** - Above the game board
- **Bottom Ad** - Below the game board
- **Game Over Ad** - In the game over popup

### How to Add AdSense Ads

1. Go to admin panel: https://bdma335.github.io/candy-crush-game/admin.html
2. Login with password
3. Paste your AdSense code in the respective ad slots
4. Click "Save Ad Settings"
5. Ads will appear automatically in the game

### Example AdSense Code
```html
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-XXXXXXXX"
     crossorigin="anonymous"></script>
<ins class="adsbygoogle"
     style="display:block"
     data-ad-client="ca-pub-XXXXXXXX"
     data-ad-slot="XXXXXXXXXX"
     data-ad-format="auto"
     data-full-width-responsive="true"></ins>
<script>
     (adsbygoogle = window.adsbygoogle || []).push({});
</script>
```

## 📱 Create Android App

### Option 1: WebView App (Easiest)

1. **Install Android Studio**
2. **Create New Project** → Empty Activity
3. **Add WebView to layout** (activity_main.xml):
```xml
<WebView
    android:id="@+id/webview"
    android:layout_width="match_parent"
    android:layout_height="match_parent" />
```

4. **Configure MainActivity.java**:
```java
WebView webView = findViewById(R.id.webview);
webView.getSettings().setJavaScriptEnabled(true);
webView.getSettings().setDomStorageEnabled(true);
webView.setWebViewClient(new WebViewClient());
webView.loadUrl("https://bdma335.github.io/candy-crush-game/");
```

5. **Add Internet Permission** (AndroidManifest.xml):
```xml
<uses-permission android:name="android.permission.INTERNET"/>
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE"/>
```

6. **Build APK** → Build → Build Bundle(s) / APK(s) → Build APK(s)

### Option 2: PWA (Progressive Web App)

1. **Add manifest.json**:
```json
{
  "name": "Candy Crush Game",
  "short_name": "Candy Crush",
  "start_url": "/",
  "display": "standalone",
  "background_color": "#667eea",
  "theme_color": "#667eea",
  "icons": [
    {
      "src": "icon-192.png",
      "sizes": "192x192",
      "type": "image/png"
    },
    {
      "src": "icon-512.png",
      "sizes": "512x512",
      "type": "image/png"
    }
  ]
}
```

2. **Add Service Worker** (sw.js)
3. Users can **"Add to Home Screen"** from browser
4. Works like a native app

### Option 3: Capacitor (Recommended for Production)

```bash
# Install Capacitor
npm install @capacitor/core @capacitor/cli

# Initialize
npx cap init

# Add Android platform
npx cap add android

# Open in Android Studio
npx cap open android

# Build APK
```

## 🔒 Security

### Change Admin Password

Edit `admin.html` line 234:
```javascript
const ADMIN_PASSWORD = 'your-secure-password-here';
```

**Important:** Change the default password before deploying to production!

## 🛠️ Technical Details

- **Framework:** Vanilla JavaScript (No dependencies)
- **Canvas API:** HTML5 Canvas for rendering
- **Storage:** LocalStorage for settings persistence
- **Responsive:** CSS media queries for mobile support
- **Touch Support:** Full touch event handling
- **Animation:** RequestAnimationFrame for smooth 60fps

## 📊 Game Mechanics

- **Match Detection:** Horizontal and vertical match-3 algorithm
- **Gravity System:** Candies drop down when matches are cleared
- **Particle System:** Physics-based particle effects
- **Drag System:** Real-time candy dragging with position tracking
- **Validation:** Invalid moves automatically revert

## 🎨 Customization

All game parameters can be adjusted via the admin panel:
- Grid size (affects difficulty)
- Number of candy types (more types = harder)
- Initial moves (game length)

## 📝 License

This project is open source and available for personal and commercial use.

## 🤝 Contributing

Feel free to fork, modify, and improve the game!

## 📧 Support

For issues or questions, please open an issue on GitHub.

---

**Made with ❤️ by Bhindi Team**

🎮 **Play Now:** https://bdma335.github.io/candy-crush-game/
⚙️ **Admin Panel:** https://bdma335.github.io/candy-crush-game/admin.html