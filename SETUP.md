# Setup & Build Instructions

## Prerequisites
- Android Studio (latest version)
- JDK 11 or higher
- Android SDK API 34+

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/adnanyasin57-sudo/invoice-app.git
   cd invoice-app
   ```

2. **Open in Android Studio:**
   - Open Android Studio
   - Select "Open an Existing Project"
   - Navigate to the cloned directory

3. **Install dependencies:**
   - Android Studio will automatically detect and install gradle dependencies
   - Wait for the Gradle build to complete

## Building

### Debug APK
```bash
./gradlew assembleDebug
```

The debug APK will be generated at: `app/build/outputs/apk/debug/app-debug.apk`

### Release APK
```bash
./gradlew assembleRelease
```

The release APK will be generated at: `app/build/outputs/apk/release/app-release.apk`

## Running on Emulator/Device

1. **Connect device or start emulator**
2. **Run the app:**
   ```bash
   ./gradlew installDebug
   ```
   Or click "Run" in Android Studio

## Features

- ✅ Create invoices with client details
- ✅ Add multiple items/services per invoice
- ✅ Automatic calculation of totals and taxes
- ✅ Generate PDF invoices
- ✅ Share invoices via email
- ✅ Offline-first with local database
- ✅ Material Design UI
- ✅ Kotlin + Coroutines

## Architecture

- **MVVM** - Model-View-ViewModel pattern
- **Room Database** - Local SQLite database
- **LiveData & StateFlow** - Reactive data binding
- **Coroutines** - Asynchronous operations

## Permissions Required

- `INTERNET` - For sharing via email
- `READ_EXTERNAL_STORAGE` - For accessing files
- `WRITE_EXTERNAL_STORAGE` - For saving PDFs

## Troubleshooting

### Build Issues
- Clean and rebuild: `./gradlew clean build`
- Invalidate caches: File → Invalidate Caches in Android Studio

### Runtime Issues
- Check logs: `adb logcat`
- Ensure permissions are granted on the device

## Support
For issues, please create a GitHub issue in the repository.
