# 📝 Notes App – Vanilla JavaScript Project

A fully functional **Notes Application** built using **HTML, CSS, and Vanilla JavaScript**, designed to help users create, view, edit, and delete notes with a clean and intuitive interface.  
All data is stored persistently using the browser’s **LocalStorage**, making this app lightweight and backend-free.

This project focuses on **core web fundamentals** such as DOM manipulation, event handling, URL-based navigation, and client-side storage.

---

## 📌 Table of Contents
- Overview
- Features
- Technologies Used
- Project Structure
- Application Flow
- Pages Explanation
- LocalStorage Data Design
- Key JavaScript Concepts Used
- Validation & Edge Case Handling
- UI & Design Choices
- How Navigation Works
- How to Run the Project
- Limitations
- Future Enhancements
- Learning Outcomes
- Author

---

## 📖 Overview

The Notes App allows users to:
- Write personal notes
- Save them locally in the browser
- Reopen notes even after refreshing the page
- Edit or delete notes on a separate page

The application is intentionally built **without frameworks** to strengthen understanding of **pure JavaScript logic** and browser APIs.

---

## ✨ Features

- ➕ Create notes with title and content  
- 📋 Display notes in a grid (sticky-note style)  
- ✏️ Edit existing notes  
- 🗑️ Delete notes permanently  
- 🔗 Navigate between pages using URL parameters  
- 💾 Persistent storage with LocalStorage  
- 🧼 Input validation using `.trim()`  
- 📱 Responsive and user-friendly UI  
- 🎨 Soft, notebook-inspired color scheme  

---

## 🛠️ Technologies Used

- **HTML5** – Structure and layout  
- **CSS3** – Styling, layout, and responsiveness  
- **JavaScript (ES6)** – Logic and interactivity  
- **Browser LocalStorage API** – Data persistence  

> ❌ No frameworks  
> ❌ No backend  
> ✅ Runs entirely in the browser  

---

## 🗂️ Project Structure


---

## 🔁 Application Flow

1. User opens `index.html`
2. User adds a new note (title + content)
3. Note is saved to LocalStorage with a unique ID
4. All notes are displayed as clickable cards
5. Clicking a note redirects to `note.html?id=<noteId>`
6. User edits or deletes the note
7. Changes are saved back to LocalStorage
8. User is redirected back to the main page

---

## 📄 Pages Explanation

### 1️⃣ `index.html` – Main Notes Page

**Responsibilities:**
- Collect note title and content
- Display all saved notes
- Handle navigation to edit page

**Key Functionalities:**
- Reads existing notes from LocalStorage
- Generates unique IDs for each note
- Prevents empty note creation
- Redirects to edit page using `window.location`

**Navigation Logic:**
```js
window.location.href = `note.html?id=${note.id}`;
