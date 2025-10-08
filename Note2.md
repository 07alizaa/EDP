````markdown
# Understanding: index.html, style.css, and script-step3.js

### What Step 3 Does
Step 3 extends Step 2 by adding **dynamic button creation** and **event delegation**.

---

### What the HTML Does
```html
<input id="inputField" placeholder="Type something">
<button id="submitBtn">Submit</button>
<p id="output"></p>
<div id="buttonContainer"></div>
<button id="addBtn">Add New Button</button>
````

* **inputField** → where the user types text
* **submitBtn** → triggers the event when clicked
* **output** → shows the submitted text
* **addBtn** → adds new buttons dynamically
* **buttonContainer** → holds all dynamically added buttons

The page waits for user actions — that’s event-driven behavior.

---

### What the JavaScript Does

```javascript
// Submit button
document.getElementById('submitBtn').addEventListener('click', function() {
   let input = document.getElementById('inputField').value;
   document.getElementById('output').innerText = "You entered: " + input;
});

// Add new button dynamically
document.getElementById('addBtn').addEventListener('click', function() {
   let newButton = document.createElement('button');
   newButton.innerText = "New Button";
   document.getElementById('buttonContainer').appendChild(newButton);
});

// Event delegation for dynamic buttons
document.getElementById('buttonContainer').addEventListener('click', function(e) {
   if (e.target.tagName === 'BUTTON') {
       alert('You clicked ' + e.target.innerText);
   }
});
```

* **Submit button** → waits for click, then shows: `You entered: <text>`
* **Add New Button** → creates a new button dynamically inside `buttonContainer`
* **Event delegation** → detects clicks on any button inside `buttonContainer` and shows an alert with its text

---

### In Simple Words

Nothing happens until you click something.
Click **Submit** → shows input text.
Click **Add New Button** → adds a new button.
Click any button inside the container → shows alert with its name.

---

### Summary Table

| Concept            | Example / Action                       |
| ------------------ | -------------------------------------- |
| **Event**          | Button click                           |
| **Event Source**   | `submitBtn`, `addBtn`, dynamic buttons |
| **Event Listener** | `addEventListener('click', ...)`       |
| **Event Handler**  | Function updates output or shows alert |
| **Response**       | Text displayed or alert shown          |

---


```
```
