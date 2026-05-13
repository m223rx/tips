# Challenge: Build a Dynamic To‑Do List with React

## Difficulty
Medium

## Description
Create a single‑page web application using React that allows users to manage a simple to‑do list. The app should let users add new tasks, mark them as completed, edit existing tasks, and delete tasks they no longer need. The interface must be responsive and provide immediate visual feedback for user actions.

## Requirements
- Use **function components** and **React Hooks** (`useState`, `useEffect`, etc.) to manage state.
- Display the list of tasks in a clean, readable layout.
- Provide an input field and an “Add” button (or press **Enter**) to create new tasks.
- Each task item should include:
  - The task text.
  - A checkbox (or similar control) to toggle completion status.
  - An “Edit” button that allows the user to modify the task text inline.
  - A “Delete” button to remove the task from the list.
- Persist the to‑do list in **localStorage** so that the data remains after a page refresh.
- Show a message or placeholder when the list is empty.
- Ensure the UI updates instantly without requiring a page reload.

## Bonus
- Implement **filtering** options to view All / Active / Completed tasks.
- Use **React Context** to share the task list and actions across components.
- Add basic **unit tests** with Jest and React Testing Library that cover adding, editing, completing, and deleting tasks.
- Write the application in **TypeScript** to enforce type safety.
- Add simple **animations** (e.g., fade‑in/out) when tasks are added or removed.