# Challenge: Interactive Todo List with Drag‑and‑Drop

## Difficulty
Medium

## Description
Create a single‑page React application that manages a list of todo items. Users should be able to:

* Add new todos with a title and optional description.
* Mark todos as completed or uncompleted.
* Delete todos.
* Reorder todos by dragging and dropping them into a new position.

The UI should update instantly without requiring a page refresh, and the state of the todo list must persist across browser reloads using `localStorage`.

## Requirements
- Use **React 18** with functional components and hooks only (no class components).
- The main component should be named `TodoApp`.
- Implement a controlled input form for adding new todos.
- Display each todo with:
  - A checkbox to toggle its completed state.
  - The todo title (and description, if provided).
  - A delete button.
- Use a popular drag‑and‑drop library (e.g., `react-beautiful-dnd` or `@dnd-kit/core`) to enable reordering of todos.
- Store the todo list in `localStorage` after any change (add, toggle, delete, reorder) and load it on app initialization.
- Apply basic styling so the app is visually clear and responsive (you may use CSS modules, styled‑components, or plain CSS).

## Bonus
- Implement an edit mode that lets users modify the title and description of an existing todo.
- Add a filter to show **All**, **Active**, or **Completed** todos.
- Include a light/dark theme toggle that persists the selected theme in `localStorage`.
- Write unit tests for the main components using **React Testing Library** and **Jest**.