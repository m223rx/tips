# Challenge: Flutter Todo Tracker

## Difficulty  
**Medium**

## Description  
Build a simple yet polished **Todo Tracker** mobile app using Flutter. The app should allow users to create, view, edit, and delete todo items. Each todo item must contain a title, an optional description, and a completion status. The UI should be responsive and follow Material Design guidelines. Persist the data locally so that the list is retained between app launches.

## Requirements  
- **Home Screen** displaying a scrollable list of todos.  
- **Add Todo**: a screen or modal where users can enter a title (required) and description (optional).  
- **Edit Todo**: tapping an existing item opens a screen/modal allowing the user to modify its details.  
- **Toggle Completion**: users can mark a todo as completed/incomplete directly from the list (e.g., via a checkbox or swipe action).  
- **Delete Todo**: provide a way to remove a todo permanently (e.g., long‑press, swipe, or a delete button).  
- **Persistence**: store todos locally using a suitable method (e.g., `shared_preferences`, `sqflite`, `hive`, or `moor`). The data must survive app restarts.  
- **State Management**: implement state handling using a pattern/library of your choice (e.g., Provider, Riverpod, Bloc, GetX, etc.).  
- **Input Validation**: prevent adding or saving a todo with an empty title and display appropriate error messages.  
- **Responsive Layout**: ensure the UI works well on both portrait and landscape orientations and adapts to different screen sizes.  

## Bonus  
- Implement a **dark mode** toggle that respects the device’s theme settings.  
- Add **search** functionality to filter todos by title or description.  
- Include **animations** for adding, editing, and deleting items (e.g., fade‑in/out, slide transitions).  
- Write **unit and widget tests** covering core functionalities (adding, editing, deleting, persistence).  
- Allow users to **reorder** todos via drag‑and‑drop.  
- Sync todos with a simple **REST API** using `http` or `dio`, handling offline scenarios gracefully.  