## Beginner Mini Project: Interactive Profile Card

Build a tiny "profile card" page and make a few upgrades. Each step gives you one more thing to tweak so you get used to editing both HTML and JavaScript.

- **What you'll practice**
  - Organizing a basic layout with HTML containers.
  - Styling elements with a bit of inline CSS (feel free to move styles into a `<style>` block or external file later).
  - Updating text content and styles in response to button clicks and input changes.

### Starter Markup

Paste this into `profile.html` (or re-use `index.html` if you want). Then complete the TODOs below.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Mini Profile Card</title>
    <style>
      body {
        font-family: Arial, sans-serif;
        background: #f2f5f9;
        display: flex;
        align-items: center;
        justify-content: center;
        min-height: 100vh;
      }
      .card {
        background: white;
        width: 320px;
        padding: 1.5rem;
        border-radius: 12px;
        box-shadow: 0 20px 40px rgba(15, 23, 42, 0.15);
        transition: transform 0.2s ease;
      }
      .card h1 {
        margin-bottom: 0.25rem;
      }
      .badge {
        display: inline-block;
        padding: 0.25rem 0.75rem;
        border-radius: 999px;
        background: #e0f2ff;
        color: #0369a1;
        font-size: 0.75rem;
        text-transform: uppercase;
        letter-spacing: 0.05em;
      }
      button {
        padding: 0.5rem 1rem;
        border: none;
        border-radius: 6px;
        background: #2563eb;
        color: white;
        cursor: pointer;
        transition: background 0.2s ease;
      }
      button:hover {
        background: #1d4ed8;
      }
      .hidden {
        display: none;
      }
    </style>
  </head>
  <body>
    <div class="card" id="profileCard">
      <span class="badge" id="statusBadge">Newbie</span>
      <h1 id="displayName">Your Name</h1>
      <p id="displayRole">Aspiring Front-End Developer</p>

      <input
        id="nameInput"
        type="text"
        placeholder="Type a display name"
        style="width: 100%; margin: 0.75rem 0; padding: 0.5rem"
      />

      <div style="display: flex; gap: 0.5rem">
        <button id="toggleDetails">Toggle Details</button>
        <button id="levelUp">Level Up Badge</button>
      </div>

      <p id="details" style="margin-top: 1rem">
        🧠 Favorite topic: <span id="favoriteTopic">DOM & Events</span>
      </p>
    </div>

    <script>
      const nameInput = document.getElementById("nameInput");
      const displayName = document.getElementById("displayName");
      const favoriteTopic = document.getElementById("favoriteTopic");
      const toggleDetailsButton = document.getElementById("toggleDetails");
      const detailsSection = document.getElementById("details");
      const levelUpButton = document.getElementById("levelUp");
      const statusBadge = document.getElementById("statusBadge");
      const profileCard = document.getElementById("profileCard");

      // TODO 1: whenever the input changes, update the heading text.

      // TODO 2: make the topic change to "JavaScript Events" the first time the card gets clicked.
      // (Hint: listen for `click` on profileCard, and only update if the topic isn't already changed.)

      // TODO 3: when the "Toggle Details" button is pressed, hide/show the entire details paragraph.
      // (Hint: toggle the "hidden" class on detailsSection.)

      // TODO 4: when "Level Up Badge" is clicked, change the badge text from "Newbie" to "Rising Star"
      // and add a subtle card hover effect by temporarily scaling the card slightly (use transform).

      // TODO 5 (optional): change the page background color to something else after 5 seconds using setTimeout.
      
    </script>
  </body>
</html>
```

- **Bonus ideas**
  - Add an `<img>` to show an avatar.
  - Swap the badge colors when the badge text changes.
  - Count how many times the details have been toggled and show it next to the button.

