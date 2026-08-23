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
            overflow-x: hidden;
        }

        body {
            overflow-x: hidden;
            font-family: Arial, Helvetica, sans-serif;
            background: #08080d;
            color: white;
            line-height: 1.6;
        }

        /* BACKGROUND */

        .background {
            position: fixed;
            inset: 0;
            overflow: hidden;
            pointer-events: none;
            z-index: -1;
        }

        .orb {
            position: absolute;
            width: 350px;
            height: 350px;
            border-radius: 50%;
            background: #6c4cff;
            filter: blur(120px);
            opacity: 0.12;
            animation: float 8s ease-in-out infinite;
        }

        .orb.one {
            top: 5%;
            left: -150px;
        }

        .orb.two {
            right: -150px;
            top: 45%;
            background: #00b7ff;
            animation-delay: -3s;
        }

        .orb.three {
            bottom: -180px;
            left: 35%;
            background: #a855f7;
            animation-delay: -5s;
        }

        @keyframes float {
            0%, 100% {
                transform: translate(0, 0);
            }

            50% {
                transform: translate(30px, -40px);
            }
        }

        /* NAVBAR */

        nav {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            padding: 18px 6%;
            background: rgba(8, 8, 13, 0.75);
            backdrop-filter: blur(15px);
            border-bottom: 1px solid rgba(255,255,255,0.08);
            display: flex;
            justify-content: space-between;
            align-items: center;
            z-index: 1000;
        }

        .logo {
            font-size: 22px;
            font-weight: 800;
        }

        .logo span {
            color: #8b6cff;
        }

        .links {
            display: flex;
            gap: 25px;
        }

        .links a {
            color: #999;
            text-decoration: none;
            transition: 0.25s;
        }

        .links a:hover {
            color: white;
        }

        /* GENERAL */

        section {
            width: 100%;
            max-width: 1050px;
            margin: auto;
            padding: 110px 25px;
        }

        .section-title {
            font-size: 38px;
            margin-bottom: 35px;
        }

        .section-title span {
            color: #8b6cff;
        }

        .text {
            color: #a5a5b0;
            font-size: 17px;
            max-width: 760px;
        }

        /* HERO */

        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
        }

        .hero-content {
            animation: heroAppear 1s ease forwards;
        }

        @keyframes heroAppear {
            from {
                opacity: 0;
                transform: translateY(30px);
            }

            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hello {
            color: #8b6cff;
            font-size: 18px;
            font-weight: bold;
            margin-bottom: 10px;
        }

        .hero h1 {
            font-size: clamp(55px, 11vw, 100px);
            line-height: 0.95;
            letter-spacing: -4px;
            margin-bottom: 20px;
        }

        .hero h2 {
            color: #aaa;
            font-size: 25px;
            font-weight: normal;
        }

        .hero-description {
            color: #858591;
            max-width: 650px;
            margin-top: 20px;
            font-size: 17px;
        }

        .buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin-top: 30px;
        }

        .button {
            display: inline-block;
            padding: 12px 22px;
            border-radius: 9px;
            text-decoration: none;
            color: white;
            border: 1px solid #33333e;
            transition: 0.25s;
        }

        .button.primary {
            background: #7657ff;
            border-color: #7657ff;
        }

        .button:hover {
            transform: translateY(-3px);
            border-color: #8b6cff;
            box-shadow: 0 10px 30px rgba(118, 87, 255, 0.18);
        }

        /* ABOUT */

        .about-grid {
            display: grid;
            grid-template-columns: 280px 1fr;
            gap: 45px;
            align-items: center;
        }

        .profile-image {
            width: 280px;
            height: 280px;
            object-fit: cover;
            border-radius: 25px;
            border: 1px solid #292936;
            background: #111118;
            transition: 0.4s;
        }

        .profile-image:hover {
            transform: rotate(-2deg) scale(1.03);
            border-color: #7657ff;
        }

        .facts {
            margin-top: 25px;
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .fact {
            background: #111118;
            border: 1px solid #252530;
            padding: 9px 14px;
            border-radius: 8px;
            color: #aaa;
        }

        /* SKILLS */

        .skills {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 15px;
        }

        .skill {
            padding: 22px;
            background: rgba(17,17,24,0.8);
            border: 1px solid #252530;
            border-radius: 14px;
            transition: 0.3s;
        }

        .skill:hover {
            transform: translateY(-6px);
            border-color: #7657ff;
        }

        .skill h3 {
            margin-bottom: 5px;
        }

        .skill p {
            color: #777783;
            font-size: 14px;
        }

        /* WORK HISTORY */

        .timeline {
            position: relative;
            border-left: 2px solid #282832;
            padding-left: 30px;
        }

        .history-card {
            position: relative;
            background: rgba(17,17,24,0.85);
            border: 1px solid #252530;
            padding: 25px;
            border-radius: 14px;
            margin-bottom: 20px;
            transition: 0.3s;
        }

        .history-card::before {
            content: "";
            position: absolute;
            width: 11px;
            height: 11px;
            border-radius: 50%;
            background: #7657ff;
            left: -37px;
            top: 30px;
            box-shadow: 0 0 15px #7657ff;
        }

        .history-card:hover {
            transform: translateX(6px);
            border-color: #7657ff;
        }

        .history-card h3 {
            font-size: 21px;
        }

        .role {
            color: #8b6cff;
            margin: 4px 0;
        }

        .date {
            color: #666673;
            font-size: 14px;
            margin-bottom: 12px;
        }

        .history-card p {
            color: #9999a5;
        }

        /* PROJECTS */

        .project {
            overflow: hidden;
            background: #111118;
            border: 1px solid #252530;
            border-radius: 16px;
            margin-bottom: 25px;
            transition: 0.3s;
        }

        .project:hover {
            transform: translateY(-6px);
            border-color: #7657ff;
        }

        .project-image {
            width: 100%;
            height: 330px;
            object-fit: cover;
            display: block;
            background: #171720;
        }

        .project-content {
            padding: 25px;
        }

        .project-content h3 {
            font-size: 24px;
            margin-bottom: 8px;
        }

        .project-content p {
            color: #9999a5;
        }

        .status {
            display: inline-block;
            margin-top: 15px;
            padding: 6px 11px;
            border-radius: 7px;
            background: #1a1925;
            color: #9c8cff;
            font-size: 13px;
        }

        /* VIDEO */

        .video-container {
            margin-top: 30px;
            border-radius: 15px;
            overflow: hidden;
            border: 1px solid #252530;
            background: #111118;
        }

        .video-container video {
            width: 100%;
            display: block;
        }

        /* CONTACT */

        .contact-box {
            text-align: center;
            padding: 60px 25px;
            background: rgba(17,17,24,0.85);
            border: 1px solid #252530;
            border-radius: 20px;
        }

        .contact-box .text {
            margin: auto;
        }

        /* SOCIALS */

        .socials {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 12px;
            margin-top: 35px;
        }

        .social {
            padding: 12px 25px;
            border-radius: 9px;
            border: 1px solid #30303b;
            color: white;
            text-decoration: none;
            background: #111118;
            transition: 0.25s;
        }

        .social:hover {
            transform: translateY(-4px);
            border-color: #7657ff;
            background: #171522;
        }

        /* FOOTER */

        footer {
            text-align: center;
            padding: 45px 20px;
            border-top: 1px solid #202027;
            color: #666673;
        }

        /* MOBILE */

        @media (max-width: 750px) {

            nav {
                padding: 15px 20px;
            }

            .links {
                display: none;
            }

            section {
                padding: 90px 20px;
            }

            .hero h1 {
                font-size: clamp(50px, 17vw, 75px);
                letter-spacing: -3px;
            }

            .hero h2 {
                font-size: 21px;
            }

            .about-grid {
                grid-template-columns: 1fr;
                gap: 30px;
            }

            .profile-image {
                width: 210px;
                height: 210px;
            }

            .skills {
                grid-template-columns: 1fr;
            }

            .section-title {
                font-size: 31px;
            }

            .project-image {
                height: 220px;
            }

            .history-card::before {
                left: -37px;
            }
        }
    </style>
</head>

<body>

    <!-- ANIMATED BACKGROUND -->

    <div class="background">
        <div class="orb one"></div>
        <div class="orb two"></div>
        <div class="orb three"></div>
    </div>


    <!-- NAVIGATION -->

    <nav>

        <div class="logo">
            Stary<span>jump</span>
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

        <div class="hero-content">

            <div class="hello">
                Hey, I'm
            </div>

            <h1>
                Staryjump
            </h1>

            <h2>
                Roblox Developer
            </h2>

            <p class="hero-description">
                I enjoy building Roblox experiences, working on
                development projects and learning new things along
                the way.
            </p>

            <div class="buttons">

                <a class="button primary" href="#projects">
                    View my work
                </a>

                <a class="button" href="#contact">
                    Get in touch
                </a>

            </div>

        </div>

    </section>


    <!-- ABOUT -->

    <section id="about">

        <h2 class="section-title">
            About <span>Me</span>
        </h2>

        <div class="about-grid">

            <img
                class="profile-image"
                src="profile.png"
                alt="Staryjump profile picture"
            >

            <div>

                <p class="text">
                    Hey! I'm Staryjump. I'm a Roblox developer who
                    enjoys creating games, building environments and
                    working on different Roblox projects.
                </p>

                <br>

                <p class="text">
                    I mainly work with Roblox Studio and Luau.
                    I'm also learning web development with HTML
                    and JavaScript.
                </p>

                <div class="facts">

                    <div class="fact">
                        🎮 Roblox Developer
                    </div>

                    <div class="fact">
                        💻 Luau
                    </div>

                    <div class="fact">
                        🧱 Building
                    </div>

                    <div class="fact">
                        🌐 Web Development
                    </div>

                </div>

            </div>

        </div>

    </section>


    <!-- SKILLS -->

    <section id="skills">

        <h2 class="section-title">
            My <span>Skills</span>
        </h2>

        <div class="skills">

            <div class="skill">
                <h3>Luau</h3>
                <p>Roblox scripting and game systems.</p>
            </div>

            <div class="skill">
                <h3>Roblox Studio</h3>
                <p>Creating and developing Roblox experiences.</p>
            </div>

            <div class="skill">
                <h3>Building</h3>
                <p>Creating maps, environments and structures.</p>
            </div>

            <div class="skill">
                <h3>Game Development</h3>
                <p>Working on gameplay and Roblox projects.</p>
            </div>

            <div class="skill">
                <h3>HTML</h3>
                <p>Building websites and portfolio pages.</p>
            </div>

            <div class="skill">
                <h3>JavaScript</h3>
                <p>Learning web development and programming.</p>
            </div>

        </div>

    </section>


    <!-- WORK HISTORY -->

    <section id="experience">

        <h2 class="section-title">
            Work <span>History</span>
        </h2>

        <div class="timeline">

            <div class="history-card">

                <h3>
                    Freshly
                </h3>

                <div class="role">
                    Store Management
                </div>

                <div class="date">
                    2026
                </div>

                <p>
                    I gained experience working within a Roblox
                    company environment and helping with store
                    management and company activities.
                </p>

            </div>


            <div class="history-card">

                <h3>
                    Nexo Corporation
                </h3>

                <div class="role">
                    Corporate Intern
                </div>

                <div class="date">
                    2026
                </div>

                <p>
                    I worked as a Corporate Intern and gained
                    experience working with a Roblox corporate
                    team and taking part in company activities.
                </p>

            </div>

        </div>

    </section>


    <!-- PROJECTS -->

    <section id="projects">

        <h2 class="section-title">
            My <span>Projects</span>
        </h2>

        <div class="project">

            <img
                class="project-image"
                src="project1.png"
                alt="Dropper Game"
            >

            <div class="project-content">

                <h3>
                    Dropper Game
                </h3>

                <p>
                    A Roblox Dropper game currently in development.
                    I created the map and environment myself from
                    scratch and I'm continuing to work on the game.
                </p>

                <span class="status">
                    In Development
                </span>

            </div>

        </div>


        <!-- VIDEO -->

        <div class="project">

            <div class="project-content">

                <h3>
                    Project Showcase
                </h3>

                <p>
                    A short video showing some of my work in Roblox.
                </p>

            </div>

            <div class="video-container">

                <video controls preload="metadata">

                    <source
                        src="project1.mp4"
                        type="video/mp4"
                    >

                    Your browser does not support videos.

                </video>

            </div>

        </div>

    </section>


    <!-- CONTACT -->

    <section id="contact">

        <div class="contact-box">

            <h2 class="section-title">
                Let's <span>Connect</span>
            </h2>

            <p class="text">
                Want to talk about a project, development,
                Roblox or just get in touch? You can find
                me through the links below.
            </p>

            <div class="socials">

                <a
                    class="social"
                    href="TON_DISCORD_LINK"
                    target="_blank"
                >
                    💬 Discord
                </a>

                <a
                    class="social"
                    href="TON_GITHUB_LINK"
                    target="_blank"
                >
                    💻 GitHub
                </a>

                <a
                    class="social"
                    href="TON_ROBLOX_LINK"
                    target="_blank"
                >
                    🎮 Roblox
                </a>

            </div>

        </div>

    </section>


    <!-- FOOTER -->

    <footer>

        <p>
            © 2026 Staryjump
        </p>

        <p>
            Roblox Developer
        </p>

    </footer>


    <!-- SCROLL ANIMATIONS -->

    <script>

        const cards = document.querySelectorAll(
            ".skill, .history-card, .project"
        );

        const observer = new IntersectionObserver(
            (entries) => {

                entries.forEach((entry) => {

                    if (entry.isIntersecting) {

                        entry.target.style.opacity = "1";

                        entry.target.style.transform =
                            "translateY(0)";

                    }

                });

            },
            {
                threshold: 0.12
            }
        );


        cards.forEach((card) => {

            card.style.opacity = "0";

            card.style.transform =
                "translateY(25px)";

            card.style.transition =
                "opacity 0.6s ease, transform 0.6s ease";

            observer.observe(card);

        });

    </script>

</body>
</html>           BACKGROUND
        ========================= */ 

        .background {
            position: fixed;
            inset: 0;
            overflow: hidden;
            pointer-events: none;
            z-index: -1;
        } 

        .orb {
            position: absolute;
            width: 350px;
            height: 350px;
            border-radius: 50%;
            background: #6c4cff;
            filter: blur(120px);
            opacity: 0.12;
            animation: float 8s ease-in-out infinite;
        } 

        .orb.one {
            top: 5%;
            left: -150px;
        } 

        .orb.two {
            right: -150px;
            top: 45%;
            background: #00b7ff;
            animation-delay: -3s;
        } 

        .orb.three {
            bottom: -180px;
            left: 35%;
            background: #a855f7;
            animation-delay: -5s;
        } 

        @keyframes float {
            0%, 100% {
                transform: translate(0, 0);
            } 

            50% {
                transform: translate(30px, -40px);
            }
        } 

        /* =========================
           NAVBAR
        ========================= */ 

        nav {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            padding: 18px 6%;
            background: rgba(8, 8, 13, 0.75);
            backdrop-filter: blur(15px);
            border-bottom: 1px solid rgba(255,255,255,0.08);
            display: flex;
            justify-content: space-between;
            align-items: center;
            z-index: 1000;
        } 

        .logo {
            font-size: 22px;
            font-weight: 800;
        } 

        .logo span {
            color: #8b6cff;
        } 

        .links {
            display: flex;
            gap: 25px;
        } 

        .links a {
            color: #999;
            text-decoration: none;
            transition: 0.25s;
        } 

        .links a:hover {
            color: white;
        } 

        /* =========================
           GENERAL
        ========================= */ 

        section {
            width: 100%;
            max-width: 1050px;
            margin: auto;
            padding: 110px 25px;
        } 

        .section-title {
            font-size: 38px;
            margin-bottom: 35px;
        } 

        .section-title span {
            color: #8b6cff;
        } 

        .text {
            color: #a5a5b0;
            font-size: 17px;
            max-width: 760px;
        } 

        /* =========================
           HERO
        ========================= */ 

        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
        } 

        .hero-content {
            animation: heroAppear 1s ease forwards;
        } 

        @keyframes heroAppear {
            from {
                opacity: 0;
                transform: translateY(30px);
            } 

            to {
                opacity: 1;
                transform: translateY(0);
            }
        } 

        .hello {
            color: #8b6cff;
            font-size: 18px;
            font-weight: bold;
            margin-bottom: 10px;
        } 

        .hero h1 {
            font-size: clamp(55px, 11vw, 100px);
            line-height: 0.95;
            letter-spacing: -4px;
            margin-bottom: 20px;
        } 

        .hero h2 {
            color: #aaa;
            font-size: 25px;
            font-weight: normal;
        } 

        .hero-description {
            color: #858591;
            max-width: 650px;
            margin-top: 20px;
            font-size: 17px;
        } 

        .buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin-top: 30px;
        } 

        .button {
            display: inline-block;
            padding: 12px 22px;
            border-radius: 9px;
            text-decoration: none;
            color: white;
            border: 1px solid #33333e;
            transition: 0.25s;
        } 

        .button.primary {
            background: #7657ff;
            border-color: #7657ff;
        } 

        .button:hover {
            transform: translateY(-3px);
            border-color: #8b6cff;
            box-shadow: 0 10px 30px rgba(118, 87, 255, 0.1

