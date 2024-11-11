<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Welcome to My Profile</title>
    <style>
        /* Basic reset */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        /* Body styling */
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            color: #333;
            line-height: 1.6;
            text-align: center;
            padding-top: 50px;
        }

        /* Header section */
        header {
            background-color: #4CAF50;
            color: white;
            padding: 20px 0;
        }

        header h1 {
            font-size: 3em;
        }

        /* Profile card styling */
        .profile-card {
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            max-width: 400px;
            margin: 20px auto;
            padding: 30px;
            text-align: center;
        }

        .profile-card img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 5px solid #4CAF50;
            margin-bottom: 20px;
        }

        .profile-card h2 {
            font-size: 2em;
            margin-bottom: 10px;
        }

        .profile-card p {
            font-size: 1.2em;
            color: #777;
        }

        /* Buttons */
        .btn {
            background-color: #4CAF50;
            color: white;
            border: none;
            padding: 10px 20px;
            font-size: 1.2em;
            border-radius: 5px;
            cursor: pointer;
            text-decoration: none;
            display: inline-block;
            margin-top: 20px;
        }

        .btn:hover {
            background-color: #45a049;
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <h1>Welcome to My Profile</h1>
    </header>

    <!-- Profile Card -->
    <div class="profile-card">
        <img src="https://via.placeholder.com/150" alt="Profile Picture">
        <h2>John Doe</h2>
        <p>Web Developer | Tech Enthusiast | Lifelong Learner</p>
        <a href="#" class="btn">Contact Me</a>
    </div>

    <!-- Footer -->
    <footer>
        <p>&copy; 2024 John Doe. All Rights Reserved.</p>
    </footer>

</body>
</html>
