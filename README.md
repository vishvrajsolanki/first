<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday Mahi</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600&display=swap" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #f8bbd9 0%, #e1bee7 100%);
            color: #4a148c;
            overflow-x: hidden;
            position: relative;
        }

        /* Floating balloons */
        .balloon {
            position: absolute;
            width: 50px;
            height: 70px;
            background: radial-gradient(circle at 30% 30%, #ffeb3b, #ffc107);
            border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
            animation: float 6s ease-in-out infinite;
            opacity: 0.7;
        }

        .balloon:nth-child(1) { left: 10%; animation-delay: 0s; }
        .balloon:nth-child(2) { left: 20%; animation-delay: 1s; }
        .balloon:nth-child(3) { left: 30%; animation-delay: 2s; }
        .balloon:nth-child(4) { left: 40%; animation-delay: 3s; }
        .balloon:nth-child(5) { left: 50%; animation-delay: 4s; }
        .balloon:nth-child(6) { left: 60%; animation-delay: 5s; }
        .balloon:nth-child(7) { left: 70%; animation-delay: 6s; }
        .balloon:nth-child(8) { left: 80%; animation-delay: 7s; }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }

        section {
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 20px;
            opacity: 0;
            transform: translateY(50px);
            transition: opacity 1s ease, transform 1s ease;
        }

        section.visible {
            opacity: 1;
            transform: translateY(0);
        }

        .hero {
            background: url('https://images.unsplash.com/photo-1529634897190-4b8a5b2b3b0f') no-repeat center center/cover;
            color: white;
            text-align: center;
            position: relative;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(74, 20, 140, 0.5);
            z-index: 1;
        }

        .hero h1 {
            font-family: 'Playfair Display', serif;
            font-size: 3rem;
            font-weight: 600;
            position: relative;
            z-index: 2;
            animation: glow 2s ease-in-out infinite alternate;
        }

        @keyframes glow {
            from { text-shadow: 0 0 10px #ffd700; }
            to { text-shadow: 0 0 20px #ffd700, 0 0 30px #ffd700; }
        }

        .friendship {
            background: linear-gradient(135deg, #e1bee7 0%, #f8bbd9 100%);
            text-align: center;
        }

        .friendship h2 {
            font-family: 'Playfair Display', serif;
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: #4a148c;
        }

        .friendship p {
            font-size: 1.2rem;
            max-width: 600px;
            line-height: 1.6;
        }

        .wishes {
            background: url('https://images.unsplash.com/photo-1513151233558-d860c5398176') no-repeat center center/cover;
            text-align: center;
            position: relative;
        }

        .wishes::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(248, 187, 217, 0.8);
            z-index: 1;
        }

        .wishes h2 {
            font-family: 'Playfair Display', serif;
            font-size: 2.5rem;
            margin-bottom: 40px;
            position: relative;
            z-index: 2;
            color: #4a148c;
        }

        .wish-cards {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            position: relative;
            z-index: 2;
        }

        .wish-card {
            background: rgba(255, 255, 255, 0.9);
            border-radius: 10px;
            padding: 20px;
            width: 250px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            animation: fadeIn 1s ease-in-out;
        }

        .wish-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.2);
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .surprise {
            background: linear-gradient(135deg, #f8bbd9 0%, #e1bee7 100%);
            text-align: center;
        }

        .surprise button {
            background: linear-gradient(135deg, #ffd700 0%, #ffeb3b 100%);
            border: none;
            padding: 15px 30px;
            font-size: 1.2rem;
            font-weight: 600;
            border-radius: 50px;
            cursor: pointer;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            color: #4a148c;
        }

        .surprise button:hover {
            transform: scale(1.05);
            box-shadow: 0 4px 15px rgba(255, 215, 0, 0.5);
        }

        footer {
            background: #4a148c;
            color: white;
            text-align: center;
            padding: 20px;
            font-size: 1rem;
        }

        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2rem;
            }
            .friendship h2, .wishes h2 {
                font-size: 2rem;
            }
            .wish-cards {
                flex-direction: column;
                align-items: center;
            }
            .wish-card {
                width: 90%;
            }
        }
    </style>
</head>
<body>
    <!-- Floating balloons -->
    <div class="balloon"></div>
    <div class="balloon"></div>
    <div class="balloon"></div>
    <div class="balloon"></div>
    <div class="balloon"></div>
    <div class="balloon"></div>
    <div class="balloon"></div>
    <div class="balloon"></div>

    <section id="hero" class="hero">
        <h1>Happy Birthday Mahi 🎉</h1>
    </section>

    <section id="friendship" class="friendship">
        <h2>Mahi is my first and best friend.</h2>
        <p>From the moment we met, you've been the light in my life. Your laughter, your kindness, and your unwavering support have made every day brighter. Here's to many more adventures together!</p>
    </section>

    <section id="wishes" class="wishes">
        <h2>Birthday Wishes</h2>
        <div class="wish-cards">
            <div class="wish-card">
                <p>May your year ahead be filled with joy, success, and endless happiness. Happy Birthday!</p>
            </div>
            <div class="wish-card">
                <p>You deserve all the best in the world. Wishing you a birthday as amazing as you are!</p>
            </div>
            <div class="wish-card">
                <p>Cheers to another year of making memories. May it be your best one yet!</p>
            </div>
        </div>
    </section>

    <section id="surprise" class="surprise">
        <button id="surprise-btn">Click for a Surprise 🎁</button>
    </section>

    <footer>
        <p>Specially created for Mahi</p>
    </footer>

    <script>
        // Smooth scroll animations
        const sections = document.querySelectorAll('section');
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, { threshold: 0.1 });

        sections.forEach(section => observer.observe(section));

        // Confetti on surprise button click
        document.getElementById('surprise-btn').addEventListener('click', () => {
            confetti({
                particleCount: 100,
                spread: 70,
                origin: { y: 0.6 }
            });
        });

        // Smooth scrolling for navigation (if needed, but none here)
        // Add any additional JS for scroll effects if required
    </script>
</body>
</html>
