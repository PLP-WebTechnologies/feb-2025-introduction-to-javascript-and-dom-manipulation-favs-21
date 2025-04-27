# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.


<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Interactive Page</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      padding: 50px;
    }
    #dynamicText {
      font-size: 24px;
      color: darkblue;
      margin: 20px;
    }
    #specialElement {
      margin-top: 20px;
      color: green;
    }
    button {
      margin: 10px;
      padding: 10px 20px;
      font-size: 16px;
    }
  </style>
</head>
<body>

  <h1>My Webpage</h1>
  <div id="dynamicText">Click the buttons below!</div>

  <button onclick="changeText()">Change Text</button>
  <button onclick="changeStyle()">Change Style</button>
  <button onclick="toggleElement()">Add/Remove Element</button>

  <div id="container"></div>

  <script>
    function changeText() {
      document.getElementById('dynamicText').textContent = "You changed the text!";
    }

    function changeStyle() {
      let text = document.getElementById('dynamicText');
      text.style.color = "crimson";
      text.style.fontSize = "30px";
      text.style.fontWeight = "bold";
    }

    function toggleElement() {
      const container = document.getElementById('container');
      const existing = document.getElementById('specialElement');

      if (existing) {
        container.removeChild(existing);
      } else {
        const newElement = document.createElement('div');
        newElement.id = "specialElement";
        newElement.textContent = "Hello! I was added dynamically.";
        container.appendChild(newElement);
      }
    }
  </script>

</body>
</html>


Happy Coding! 💻✨
