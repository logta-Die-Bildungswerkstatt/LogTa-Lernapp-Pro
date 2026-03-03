# 📱 LogTa Pro - App Build Anleitung

## ✅ Was bereits erledigt ist:
- [x] Capacitor installiert
- [x] Konfiguration erstellt (`capacitor.config.ts`)
- [x] Web-Build erstellt (`dist/` Ordner)

---

## 🚀 SCHRITT 3: Android-Projekt erstellen

Öffne dein Terminal im Projektordner und führe diesen Befehl aus:

```bash
npx cap add android
```

**Was passiert:**
- Erstellt einen `android/` Ordner
- Konfiguriert das Android-Projekt für deine App

---

## 🚀 SCHRITT 4: App synchronisieren

Nachdem Android hinzugefügt wurde, synchronisiere den Web-Code:

```bash
npx cap sync
```

**Was passiert:**
- Kopiert deine gebaute Web-App (`dist/`) in das Android-Projekt
- Aktualisiert alle Plugins und Einstellungen

---

## 🚀 SCHRITT 5: Android Studio öffnen

Öffne das Android-Projekt in Android Studio:

```bash
npx cap open android
```

**Was passiert:**
- Öffnet Android Studio (muss installiert sein)
- Zeigt dein fertiges Android-Projekt

---

## 🚀 SCHRITT 6: APK bauen (in Android Studio)

1. In Android Studio: **Build** → **Build Bundle(s) / APK(s)** → **Build APK(s)**
2. Warte bis der Build fertig ist
3. Klicke auf **locate** um die APK-Datei zu finden

**Wo ist die APK?**
```
dein-projekt/android/app/build/outputs/apk/debug/app-debug.apk
```

---

## 📤 SCHRITT 7: App verteilen

### **Option A: Direkt an Azubis schicken (kostenlos)**
- Schicke die `app-debug.apk` Datei per E-Mail/WhatsApp
- Azubis installieren sie auf ihrem Android-Handy
- **Wichtig:** Azubis müssen "Installation aus unbekannten Quellen" erlauben

### **Option B: Google Play Store (25€ einmalig)**
1. Erstelle ein Google Play Developer Konto (25€)
2. Erstelle einen **Release Build** (statt Debug):
   ```bash
   cd android
   ./gradlew assembleRelease
   ```
3. Lade die `app-release.apk` im Play Store hoch

---

## 🍎 iOS (optional, nur für iPhone)

Falls du auch eine iPhone-App willst:

```bash
npx cap add ios
npx cap sync
npx cap open ios
```

**Voraussetzung:**
- Mac Computer mit macOS
- Xcode installiert
- Apple Developer Konto (99€/Jahr)

---

## 🎯 Zusammenfassung der Dateien

| Datei | Pfad | Verwendung |
|-------|------|------------|
| **capacitor.config.ts** | Projektroot | Capacitor-Einstellungen |
| **dist/** | Projektroot | Gebaute Web-App |
| **android/** | Projektroot | Android-Projekt (nach Schritt 3) |
| **app-debug.apk** | `android/app/build/outputs/apk/debug/` | Test-APK für Azubis |

---

## ❓ Häufige Fragen

### **Brauche ich Android Studio?**
Ja, zum Bauen der APK. [Hier herunterladen](https://developer.android.com/studio)

### **Kann ich die APK einfach so verteilen?**
Ja! Schicke die `app-debug.apk` an deine Azubis. Sie müssen nur in den Einstellungen "Installation aus unbekannten Quellen" erlauben.

### **Was kostet das?**
- **Capacitor:** Kostenlos ✅
- **Android Studio:** Kostenlos ✅
- **Direktverteilung:** Kostenlos ✅
- **Google Play Store:** 25€ einmalig (optional)
- **Apple App Store:** 99€/Jahr (optional)

---

## 🎉 Fertig!

Wenn du alle Schritte durchgeführt hast, hast du eine **echte, installierbare App** für deine Azubis! 📦✨

Bei Fragen einfach melden!
