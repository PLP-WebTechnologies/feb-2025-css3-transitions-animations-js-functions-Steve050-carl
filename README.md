# CSS3 Transitions, Animations, and Advanced JavaScript Functions

## Objectives

Create smooth CSS transitions and animations.
Use JavaScript functions for dynamic behavior.
Implement local storage for data persistence.

## Instructions
Add CSS animations to elements like buttons or images.

>[!NOTE]
> - Write a JavaScript function that:
> - Stores and retrieves user preferences using localStorage.
> - Implements an animation triggered by user actions.

## Tasks

Create a CSS animation.
Store data in localStorage.
Apply JavaScript to trigger animations.

Happy Coding! 💻✨


//CSS3 Animation
/* style.css */
button {
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
  border: none;
  border-radius: 5px;
  transition: transform 0.3s ease, background-color 0.3s ease;
}

button:hover {
  transform: scale(1.1);
  background-color: #3498db;
}


//JS Function to store and retrieve user preferences
// script.js
function saveUserPreferences(preferenceKey, preferenceValue) {
  localStorage.setItem(preferenceKey, preferenceValue);
}

function loadUserPreferences(preferenceKey) {
  return localStorage.getItem(preferenceKey);
}

// Example: Save the button color preference
let button = document.querySelector('button');
button.addEventListener('click', () => {
  let newColor = button.style.backgroundColor === 'rgb(52, 152, 219)' ? '#e74c3c' : '#3498db';
  button.style.backgroundColor = newColor;
  
  // Save user preference
  saveUserPreferences('buttonColor', newColor);
});

// Retrieve and apply the user preference (if any)
let savedColor = loadUserPreferences('buttonColor');
if (savedColor) {
  button.style.backgroundColor = savedColor;
}

