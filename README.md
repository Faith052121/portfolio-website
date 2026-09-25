<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Faith Nacion | Portfolio</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        :root {
            --sky: #8ed8f6;
            --red: #e94335;
            --yellow: #ffd447;
            --blue: #3b9fd2;
            --wood: #8a542c;
            --ink: #49351f;
            --paper: #fff8df;
        }

        body {
            font-family: "Trebuchet MS", Arial, sans-serif;
            background: var(--sky);
            color: var(--ink);
            line-height: 1.6;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        /* NAVIGATION */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background: var(--red);
            border-bottom: 5px solid var(--yellow);
            box-shadow: 0 5px 0 rgba(90, 50, 20, .16);
            z-index: 1000;
        }

        nav {
            max-width: 1200px;
            margin: auto;
            padding: 18px 30px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 20px;
        }

        .logo {
            font-size: 24px;
            color: var(--yellow);
            font-weight: 900;
            text-shadow: 2px 2px #92301d;
        }

        nav ul {
            list-style: none;
            display: flex;
            gap: 22px;
        }

        nav ul li a {
            color: white;
            font-weight: bold;
            transition: .3s;
        }

        nav ul li a:hover {
            color: var(--yellow);
        }

        /* HOME / HERO */
        .hero {
            min-height: 100vh;
            max-width: 1200px;
            margin: auto;
            padding: 150px 30px 80px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 60px;
            position: relative;
            overflow: hidden;
            background:
                radial-gradient(ellipse at 12% 22%, white 0 5%, transparent 5.5%),
                radial-gradient(ellipse at 17% 18%, white 0 7%, transparent 7.5%),
                radial-gradient(ellipse at 23% 22%, white 0 5%, transparent 5.5%),
                radial-gradient(ellipse at 75% 31%, white 0 5%, transparent 5.5%),
                radial-gradient(ellipse at 81% 27%, white 0 7%, transparent 7.5%),
                radial-gradient(ellipse at 87% 31%, white 0 5%, transparent 5.5%),
                linear-gradient(180deg, #62c5f3 0%, #b8e9ff 100%);
        }

        .hero::before,
        .hero::after {
            content: "★";
            position: absolute;
            color: var(--yellow);
            font-size: 54px;
            text-shadow: 2px 3px #b97824;
            pointer-events: none;
        }

        .hero::before {
            top: 22%;
            left: 5%;
        }

        .hero::after {
            right: 7%;
            bottom: 16%;
            font-size: 40px;
        }

        .hero-text {
            max-width: 650px;
            position: relative;
            z-index: 1;
        }

        .hello {
            color: #b92f25;
            font-weight: 900;
            letter-spacing: 3px;
            margin-bottom: 10px;
        }

        .hero h1 {
            color: white;
            font-size: 65px;
            line-height: 1.1;
            margin-bottom: 15px;
            text-shadow: 3px 4px #b35c26, 5px 6px #74421e;
        }

        .hero h1 span {
            color: var(--yellow);
        }

        .hero h2 {
            color: #8d301d;
            font-size: 25px;
            margin-bottom: 20px;
        }

        .hero-text > p:not(.hello) {
            color: #3f4c53;
            margin-bottom: 30px;
        }

        .profile {
            position: relative;
            z-index: 1;
            padding: 10px;
            background: var(--yellow);
            border: 5px solid white;
            border-radius: 50%;
            box-shadow: 7px 9px 0 var(--wood);
            transform: rotate(3deg);
        }

        .profile img {
            width: 320px;
            height: 320px;
            object-fit: cover;
            border-radius: 50%;
            border: 5px solid var(--red);
        }

        /* BUTTONS */
        .button {
            display: inline-block;
            background: var(--red);
            color: white;
            padding: 12px 25px;
            border: 3px solid #b92f25;
            border-radius: 8px;
            font-weight: bold;
            margin-right: 10px;
            transition: .3s;
            box-shadow: 3px 4px 0 #8a542c;
        }

        .button:hover {
            transform: translateY(-3px);
            background: #c93429;
        }

        .button.second {
            background: var(--blue);
            border-color: #247eae;
        }

        /* GENERAL SECTIONS */
        .section {
            max-width: 1200px;
            margin: auto;
            padding: 100px 30px;
        }

        .section-title {
            text-align: center;
            font-size: 40px;
            margin-bottom: 50px;
            color: #a93427;
            text-shadow: 1px 2px #fff;
        }

        .section-title::after {
            content: "";
            display: block;
            width: 70px;
            height: 5px;
            background: var(--yellow);
            border: 1px solid #d39e16;
            margin: 12px auto;
            border-radius: 10px;
        }

        /* ABOUT */
        .about-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
        }

        .about-container h3 {
            font-size: 25px;
            margin-bottom: 15px;
            color: #a93427;
        }

        .about-container p {
            color: #594c3d;
            margin-bottom: 15px;
        }

        .info {
            background: var(--paper);
            padding: 30px;
            border-radius: 15px;
            border: 4px solid #e5b72e;
            box-shadow: 5px 6px 0 #b57b3e;
        }

        .info p {
            border-bottom: 1px dashed #c9a65b;
            padding: 10px 0;
        }

        .info strong {
            color: #a93427;
        }

        /* SKILLS */
        .skills-section {
            max-width: 100%;
            background: #d8f3ff;
        }

        .skills-container {
            max-width: 1100px;
            margin: auto;
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
        }

        .skill-card,
        .project-card {
            background: white;
            padding: 30px;
            border-radius: 15px;
            border: 4px solid #e5b72e;
            box-shadow: 5px 6px 0 #b57b3e;
            transition: .3s;
        }

        .skill-card:hover,
        .project-card:hover {
            transform: translateY(-6px) rotate(-.5deg);
            border-color: var(--blue);
        }

        .skill-card h3 {
            color: #b93428;
            margin-bottom: 10px;
        }

        .skill-card p,
        .project-card p {
            color: #594c3d;
        }

        /* PROJECTS */
        .projects-container {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
        }

        .project-icon {
            width: 50px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: var(--yellow);
            color: #8b321f;
            border: 3px solid #d39e16;
            border-radius: 12px;
            font-weight: bold;
            margin-bottom: 20px;
        }

        .project-card h3 {
            margin-bottom: 10px;
            color: #a93427;
        }

        .project-card p {
            margin-bottom: 20px;
        }

        .project-card span {
            display: inline-block;
            padding: 4px 12px;
            color: white;
            background: var(--blue);
            border-radius: 15px;
            font-size: 14px;
            font-weight: bold;
        }

        /* RESUME */
        .resume-section {
            background: #d8f3ff;
            max-width: 100%;
        }

        .resume {
            max-width: 1100px;
            margin: auto;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
        }

        .resume-column h3 {
            font-size: 25px;
            color: #a93427;
            margin-bottom: 20px;
        }

        .resume-item {
            border-left: 5px solid var(--blue);
            padding-left: 20px;
            margin-bottom: 40px;
        }

        .resume-item h4 {
            font-size: 20px;
        }

        .resume-item p {
            color: #594c3d;
        }

        .resume-item .date {
            color: #b33a2a;
            font-size: 14px;
            margin: 5px 0;
        }

        .resume-list {
            list-style: none;
            margin-bottom: 40px;
        }

        .resume-list li {
            background: #fff1bd;
            border-left: 5px solid #e9b932;
            padding: 10px 15px;
            margin-bottom: 8px;
            border-radius: 6px;
            color: #594c3d;
        }

        /* CONTACT */
        #contact {
            max-width: 100%;
            background: var(--paper);
            border-top: 8px dashed #e7b63d;
        }

        .contact-section {
            text-align: center;
        }

        .contact-section > p {
            color: #594c3d;
            margin-bottom: 25px;
        }

        .contact-info {
            margin-bottom: 30px;
        }

        .contact-info p {
            margin: 8px;
            color: #594c3d;
        }

        /* FOOTER */
        footer {
            text-align: center;
            padding: 25px;
            background: var(--red);
            border-top: 6px solid var(--yellow);
            color: white;
            font-size: 14px;
            font-weight: bold;
        }

        /* RESPONSIVE DESIGN */
        @media (max-width: 900px) {
            nav ul {
                gap: 12px;
            }

            .hero {
                flex-direction: column-reverse;
                text-align: center;
            }

            .hero h1 {
                font-size: 45px;
            }

            .skills-container,
            .projects-container {
                grid-template-columns: 1fr 1fr;
            }

            .about-container,
            .resume {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 600px) {
            nav {
                flex-direction: column;
                gap: 15px;
            }

            nav ul {
                flex-wrap: wrap;
                justify-content: center;
            }

            .hero {
                padding-top: 180px;
            }

            .hero h1 {
                font-size: 38px;
            }

            .profile img {
                width: 220px;
                height: 220px;
            }

            .skills-container,
            .projects-container {
                grid-template-columns: 1fr;
            }

            .button {
                margin-bottom: 10px;
            }
        }
    </style>
</head>

<body>

    <!-- NAVIGATION -->
    <header>
        <nav>
            <h2 class="logo">MyPortfolio</h2>

            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#resume">Resume</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- HOME -->
    <section id="home" class="hero">
        <div class="hero-text">
            <p class="hello">HELLO, I'M</p>

            <h1>
                Faith
                <span>Nacion</span>
            </h1>

            <h2>IT Student &amp; Future Web Developer</h2>

            <p>
                I am an Information Technology student who enjoys learning
                about programming, web development, and technology.
            </p>

            <a href="#contact" class="button">Contact Me</a>
            <a href="#resume" class="button second">View Resume</a>
        </div>

        <div class="profile">
            <img src="https://uploads.onecompiler.io/454ab27he/1790332325767/profile%20website.jpg" alt="Faith Nacion">
        </div>
    </section>

    <!-- ABOUT -->
    <section id="about" class="section">
        <h2 class="section-title">About Me</h2>

        <div class="about-container">
            <div>
                <h3>Who Am I?</h3>

                <p>
                    I am an IT student interested in technology and
                    programming. I am currently developing my skills in
                    HTML, CSS, Python, C++, and database systems.
                </p>

                <p>
                    My goal is to improve my technical skills and gain
                    experience in creating useful and creative digital
                    projects.
                </p>
            </div>

            <div class="info">
                <p><strong>Name:</strong> Angel Faith B. Nacion</p>
                <p><strong>Course:</strong> Bachelor of Science Information Technology</p>
                <p><strong>Year Level:</strong> 2nd Year</p>
                <p><strong>Location:</strong> Cainta, Rizal</p>
                <p><strong>Email:</strong> fnacion40@gmail.com</p>
            </div>
        </div>
    </section>

    <!-- SKILLS -->
    <section id="skills" class="section skills-section">
        <h2 class="section-title">My Skills</h2>

        <div class="skills-container">
            <div class="skill-card">
                <h3>HTML</h3>
                <p>Creating structured and semantic web pages.</p>
            </div>

            <div class="skill-card">
                <h3>CSS</h3>
                <p>Designing responsive and attractive websites.</p>
            </div>

            <div class="skill-card">
                <h3>Python</h3>
                <p>Creating simple programs and solving problems.</p>
            </div>

            <div class="skill-card">
                <h3>C++</h3>
                <p>Developing programs using functions, loops, and OOP.</p>
            </div>

            <div class="skill-card">
                <h3>Database</h3>
                <p>Learning SQL, ERD, databases, and data management.</p>
            </div>

            <div class="skill-card">
                <h3>Problem Solving</h3>
                <p>Finding logical solutions to programming problems.</p>
            </div>
        </div>
    </section>

    <!-- PROJECTS -->
    <section id="projects" class="section">
        <h2 class="section-title">My Projects</h2>

        <div class="projects-container">
            <div class="project-card">
                <div class="project-icon">01</div>
                <h3>Online Banking System</h3>
                <p>
                    A C++ project that allows users to log in, deposit,
                    withdraw, transfer money, check balance, and view
                    transaction history.
                </p>
                <span>C++</span>
            </div>

            <div class="project-card">
                <div class="project-icon">02</div>
                <h3>Student Information System</h3>
                <p>
                    A simple programming project for storing and displaying
                    student information using classes and objects.
                </p>
                <span>Python / OOP</span>
            </div>

            <div class="project-card">
                <div class="project-icon">03</div>
                <h3>Study Tips Website</h3>
                <p>
                    A simple HTML website containing useful study tips
                    and information for students.
                </p>
                <span>HTML / CSS</span>
            </div>
        </div>
    </section>

    <!-- RESUME -->
    <section id="resume" class="section resume-section">
        <h2 class="section-title">Digital Resume</h2>

        <div class="resume">
            <div class="resume-column">
                <h3>Education</h3>

                <div class="resume-item">
                    <h4>Information Technology</h4>
                    <p class="date">2026 - Present</p>
                    <p>
                        Currently studying Information Technology and
                        developing skills in programming, web development,
                        and database systems.
                    </p>
                </div>

                <h3>Experience</h3>

                <div class="resume-item">
                    <h4>Student Projects</h4>
                    <p class="date">2026 - Present</p>
                    <p>
                        Created various academic projects involving
                        programming, HTML/CSS, databases, and system design.
                    </p>
                </div>
            </div>

            <div class="resume-column">
                <h3>Technical Skills</h3>

                <ul class="resume-list">
                    <li>HTML &amp; CSS</li>
                    <li>Python</li>
                    <li>C++</li>
                    <li>SQL</li>
                    <li>Object-Oriented Programming</li>
                    <li>Database Design</li>
                    <li>Basic Web Development</li>
                </ul>

                <h3>Personal Skills</h3>

                <ul class="resume-list">
                    <li>Problem Solving</li>
                    <li>Creativity</li>
                    <li>Communication</li>
                    <li>Teamwork</li>
                    <li>Willingness to Learn</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- CONTACT -->
    <section id="contact" class="section contact-section">
        <h2 class="section-title">Contact Me</h2>

        <p>Want to get in touch? Feel free to contact me.</p>

        <div class="contact-info">
            <p>📧 fnacion40@gmail.com</p>
            <p>📱 +639509098313</p>
            <p>📍 Cainta, Rizal</p>
        </div>

        <a href="mailto:fnacion40@gmail.com" class="button">
            Send Me an Email
        </a>
    </section>

    <!-- FOOTER -->
    <footer>
        <p>© 2026 Angel Faith Nacion. All Rights Reserved.</p>
    </footer>

</body>
</html>
