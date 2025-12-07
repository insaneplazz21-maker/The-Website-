
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The DeXTOz - Innovating Your Digital Future</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Poppins', sans-serif;
            background: #000;
            color: #fff;
            overflow-x: hidden;
        }
        header {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(0, 0, 0, 0.95);
            z-index: 1000;
            padding: 15px 0;
            box-shadow: 0 2px 10px rgba(255, 255, 255, 0.1);
        }
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        .logo {
            font-family: 'Playfair Display', serif;
            font-size: 1.8em;
            font-weight: 700;
            color: #fff;
        }
        nav ul {
            list-style: none;
            display: flex;
        }
        nav ul li {
            margin: 0 20px;
        }
        nav ul li a {
            color: #fff;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        nav ul li a:hover {
            color: #ccc;
        }
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            background: #000;
            position: relative;
            overflow: hidden;
        }
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://via.placeholder.com/1920x1080?text=Business+Background') no-repeat center center/cover;
            opacity: 0.1;
            transform: translateY(0);
            transition: transform 0.1s linear;
        }
        .hero-content {
            z-index: 1;
            max-width: 800px;
            padding: 20px;
        }
        .hero h1 {
            font-family: 'Playfair Display', serif;
            font-size: 3.5em;
            margin-bottom: 15px;
            color: #fff;
        }
        .hero p {
            font-size: 1.3em;
            margin-bottom: 40px;
            color: #ccc;
        }
        .btn {
            display: inline-block;
            padding: 15px 30px;
            margin: 0 10px;
            background: #fff;
            color: #000;
            text-decoration: none;
            border-radius: 0;
            font-weight: 600;
            font-family: 'Poppins', sans-serif;
            transition: all 0.3s;
            box-shadow: 0 4px 8px rgba(255, 255, 255, 0.2);
        }
        .btn:hover {
            background: #000;
            color: #fff;
            box-shadow: 0 4px 8px rgba(255, 255, 255, 0.3);
        }
        section {
            padding: 100px 20px;
            max-width: 1200px;
            margin: 0 auto;
            opacity: 0;
            transform: translateY(50px);
            transition: all 0.6s ease;
        }
        section.visible {
            opacity: 1;
            transform: translateY(0);
        }
        .about, .services, .portfolio, .testimonials, .contact {
            background: #fff;
            color: #000;
            border-radius: 0;
            margin-bottom: 60px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }
        h2 {
            text-align: center;
            font-family: 'Playfair Display', serif;
            font-size: 2.8em;
            margin-bottom: 50px;
            color: #000;
        }
        .about-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }
        .about-content img {
            width: 50%;
            border-radius: 0;
            transition: transform 0.3s;
        }
        .about-content img:hover {
            transform: scale(1.02);
        }
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }
        .service {
            background: #f9f9f9;
            padding: 30px;
            border-radius: 0;
            text-align: center;
            transition: transform 0.3s;
            border: 1px solid #e0e0e0;
        }
        .service:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 30px;
        }
        .portfolio-item {
            background: #f9f9f9;
            border-radius: 0;
            overflow: hidden;
            transition: transform 0.3s;
            border: 1px solid #e0e0e0;
        }
        .portfolio-item:hover {
            transform: scale(1.02);
        }
        .portfolio-item img {
            width: 100%;
            height: 220px;
            object-fit: cover;
        }
        .testimonials {
            position: relative;
        }
        .testimonial-slider {
            display: flex;
            overflow: hidden;
        }
        .testimonial {
            min-width: 100%;
            padding: 40px;
            text-align: center;
        }
        .testimonial p {
            font-style: italic;
            font-size: 1.2em;
        }
        .slider-dots {
            text-align: center;
            margin-top: 30px;
        }
        .dot {
            display: inline-block;
            width: 12px;
            height: 12px;
            background: #ccc;
            border-radius: 50%;
            margin: 0 8px;
            cursor: pointer;
            transition: background 0.3s;
        }
        .dot.active {
            background: #000;
        }
        .contact-form {
            max-width: 600px;
            margin: 0 auto;
        }
        .contact-form input, .contact-form textarea {
            width: 100%;
            padding: 15px;
            margin-bottom: 20px;
            border: 1px solid #ccc;
            border-radius: 0;
            background: #fff;
            color: #000;
            font-family: 'Poppins', sans-serif;
        }
        .contact-form button {
            width: 100%;
            padding: 15px;
            background: #000;
            border: none;
            border-radius: 0;
            color: #fff;
            font-weight: 600;
            cursor: pointer;
            transition: background 0.3s;
        }
        .contact-form button:hover {
            background: #333;
        }
        footer {
            background: #000;
            padding: 50px 20px;
            text-align: center;
            color: #fff;
        }
        .social-icons a {
            color: #fff;
            margin: 0 15px;
            font-size: 1.8em;
            transition: color 0.3s;
        }
        .social-icons a:hover {
            color: #ccc;
        }
        .trust-logos {
            margin-top: 20px;
        }
        .trust-logos img {
            height: 40px;
            margin: 0 10px;
            opacity: 0.7;
        }
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5em;
            }
            .about-content {
                flex-direction: column;
            }
            .about-content img {
                width: 100%;
            }
            nav ul {
                display: none; /* Expand for mobile menu if needed */
            }
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <div class="logo">The DeXTOz</div>
            <ul>
                <li><a href="#hero">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#portfolio">Portfolio</a></li>
                <li><a href="#testimonials">Testimonials</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="hero" class="hero">
        <div class="hero-content">
            <h1>Welcome to The DeXTOz – Innovating Your Digital Future</h1>
            <p>We deliver smart solutions that transform businesses.</p>
            <a href="#contact" class="btn">Get Started</a>
            <a href="#contact" class="btn">Contact Us</a>
        </div>
    </section>

    <section id="about" class="about">
        <h2>About Us</h2>
        <div class="about-content">
            <img src="https://via.placeholder.com/500x300?text=Professional+Team" alt="About Us">
            <div>
                <p>At The DeXTOz, we are committed to driving digital excellence for businesses worldwide. With years of expertise in technology and innovation, our team delivers tailored solutions that enhance efficiency, growth, and customer engagement. Partner with us to unlock your potential.</p>
            </div>
        </div>
    </section>

    <section id="services" class="services">
        <h2>Our Services</h2>
        <div class="services-grid">
            <div class="service">
                <h3>Web Development</h3>
                <p>Custom, scalable websites designed for performance and user experience.</p>
            </div>
            <div class="service">
                <h3>App Development</h3>
                <p>Innovative mobile and web applications to meet your business needs.</p>
            </div>
            <div class="service">
                <h3>Business Branding</h3>
                <p>Strategic branding that builds trust and differentiates your market presence.</p>
            </div>
            <div class="service">
                <h3>Digital Marketing</h3>
                <p>Data-driven campaigns to boost visibility and drive measurable results.</p>
            </div>
        </div>
    </section>

    <section id="portfolio" class="portfolio">
        <h2>Portfolio</h2>
        <div class="portfolio-grid">
            <div class="portfolio-item">
                <img src="https://via.placeholder.com/320x220?text=E-commerce+Platform" alt="Project 1">
                <p>E-commerce Platform for Retail Client</p>
            </div>
            <div class="portfolio-item">
                <img src="https://via.placeholder.com/320x220?text=Mobile+App+UI" alt="Project 2">
                <p>Mobile App UI for FinTech Startup</p>
            </div>
            <div class="portfolio-item">
                <img src="https://via.placeholder.com/320x220?text=Branding+Campaign" alt="Project 3">
                <p>Branding Campaign for Corporate Brand</p>
            </div>
        </div>
    </section>

    <section id="testimonials" class="testimonials">
        <h2>Testimonials</h2>
        <div class="testimonial-slider">
            <div class="testimonial">
                <p>"The DeXTOz exceeded our expectations with their professional approach and innovative solutions." - John Doe, CEO</p>
            </div>
            <div class="testimonial">
                <p>"A trustworthy partner that delivers on time and with excellence." - Jane Smith, Marketing Director</p>
            </div>
            <div class="testimonial">
                <p>"Their expertise transformed our digital presence." - Alex Johnson, Founder</p>
            </div>
        </div>
        <div class="slider-dots">
            <span class="dot active" data-slide="0"></span>
            <span class="dot" data-slide="1"></span>
            <span class="dot" data-slide="2"></span>
        </div>
    </section>

    <section id="contact" class="contact">
        <h2>Contact Us</h2>
        <form class="contact-form">
            <input type="text" placeholder="Your Name" required>
            <input type="email" placeholder="Your Email" required>
            <textarea placeholder="Your Message" rows="5" required></textarea>
            <button type="submit">Send Message</button>
        </form>
    </section>

    <footer>
        <p>&copy; 2023 The DeXTOz. All rights reserved. | Privacy Policy | Terms of Service</p>
        <div class="social-icons">
            <a href="#">&#xf099;</a> <!-- Twitter -->
            <a href="#">&#xf16d;</a> <!-- LinkedIn -->
            <a href="#">&#xf09a;</a> <!-- Facebook -->
        </div>
        <div class="trust-logos">
            <img src="https://via.placeholder.com/100x40?text=Client+1" alt="Client 1">
            <img src="https://via.placeholder.com/100x40?text=Client+2" alt="Client 2">
            <img src="https://via.placeholder.com/100x40?text=Client+3" alt="Client 3">
        </div>
    </footer>

    <script>
        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Parallax effect
        window.addEventListener('scroll', () => {
            const scrolled = window.pageYOffset;
            const parallaxElement = document.querySelector('.hero::before');
            if (parallaxElement) {
                parallaxElement.style.transform = `translateY(${scrolled * 0.3}px)`;
            }
        });

        // Fade-in on scroll
        const observer = new IntersectionObserver(entries => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        });
        document.querySelectorAll('section').forEach(section => {
            observer.observe(section);
        });

        // Testimonial slider
        let currentSlide = 0;
        const slides = document.querySelectorAll('.testimonial');
        const dots = document.querySelectorAll('.dot');
        function showSlide(index) {
            slides.forEach((slide, i) => {
                slide.style.transform = `translateX(${100 * (i - index)}%)`;
            });
            dots.forEach(dot => dot.classList.remove('active'));
            dots[index].classList.add('active');
        }
        dots.forEach((dot, index) => {
            dot.addEventListener('click', () => {
                currentSlide = index;
                showSlide(currentSlide);
            });
        });
        showSlide(currentSlide);

        // Contact form submit
        document.querySelector('.contact-form').addEventListener('submit', e => {
            e.preventDefault();
            alert('Thank you! Your message has been sent. We will respond shortly.');
        });
    </script>
</body>
</html>
