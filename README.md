<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gino James - Portfolio</title>
    <!-- Google Fonts - Inter -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        /* General Body Styles */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #000000; /* Black background */
            color: #ffffff; /* White text for contrast */
            -webkit-font-smoothing: antialiased; /* For smooth text rendering */
            -moz-osx-font-smoothing: grayscale;
            margin: 0;
            padding: 0;
            box-sizing: border-box; /* Ensure padding and border are included in element's total width and height */
        }

        /* Smooth scroll behavior */
        html {
            scroll-behavior: smooth;
        }

        /* Red Color Definitions */
        .text-red {
            color: #dc2626; /* Tailwind's default red */
        }
        .bg-red {
            background-color: #dc2626;
        }
        .border-red {
            border-color: #dc2626;
        }
        .hover-bg-red-darker:hover {
            background-color: #b91c1c; /* A darker shade of red for hover effects */
        }
        .hover-text-red:hover {
            color: #dc2626;
        }

        /* Section Heading Underline Effect */
        .section-heading {
            position: relative;
            display: inline-block;
            padding-bottom: 0.5rem; /* Space for the underline */
        }
        .section-heading::after {
            content: '';
            position: absolute;
            left: 0;
            bottom: 0;
            width: 100%;
            height: 4px;
            background-color: #dc2626; /* Red underline */
            border-radius: 9999px; /* Rounded corners for the underline */
        }

        /* Navigation Bar */
        .navbar {
            background-color: #000000;
            color: #ffffff;
            padding: 1rem;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); /* shadow-lg */
            position: sticky;
            top: 0;
            z-index: 50;
        }
        .navbar-container {
            max-width: 1280px; /* Equivalent to container mx-auto */
            margin-left: auto;
            margin-right: auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .navbar-title {
            font-size: 2.25rem; /* text-3xl */
            font-weight: 800; /* font-extrabold */
            color: #dc2626; /* text-red-600 */
            border-radius: 0.375rem; /* rounded-md */
            padding: 0.5rem; /* p-2 */
            transition: background-color 0.3s ease; /* transition-colors duration-300 */
        }
        .navbar-title:hover {
            background-color: #1f2937; /* hover:bg-gray-800 */
        }
        .navbar-links {
            display: flex;
            align-items: center;
            gap: 1rem; /* space-x-4 */
        }
        .navbar-links a {
            font-size: 1.125rem; /* text-lg */
            font-weight: 500; /* font-medium */
            padding: 0.5rem 0.75rem; /* py-2 px-3 */
            border-radius: 0.375rem; /* rounded-md */
            transition: all 0.3s ease; /* transition-all duration-300 */
            text-decoration: none; /* Remove underline */
            color: #ffffff; /* Default link color */
        }
        .navbar-links a:hover {
            color: #dc2626; /* hover:text-red-600 */
        }
        .nav-link-underline-hover:hover {
            border-bottom: 2px solid #dc2626; /* Red underline on hover */
        }
        .navbar-contact-button {
            background-color: #dc2626; /* bg-red-600 */
            color: #ffffff;
            padding: 0.5rem 1.25rem; /* px-5 py-2 */
            border-radius: 9999px; /* rounded-full */
            font-size: 1.125rem; /* text-lg */
            font-weight: 600; /* font-semibold */
            transition: all 0.3s ease; /* transition-all duration-300 */
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); /* shadow-md */
            text-decoration: none; /* Remove underline */
        }
        .navbar-contact-button:hover {
            background-color: #b91c1c; /* hover:bg-red-700 */
        }

        /* Hero Section */
        .hero-section {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            background-color: #000000;
            color: #ffffff;
            text-align: center;
            padding: 2rem;
        }
        .hero-content {
            max-width: 960px; /* max-w-4xl */
            margin-left: auto;
            margin-right: auto;
        }
        .hero-title {
            font-size: 3rem; /* text-5xl */
            line-height: 1.25; /* leading-tight */
            font-weight: 800; /* font-extrabold */
            margin-bottom: 1rem; /* mb-4 */
        }
        .hero-subtitle {
            font-size: 1.5rem; /* text-2xl */
            font-weight: 300; /* font-light */
            margin-bottom: 2rem; /* mb-8 */
        }
        .hero-button {
            background-color: #dc2626;
            color: #ffffff;
            padding: 1rem 2rem; /* px-8 py-4 */
            border-radius: 9999px; /* rounded-full */
            font-size: 1.25rem; /* text-xl */
            font-weight: 600; /* font-semibold */
            transition: all 0.3s ease; /* transition-all duration-300 */
            transform: scale(1); /* initial scale for hover effect */
            box-shadow: 0 10px 15px rgba(0, 0, 0, 0.1); /* shadow-lg */
            text-decoration: none;
            display: inline-block; /* To apply transform */
        }
        .hero-button:hover {
            background-color: #b91c1c;
            transform: scale(1.05); /* hover:scale-105 */
        }

        /* About Section */
        .about-section {
            padding-top: 5rem; /* py-20 */
            padding-bottom: 5rem; /* py-20 */
            background-color: #111827; /* bg-gray-900 */
            color: #ffffff;
            padding: 2rem;
        }
        .about-container {
            max-width: 1024px; /* max-w-5xl */
            margin-left: auto;
            margin-right: auto;
        }
        .about-heading {
            font-size: 2.25rem; /* text-4xl */
            font-weight: 700; /* font-bold */
            text-align: center;
            margin-bottom: 3rem; /* mb-12 */
        }
        .about-content {
            display: flex;
            flex-direction: column; /* flex-col */
            align-items: center;
            gap: 2.5rem; /* gap-10 */
        }
        .about-text {
            font-size: 1.125rem; /* text-lg */
            line-height: 1.625; /* leading-relaxed */
        }
        .about-text p {
            margin-bottom: 1rem; /* mb-4 */
        }
        .about-text .highlight {
            font-weight: 600; /* font-semibold */
            color: #dc2626; /* text-red-600 */
        }

        /* Animation for About section */
        .animated-text-container {
            display: flex;
            align-items: center;
            justify-content: center;
            height: 300px; /* Adjust height as needed */
            width: 300px; /* Adjust width as needed */
            overflow: hidden;
            position: relative;
            border: 4px solid #dc2626; /* Red border */
            border-radius: 50%; /* Circular shape */
            background-color: #1a1a1a; /* Dark background for animation */
            box-shadow: 0 0 20px rgba(220, 38, 38, 0.5); /* Red glow effect */
        }

        .animated-text {
            font-size: 1.5rem; /* Adjust font size */
            font-weight: 700;
            color: #ffffff;
            text-align: center;
            position: absolute;
            opacity: 0;
            animation: text-fade-in-out 12s infinite; /* 4s per text, 3 texts = 12s cycle */
            padding: 1rem;
        }

        .animated-text:nth-child(1) {
            animation-delay: 0s;
        }
        .animated-text:nth-child(2) {
            animation-delay: 4s;
        }
        .animated-text:nth-child(3) {
            animation-delay: 8s;
        }

        @keyframes text-fade-in-out {
            0% { opacity: 0; transform: translateY(20px); }
            10% { opacity: 1; transform: translateY(0); }
            30% { opacity: 1; transform: translateY(0); }
            40% { opacity: 0; transform: translateY(-20px); }
            100% { opacity: 0; }
        }

        /* Section Cards (Data Science, Web Dev, AI/ML) */
        .section-cards-grid {
            display: grid;
            grid-template-columns: 1fr; /* Default to single column */
            gap: 2.5rem; /* gap-10 */
        }
        .card {
            background-color: #1f2937; /* bg-gray-800 */
            padding: 2rem; /* p-8 */
            border-radius: 0.5rem; /* rounded-lg */
            box-shadow: 0 10px 15px rgba(0, 0, 0, 0.1); /* shadow-xl */
            border: 1px solid #dc2626; /* border border-red-600 */
        }
        .card-heading {
            font-size: 1.5rem; /* text-2xl */
            font-weight: 600; /* font-semibold */
            color: #dc2626; /* text-red-600 */
            margin-bottom: 1rem; /* mb-4 */
        }
        .card-list {
            list-style-type: disc;
            list-style-position: inside;
            font-size: 1.125rem; /* text-lg */
            line-height: 1.5; /* space-y-2 (approximated) */
        }
        .card-list li {
            margin-bottom: 0.5rem; /* Adjust as needed for spacing */
        }
        .card-list .bold-text {
            font-weight: 600; /* font-semibold */
        }

        /* Contact Section */
        .contact-section {
            padding-top: 5rem; /* py-20 */
            padding-bottom: 5rem; /* py-20 */
            background-color: #111827; /* bg-gray-900 */
            color: #ffffff;
            padding: 2rem;
        }
        .contact-container {
            max-width: 768px; /* max-w-3xl */
            margin-left: auto;
            margin-right: auto;
            text-align: center;
        }
        .contact-heading {
            font-size: 2.25rem; /* text-4xl */
            font-weight: 700; /* font-bold */
            margin-bottom: 3rem; /* mb-12 */
        }
        .contact-text {
            font-size: 1.125rem; /* text-lg */
            margin-bottom: 2rem; /* mb-8 */
        }
        .contact-buttons {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 1.5rem; /* space-y-6 */
        }
        .contact-email-button {
            background-color: #dc2626;
            color: #ffffff;
            padding: 1rem 2rem; /* px-8 py-4 */
            border-radius: 9999px; /* rounded-full */
            font-size: 1.25rem; /* text-xl */
            font-weight: 600; /* font-semibold */
            transition: all 0.3s ease;
            transform: scale(1);
            box-shadow: 0 10px 15px rgba(0, 0, 0, 0.1);
            text-decoration: none;
            display: inline-block;
        }
        .contact-email-button:hover {
            background-color: #b91c1c;
            transform: scale(1.05);
        }
        .social-icons {
            display: flex;
            gap: 1.5rem; /* space-x-6 */
            font-size: 1.875rem; /* text-3xl */
        }
        .social-icons a {
            color: #ffffff; /* Default icon color */
            transition: color 0.3s ease;
        }
        .social-icons a:hover {
            color: #dc2626; /* hover:text-red-600 */
        }

        /* Footer */
        .footer {
            background-color: #000000;
            color: #ffffff;
            padding-top: 2rem; /* py-8 */
            padding-bottom: 2rem; /* py-8 */
            text-align: center;
            font-size: 0.875rem; /* text-sm */
        }
        .footer-container {
            max-width: 1280px; /* container mx-auto */
            margin-left: auto;
            margin-right: auto;
        }
        .footer-heart {
            color: #dc2626; /* text-red-600 */
        }

        /* Responsive Adjustments */
        @media (min-width: 768px) { /* md breakpoint */
            .hero-title {
                font-size: 4.5rem; /* md:text-7xl */
            }
            .hero-subtitle {
                font-size: 1.875rem; /* md:text-3xl */
            }
            .about-content {
                flex-direction: row; /* md:flex-row */
            }
            .about-content > div:first-child { /* md:w-1/3 */
                width: 33.333333%;
            }
            .about-content > div:last-child { /* md:w-2/3 */
                width: 66.666667%;
            }
            .animated-text-container {
                margin-bottom: 0; /* Remove margin on larger screens */
            }
            .section-cards-grid {
                grid-template-columns: repeat(2, 1fr); /* md:grid-cols-2 */
            }
            .navbar-links {
                gap: 1.5rem; /* md:space-x-6 */
            }
        }
    </style>
