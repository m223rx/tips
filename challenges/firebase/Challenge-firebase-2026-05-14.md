# Challenge: Real‑time Chat Application with Firebase

## Difficulty
Medium

## Description  
Create a minimal web‑based chat application that leverages Firebase services to enable users to sign in and exchange messages in real time. The app should be responsive, store messages persistently, and display new messages instantly as they are posted by any participant.

## Requirements
- **Firebase Authentication**: Users must sign in using **email/password** (no third‑party providers required). Display the logged‑in user’s email or display name in the UI.
- **Firestore (or Realtime Database)**: Store each chat message with at least the following fields:  
  - `authorId` (UID of the sender)  
  - `authorEmail` (email of the sender)  
  - `content` (text of the message)  
  - `timestamp` (server‑generated time of creation)
- **Real‑time Updates**: The UI must automatically display new messages as soon as they are added to the database without requiring a page refresh.
- **Message Input**: Provide a text input field and a “Send” button that lets the authenticated user post a new message.
- **Message List**: Show the list of messages in chronological order, displaying the sender’s email, the message text, and a formatted timestamp.
- **Security Rules**: Write Firebase security rules that allow only authenticated users to read/write messages and ensure users can only modify (edit/delete) their own messages.
- **Deployment**: Deploy the finished application to a public URL using **Firebase Hosting** (or any static‑site hosting service that can serve the built assets).

## Bonus
- **Anonymous (guest) chat**: Allow users to join the chat without creating an account, using Firebase’s anonymous authentication, while still preserving a unique identifier for each guest.
- **Message Editing / Deletion**: Implement UI controls for a user to edit or delete *their own* messages and update the database accordingly.
- **Typing Indicator**: Show a “User is typing…” indicator when another participant is currently composing a message.
- **Pagination / Infinite Scroll**: Load the most recent N messages initially and lazily load older messages as the user scrolls up.
- **Offline Support**: Enable the app to queue messages while offline and automatically sync them when the network connection is restored, using Firebase’s offline persistence features.