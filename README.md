index.html
 <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Interactive Webpage</title>
  <style>
    .dynamic-text {
      font-size: 20px;
      color: blue;
    }
    .new-element {
      color: green;
      margin-top: 10px;
    }
  </style>
</head>
<body>
  <h1>Interactive Webpage</h1>

  <!-- Button to change text -->
  <button id="changeTextBtn">Change Text</button>

  <!-- Button to toggle background color -->
  <button id="toggleColorBtn">Toggle Background Color</button>

  <!-- Button to add a new element -->
  <button id="addElementBtn">Add New Element</button>

  <!-- Paragraph to change text content -->
  <p id="dynamicText" class="dynamic-text">This is a dynamic text.</p>

  <!-- Container to hold new elements -->
  <div id="elementContainer"></div>

  <script src="script.js"></script>
</body>
</html>

script.js

document.getElementById('changeTextBtn').addEventListener('click', function() {
  const dynamicText = document.getElementById('dynamicText');
  dynamicText.textContent = 'The text has been changed!';
});

document.getElementById('toggleColorBtn').addEventListener('click', function() {
  const body = document.body;
  body.style.backgroundColor = body.style.backgroundColor === 'lightblue' ? 'white' : 'lightblue';
});

document.getElementById('addElementBtn').addEventListener('click', function() {
  const elementContainer = document.getElementById('elementContainer');
  const newElement = document.createElement('p');
  newElement.classList.add('new-element');
  newElement.textContent = 'This is a newly added element!';
  elementContainer.appendChild(newElement);
});
