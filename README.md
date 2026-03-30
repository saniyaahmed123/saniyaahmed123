<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Course Portfolio</title>
    <style>
        /* 1. Basic Page Styling */
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f8f9fa;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 50px 20px;
            margin: 0;
        }

        /* 2. Profile GIF Styling */
        .profile-gif {
            border-radius: 20px;
            box-shadow: 0 8px 24px rgba(0,0,0,0.12);
            margin-bottom: 30px;
            max-width: 100%;
        }

        /* 3. "Thanks for visiting" Typewriter Animation */
        .welcome-msg {
            font-size: 28px;
            font-weight: bold;
            color: #2c3e50;
            white-space: nowrap;
            overflow: hidden;
            border-right: 3px solid #2ecc71; /* The blinking cursor */
            width: 0;
            margin-bottom: 40px;
            animation: 
                typing 3s steps(30) forwards, 
                blink 0.8s infinite;
        }

        @keyframes typing {
            from { width: 0; }
            to { width: 400px; } /* Adjust width based on text length */
        }

        @keyframes blink {
            50% { border-color: transparent; }
        }

        /* 4. Table Styling */
        table {
            width: 100%;
            max-width: 900px;
            border-collapse: collapse;
            background: white;
            border-radius: 10px;
            overflow: hidden; /* Rounds the table corners */
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
        }

        th {
            background-color: #2ecc71;
            color: white;
            padding: 15px;
            text-align: left;
            font-size: 14px;
            text-transform: uppercase;
        }

        td {
            padding: 15px;
            border-bottom: 1px solid #edf2f7;
            color: #4a5568;
            font-size: 15px;
        }

        tr:last-child td {
            border-bottom: none;
        }

        tr:hover {
            background-color: #f0fff4;
        }
    </style>
</head>
<body>

    <img src="https://user-images.githubusercontent.com/74038190/215283039-83bf4f37-3fe5-4d25-a42a-249d1a7e9e4f.gif" 
         alt="Coding Animation" 
         width="300" 
         class="profile-gif">

    <div class="welcome-msg">Thanks for visiting my profile!</div>

    <table id="courseTable">
        </table>

    <script>
        // Data Objects (Simple and easy to edit)
        var course1 = {
            title: "Full-Stack Web Development",
            instructor: "Sarah Jenkins",
            duration: "12 Weeks",
            isAdvanced: "Yes 🚀",
            topics: "MongoDB, Express, React, Node.js"
        };

        var course2 = {
            title: "Mobile App Design",
            instructor: "Marcus Thorne",
            duration: "6 Weeks",
            isAdvanced: "No",
            topics: "Figma, User Research, Prototyping"
        };

        var course3 = {
            title: "Python for Data Analysis",
            instructor: "Dr. Aris Thorne",
            duration: "10 Weeks",
            isAdvanced: "Yes 🚀",
            topics: "NumPy, Pandas, Data Visualization"
        };

        // Manual injection using Template Literals
        document.getElementById("courseTable").innerHTML = `
            <tr>
                <th>Course Title</th>
                <th>Instructor</th>
                <th>Duration</th>
                <th>Advanced</th>
                <th>Topics</th>
            </tr>
            <tr>
                <td>${course1.title}</td>
                <td>${course1.instructor}</td>
                <td>${course1.duration}</td>
                <td>${course1.isAdvanced}</td>
                <td>${course1.topics}</td>
            </tr>
            <tr>
                <td>${course2.title}</td>
                <td>${course2.instructor}</td>
                <td>${course2.duration}</td>
                <td>${course2.isAdvanced}</td>
                <td>${course2.topics}</td>
            </tr>
            <tr>
                <td>${course3.title}</td>
                <td>${course3.instructor}</td>
                <td>${course3.duration}</td>
                <td>${course3.isAdvanced}</td>
                <td>${course3.topics}</td>
            </tr>
        `;
    </script>
</body>
</html>
