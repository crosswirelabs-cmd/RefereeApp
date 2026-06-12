(Screenshot_20260612-144126.png)
Spinastra Referee App

Real-time mobile scoring application for the Spinastra Tournament Ecosystem.

The Spinastra Referee App allows referees to score matches directly from an Android device while automatically synchronizing scores with:

- Spinastra Tournament Manager
- Spinastra Scoring Server
- Digital Scoreboards (ESP32)
- Live Results
- OBS Broadcast Overlays
- YouTube Live Streams

Built with .NET MAUI for Android.

---

Features

Real-Time Match Scoring

Referees can:

- Start matches
- Record scores
- Change serving side
- Call timeouts
- Finish matches
- Retire matches
- Default matches

All updates are synchronized instantly.

---

Live Score Synchronization

Scores automatically update across:

- Tournament Manager
- Live Queue
- Live Results
- Digital Scoreboards
- OBS Overlays
- Streaming Broadcasts

No manual score reporting required.

---

Court-Based Match Assignment

Each referee can:

- Select a court
- View assigned matches
- Start scoring immediately

Match information includes:

- Court Number
- Division
- Stage
- Team Names
- Target Score

---

Server Mode

Connect directly to the Spinastra Scoring Server using SignalR.

Benefits:

- Automatic match assignments
- Live synchronization
- Tournament integration
- Broadcast integration

---

Bluetooth Mode

Supports direct Bluetooth communication with ESP32 scoreboards.

Perfect for:

- Club play
- Practice sessions
- Small tournaments
- Offline environments

No server required.

---

Serving Indicator

Track and display the current serving side.

Serving changes are immediately reflected on:

- Referee App
- Broadcast Overlays
- Digital Scoreboards

---

Timeout Management

Supports configurable timeout rules.

Features:

- Team A timeout
- Team B timeout
- Countdown timer
- Resume match functionality

---

Offline Friendly

The application is designed for tournament environments where internet connectivity may not be available.

Supports:

- Local Wi-Fi networks
- Bluetooth scoring
- Local server deployments

---

Screenshots

Coming Soon

- Connection Screen
- Court Selection
- Match Selection
- Live Scoring Screen
- Timeout Screen

---

Technology Stack

- .NET MAUI
- C#
- SignalR
- Bluetooth LE
- SQLite
- MQTT Integration
- Android

---

Requirements

Development

- Visual Studio 2022 or later
- .NET SDK
- Android SDK

Device

Recommended:

- Android 10+
- 3GB RAM
- Wi-Fi Connection

---

Getting Started

Clone Repository

git clone https://github.com/yourusername/SpinastraRefereeApp.git

Open Solution

Open:

SpinastraRefereeApp.sln

using Visual Studio.

---

Restore Packages

dotnet restore

---

Build

dotnet build

---

Run on Android

Connect an Android device or emulator.

dotnet build -t:Run -f net10.0-android

---

Connecting to a Tournament

Server Mode

1. Launch the Referee App.
2. Select Server Mode.
3. Enter the server address if required.
4. Tap Connect.
5. Select assigned match.

Connection status:

🟢 Connected

🟡 Connecting

🔴 Disconnected

---

Bluetooth Mode

1. Launch the Referee App.
2. Select Bluetooth Mode.
3. Scan for devices.
4. Select:

Spinastra Court X

5. Connect.

Scores will be sent directly to the scoreboard.

---

Match Workflow

Start Match

Select Match
↓
Start Match
↓
Score 0-0 Sent
↓
Match Status = On Court

---

Update Score

Use:

+ Team A
- Team A

+ Team B
- Team B

All connected systems update instantly.

---

Change Server

Tap:

Switch Server

The serving indicator updates immediately.

---

Finish Match

Finish Match
↓
Confirm Winner
↓
Submit Result

Tournament standings and brackets update automatically.

---

Architecture

Referee App
       │
       ▼
Spinastra Scoring Server
       │
 ┌─────┼─────┐
 ▼     ▼     ▼
Live   ESP32 OBS
Queue  Score  Overlay
       Board

---

Permissions

Android permissions used:

INTERNET
ACCESS_NETWORK_STATE
BLUETOOTH
BLUETOOTH_CONNECT
BLUETOOTH_SCAN
NEARBY_WIFI_DEVICES

Additional permissions may vary by Android version.

---

Troubleshooting

Cannot Connect To Server

Verify:

- Server is running
- Same Wi-Fi network
- Correct server IP
- Firewall allows connection

---

Bluetooth Device Not Found

Verify:

- Scoreboard powered on
- Bluetooth enabled
- Device within range

---

Scores Not Updating

Verify:

- Active connection
- Correct court assignment
- Server running

---

Roadmap

Planned features:

- Cloud Synchronization
- Referee Login System
- Match History
- Voice Score Announcements
- Smartwatch Support
- Multi-Language Support
- Advanced Statistics

---

Related Projects

Spinastra Tournament Manager

Tournament creation, scheduling, live queue, standings, and tournament operations.

Spinastra Scoring Server

SignalR and MQTT server responsible for real-time score distribution.

Spinastra Digital Scoreboard

ESP32-powered wireless LED scoreboard system

License

Copyright © Spinastra

All Rights Reserved.

---

Support

For bug reports, feature requests, and support:

Create an issue in this repository.

---

Built with ❤️ for tournament organizers, referees, players, and spectators.
