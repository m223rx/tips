# Challenge: Flutter Todo List App

## Difficulty
Medium

## Description
Create a mobile Todo List application using Flutter. The app should allow users to manage their tasks efficiently with a clean and responsive UI. Users must be able to add new tasks, mark them as completed, edit task details, and delete tasks. All data should persist between app launches.

## Requirements
- **User Interface**
  - A main screen displaying a scrollable list of tasks.
  - Each task item should show its title, an optional description, and a checkbox to mark completion.
  - Floating Action Button (FAB) to add a new task.
- **Task Management**
  - Ability to add a new task with a title (required) and description (optional).
  - Ability to edit an existing task's title and description.
  - Ability to delete a task with a confirmation prompt.
  - Ability to toggle a task's completed state via the checkbox.
- **Persistence**
  - Store tasks locally so they persist across app restarts (e.g., using `shared_preferences`, `hive`, or `sqflite`).
- **State Management**
  - Use a state management solution such as Provider, Riverpod, Bloc, or GetX to handle UI updates.
- **Responsiveness**
  - Ensure the UI adapts gracefully to different screen sizes and orientations.

## Bonus
- Implement drag‑and‑drop reordering of tasks.
- Add a filter to view All / Active / Completed tasks.
- Support dark mode with automatic theme switching.
- Sync tasks with a cloud backend (e.g., Firebase Firestore) for cross‑device access.
- Add local notifications to remind users of pending tasks at a scheduled time.