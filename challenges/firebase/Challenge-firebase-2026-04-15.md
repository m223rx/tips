# Challenge: Firebase Todo App with Real‑Time Sync

## Difficulty  
Medium  

## Description  
Create a web‑based Todo application that uses **Firebase** for authentication and data storage. Users should be able to sign up/in with email & password, add, edit, delete, and toggle completion of todo items. All changes must be synchronized in real time across multiple devices or browser tabs logged in with the same account.

## Requirements  

- **Authentication**  
  - Implement sign‑up and sign‑in using Firebase Authentication (email & password).  
  - Include a secure sign‑out button.  

- **Data Model**  
  - Store todo items in **Cloud Firestore** under a collection that is scoped to the authenticated user (e.g., `users/{uid}/todos`).  
  - Each todo document must contain at least:  
    - `title` (string)  
    - `completed` (boolean)  
    - `createdAt` (timestamp)  

- **CRUD Operations**  
  - **Create**: Allow the user to add a new todo with a title.  
  - **Read**: Display the list of todos, ordered by `createdAt` (newest first).  
  - **Update**: Enable editing the title and toggling the `completed` status.  
  - **Delete**: Allow removal of a todo item.  

- **Real‑Time Sync**  
  - Use Firestore real‑time listeners so that any change (add, edit, delete, toggle) is instantly reflected in the UI on all active sessions of the same user.  

- **UI/UX**  
  - Simple, responsive UI (plain HTML/CSS or a framework of your choice).  
  - Show a loading indicator while authentication state or data is being fetched.  
  - Display appropriate error messages for authentication failures and Firestore operations.  

- **Deployment**  
  - Deploy the finished app to **Firebase Hosting** (or any static hosting) and ensure it works over HTTPS.  

## Bonus  

- **Social Login**: Add Google and/or Facebook sign‑in using Firebase Authentication.  
- **Offline Support**: Enable Firestore offline persistence so the app works without an internet connection and syncs when back online.  
- **Optimistic UI**: Implement optimistic UI updates for a smoother user experience.  
- **Security Rules**: Write Firestore security rules that enforce that users can only read/write their own todo documents.  
- **Unit Tests**: Add a suite of unit/integration tests (e.g., using Jest with the Firebase emulator suite).  
- **CI/CD**: Set up continuous integration that runs tests and automatically deploys to Firebase Hosting on successful merges.  