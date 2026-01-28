<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ashish English Academy | Excellence in Education</title>
    
    <!-- Google Fonts for typography -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Playfair+Display:wght@600;700&display=swap" rel="stylesheet">
    
    <!-- FontAwesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <style>
        /* --- CSS Variables & Reset --- */
        :root {
            --primary-blue: #004aad;       /* Deep Royal Blue */
            --secondary-blue: #007bff;     /* Bright Accent Blue */
            --light-blue-bg: #f0f7ff;       /* Very light blue background */
            --white: #ffffff;
            --text-dark: #333333;
            --text-light: #666666;
            --accent-gold: #ffc107;        /* Subtle highlight for credibility */
            
            --font-heading: 'Playfair Display', serif;
            --font-body: 'Poppins', sans-serif;
            
            --shadow: 0 5px 20px rgba(0, 74, 173, 0.1);
            --radius: 12px;
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: var(--font-body);
            color: var(--text-dark);
            line-height: 1.6;
            background-color: var(--white);
            overflow-x: hidden;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        ul {
            list-style: none;
        }

        img {
            max-width: 100%;
            display: block;
        }

        /* --- Reusable Components --- */
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }

        .section-padding {
            padding: 80px 0;
        }

        .btn {
            display: inline-block;
            padding: 12px 30px;
            border-radius: 50px;
            font-weight: 600;
            text-transform: uppercase;
            font-size: 0.9rem;
            cursor: pointer;
            transition: var(--transition);
            border: 2px solid transparent;
        }

        .btn-primary {
            background-color: var(--primary-blue);
            color: var(--white);
        }

        .btn-primary:hover {
            background-color: var(--secondary-blue);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 123, 255, 0.3);
        }

        .btn-outline {
            border-color: var(--white);
            color: var(--white);
            background: transparent;
        }

        .btn-outline:hover {
            background-color: var(--white);
            color: var(--primary-blue);
        }

        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-title h2 {
            font-family: var(--font-heading);
            font-size: 2.5rem;
            color: var(--primary-blue);
            margin-bottom: 15px;
        }

        .section-title p {
            color: var(--text-light);
            max-width: 600px;
            margin: 0 auto;
        }

        /* --- Header / Navigation --- */
        header {
            background-color: var(--white);
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 80px;
        }

        .logo {
            font-family: var(--font-heading);
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary-blue);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo i {
            color: var(--secondary-blue);
        }

        .nav-links {
            display: flex;
            gap: 30px;
        }

        .nav-links a {
            font-weight: 500;
            color: var(--text-dark);
            transition: var(--transition);
            position: relative;
        }

        .nav-links a:hover {
            color: var(--primary-blue);
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 0;
            background-color: var(--primary-blue);
            transition: var(--transition);
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        /* --- Hero Section --- */
        .hero {
            position: relative;
            height: 90vh; /* Full viewport height */
            min-height: 600px;
            background: linear-gradient(rgba(0, 74, 173, 0.8), rgba(0, 30, 80, 0.8)), 
                        url('https://picsum.photos/seed/schoolbuilding/1920/1080.jpg') center/cover no-repeat;
            display: flex;
            align-items: center;
            text-align: center;
            color: var(--white);
        }

        .hero-content h1 {
            font-family: var(--font-heading);
            font-size: 3.5rem;
            margin-bottom: 20px;
            line-height: 1.2;
        }

        .hero-content p {
            font-size: 1.2rem;
            margin-bottom: 40px;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
            opacity: 0.9;
        }

        .hero-badges {
            margin-top: 30px;
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }

        .badge {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(5px);
            padding: 10px 20px;
            border-radius: 30px;
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            gap: 8px;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        /* --- About Section --- */
        .about {
            background-color: var(--white);
        }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .about-img {
            position: relative;
        }

        .about-img img {
            border-radius: var(--radius);
            box-shadow: var(--shadow);
            width: 100%;
        }

        .about-img::before {
            content: '';
            position: absolute;
            top: -20px;
            left: -20px;
            width: 100px;
            height: 100px;
            background-color: var(--light-blue-bg);
            z-index: -1;
            border-radius: var(--radius);
        }

        .about-text h3 {
            color: var(--primary-blue);
            margin-bottom: 20px;
            font-size: 1.8rem;
        }

        .about-text p {
            color: var(--text-light);
            margin-bottom: 20px;
        }

        .grade-highlight {
            display: inline-block;
            background: var(--light-blue-bg);
            color: var(--primary-blue);
            padding: 5px 15px;
            border-radius: 5px;
            font-weight: 600;
            margin-top: 10px;
        }

        /* --- Facilities Section --- */
        .facilities {
            background-color: var(--light-blue-bg);
        }

        .facilities-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .facility-card {
            background: var(--white);
            padding: 40px 30px;
            border-radius: var(--radius);
            text-align: center;
            box-shadow: var(--shadow);
            transition: var(--transition);
        }

        .facility-card:hover {
            transform: translateY(-10px);
        }

        .icon-box {
            width: 80px;
            height: 80px;
            background-color: rgba(0, 74, 173, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 25px;
            color: var(--primary-blue);
            font-size: 2rem;
        }

        .facility-card h4 {
            font-size: 1.4rem;
            margin-bottom: 15px;
            color: var(--text-dark);
        }

        .facility-card p {
            color: var(--text-light);
            font-size: 0.95rem;
        }

        /* --- Leadership Section --- */
        .leadership {
            background-color: var(--white);
        }

        .leadership-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 40px;
        }

        .leader-card {
            display: flex;
            align-items: center;
            gap: 20px;
            background: var(--white);
            border: 1px solid #eee;
            border-radius: var(--radius);
            padding: 30px;
            box-shadow: var(--shadow);
            position: relative;
            overflow: hidden;
        }

        .leader-card::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background-color: var(--primary-blue);
        }

        .leader-img img {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            object-fit: cover;
            border: 3px solid var(--light-blue-bg);
        }

        .leader-info h4 {
            font-size: 1.25rem;
            color: var(--primary-blue);
            margin-bottom: 5px;
        }

        .leader-info span {
            display: block;
            color: var(--secondary-blue);
            font-weight: 600;
            font-size: 0.9rem;
            text-transform: uppercase;
            margin-bottom: 10px;
        }

        .leader-info p {
            font-size: 0.9rem;
            color: var(--text-light);
        }

        /* --- Stats/Staff Banner --- */
        .stats-banner {
            background: linear-gradient(90deg, var(--primary-blue), var(--secondary-blue));
            color: var(--white);
            padding: 60px 0;
            text-align: center;
        }

        .stats-content h3 {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 10px;
        }

        .stats-content p {
            font-size: 1.1rem;
            opacity: 0.9;
        }

        /* --- CTA / Footer Top --- */
        .cta-section {
            background-color: var(--text-dark);
            color: var(--white);
            text-align: center;
            padding: 60px 20px;
            border-radius: var(--radius);
            margin-top: 40px;
        }

        .cta-section h3 {
            font-family: var(--font-heading);
            font-size: 2rem;
            margin-bottom: 15px;
        }

        /* --- Footer --- */
        footer {
            background-color: #002a55; /* Darker blue */
            color: #dbeaff;
            padding: 60px 0 20px;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
            padding-bottom: 40px;
            border-bottom: 1px solid rgba(255,255,255,0.1);
        }

        .footer-col h4 {
            color: var(--white);
            margin-bottom: 20px;
            font-size: 1.2rem;
        }

        .footer-col p {
            margin-bottom: 15px;
            font-size: 0.9rem;
            opacity: 0.8;
        }

        .footer-links li {
            margin-bottom: 10px;
        }

        .footer-links a:hover {
            color: var(--white);
            text-decoration: underline;
        }

        .social-links a {
            display: inline-flex;
            width: 35px;
            height: 35px;
            background: rgba(255,255,255,0.1);
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            margin-right: 10px;
            transition: var(--transition);
        }

        .social-links a:hover {
            background: var(--secondary-blue);
        }

        .copyright {
            text-align: center;
            font-size: 0.85rem;
            opacity: 0.6;
        }

        /* --- Responsive Design --- */
        @media (max-width: 992px) {
            .hero-content h1 {
                font-size: 2.8rem;
            }
            .about-grid {
                grid-template-columns: 1fr;
            }
            .about-img {
                margin-bottom: 40px;
            }
        }

        @media (max-width: 768px) {
            nav {
                flex-direction: column;
                height: auto;
                padding: 15px 0;
            }
            .nav-links {
                margin-top: 20px;
                gap: 15px;
                font-size: 0.9rem;
            }
            .hero-content h1 {
                font-size: 2.2rem;
            }
            .leader-card {
                flex-direction: column;
                text-align: center;
            }
            .leader-card::after {
                width: 100%;
                height: 5px;
                top: 0;
                left: 0;
            }
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <div class="container">
            <nav>
                <div class="logo">
                    <i class="fa-solid fa-graduation-cap"></i>
                    ASHISH ENGLISH ACADEMY
                </div>
                <ul class="nav-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#facilities">Facilities</a></li>
                    <li><a href="#leadership">Leadership</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>Empowering Minds,<br>Shaping Futures</h1>
                <p>Welcome to Ashish English Academy. Providing international standard education with a personal touch in a safe and nurturing environment.</p>
                <a href="#contact" class="btn btn-primary">Admissions Open</a>
                
                <div class="hero-badges">
                    <div class="badge"><i class="fa-solid fa-star"></i> LKG to Grade 8</div>
                    <div class="badge"><i class="fa-solid fa-earth-americas"></i> International Standards</div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about section-padding">
        <div class="container">
            <div class="about-grid">
                <div class="about-img">
                    <!-- Placeholder for school image -->
                    <img src="https://picsum.photos/seed/classroom123/600/400" alt="Students in a classroom">
                </div>
                <div class="about-text">
                    <div class="section-title" style="text-align: left; margin-bottom: 20px;">
                        <h2>Our Vision</h2>
                    </div>
                    <h3>A Foundation for Success</h3>
                    <p>At Ashish English Academy, we believe in holistic development. We provide a robust curriculum that prepares children for a competitive world while maintaining ethical values.</p>
                    <p>From the early years in <strong>LKG</strong> to the pivotal <strong>Grade 8</strong>, our focus remains on academic excellence, character building, and innovation.</p>
                    <div class="grade-highlight">
                        <i class="fa-solid fa-check-circle"></i> Comprehensive Curriculum
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Facilities Section -->
    <section id="facilities" class="facilities section-padding">
        <div class="container">
            <div class="section-title">
                <h2>World-Class Facilities</h2>
                <p>We ensure our students have the best environment to learn, grow, and excel.</p>
            </div>

            <div class="facilities-grid">
                <!-- Facility 1 -->
                <article class="facility-card">
                    <div class="icon-box">
                        <i class="fa-solid fa-snowflake"></i>
                    </div>
                    <h4>AC Classrooms</h4>
                    <p>Climate-controlled, comfortable learning spaces that ensure students remain focused and relaxed regardless of the weather outside.</p>
                </article>

                <!-- Facility 2 -->
                <article class="facility-card">
                    <div class="icon-box">
                        <i class="fa-solid fa-chalkboard-user"></i>
                    </div>
                    <h4>Smart Boards</h4>
                    <p>Interactive digital smart boards in every class to make learning engaging, visual, and aligned with modern teaching methodologies.</p>
                </article>

                <!-- Facility 3 -->
                <article class="facility-card">
                    <div class="icon-box">
                        <i class="fa-solid fa-bus"></i>
                    </div>
                    <h4>Safe Transport</h4>
                    <p>Fast and comfortable transport service covering key areas. We prioritize safety, punctuality, and peace of mind for parents.</p>
                </article>
            </div>
        </div>
    </section>

    <!-- Leadership & Staff -->
    <section id="leadership" class="leadership section-padding">
        <div class="container">
            <div class="section-title">
                <h2>Our Leadership</h2>
                <p>Guided by experience, driven by passion.</p>
            </div>

            <div class="leadership-grid">
                <!-- Principal -->
                <div class="leader-card">
                    <div class="leader-img">
                        <img src="https://picsum.photos/seed/principal/200/200" alt="Mrs. Sibi Blesson">
                    </div>
                    <div class="leader-info">
                        <span>Principal</span>
                        <h4>Mrs. Sibi Blesson</h4>
                        <p>Dedicated to fostering a nurturing environment where every child feels valued and encouraged to reach their full potential.</p>
                    </div>
                </div>

                <!-- Manager -->
                <div class="leader-card">
                    <div class="leader-img">
                        <img src="https://picsum.photos/seed/manager/200/200" alt="Blesson KL">
                    </div>
                    <div class="leader-info">
                        <span>Manager</span>
                        <h4>Blesson KL</h4>
                        <p>Providing strategic vision and management to ensure the school maintains high standards and operational excellence.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Stats/Staff Banner -->
    <section class="stats-banner">
        <div class="container stats-content">
            <h3>10+ Trained Staff</h3>
            <p>Our team of qualified educators ensures better stability and individual attention for every student.</p>
        </div>
    </section>

    <!-- Contact / Footer Area -->
    <footer id="contact">
        <div class="container">
            <div class="footer-grid">
                <!-- Column 1 -->
                <div class="footer-col">
                    <h4>Ashish English Academy</h4>
                    <p>An international standard school committed to academic brilliance from LKG to Grade 8.</p>
                    <div class="social-links">
                        <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
                        <a href="#"><i class="fa-brands fa-instagram"></i></a>
                        <a href="#"><i class="fa-brands fa-whatsapp"></i></a>
                    </div>
                </div>

                <!-- Column 2 -->
                <div class="footer-col">
                    <h4>Quick Links</h4>
                    <ul class="footer-links">
                        <li><a href="#home">Home</a></li>
                        <li><a href="#about">About Us</a></li>
                        <li><a href="#facilities">Facilities</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>

                <!-- Column 3 -->
                <div class="footer-col">
                    <h4>Contact Us</h4>
                    <p><i class="fa-solid fa-location-dot"></i> School Campus Location</p>
                    <p><i class="fa-solid fa-phone"></i> +91 98765 43210</p>
                    <p><i class="fa-solid fa-envelope"></i> info@ashishacademy.edu</p>
                </div>
            </div>
            
            <div class="cta-section">
                <h3>Join the Ashish Family</h3>
                <p style="margin-bottom: 20px; color: #ddd;">Admissions are open for the upcoming academic year.</p>
                <a href="#" class="btn btn-primary">Enquire Now</a>
            </div>

            <div class="copyright">
                <p>&copy; 2023 Ashish English Academy. All Rights Reserved.</p>
            </div>
        </div>
    </footer>

</body>
</html>
