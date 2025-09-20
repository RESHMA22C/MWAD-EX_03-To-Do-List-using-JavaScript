# MWAD-EX_03-To-Do-List-using-JavaScript
## Date:

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
# HTML 
~~~
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>To-Do List</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="todo-container">
    <h2>My To-Do List</h2>
    <input type="text" id="taskInput" placeholder="Enter a task">
    <button id="addBtn">Add</button>
    <ul id="taskList"></ul>
  </div>
  <script src="script.js"></script>
</body>
</html>
~~~

# CSS 
~~~
body {
  font-family: Arial, sans-serif;
  background: linear-gradient(135deg, #667eea, #764ba2); /* gradient background */
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.todo-container {
  background: #ffffff;
  padding: 25px;
  border-radius: 20px;
  box-shadow: 0 6px 15px rgba(0,0,0,0.2);
  width: 380px;
  text-align: center;
}

h2 {
  margin-bottom: 15px;
  color: #4a4a4a;
  font-size: 24px;
}

input {
  padding: 12px;
  width: 65%;
  border: 2px solid #764ba2;
  border-radius: 10px;
  outline: none;
  transition: 0.3s;
}

input:focus {
  border-color: #667eea;
  box-shadow: 0 0 5px rgba(102,126,234,0.6);
}

button {
  padding: 12px 18px;
  margin-left: 5px;
  border: none;
  background: #667eea;
  color: white;
  border-radius: 10px;
  cursor: pointer;
  font-weight: bold;
  transition: 0.3s;
}

button:hover {
  background: #5a67d8;
}

ul {
  list-style-type: none;
  padding: 0;
  margin-top: 20px;
  max-height: 250px;
  overflow-y: auto;
}

li {
  padding: 12px;
  background: #f1f3f8;
  margin-bottom: 10px;
  border-radius: 10px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 16px;
  transition: background 0.3s;
}

li:hover {
  background: #e2e6f3;
}

li.completed {
  text-decoration: line-through;
  color: #9b9b9b;
  background: #e0d7f5;
}

.delete-btn {
  background: #ff4d4d;
  border: none;
  color: white;
  padding: 6px 12px;
  border-radius: 8px;
  cursor: pointer;
  font-size: 14px;
  font-weight: bold;
  transition: 0.3s;
}

.delete-btn:hover {
  background: #cc0000;
}
~~~
# JS 
~~~
document.getElementById("addBtn").addEventListener("click", addTask);

function addTask() {
  let input = document.getElementById("taskInput");
  let taskText = input.value.trim();

  if (taskText === "") {
    alert("Please enter a task!");
    return;
  }

  let li = document.createElement("li");
  li.textContent = taskText;

  // Toggle completed on click
  li.addEventListener("click", function () {
    li.classList.toggle("completed");
  });

  // Delete button
  let delBtn = document.createElement("button");
  delBtn.textContent = "X";
  delBtn.className = "delete-btn";
  delBtn.onclick = function () {
    li.remove();
  };

  li.appendChild(delBtn);
  document.getElementById("taskList").appendChild(li);

  input.value = "";
}

~~~
## OUTPUT

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c65d4894-e062-468a-a0b2-fefd619a0fd7" />


## RESULT
The program for creating To-do list using JavaScript is executed successfully .
