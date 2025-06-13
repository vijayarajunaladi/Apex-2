<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Intermediate Web Project</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    header, footer {
      background: #333;
      color: white;
      padding: 1em;
      text-align: center;
    }

    nav {
      display: flex;
      justify-content: space-around;
      background-color: #444;
      padding: 0.5em;
    }

    nav a {
      color: white;
      text-decoration: none;
    }

    .container {
      display: grid;
      grid-template-columns: 1fr 2fr;
      gap: 20px;
      padding: 20px;
    }

    form {
      display: flex;
      flex-direction: column;
      gap: 10px;
    }

    input, button {
      padding: 10px;
      font-size: 1em;
    }

    .todo-section {
      margin-top: 20px;
    }

    ul {
      list-style: none;
      padding: 0;
    }

    ul li {
      background: #eee;
      margin: 5px 0;
      padding: 10px;
      display: flex;
      justify-content: space-between;
    }

    @media (max-width: 768px) {
      .container {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>Intermediate HTML, CSS & JS</h1>
  </header>

  <nav>
    <a href="#">Home</a>
    <a href="#">Form</a>
    <a href="#">To-Do</a>
  </nav>

  <div class="container">
    <!-- Contact Form -->
    <div>
      <h2>Contact Form</h2>
      <form id="contactForm">
        <input type="text" id="name" placeholder="Your Name" required />
        <input type="email" id="email" placeholder="Your Email" required />
        <button type="submit">Submit</button>
      </form>
    </div>

    <!-- To-Do List -->
    <div class="todo-section">
      <h2>To-Do List</h2>
      <input type="text" id="todoInput" placeholder="Add a new task" />
      <button onclick="addTodo()">Add Task</button>
      <ul id="todoList"></ul>
    </div>
  </div>

  <footer>
    <p>&copy; 2025 Intermediate Web Project</p>
  </footer>

  <script>
    // Form validation
    document.getElementById('contactForm').addEventListener('submit', function(e) {
      const name = document.getElementById('name').value.trim();
      const email = document.getElementById('email').value.trim();
      const emailRegex = /^[^@\s]+@[^@\s]+\.[^@\s]+$/;

      if (!name || !email) {
        alert("All fields are required.");
        e.preventDefault();
      } else if (!emailRegex.test(email)) {
        alert("Please enter a valid email address.");
        e.preventDefault();
      }
    });

    // To-do list logic
    function addTodo() {
      const input = document.getElementById('todoInput');
      const task = input.value.trim();
      if (task === '') return;

      const li = document.createElement('li');
      li.innerHTML = `${task} <button onclick="this.parentElement.remove()">Delete</button>`;
      document.getElementById('todoList').appendChild(li);
      input.value = '';
    }
  </script>
</body>
</html>
