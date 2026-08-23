<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Staryjump | Developer Portfolio</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            font-family: Arial, Helvetica, sans-serif;
            background: #0b0b0f;
            color: #ffffff;
            line-height: 1.6;
        }

        nav {
            position: fixed;
            top: 0;
            width: 100%;
            padding: 20px 8%;
            background: rgba(11, 11, 15, 0.9);
            backdrop-filter: blur(10px);
            display: flex;
            justify-content: space-between;
            align-items: center;
            z-index: 1000;
            border-bottom: 1px solid #202027;
        }

        nav .logo {
            font-size: 22px;
            font-weight: bold;
        }

        nav a {
            color: #aaa;
            text-decoration: none;
            margin-left: 25px;
            transition: 0.2s;
        }

        nav a:hover {
            color: white;
        }

        section {
            max-width: 1000px;
            margin: auto;
            padding: 100px 25px;
        }

        .hero {
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        .hero p {
            color: #888;
            font-size: 18px;
            margin-bottom: 10px;
        }

        .hero h1 {
            font-size: clamp(50px, 10vw, 90px);
            line-height: 1;
            margin-bottom: 20px;
        }

        .hero h2 {
            color: #999;
            font-size: 25px;
            font-weight: normal;
        }

        .button {
            display: inline-block;
            margin-top: 30px;
            padding: 12px 22px;
            border: 1px solid #444;
            border-radius: 8px;
            color: white;
            text-decoration: none;
            transition: 0.2s;
        }

        .button:hover {
            background: white;
            color: black;
        }

        h2.section-title {
            font-size: 35px;
            margin-bottom: 30px;
        }

        .text {
            color: #aaa;
            max-width: 750px;
            font-size: 17px;
        }

        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin-top: 25px;
        }

        .skill {
            background: #15151c;
            border: 1px solid #252530;
            padding: 10px 18px;
            border-radius: 8px;
        }

        .card {
            background: #111118;
            border: 1px solid #24242d;
            padding: 25px;
            border-radius: 12px;
            margin-bottom: 18px;
            transition: 0.2s;
        }

        .card:hover {
            transform: translateY(-3px);
            border-color: #444;
        }

        .card h3 {
            margin-bottom: 5px;
            font-size: 21px;
        }

        .card .role {
            color: #888;
            margin-bottom: 12px;
        }

        .card p {
            color: #aaa;
        }

        .project-status {
            display: inline-block;
            margin-top: 15px;
            padding: 5px 10px;
            border-radius: 6px;
            background: #191923;
            color: #aaa;
            font-size: 13px;
        }

        .contact a {
            color: white;
            text-decoration: none;
        }

        footer {
            text-align: center;
            padding: 40px 20px;
            border-top: 1px solid #202027;
            color: #666;
        }

        @media (max-width: 700px) {
            nav {
                padding: 15px 20px;
            }

            nav .links {
                display: none;
            }

            section {
                padding: 80px 20px;
            }
        }
    </style>
</head>

<body>

    <nav>
        <div class="logo">Staryjump</div>

        <div class="links">
            <a href="#about">About</a>
            <a href="#skills">Skills</a>
            <a href="#experience">Experience</a>
            <a href="#projects">Projects</a>
            <a href="#contact">Contact</a>
        </div>
    </nav>


    <!-- HOME -->

    <section class="hero">

        <p>Hello, my name is</p>

        <h1>Staryjump</h1>

        <h2>Roblox Developer</h2>

        <a class="button" href="#about">View Portfolio</a>

    </section>


    <!-- ABOUT -->

    <section id="about">

        <h2 class="section-title">About Me</h2>

        <p class="text">
            Hello! I'm Staryjump, a Roblox Developer interested in creating
            games and interactive experiences on Roblox.

            I work with Lua, HTML and JavaScript, and I enjoy developing
            projects while improving my technical skills and creating
            new experiences.
        </p>

    </section>


    <!-- SKILLS -->

    <section id="skills">

        <h2 class="section-title">Skills</h2>

        <div class="skills">

            <div class="skill">Lua</div>
            <div class="skill">HTML</div>
            <div class="skill">JavaScript</div>
            <div class="skill">Roblox Studio</div>
            <div class="skill">Game Development</div>

        </div>

    </section>


    <!-- EXPERIENCE -->

    <section id="experience">

        <h2 class="section-title">Work History</h2>

        <div class="card">

            <h3>Freshly</h3>

            <div class="role">
                Store Management
            </div>

            <p>
                Experience in store management and working within
                the company's Roblox environment.
            </p>

        </div>


        <div class="card">

            <h3>Nexo Corporation</h3>

            <div class="role">
                Corporate Intern
            </div>

            <p>
                Experience as a Corporate Intern, contributing to
                the company's activities and gaining experience
                within a Roblox corporate environment.
            </p>

        </div>

    </section>


    <!-- PROJECTS -->

    <section id="projects">

        <h2 class="section-title">Projects</h2>

        <div class="card">

            <h3>Dropper Game</h3>

            <p>
                A Roblox Dropper game currently in development.
                The entire build was created by me from scratch,
                including the game's environment and structures.
            </p>

            <span class="project-status">
                In Development
            </span>

        </div>

    </section>


    <!-- CONTACT -->

    <section id="contact" class="contact">

        <h2 class="section-title">Contact</h2>

        <p class="text">
            Interested in working with me or want to learn more
            about my projects? Feel free to contact me.
        </p>

        <a class="button" href="https://discord.com/" target="_blank">
            Discord
        </a>

    </section>


    <footer>

        © 2026 Staryjump. All rights reserved.

    </footer>

</body>
</html>
