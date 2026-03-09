# 📝 Interactive To-Do List

A sleek, responsive Task Management application built with **Vanilla JavaScript**, **HTML5**, and **CSS3**. This project features persistent data storage using the browser's **LocalStorage API**, ensuring your tasks remain saved even after a page refresh.

## 🚀 Live Demo
[Explore the Live Project](https://mooraxx1.github.io/To-Do-List/)

## ✨ Key Features
* **Add & Manage Tasks:** Quickly add new items to your daily workflow.
* **Interactive UI:** Toggle completion status with a single click (includes visual "checked" state).
* **Persistent Storage:** Uses `LocalStorage` so your data stays on your device—no database required.
* **Quick Delete:** Instantly remove individual tasks using the "×" action button.
* **Fully Responsive:** Optimized for a seamless experience across mobile, tablet, and desktop.

## 🛠️ Tech Stack
* **HTML5:** Semantic structure for better SEO and accessibility.
* **CSS3:** Custom styling using Flexbox and CSS Grid for a modern layout.
* **JavaScript (ES6):** Efficient DOM manipulation and event handling.
* **LocalStorage API:** Client-side data persistence.

## 🧠 How It Works
### Efficient Event Logic
The application utilizes **Event Delegation** on the main container. Instead of attaching listeners to every task, a single listener handles clicks for both the list items (`<li>`) and the delete buttons (`<span>`), making the app faster and more memory-efficient.

### Data Persistence
Every time a task is added, checked, or deleted, the `saveData()` function is triggered:
```javascript
function saveData(){
    localStorage.setItem("data", listContainer.innerHTML);
}
