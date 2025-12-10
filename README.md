# StickerSmash (Personal Portfolio & Task Manager App)

**Made by:** Dhiraj Kumar  
**Version:** `1.0.2`  

StickerSmash is a personal React Native app built with **Expo**.  
It combines:

- A personal **profile / portfolio home screen**
- A **GitHub Explorer** page
- A **Task Manager** with local storage
- A **Settings** screen with **Light/Dark theme toggle**

---

## 📲 Download the App (APK)

> 👉 Once you have a successful EAS build, copy the APK link from Expo and paste it below.

[⬇️ Download StickerSmash APK](https://expo.dev/your-apk-download-link-here)

> Replace the URL above with the APK link from your Expo build page (from `eas build`).

---

## 🧩 Features

### 🏠 Home Screen

- Large **profile avatar** – tap to select and upload an image from the local gallery.
- Editable **profile details**:
  - **Name:** Dhiraj Kumar
  - **DOB:** 15 Aug 2002
  - **Email:** `dhiraj7kr@gmail.com` (tap to open default mail app)
  - **LinkedIn:** `https://www.linkedin.com/in/dhiraj7kr/` (tap to open in browser)
  - **GitHub:** `https://github.com/dhiraj7kr` (tap to open in browser)
  - **Title:** e.g. “Software Engineer at Acuvate Software” (editable)
  - **YOE (Years of Experience):** editable field, displayed as `YOE: 1.5`
- Single **Edit** button on the card to toggle edit mode for all profile fields.
- “About This App” section summarizing:
  - Overview
  - GitHub Explorer
  - Task Manager
- Bottom navigation icons:
  - **Home**
  - **Git**
  - **Tasks**
  - **Settings**

---

### 🐙 GitHub Explorer (Git Screen)

- Input field for **GitHub username**.
- Fetches all public repos for that user and shows **one random repo**.
- Shows repo details:
  - Name
  - Description
  - Stars
  - Language
  - Clickable **GitHub URL** (opens in browser).
- Error and loading states:
  - Handles “user not found”, “no public repos”, etc.

---

### ✅ Tasks Screen

- **Add Task** button that toggles the task form visibility:
  - When closed: only button and tasks list are visible.
  - When open: shows task form + tasks list below.
- Task form fields:
  - **Title** *(required)*
  - **Description** (optional)
  - **Due date** (optional, free text, e.g. `25 Dec 2025`)
  - **Time** (optional, e.g. `10:00 AM`)
  - **Link** (optional, clickable in details)
  - **Location** (optional)
  - **User** (optional – assigned to)
- Task list:
  - Shows **all tasks in a list**, with only the **Title** visible by default.
  - Tap a task to **expand/collapse** its details.
- In expanded view:
  - Shows all entered fields where available.
  - Action chips:
    - **Edit** – loads task into the form and opens the form.
    - **Mark complete / Mark as active** – toggles completion state.
    - **Delete** – deletes the task with confirmation dialog.
- Completed tasks:
  - Displayed with line-through text and slightly dimmed.
- All tasks are **persisted in local storage** via `AsyncStorage`:
  - Tasks are restored when the app is reopened.

---

### ⚙️ Settings Screen

- **Theme** card:
  - Switch between **Day Mode** (light theme by default) and **Night Mode** (dark theme).
  - Uses a custom `ThemeProvider` and `useTheme` hook.
- Settings list items (UI only placeholders for now):
  - Profile
  - Notifications
  - Security
  - About App
- “About This App” section:
  - Short description of the app.
  - **Made by:** Dhiraj Kumar
  - **Initial Release:** December 2025
  - **Version:** `1.0.2`
- Footer:
  - “Made by Dhiraj Kumar”
  - “Version 1.0.2”

---

## 🏗 Tech Stack

- **Framework:** React Native
- **App Runtime:** Expo
- **Navigation:** Expo Router (`Stack` navigation)
- **Styling:** React Native `StyleSheet`
- **Icons:** `@expo/vector-icons` (`Ionicons`, `MaterialIcons`)
- **Image Picker:** `expo-image-picker` (for avatar upload)
- **Local Storage:** `@react-native-async-storage/async-storage`
- **Build System:** EAS Build (Expo Application Services)

---

## 📂 Project Structure (simplified)

```text
StickerSmash/
  app/
    _layout.tsx          # Root navigation stack with theme
    index.tsx            # Home screen (Profile & overview)
    git.tsx              # GitHub Explorer screen
    tasks.tsx            # Task Manager screen
    settings.tsx         # Settings + Theme + About
    theme-context.tsx    # ThemeProvider and useTheme hook
  assets/
    icon.png
    splash.png
  app.json
  eas.json
  package.json
  README.md              # You are here
