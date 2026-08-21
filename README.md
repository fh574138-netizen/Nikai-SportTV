# Nikai Smart TV Sports Streaming App 🏏⚽

A lightweight, high-performance Android Application built specifically for older Smart TVs (specifically targetting **Android 4.4.4 KitKat**, **Quad-Core CPU**, and **Mali-400 GPU**).

## 🌟 Features
- **Low Hardware Overhead:** Smooth 720p H.264 playback tailored for Mali-400 GPUs.
- **TV Remote Integration:** Native D-Pad navigation support with custom focus selectors.
- **AI-Powered Schedule Updates:** Integrates with Node.js & Gemini AI backend to dynamically parse and display live cricket and football schedules.
- **TLS/SSL Supported:** Powered by `OkHttp 3.12.13` to handle HTTPS stream URLs on Android 4.4 KitKat seamlessly.

---

## 📺 Supported Channels & Categories
- **Bangladesh (BD):** T Sports, GTV (Gazi TV), BTV Sports
- **India (IND):** Star Sports Network, Sony Sports Network, Sports18
- **Pakistan (PAK):** PTV Sports, A Sports, Geo Super
- **International:** beIN Sports Network

---

## 🏗️ Project Setup & Installation

### Requirements
- **Target OS:** Android 4.4.4 (API 19) or higher
- **GPU Architecture:** Mali-400 or compatible ARM GPUs
- **Dependencies:** AndroidX, OkHttp `3.12.13`, RecyclerView

### How to Build
1. Clone this repository:
   ```bash
   git clone [https://github.com/YOUR_USERNAME/NikaiSportsTV.git](https://github.com/YOUR_USERNAME/NikaiSportsTV.git)


MIT License

Copyright (c) 2026 Nikai TV Sports App Developer

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY FROM_OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER
DEALINGS IN THE SOFTWARE.



# Built application files
*.apk
*.aar
*.war
*.ear

apply plugin: 'com.android.application'

android {
    compileSdkVersion 28
    defaultConfig {
        applicationId "com.nikai.crickettv"
        minSdkVersion 19
        targetSdkVersion 28
        versionCode 1
        versionName "1.0"
    }
}

dependencies {
    implementation 'androidx.appcompat:appcompat:1.0.2'
    implementation 'androidx.recyclerview:recyclerview:1.0.0'
    implementation 'com.squareup.okhttp3:okhttp:3.12.13'
}

<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.nikai.crickettv">

    <uses-permission android:name="android.permission.INTERNET" />

    <application
        android:hardwareAccelerated="true"
        android:label="CricTV Live"
        android:theme="@style/Theme.AppCompat.NoActionBar">
       
        <activity android:name=".MainActivity">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />
                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>

        <activity
            android:name=".PlayerActivity"
            android:configChanges="orientation|screenSize"
            android:screenOrientation="landscape" />
    </application>
</manifest>
# Gradle files
.gradle/
build/
*/build/

# IDE specific files
.idea/
.navigation/
*.iml
*.iws
*.ipr
.DS_Store

# Local configuration file (sdk path, etc)
local.properties

# Log files
*.log
