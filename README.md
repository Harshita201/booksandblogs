<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Harshita Jaswani | Love Locked in Time and Death</title>
    <link rel="stylesheet" href="styles.css">
    <style>
        /* General Styles */
        body {
            font-family: 'Garamond', serif;
            margin: 0;
            padding: 0;
            background-color: #0A192F; /* Navy Teal Dark Blue */
            color: #ffffff; /* White Text */
            overflow-x: hidden;
        }

        header {
            background-color: #112240; /* Darker Navy Blue */
            padding: 20px;
            text-align: center;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }

        nav ul {
            list-style: none;
            padding: 0;
            margin: 0;
        }

        nav ul li {
            display: inline;
            margin: 0 15px;
        }

        nav ul li a {
            color: #64ffda; /* Teal Accent */
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s ease;
        }

        nav ul li a:hover {
            color: #ffffff; /* White Text on Hover */
        }

        section {
            padding: 50px;
            text-align: center;
        }

        #book {
            overflow-y: auto;
            max-height: 80vh;
            padding: 20px;
            text-align: center;
            background-color: #112240;
            border-radius: 10px;
            margin: 20px;
        }

        #book a {
            display: inline-block;
            margin-top: 10px;
            padding: 10px 20px;
            background-color: #64ffda; /* Teal Accent */
            color: #0A192F; /* Dark Background */
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            transition: background-color 0.3s ease;
        }

        #book a:hover {
            background-color: #52e0c4; /* Lighter Teal on Hover */
        }

        #book img {
            max-width: 300px;
            border-radius: 10px;
            margin: 20px 0;
            transition: transform 0.3s ease;
        }

        #book img:hover {
            transform: scale(1.05); /* Slightly enlarge the image on hover */
        }

        /* Falling Hearts Animation */
        @keyframes fall {
            0% { transform: translateY(-10px) scale(0.9); opacity: 1; }
            100% { transform: translateY(100vh) scale(1.1); opacity: 0; }
        }

        .heart {
            position: absolute;
            top: -10px;
            color: white;
            font-size: 20px;
            animation: fall linear infinite;
        }

        /* Back to Top Button */
        #back-to-top {
            position: fixed;
            bottom: 40px;
            right: 40px;
            background-color: #64ffda; /* Teal Accent */
            color: #0A192F; /* Dark Background */
            padding: 10px 15px;
            border-radius: 5px;
            text-align: center;
            cursor: pointer;
            transition: background-color 0.3s ease;
            display: none; /* Hidden by default */
        }

        #back-to-top:hover {
            background-color: #52e0c4; /* Lighter Teal on Hover */
        }

        /* Smooth Scrolling */
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body>
    <header>
        <h1>Harshita Jaswani</h1>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#book">Book</a></li>
                <li><a href="#blog">Blog</a></li>
                <li><a href="#admin">Admin</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <script>
        function createHearts() {
            const heart = document.createElement("div");
            heart.classList.add("heart");
            heart.innerHTML = "🤍"; /* White Heart */
            heart.style.left = Math.random() * window.innerWidth + "px";
            heart.style.animationDuration = Math.random() * 3 + 2 + "s";
            document.body.appendChild(heart);
            setTimeout(() => heart.remove(), 5000);
        }
        setInterval(createHearts, 300);

        // Back to Top Button
        const backToTopButton = document.createElement("div");
        backToTopButton.id = "back-to-top";
        backToTopButton.innerHTML = "↑";
        document.body.appendChild(backToTopButton);

        window.addEventListener("scroll", () => {
            if (window.scrollY > 300) {
                backToTopButton.style.display = "block";
            } else {
                backToTopButton.style.display = "none";
            }
        });

        backToTopButton.addEventListener("click", () => {
            window.scrollTo({ top: 0, behavior: "smooth" });
        });
    </script>

    <section id="home">
        <h2>Welcome to the World of Love Locked in Time and Death</h2>
        <p>Discover the journey of love, time, and destiny in Harshita Jaswani's latest book.</p>
    </section>
    
    <section id="about">
        <h2>About the Author</h2>
        <p>Harshita Jaswani is a passionate writer bringing you heartfelt stories.</p>
    </section>
    
    <section id="book">
        <h2>Love Locked in Time and Death</h2>
        <p>What if you knew the reason behind your own death but couldn’t stop it?</p>
        <img src="https://m.media-amazon.com/images/I/81jdTLLN71L._SY466_.jpg" alt="Love Locked in Time and Death Book Cover">
        <p>
            <strong>Love Locked in Time and Death</strong> is an enthralling tale of Jia, a time traveller caught in the unrelenting grip of love, time, and fate. With every twist, she learns the impossible truths: you cannot alter time, escape death, or let go of true love. Her journey is a haunting dance between the past and future, filled with heartbreak, mystery, and the desperate hope to rewrite destiny.
        </p>
        <br>
        <a href="https://www.amazon.in/LOCKED-LOVE-Unreal-story-ebook/dp/B08HNBW9F3/ref=tmm_kin_swatch_0" target="_blank">Get the eBook</a>
    </section>
    
    <footer>
        <p>&copy; 2025 Harshita Jaswani. All rights reserved.</p>
    </footer>
</body>
</html>
