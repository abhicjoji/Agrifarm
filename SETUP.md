# Setup Guide

## Quick Start

1. **Open in Android Studio**
   - Open Android Studio
   - Select "Open" and choose this project directory
   - Wait for Gradle sync to complete

2. **Add Launcher Icons** (Required)
   - Right-click on `app/src/main/res` → New → Image Asset
   - Create launcher icons for `ic_launcher` and `ic_launcher_round`
   - Or use Android Studio's built-in icon generator

3. **Configure API Key** (Optional for full AI features)
   - Open `app/src/main/java/com/learnnotes/app/data/api/ApiClient.kt`
   - Uncomment and add your OpenAI API key:
   ```kotlin
   requestBuilder.header("Authorization", "Bearer YOUR_API_KEY_HERE")
   ```
   - Note: The app works in demo mode without an API key

4. **Build and Run**
   - Connect an Android device or start an emulator (API 24+)
   - Click the Run button or press Shift+F10
   - The app will install and launch

## Building Release APK

1. **Generate Signed Bundle/APK**
   - Build → Generate Signed Bundle / APK
   - Create a new keystore or use existing
   - Select release build variant
   - Follow the wizard to complete

2. **Or use Gradle**
   ```bash
   ./gradlew assembleRelease
   ```
   APK will be in `app/build/outputs/apk/release/`

## Troubleshooting

- **Gradle Sync Failed**: Check internet connection, ensure JDK 17+ is installed
- **Build Errors**: Clean project (Build → Clean Project) then rebuild
- **API Errors**: Check API key configuration and internet connection
- **Missing Icons**: Create launcher icons using Android Studio's Image Asset Studio

## Requirements

- Android Studio Hedgehog (2023.1.1) or later
- JDK 17 or later
- Android SDK 24 (minimum), 34 (target)
- Internet connection (for AI features)

