# LearnNotes - AI-Powered Note Management & Learning App

An Android application built with Kotlin and Jetpack Compose that combines note-taking, AI chatbot assistance, and interactive learning tools.

## Features

### 📝 Note Management
- Create, edit, and delete notes
- Persistent local storage using Room Database
- Clean, modern UI with Material Design 3
- Timestamp tracking for all notes

### 🤖 AI Chatbot
- Interactive AI assistant powered by OpenAI API
- Context-aware conversations
- Help with note organization and learning
- Real-time chat interface

### 🎓 Learning System
- Interactive flashcards for studying
- Flip animation for question/answer cards
- Navigate through flashcard sets
- Create custom flashcards from your notes

## Tech Stack

- **Language**: Kotlin
- **UI Framework**: Jetpack Compose
- **Architecture**: MVVM (Model-View-ViewModel)
- **Database**: Room Database
- **Networking**: Retrofit + OkHttp
- **Dependency Injection**: Manual (Factory pattern)
- **Coroutines**: For asynchronous operations

## Setup Instructions

### Prerequisites
- Android Studio Hedgehog (2023.1.1) or later
- JDK 17 or later
- Android SDK 24+ (minimum), 34 (target)

### Installation

1. Clone or download this repository
2. Open the project in Android Studio
3. Sync Gradle files
4. (Optional) Configure AI API:
   - Open `app/src/main/java/com/learnnotes/app/data/api/ApiClient.kt`
   - Add your OpenAI API key in the interceptor:
   ```kotlin
   requestBuilder.header("Authorization", "Bearer YOUR_API_KEY")
   ```
   - Note: The app includes a demo mode that works without an API key

5. Build and run the app on an emulator or physical device

## Project Structure

```
app/
├── src/main/
│   ├── java/com/learnnotes/app/
│   │   ├── data/
│   │   │   ├── api/          # API service and client
│   │   │   ├── dao/          # Room DAOs
│   │   │   ├── database/     # Room database
│   │   │   ├── model/        # Data models
│   │   │   └── repository/   # Repository layer
│   │   ├── ui/
│   │   │   ├── navigation/   # Navigation setup
│   │   │   ├── screens/      # Compose screens
│   │   │   ├── theme/        # App theme
│   │   │   └── viewmodel/    # ViewModels
│   │   └── MainActivity.kt
│   └── res/                   # Resources
└── build.gradle.kts
```

## Building for Production

1. Update version code and name in `app/build.gradle.kts`
2. Configure ProGuard rules (already included)
3. Build release APK:
   ```bash
   ./gradlew assembleRelease
   ```
4. Or generate signed bundle:
   ```bash
   ./gradlew bundleRelease
   ```

## API Configuration

The app uses OpenAI's GPT API for the chatbot feature. To enable full functionality:

1. Get an API key from [OpenAI](https://platform.openai.com/)
2. Add it to `ApiClient.kt` (consider using environment variables or secure storage for production)
3. The app will fall back to demo mode if no API key is configured

## License

This project is created for educational purposes.

## Contributing

Feel free to submit issues and enhancement requests!

