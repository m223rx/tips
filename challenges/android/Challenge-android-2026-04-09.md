# Challenge: **Dynamic Theme Switcher for Android Apps**

## Difficulty  
Medium

## Description  
Create an Android application that allows users to switch between multiple visual themes (e.g., Light, Dark, and a custom Colorful theme) at runtime without restarting the app. The selected theme should persist across app restarts and be applied automatically when the app launches.  

Key aspects to consider:  
- Use Android’s theming system (`styles.xml`, `themes.xml`).  
- Implement a settings screen where the user can pick a theme.  
- Apply the chosen theme instantly to all visible activities/fragments.  
- Store the user’s preference using a persistent mechanism (e.g., `SharedPreferences` or Jetpack DataStore).  
- Ensure that UI elements (toolbar, status bar, navigation bar, dialogs, etc.) respect the current theme.

## Requirements  
- The app must contain at least **two** activities (or fragments) to demonstrate that the theme change propagates throughout the app.  
- Provide a **Settings** screen where the user can select one of the available themes.  
- Changing the theme should be reflected **immediately** on the current screen and any subsequently opened screens.  
- Persist the selected theme so that after the app is closed and reopened, the last chosen theme is applied automatically.  
- Use only Android SDK and Jetpack libraries that are publicly available (no third‑party UI kits).  
- The UI should be responsive and handle configuration changes (e.g., rotation) without losing the theme selection.

## Bonus  
- Add a **preview** of each theme in the Settings screen before the user confirms the selection.  
- Support **system default** mode: if the user selects this option, the app follows the device’s current dark/light mode automatically.  
- Implement a **custom Theme Builder** that lets users pick primary and accent colors using Material Color Picker dialogs, generating a new theme on the fly.  
- Use **Jetpack Compose** for the UI instead of XML layouts.  
- Write unit/instrumented tests to verify that the theme persists correctly and that UI components update as expected.  