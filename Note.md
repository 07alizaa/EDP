````markdown
# Understanding: index.html, style.css, and script-step2.js


---

### What the HTML Does
```html
<input id="inputField" placeholder="Type something">
<button id="submitBtn">Submit</button>
<p id="output"></p>
````

* **inputField** → where the user types text
* **submitBtn** → triggers the event when clicked
* **output** → shows the submitted text

The page waits for user action — that’s event-driven behavior.

---

### What the JavaScript Does

```javascript
document.getElementById('submitBtn').addEventListener('click', function() {
    let input = document.getElementById('inputField').value;
    document.getElementById('output').innerText = "You entered: " + input;
});
```

* Waits for the **click** event on the Submit button.
* When clicked → reads the input text and displays:
  `You entered: HelloWorld` (or whatever the user typed).

---

### In Simple Words

Nothing happens until you click the button.
Clicking Submit → shows what you typed in the output paragraph.

---

### Summary Table

| Concept            | Example / Action                 |
| ------------------ | -------------------------------- |
| **Event**          | Button click                     |
| **Event Source**   | `submitBtn`                      |
| **Event Listener** | `addEventListener('click', ...)` |
| **Event Handler**  | Function updates the output text |
| **Response**       | Text displayed on the page       |

---




