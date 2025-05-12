index.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>JavaScript and DOM Manipulation</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <h1>Welcome to JavaScript DOM Manipulation</h1>
  </header>

  <section>
    <p id="intro">This is a simple demonstration of DOM manipulation.</p>

    <button id="changeTextBtn">Change Text</button>
    <button id="changeStyleBtn">Change Style</button>
    <button id="addElementBtn">Add New Element</button>
    <button id="removeElementBtn">Remove Element</button>

    <div id="newElementContainer"></div>
  </section>

  <footer>
    <p>Created as part of an introduction to JavaScript and DOM manipulation.</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>

style.css
body {
  font-family: Arial, sans-serif;
  background-color: #f4f4f4;
  margin: 0;
  padding: 0;
}

header {
  background-color: #333;
  color: white;
  padding: 10px 0;
  text-align: center;
}

section {
  padding: 20px;
}

button {
  margin: 10px;
  padding: 10px;
  background-color: #4CAF50;
  color: white;
  border: none;
  cursor: pointer;
}

button:hover {
  background-color: #45a049;
}

#newElementContainer {
  margin-top: 20px;
}

style.js

// Changing the text content dynamically
document.getElementById('changeTextBtn').addEventListener('click', function() {
  document.getElementById('intro').textContent = "The text has been changed dynamically!";
});

document.getElementById('changeStyleBtn').addEventListener('click', function() {
  document.body.style.backgroundColor = "#e0f7fa"; // Change background color
  document.getElementById('intro').style.color = "#00796b"; // Change text color
});

document.getElementById('addElementBtn').addEventListener('click', function() {
  const newDiv = document.createElement('div');
  newDiv.textContent = "This is a newly added element!";
  newDiv.style.padding = "10px";
  newDiv.style.backgroundColor = "#80deea";
  document.getElementById('newElementContainer').appendChild(newDiv);
});

document.getElementById('removeElementBtn').addEventListener('click', function() {
  const newElement = document.querySelector('#newElementContainer div');
  if (newElement) {
    newElement.remove();
  }
});

