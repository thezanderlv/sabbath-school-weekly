# Sabbath School – Weekly (Android)

An Android port of the **Sabbath School – Weekly Grabber** web tool. It collects weekly lessons from the Adventech Sabbath School repository and presents them with selectable spacing, separators and Bible verse text.

## Features
- Automatically fetch the current or previous week's lesson.
- Merge individual day markdown files into one document.
- Include verse text using KJV, ASV, WEB or a custom translation code.
- Copy the generated markdown or download it as a `.txt` file.

## Building and running
1. Install the [Android SDK or Android Studio](https://developer.android.com/studio).
2. Connect a device or start an emulator.
3. From the project root, build and install the debug variant:

   ```bash
   ./gradlew installDebug
   ```

The app loads the HTML interface from `app/src/main/assets/index.html` inside a `WebView`.

## Project structure
- `app/src/main/assets/index.html` – original browser-based interface.
- `app/src/main/java/com/zuntopia/sabbath_school_weekly/MainActivity.kt` – hosts the interface in a WebView using Jetpack Compose.
- `app/src/main/AndroidManifest.xml` – declares the `MainActivity` and requests Internet access.

## Usage
1. Launch the app.
2. Choose language, quarter and week, or use **Auto: Last Week** / **Auto: This Week** for quick filling.
3. Optionally adjust the separator, spacing and Bible version options.
4. Tap **Fetch** to download content.
5. Copy or download the combined markdown once the status reads `Done.`

## License
[MIT](LICENSE)
