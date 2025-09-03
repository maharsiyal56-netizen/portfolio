<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tahir Mehdi | Web Developer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #2563eb;
            --secondary: #3b82f6;
            --dark: #1e293b;
            --light: #f8fafc;
            --gray: #64748b;
            --transition: all 0.3s ease;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: var(--dark);
            background-color: var(--light);
            overflow-x: hidden;
        }
        
        a {
            text-decoration: none;
            color: inherit;
        }
        
        ul {
            list-style: none;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .btn {
            display: inline-block;
            padding: 12px 28px;
            background: var(--primary);
            color: white;
            border-radius: 5px;
            font-weight: 500;
            transition: var(--transition);
            border: none;
            cursor: pointer;
        }
        
        .btn:hover {
            background: var(--secondary);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        section {
            padding: 80px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
            position: relative;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            margin-bottom: 15px;
            position: relative;
            display: inline-block;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: var(--primary);
            border-radius: 2px;
        }
        
        /* Header & Navigation */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background: rgba(255, 255, 255, 0.95);
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
            padding: 15px 0;
            transition: var(--transition);
        }
        
        header.sticky {
            padding: 10px 0;
        }
        
        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary);
        }
        
        .logo span {
            color: var(--dark);
        }
        
        .nav-menu {
            display: flex;
        }
        
        .nav-menu li {
            margin: 0 15px;
        }
        
        .nav-menu a {
            font-weight: 500;
            transition: var(--transition);
            position: relative;
        }
        
        .nav-menu a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--primary);
            transition: var(--transition);
        }
        
        .nav-menu a:hover::after {
            width: 100%;
        }
        
        .hamburger {
            display: none;
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            background: linear-gradient(135deg, rgba(37, 99, 235, 0.1) 0%, rgba(59, 130, 246, 0.1) 100%);
            position: relative;
            overflow: hidden;
        }
        
        .hero-content {
            max-width: 600px;
        }
        
        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            line-height: 1.2;
        }
        
        .hero-content p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            color: var(--gray);
        }
        
        .hero-image {
            position: absolute;
            right: 10%;
            bottom: 0;
            width: 40%;
            max-width: 500px;
            animation: float 5s ease-in-out infinite;
        }
        
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
            100% { transform: translateY(0px); }
        }
        
        /* About Section */
        .about-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }
        
        .about-image {
            flex: 1;
            position: relative;
        }
        
        .about-image img {
            width: 100%;
            border-radius: 10px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
        }
        
        .about-image::before {
            content: '';
            position: absolute;
            top: -20px;
            left: -20px;
            width: 100%;
            height: 100%;
            border: 3px solid var(--primary);
            border-radius: 10px;
            z-index: -1;
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-text h3 {
            font-size: 2rem;
            margin-bottom: 20px;
        }
        
        .about-text p {
            margin-bottom: 15px;
            color: var(--gray);
        }
        
        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 20px;
        }
        
        .skill {
            padding: 8px 15px;
            background: rgba(37, 99, 235, 0.1);
            color: var(--primary);
            border-radius: 50px;
            font-size: 0.9rem;
            font-weight: 500;
        }
        
        /* Projects Section */
        .projects {
            background: linear-gradient(135deg, rgba(37, 99, 235, 0.05) 0%, rgba(59, 130, 246, 0.05) 100%);
        }
        
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .project-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            transition: var(--transition);
        }
        
        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.15);
        }
        
        .project-img {
            height: 200px;
            width: 100%;
            background: linear-gradient(45deg, #2563eb, #3b82f6);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 2rem;
        }
        
        .project-info {
            padding: 20px;
        }
        
        .project-info h3 {
            font-size: 1.3rem;
            margin-bottom: 10px;
        }
        
        .project-info p {
            color: var(--gray);
            margin-bottom: 15px;
            font-size: 0.95rem;
        }
        
        .project-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 15px;
        }
        
        .project-tag {
            padding: 4px 10px;
            background: rgba(37, 99, 235, 0.1);
            color: var(--primary);
            border-radius: 50px;
            font-size: 0.8rem;
        }
        
        /* Contact Section */
        .contact-content {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 50px;
        }
        
        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .contact-icon {
            width: 50px;
            height: 50px;
            background: rgba(37, 99, 235, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary);
            font-size: 1.2rem;
        }
        
        .contact-text h4 {
            font-size: 1.1rem;
            margin-bottom: 5px;
        }
        
        .contact-text p {
            color: var(--gray);
        }
        
        .contact-form {
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }
        
        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-family: 'Poppins', sans-serif;
            transition: var(--transition);
        }
        
        .form-control:focus {
            border-color: var(--primary);
            outline: none;
            box-shadow: 0 0 0 3px rgba(37, 99, 235, 0.2);
        }
        
        textarea.form-control {
            min-height: 120px;
            resize: vertical;
        }
        
        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 50px 0 20px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: white;
            margin-bottom: 15px;
            display: inline-block;
        }
        
        .footer-about p {
            color: #cbd5e1;
            margin-bottom: 20px;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
        }
        
        .social-link {
            width: 40px;
            height: 40px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: var(--transition);
        }
        
        .social-link:hover {
            background: var(--primary);
            transform: translateY(-3px);
        }
        
        .footer-links h4 {
            font-size: 1.2rem;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-links h4::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 40px;
            height: 3px;
            background: var(--primary);
        }
        
        .footer-links ul li {
            margin-bottom: 10px;
        }
        
        .footer-links a {
            color: #cbd5e1;
            transition: var(--transition);
        }
        
        .footer-links a:hover {
            color: white;
            padding-left: 5px;
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #94a3b8;
            font-size: 0.9rem;
        }
        
        /* Responsive Design */
        @media (max-width: 992px) {
            .hero-content h1 {
                font-size: 2.8rem;
            }
            
            .about-content {
                flex-direction: column;
            }
            
            .about-image, .about-text {
                flex: none;
                width: 100%;
            }
            
            .about-image::before {
                display: none;
            }
            
            .contact-content {
                grid-template-columns: 1fr;
            }
            
            .footer-content {
                grid-template-columns: repeat(2, 1fr);
            }
        }
        
        @media (max-width: 768px) {
            .nav-menu {
                position: fixed;
                top: 70px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 70px);
                background: white;
                flex-direction: column;
                align-items: center;
                justify-content: center;
                transition: var(--transition);
            }
            
            .nav-menu.active {
                left: 0;
            }
            
            .nav-menu li {
                margin: 15px 0;
            }
            
            .hamburger {
                display: block;
            }
            
            .hero {
                padding-top: 70px;
                text-align: center;
            }
            
            .hero-content {
                margin: 0 auto;
            }
            
            .hero-image {
                display: none;
            }
            
            .footer-content {
                grid-template-columns: 1fr;
            }
        }
        
        @media (max-width: 576px) {
            .section-title h2 {
                font-size: 2rem;
            }
            
            .hero-content h1 {
                font-size: 2.2rem;
            }
            
            .projects-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header id="header">
        <div class="container nav-container">
            <a href="#" class="logo">Tahir<span>Mehdi</span></a>
            <ul class="nav-menu">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <div class="hamburger">
                <i class="fas fa-bars"></i>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>Web Developer & UI/UX Designer</h1>
                <p>I create beautiful, functional websites and applications with a focus on user experience and clean code.</p>
                <a href="#projects" class="btn">View My Work</a>
            </div>
        </div>
        <div class="hero-image">
            <svg viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
                <path fill="#2563eb" d="M45.7,-58.2C59.2,-49.3,70.1,-36.2,75.1,-20.4C80.1,-4.6,79.2,13.9,72.5,29.7C65.8,45.5,53.4,58.6,38.3,65.9C23.2,73.2,5.4,74.7,-9.3,70.8C-24,66.9,-35.5,57.7,-45.2,45.9C-54.9,34.1,-62.7,19.7,-64.9,4.1C-67.1,-11.5,-63.7,-28.3,-55.2,-41.3C-46.7,-54.3,-33.2,-63.6,-18.2,-68.5C-3.2,-73.4,13.2,-73.9,29.1,-68.7C45,-63.5,60.3,-52.5,71.1,-38.3C81.9,-24.1,88.2,-6.7,87.5,10.8C86.8,28.3,79.1,45.9,67,59.1C54.9,72.3,38.4,81.2,21.3,83.9C4.3,86.6,-13.3,83.1,-28.5,75.3C-43.7,67.5,-56.5,55.4,-64.8,40.6C-73.1,25.8,-76.9,8.4,-75.2,-8.7C-73.5,-25.8,-66.4,-42.6,-55.1,-55.1C-43.8,-67.6,-28.3,-75.8,-11.6,-79.3C5.2,-82.8,10.3,-81.6,18.7,-77.8C27.1,-74,38.6,-67.6,45.7,-58.2Z" transform="translate(100 100)" />
            </svg>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <div class="section-title">
                <h2>About Me</h2>
                <p>Get to know me better</p>
            </div>
            <div class="about-content">
                <div class="about-image">
                    <!-- Replace with your actual image -->
                    <img src=""E:\WhatsApp Image 2025-09-03 at 6.04.08 AM.jpeg"" alt="Tahir Mehdi">
                </div>
                <div class="about-text">
                    <h3>Hello! I'm Tahir Mehdi</h3>
                    <p>I'm a passionate web developer with expertise in creating dynamic, user-friendly websites and applications. With a strong foundation in both front-end and back-end technologies, I bring ideas to life with clean, efficient code.</p>
                    <p>My approach combines technical expertise with creative design thinking to deliver solutions that not only look great but also perform exceptionally well across all devices.</p>
                    <div class="skills">
                        <span class="skill">HTML</span>
                        <span class="skill">CSS</span>
                        <span class="skill">JavaScript</span>
                        <span class="skill">React</span>
                        <span class="skill">Node.js</span>
                        <span class="skill">PHP</span>
                        <span class="skill">MySQL</span>
                        <span class="skill">UI/UX Design</span>
                    </div>
                    <a href="#contact" class="btn" style="margin-top: 20px;">Hire Me</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="projects">
        <div class="container">
            <div class="section-title">
                <h2>My Projects</h2>
                <p>Check out some of my recent work</p>
            </div>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-img">
                        <i class="fas fa-shopping-cart"></i>
                    </div>
                    <div class="project-info">
                        <h3>E-Commerce Website</h3>
                        <p>A fully functional e-commerce website with product filtering, cart functionality, and secure checkout.</p>
                        <div class="project-tags">
                            <span class="project-tag">HTML</span>
                            <span class="project-tag">CSS</span>
                            <span class="project-tag">JavaScript</span>
                            <span class="project-tag">PHP</span>
                        </div>
                        <a href="#" class="btn">View Project</a>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-img">
                        <i class="fas fa-tasks"></i>
                    </div>
                    <div class="project-info">
                        <h3>Task Management App</h3>
                        <p>A responsive task management application that allows users to create, organize, and track their tasks.</p>
                        <div class="project-tags">
                            <span class="project-tag">React</span>
                            <span class="project-tag">Node.js</span>
                            <span class="project-tag">MongoDB</span>
                        </div>
                        <a href="#" class="btn">View Project</a>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-img">
                        <i class="fas fa-utensils"></i>
                    </div>
                    <div class="project-info">
                        <h3>Restaurant Website</h3>
                        <p>An elegant website for a restaurant with menu display, reservation system, and online ordering.</p>
                        <div class="project-tags">
                            <span class="project-tag">HTML</span>
                            <span class="project-tag">CSS</span>
                            <span class="project-tag">JavaScript</span>
                            <span class="project-tag">MySQL</span>
                        </div>
                        <a href="#" class="btn">View Project</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <div class="section-title">
                <h2>Contact Me</h2>
                <p>Get in touch with me</p>
            </div>
            <div class="contact-content">
                <div class="contact-info">
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div class="contact-text">
                            <h4>Location</h4>
                            <p>Lahore, Pakistan</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div class="contact-text">
                            <h4>Email</h4>
                            <p>tahir.mehdi@example.com</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-phone"></i>
                        </div>
                        <div class="contact-text">
                            <h4>Phone</h4>
                            <p>+92 300 1234567</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-globe"></i>
                        </div>
                        <div class="contact-text">
                            <h4>Website</h4>
                            <p>www.tahirmehdi.com</p>
                        </div>
                    </div>
                </div>
                <div class="contact-form">
                    <form>
                        <div class="form-group">
                            <label for="name">Your Name</label>
                            <input type="text" id="name" class="form-control" placeholder="Enter your name">
                        </div>
                        <div class="form-group">
                            <label for="email">Your Email</label>
                            <input type="email" id="email" class="form-control" placeholder="Enter your email">
                        </div>
                        <div class="form-group">
                            <label for="subject">Subject</label>
                            <input type="text" id="subject" class="form-control" placeholder="Enter subject">
                        </div>
                        <div class="form-group">
                            <label for="message">Message</label>
                            <textarea id="message" class="form-control" placeholder="Enter your message"></textarea>
                        </div>
                        <button type="submit" class="btn">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-about">
                    <a href="#" class="footer-logo">Tahir<span>Mehdi</span></a>
                    <p>I create beautiful, functional websites and applications with a focus on user experience and clean code.</p>
                    <div class="social-links">
                        <a href="#" class="[social-link](https://www.facebook.com/tahir.siyal.988)"><i class="fab fa-facebook-f"></i></a>
                        <a href="#" class="[social-link](https://x.com/tahirmehdi786)"><i class="fab fa-twitter"></i></a>
                        <a href="#" class="[social-link](https://www.instagram.com/siyal6437/)"><i class="fab fa-instagram"></i></a>
                        <a href="#" class="[social-link](https://www.linkedin.com/in/tahir-mehdi-63b651322/)"><i class="fab fa-linkedin-in"></i></a>
                        <a href="#" class="[social-link](https://github.com/maharsiyal56-netizen)"><i class="fab fa-github"></i></a>
                    </div>
                </div>
                <div class="footer-links">
                    <h4>Quick Links</h4>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#about">About</a></li>
                        <li><a href="#projects">Projects</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
                <div class="footer-links">
                    <h4>Services</h4>
                    <ul>
                        <li><a href="#">Web Development</a></li>
                        <li><a href="#">UI/UX Design</a></li>
                        <li><a href="#">Frontend Development</a></li>
                        <li><a href="#">Backend Development</a></li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 Tahir Mehdi. All Rights Reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Sticky Header
        window.addEventListener('scroll', function() {
            const header = document.getElementById('header');
            if (window.scrollY > 50) {
                header.classList.add('sticky');
            } else {
                header.classList.remove('sticky');
            }
        });
        
        // Mobile Menu Toggle
        const hamburger = document.querySelector('.hamburger');
        const navMenu = document.querySelector('.nav-menu');
        
        hamburger.addEventListener('click', function() {
            navMenu.classList.toggle('active');
        });
        
        // Smooth Scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 70,
                        behavior: 'smooth'
                    });
                    
                    // Close mobile menu if open
                    if (navMenu.classList.contains('active')) {
                        navMenu.classList.remove('active');
                    }
                }
            });
        });
        
        // Animation on Scroll
        function animateOnScroll() {
            const elements = document.querySelectorAll('.project-card, .about-image, .about-text');
            
            elements.forEach(element => {
                const position = element.getBoundingClientRect();
                
                // If element is in viewport
                if (position.top < window.innerHeight - 100) {
                    element.style.opacity = 1;
                    element.style.transform = 'translateY(0)';
                }
            });
        }
        
        // Initialize elements for animation
        document.querySelectorAll('.project-card, .about-image, .about-text').forEach(element => {
            element.style.opacity = 0;
            element.style.transform = 'translateY(50px)';
            element.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
        });
        
        window.addEventListener('scroll', animateOnScroll);
        window.addEventListener('load', animateOnScroll);
    </script>
</body>
</html>
