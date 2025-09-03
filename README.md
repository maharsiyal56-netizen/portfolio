<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tahir Mehdi Portfolio</title>
    <link rel="stylesheet" href="style.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet">
</head>
<body>
    <!-- Landing Page -->
    <header class="landing">
        <nav>
            <div class="logo">Tahir Mehdi</div>
            <ul class="nav-links">
                <li><a href="#about">About</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
        <div class="intro">
            <h1>Hello, I'm <span>Tahir Mehdi</span></h1>
            <p>Aspiring Web Developer & Designer</p>
            <a href="#projects" class="btn">View My Work</a>
        </div>
    </header>

    <!-- About Section -->
    <section id="about">
        <h2>About Me</h2>
        <p>Hello! I'm Tahir Mehdi, a passionate web developer focused on creating clean and modern websites. I enjoy solving problems and learning new technologies to deliver top-notch projects.</p>
    </section>

    <!-- Projects Section -->
    <section id="projects">
        <h2>My Projects</h2>
        <div class="project-container">
            <div class="project-card">
                <h3>Project 1</h3>
                <p>Short description of your project.</p>
                <a href="#" class="btn">View</a>
            </div>
            <div class="project-card">
                <h3>Project 2</h3>
                <p>Short description of your project.</p>
                <a href="#" class="btn">View</a>
            </div>
            <div class="project-card">
                <h3>Project 3</h3>
                <p>Short description of your project.</p>
                <a href="#" class="btn">View</a>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <h2>Contact Me</h2>
        <form>
            <input type="text" placeholder="Your Name" required>
            <input type="email" placeholder="Your Email" required>
            <textarea placeholder="Your Message" required></textarea>
            <button type="submit">Send Message</button>
        </form>
    </section>

    <footer>
        <p>&copy; 2025 Tahir Mehdi. All Rights Reserved.</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
