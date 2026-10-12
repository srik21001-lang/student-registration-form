# student-registration-form
Student Registration Form using HTML, CSS and JavaScript with DOM manipulation.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Student Registration Form</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: #eef2ff;
            padding: 30px;
        }
        .container {
            max-width: 400px;
            margin: auto;
            background: white;
            padding: 25px;
            border-radius: 12px;
        }
        input, select, button {
            width: 100%;
            padding: 10px;
            margin: 8px 0;
            box-sizing: border-box;
        }
        button {
            background: #4f46e5;
            color: white;
            border: none;
            border-radius: 6px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Student Registration Form</h2>
        <form id="studentForm">
            <input type="text" id="name" placeholder="Full Name" required>
            <input type="email" id="email" placeholder="Email Address" required>
            <input type="text" id="department" placeholder="Department" required>
            <select id="year" required>
                <option value="">Select Year</option>
                <option>1st Year</option>
                <option>2nd Year</option>
                <option>3rd Year</option>
                <option>4th Year</option>
            </select>
            <button type="submit">Register</button>
        </form>
        <p id="message"></p>
    </div>
    <script>
        document.getElementById("studentForm").addEventListener("submit", function(event) {
            event.preventDefault();
            const name = document.getElementById("name").value;
            document.getElementById("message").textContent =
                "Registration successful! Welcome, " + name + "!";
        });
    </script>
</body>
</html>
