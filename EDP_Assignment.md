# 🎯 Event-Driven Programming (EDP) Lab Report

**Files:**  
- `index.html`  
- `style.css`  
- `script-step2.js` → `script-step5.js`  

---

## Step 2 – Basic Event Handling

### What is Event-Driven Programming (EDP)?
Event-Driven Programming is a programming approach where the flow of the program is determined by events such as user actions (clicks, inputs), sensor outputs, or messages from other programs. The program waits for an event and executes specific code (event handler) in response.

### What HTML elements are used in this step?  
| Element | Purpose |
|----------|----------|
| `<input>` | Allows the user to type some text. |
| `<button>` | Used to trigger the event when clicked. |
| `<p>` | Displays the output message after the button is clicked. |

### What event does the JavaScript wait for?  
It waits for the **`click`** event on the **Submit** button.

### What happens when the user clicks the button?  
The program takes the text entered in the input field and displays it inside the paragraph as:  
> “You entered: [input text]”

### In simple words, how does this example show event-driven behavior?  
The webpage stays idle until the user clicks the button — that action (event) drives the program’s response.

### Concept Table
| Concept | Example | Description |
|----------|----------|-------------|
| **Event** | `click` | Triggered when the button is clicked |
| **Event Source** | `#submitBtn` | The button that generates the event |
| **Event Listener** | `addEventListener('click', ...)` | Listens for the click event |
| **Event Handler** | Anonymous function inside `addEventListener` | Code executed when the event occurs |
| **Response** | Displays text “You entered: ...” in the output paragraph |

---

## Step 3 – Dynamic Buttons & Event Delegation

### What new feature was added in this step?  
The ability to **dynamically create new buttons** and use **event delegation** to handle their clicks.

### What is the purpose of the Add New Button?  
It allows users to create additional buttons on the page dynamically.

### What is event delegation?  
Event delegation is a technique where a single event listener is added to a parent element to handle events from its child elements — even if those children are added later.

### How does the code detect which button was clicked?  
By checking the **`event.target`** property to see which specific button triggered the event.

### Why do we need only one event listener for multiple buttons?  
Because event delegation allows the parent (`#buttonContainer`) to handle click events for all its child buttons efficiently.

### Concept Table
| Concept | Example | Description |
|----------|----------|-------------|
| **Event** | `click` | When any button (existing or new) is clicked |
| **Event Source** | `#buttonContainer` | The container holding all buttons |
| **Event Listener** | `addEventListener('click', ...)` on container | Listens for any button click |
| **Event Handler** | Checks `e.target.tagName` | Detects and alerts which button was clicked |
| **Response** | Shows alert message like “You clicked New Button” |

---

## Step 4 – Input Validation

### What new concept was introduced in this step?  
**Input validation** — checking whether the input is empty before processing it.

### What happens when the input field is empty?  
The program displays an error message:  
> “Error: Input cannot be empty!”

### What happens when a valid input is given?  
It displays:  
> “You entered: [input text]”

### Why is input validation important in user interaction?  
It prevents invalid or missing data from being processed, improving the reliability and usability of applications.

### Concept Table
| Concept | Example | Event | Condition | Response (if true) | Response (if false) | Behavior |
|----------|----------|--------|------------|--------------------|---------------------|-----------|
| **Input Validation** | Checking input value | `click` on Submit | `input === ""` | Show error message | Display user input | Ensures only valid input is processed |

---

## Step 5 – Observer Pattern with Events

### What new concept is demonstrated in this step?  
The **Observer Pattern**, integrated with event-driven logic.

### What are observers in this example?  
The **buttons** (`Observer 1`, `Observer 2`) that automatically update when the input changes.

### What event triggers the update of all observers?  
The **`input`** event on the text field.

### How does each observer react when the input changes?  
Each observer updates its text to show:  
> “Updated with: [new input value]”

### How is the Observer Pattern connected to Event-Driven Programming?  
The observer pattern uses events to notify multiple components about a change — aligning perfectly with event-driven principles.

### Concept Table
| Concept | Example | Event | Event Source | Observers | Event Listener | Response |
|----------|----------|--------|---------------|------------|----------------|-----------|
| **Observer Pattern** | Updating buttons when input changes | `input` | `#inputField` | `Observer 1`, `Observer 2` | `addEventListener('input', ...)` | All observers update with new value |

---

## Final Reflection

### Define Event-Driven Programming in your own words  
Event-Driven Programming is when a program reacts to different actions or events like clicks, typing, or moving the mouse. Instead of running the code from top to bottom, it waits for something to happen and then performs a specific task. It’s basically how websites and apps respond to what users do.

### How do event handlers make web pages interactive?  
Event handlers let the page react when a user does something. For example, clicking a button can show a message or update something. This makes the webpage more active and user-friendly.

### Compare Step 2 and Step 5 — what major differences do you notice?  
- **Step 2** handles a **single static event** (button click).  
- **Step 5** uses **multiple observers** reacting to a single event, showing a more advanced and dynamic event-driven system.

### Give one real-life example of event-driven behavior in a website or app  
A common example is typing in a search box — as you type, the website shows search suggestions or updates the results instantly. That’s an input event triggering a live response

### How can you improve or extend this project further?  
I could make the project better by adding more visual effects like color changes or animations when events happen. Another idea is to add notifications for each event, or show an event log on the screen to track what actions were performed.

---

