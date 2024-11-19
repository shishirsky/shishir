task1
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Navigation Menu</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            height: 2000px; /* For demonstration purposes */
        }

        /* Navigation menu styles */
        .navbar {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background-color: #333;
            color: blue;
            display: flex;
            justify-content: space-around;
            align-items: center;
            padding: 15px 0;
            transition: background-color 0.3s, color 0.3s;
            z-index: 1000;
        }

        .navbar.scrolled {
            background-color: #555; /* Darker background when scrolled */
        }

        .navbar a {
            color: green;
            text-decoration: none;
            padding: 10px 15px;
            transition: color 0.3s;
        }

        .navbar a:hover {
            color: #ffcc00; /* Change color on hover */
        }
    </style>
</head>
<body>

    <div class="navbar" id="navbar">
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#services">Services</a>
        <a href="#contact">Contact</a>
    </div>

    <script>
        // Get the navbar element
        const navbar = document.getElementById('navbar');

        // Change navbar style on scroll
        window.addEventListener('scroll', () => {
            if (window.scrollY > 50) {
                navbar.classList.add('scrolled');
            } else {
                navbar.classList.remove('scrolled');
            }
        });
    </script>

</body>
</html>
