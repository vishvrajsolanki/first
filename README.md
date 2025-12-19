<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modern Responsive Website</title>
    <!-- Google Fonts for modern typography -->
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&family=Roboto:wght@400;500&display=swap" rel="stylesheet">
    <!-- Link to external CSS -->
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Navigation Bar -->
    <nav class="navbar">
        <div class="container">
            <h1 class="logo">MySite</h1>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#features">Features</a></li>
                <li><a href="#gallery">Gallery</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <div class="hamburger" id="hamburger">
                <span></span>
                <span></span>
                <span></span>
            </div>
        </div>
    </nav>

    <!-- Home Section (Hero) -->
    <section id="home" class="hero">
        <div class="container">
            <h2>Welcome to MySite</h2>
            <p>A modern, responsive website built with HTML, CSS, and JavaScript.</p>
            <button class="cta-button" onclick="scrollToSection('about')">Learn More</button>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="section">
        <div class="container">
            <h2>About Us</h2>
            <div class="about-content">
                <img src="https://via.placeholder.com/400x300?text=About+Image" alt="About Image" class="about-image">
                <div class="about-text">
                    <p>We are a team dedicated to creating beautiful, functional websites. Our focus is on clean design, user experience, and modern technology.</p>
                    <p>Update this text easily by editing the HTML here.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Features/Services Section -->
    <section id="features" class="section">
        <div class="container">
            <h2>Features & Services</h2>
            <div class="features-grid">
                <div class="feature-card">
                    <h3>Responsive Design</h3>
                    <p>Looks great on all devices.</p>
                </div>
                <div class="feature-card">
                    <h3>Modern UI</h3>
                    <p>Clean and professional components.</p>
                </div>
                <div class="feature-card">
                    <h3>Interactive Elements</h3>
                    <p>Sliders, modals, and smooth animations.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Gallery/Portfolio Section -->
    <section id="gallery" class="section">
        <div class="container">
            <h2>Gallery & Portfolio</h2>
            <div class="slider">
                <div class="slides" id="slides">
                    <img src="https://via.placeholder.com/600x400?text=Image+1" alt="Gallery Image 1">
                    <img src="https://via.placeholder.com/600x400?text=Image+2" alt="Gallery Image 2">
                    <img src="https://via.placeholder.com/600x400?text=Image+3" alt="Gallery Image 3">
                </div>
                <button class="prev" onclick="changeSlide(-1)">&#10094;</button>
                <button class="next" onclick="changeSlide(1)">&#10095;</button>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section">
        <div class="container">
            <h2>Contact Us</h2>
            <form id="contact-form">
                <input type="text" id="name" placeholder="Your Name" required>
                <input type="email" id="email" placeholder="Your Email" required>
                <textarea id="message" placeholder="Your Message" required></textarea>
                <button type="submit" class="cta-button">Send Message</button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <p>&copy; 2023 MySite. All rights reserved.</p>
        </div>
    </footer>

    <!-- Link to external JS -->
    <script src="script.js"></script>
</body>
</html>