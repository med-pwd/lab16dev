# Chronomètre Service - Android (Java)
analyste:souaid med amine

A stopwatch Android app demonstrating **Foreground Service** + **Bound Service** architecture in pure Java.

##Features
- Foreground Service with persistent live notification
- Bound Service for Activity ↔ Service communication
- Stopwatch continues running when app is closed
- Start/Stop controls from the UI
- Compatible with Android 8.0+ (API 26+)

##Tech Stack
- **Language:** Java
- **Min SDK:** 26 (Android 8.0)
- **Architecture:** Foreground Service + Bound Service
- **Threading:** `ScheduledExecutorService`
- **Notifications:** `NotificationCompat` + `NotificationChannel`

##Project Structure
com.example.servicechronometrejava/
├── MainActivity.java        
├── ChronometreService.java  
res/layout/
└── activity_main.xml       
AndroidManifest.xml         

##Getting Started
1. Clone the repository
2. Open in **Android Studio**
3. Run on an emulator or device with **API 26+**



## 🔑 Key Concepts
| Concept | Role |
|---|---|
| `startForeground()` | Required on Android 8+, shows persistent notification |
| `START_STICKY` | Service auto-restarts if killed by the system |
| `LocalBinder` | Lets Activity get direct reference to the Service |
| `ServiceConnection` | Interface to bind/unbind Activity ↔ Service |
| `ScheduledExecutorService` | Thread-safe timer, increments every second |
