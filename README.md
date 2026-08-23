<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Staryjump | Roblox Developer</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        html {
            width: 100%;
            overflow-x: hidden;
        }

        body {
            width: 100%;
            min-height: 100%;
            overflow-x: hidden;
            font-family: Arial, Helvetica, sans-serif;
            background: #0b0b0f;
            color: #ffffff;
            line-height: 1.6;
        }

        nav {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            padding: 18px 6%;
            background: rgba(11, 11, 15, 0.92);
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
            white-space: nowrap;
        }

        nav .links {
            display: flex;
            align-items: center;
            gap: 25px;
        }

        nav a {
            color: #aaa;
            text-decoration: none;
            transition: 0.2s;
        }

        nav a:hover {
            color: white;
        }

        section {
            width: 100%;
            max-width: 1000px;
            margin: 0 auto;
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
            max-width: 100%;
            overflow-wrap: anywhere;
        }

        .hero h2 {
            color: #999;
            font-size: 25px;
            font-weight: normal;
        }

        .button {
            display: inline-block;
            width: fit-content;
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
            width: 100%;
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
            max-width: 100%;
        }

        .card {
            width: 100%;
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
            width: 100%;
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
                padding: 90px 20px;
            }

            .hero {
                min-height: 100svh;
            }

            .hero p {
                font-size: 16px;
            }

            .hero h1 {
                font-size: clamp(45px, 15vw, 70px);
            }

            .hero h2 {
                font-size: 21px;
            }

            h2.section-title {
                font-size: 30px;
            }

            .text {
                font-size: 16px;
            }

            .card {
                padding: 20px;
            }
        }
    </style>
</head>

<body>

    <nav>

        <div class="logo">
            Staryjump
        </div>

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

        <p>Hey, I'm</p>

        <h1>Staryjump</h1>

        <h2>Roblox Developer</h2>

        <a class="button" href="#about">
            View my work
        </a>

    </section>


    <!-- ABOUT -->

    <section id="about">

        <h2 class="section-title">
            About Me
        </h2>

        <p class="text">
            Hey! I'm Staryjump, a Roblox developer who enjoys
            creating games and working on different projects
            on Roblox.

            <br><br>

            I mainly work with Roblox Studio and Lua. I'm also
            learning web development with HTML and JavaScript.
            I'm always trying to improve my skills and learn
            something new with every project I work on.
        </p>

    </section>


    <!-- SKILLS -->

    <section id="skills">

        <h2 class="section-title">
            Skills
        </h2>

        <div class="skills">

            <div class="skill">Lua</div>
            <div class="skill">Roblox Studio</div>
            <div class="skill">Game Development</div>
            <div class="skill">Building</div>
            <div class="skill">HTML</div>
            <div class="skill">JavaScript</div>

        </div>

    </section>


    <!-- EXPERIENCE -->

    <section id="experience">

        <h2 class="section-title">
            Experience
        </h2>

        <div class="card">

            <h3>
                Freshly
            </h3>

            <div class="role">
                Store Management
            </div>

            <p>
                I gained experience working within the Roblox
                company environment and helping with store
                management.
            </p>

        </div>


        <div class="card">

            <h3>
                Nexo Corporation
            </h3>

            <div class="role">
                Corporate Intern
            </div>

            <p>
                I worked as a Corporate Intern and got experience
                working with a Roblox corporate team and its
                activities.
            </p>

        </div>

    </section>


    <!-- PROJECTS -->

    <section id="projects">

        <h2 class="section-title">
            Projects
        </h2>

        <div class="card">

            <h3>
                Dropper Game
            </h3>

            <p>
                A Roblox Dropper game that I'm currently working on.
                I created the map and environment myself from
                scratch and I'm continuing to develop the game.
            </p>

            <span class="project-status">
                In Development
            </span>

        </div>

    </section>


    <!-- CONTACT -->

    <section id="contact" class="contact">

        <h2 class="section-title">
            Contact
        </h2>

        <p class="text">
            Want to talk about a project, a development opportunity,
            or just get in touch? You can contact me on Discord.
        </p>

        <a class="button" href="https://discord.com/" target="_blank">
            Contact me on Discord
        </a>

    </section>


    <footer>

        © 2026 Staryjump

    </footer>

</body>
</html> 
