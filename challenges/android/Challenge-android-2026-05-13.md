# Challenge: **Dynamic Theme Switcher for Android Apps**

## Difficulty
Medium

## Description
Create an Android application that allows users to switch between multiple visual themes (e.g., Light, Dark, and a custom color theme) at runtime without restarting the app. The selected theme should persist across app launches. The UI should include a settings screen where users can select their preferred theme, and the rest of the app's UI should instantly reflect the change.

## Requirements
- Build the app using **Kotlin** and **Android Jetpack** components.
- Implement at least three distinct themes (Light, Dark, Custom) using `styles.xml` and/or **Material Design Theming**.
- Provide a **Settings** screen with a `Preference` or custom UI element (e.g., `RadioGroup`) to let the user choose a theme.
- Apply the chosen theme **immediately** across all currently visible activities/fragments without requiring a full app restart.
- Persist the selected theme using **DataStore**, **SharedPreferences**, or another appropriate storage mechanism so that the theme is retained after the app is closed and reopened.
- Ensure that the theme change also updates system UI elements where possible (e.g., status bar, navigation bar colors).
- Handle configuration changes (such as device rotation) gracefully, keeping the selected theme applied.

## Bonus
- Add a **Live Preview** on the Settings screen that shows how the app will look with each theme before the user commits to the change.
- Support a **Dynamic Color** option that pulls colors from the user's wallpaper (Android 12+ `Material You` theming).
- Implement theme transition animations for a smoother visual experience when switching themes.
- Provide an option for the app to follow the **system‑wide theme setting** (i.e., automatically switch between Light and Dark based on the device's UI mode).