</head>
<body class="antialiased">

    <!-- Navigation Bar -->
    <nav class="navbar">
        <div class="navbar-container">
            <!-- Your Name as Logo/Title -->
            <a href="#hero" class="navbar-title">Gino James</a>
            <div class="navbar-links">
                <a href="#about" class="nav-link-underline-hover">About</a>
                <a href="#data-science" class="nav-link-underline-hover">Data Science</a>
                <a href="#web-development" class="nav-link-underline-hover">Web Development</a>
                <a href="#ai-ml" class="nav-link-underline-hover">AI/ML</a>
                <!-- Contact button in nav bar -->
                <a href="#contact" class="navbar-contact-button">Contact</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="hero" class="hero-section">
        <div class="hero-content">
            <h1 class="hero-title">
                Hi, I'm <span class="text-red">Gino James</span>
            </h1>
            <p class="hero-subtitle">
                A passionate <span class="text-red">Data Scientist</span>, <span class="text-red">Web Developer</span>, and <span class="text-red">AI/ML Enthusiast</span>.
            </p>
            <a href="#about" class="hero-button">
                Learn More About Me
            </a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about-section">
        <div class="about-container">
            <h2 class="about-heading section-heading">About Me</h2>
            <div class="about-content">
                <div class="animated-text-container">
                    <div class="animated-text">Data Scientist</div>
                    <div class="animated-text">Web Developer</div>
                    <div class="animated-text">AI/ML Enthusiast</div>
                </div>
                <div class="about-text">
                    <p>
                        Hello! I'm <span class="highlight">Gino James</span>, a versatile professional with a strong foundation in data science, web development, and artificial intelligence. My journey in technology is driven by a deep curiosity and a passion for solving complex problems through innovative solutions.
                    </p>
                    <p>
                        As a <span class="highlight">Data Scientist</span>, I excel in extracting meaningful insights from raw data, building predictive models, and visualizing complex information to drive informed decisions. My expertise spans statistical analysis, machine learning algorithms, and data manipulation using tools like Python (Pandas, NumPy, Scikit-learn) and R.
                    </p>
                    <p>
                        In <span class="highlight">Web Development</span>, I enjoy crafting responsive, user-friendly, and performant web applications. I have experience with front-end technologies like HTML, CSS, JavaScript (React, Vue.js), and back-end frameworks such as Node.js and Python (Django, Flask), ensuring a full-stack approach to development.
                    </p>
                    <p>
                        My enthusiasm for <span class="highlight">AI/ML</span> pushes me to continuously explore the latest advancements in neural networks, deep learning, and natural language processing. I am dedicated to developing intelligent systems that can learn, adapt, and provide value in various domains.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Data Science Section -->
    <section id="data-science" class="about-section bg-black">
        <div class="about-container">
            <h2 class="about-heading section-heading">Data Science Expertise</h2>
            <div class="section-cards-grid">
                <div class="card">
                    <h3 class="card-heading">Skills & Tools</h3>
                    <ul class="card-list">
                        <li>Python (Pandas, NumPy, SciPy, Scikit-learn, Matplotlib, Seaborn)</li>
                        <li>Statistical Modeling & Hypothesis Testing</li>
                        <li>Machine Learning (Regression, Classification, Clustering)</li>
                        <li>Data Cleaning & Preprocessing</li>
                        <li>Data Visualization</li>
                        <li>SQL & Database Management</li>
                    </ul>
                </div>
                <div class="card">
                    <h3 class="card-heading">Projects (Examples)</h3>
                    <ul class="card-list">
                        <li><span class="bold-text">Customer Churn Prediction:</span> Developed a predictive model using logistic regression and random forests.</li>
                        <li><span class="bold-text">Sales Forecasting:</span> Implemented time series analysis to forecast future sales trends.</li>
                        <li><span class="bold-text">Sentiment Analysis:</span> Built a model to analyze social media sentiment using NLP techniques.</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Web Development Section -->
    <section id="web-development" class="about-section">
        <div class="about-container">
            <h2 class="about-heading section-heading">Web Development Skills</h2>
            <div class="section-cards-grid">
                <div class="card">
                    <h3 class="card-heading">Front-End</h3>
                    <ul class="card-list">
                        <li>HTML5, CSS3, JavaScript (ES6+)</li>
                        <li>Frameworks: React.js, Vue.js</li>
                        <li>Styling: Custom CSS, Bootstrap (if preferred, currently custom)</li>
                        <li>Responsive Design & Mobile-First Development</li>
                    </ul>
                </div>
                <div class="card">
                    <h3 class="card-heading">Back-End & Other</h3>
                    <ul class="card-list">
                        <li>Node.js, Express.js</li>
                        <li>Python: Django, Flask</li>
                        <li>Databases: MongoDB, PostgreSQL, MySQL</li>
                        <li>Version Control: Git</li>
                        <li>RESTful APIs</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- AI/ML Enthusiast Section -->
    <section id="ai-ml" class="about-section bg-black">
        <div class="about-container">
            <h2 class="about-heading section-heading">AI/ML Enthusiasm</h2>
            <div class="section-cards-grid">
                <div class="card">
                    <h3 class="card-heading">Areas of Interest</h3>
                    <ul class="card-list">
                        <li>Deep Learning (TensorFlow, Keras, PyTorch)</li>
                        <li>Natural Language Processing (NLP)</li>
                        <li>Computer Vision</li>
                        <li>Reinforcement Learning</li>
                        <li>Ethical AI & Explainable AI (XAI)</li>
                    </ul>
                </div>
                <div class="card">
                    <h3 class="card-heading">Learning & Exploration</h3>
                    <ul class="card-list">
                        <li>Continuously learning new models and architectures.</li>
                        <li>Experimenting with generative AI and large language models.</li>
                        <li>Participating in Kaggle competitions and open-source projects.</li>
                        <li>Reading research papers and staying updated with industry trends.</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact-section">
        <div class="contact-container">
            <h2 class="contact-heading section-heading">Get In Touch</h2>
            <p class="contact-text">
                I'm always open to new opportunities, collaborations, and interesting discussions. Feel free to reach out!
            </p>
            <div class="contact-buttons">
                <a href="mailto:your.email@example.com" class="contact-email-button">
                    Email Me: your.email@example.com
                </a>
                <div class="social-icons">
                    <!-- LinkedIn Icon -->
                    <a href="https://linkedin.com/in/yourprofile" target="_blank" class="hover-text-red">
                        <svg class="w-8 h-8" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                            <path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/>
                        </svg>
                    </a>
                    <!-- Instagram Icon -->
                    <a href="https://instagram.com/yourprofile" target="_blank" class="hover-text-red">
                        <svg class="w-8 h-8" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                            <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.77 1.69 4.918 4.918.058 1.265.07 1.645.07 4.85s-.012 3.584-.07 4.85c-.148 3.252-1.69 4.77-4.918 4.918-1.265.058-1.645.07-4.85.07s-3.584-.012-4.85-.07c-3.252-.148-4.77-1.69-4.918-4.918-.058-1.265-.07-1.645-.07-4.85s.012-3.584.07-4.85c.148-3.252 1.69-4.77 4.918-4.918 1.265-.058 1.645-.07 4.85-.07zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.623-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.623 6.78 6.98 6.98 1.281.058 1.689.073 4.948.073s3.668-.014 4.948-.072c4.354-.2 6.78-2.623 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.623-6.78-6.979-6.98-1.281-.059-1.689-.073-4.948-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.162 6.162 6.162 6.162-2.759 6.162-6.162c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4s1.791-4 4-4 4 1.79 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/>
                        </svg>
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="footer-container">
            <p>&copy; 2025 Gino James. All rights reserved. Designed with <span class="footer-heart">&hearts;</span> and Code.</p>
        </div>
    </footer>

    <!-- JavaScript for smooth scrolling -->
    <script>
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
