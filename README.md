# Ex03 To-Do List using JavaScript
## Date: 3/10/2025

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM
index.html

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>To-Do App</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <div class="todo-app">
    <h1>My To-Do List</h1>
    <div class="input-section">
      <input width="70%" type="text" id="task-input" placeholder="Add a new task..." />
      <button id="add-task">Add</button>
    </div>
    <ul id="task-list"></ul>
  </div>

  <script src="script.js"></script>
</body>
</html>
```
styles.css

```
body {
  font-family: Arial, sans-serif;
  background: #f4f4f4;
  display: flex;
  justify-content: center;
  padding: 50px;
}

.todo-app {
  background: white;
  padding: 20px 30px;
  border-radius: 8px;
  box-shadow: 0 4px 10px rgba(0,0,0,0.1);
  width: 300px;
}

h1 {
  text-align: center;
}

.input-section {
  display: flex;
  gap: 10px;
  margin-bottom: 20px;
}

#task-input {
  flex: 1;
  padding: 10px;
}

#add-task {
  padding: 10px;
}

#task-list {
  list-style-type: none;
  padding: 0;
}

.task-item {
  background: #eaeaea;
  padding: 10px;
  margin-bottom: 10px;
  border-radius: 4px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

```
script.js

```
document.getElementById('add-task').addEventListener('click', addTask);

function addTask() {
  const input = document.getElementById('task-input');
  const taskText = input.value.trim();

  if (taskText === '') return;

  const li = document.createElement('li');
  li.className = 'task-item';
  li.innerHTML = `
    <span>${taskText}</span>
    <button class="delete-btn">X</button>
  `;

  document.getElementById('task-list').appendChild(li);
  input.value = '';

  li.querySelector('.delete-btn').addEventListener('click', () => {
    li.remove();
  });
}
```

## OUTPUT
<img width="1439" height="834" alt="image" src="https://github.com/user-attachments/assets/57f613f3-9830-4c1b-8ee9-8d7a1531a586" />


## RESULT
The program for creating To-do list using JavaScript is executed successfully.
