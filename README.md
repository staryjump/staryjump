<!DOCTYPE html>
<html lang="en">

<head>

    <meta charset="UTF-8">

    <meta
        name="viewport"
        content="width=device-width, initial-scale=1.0"
    >

    <title>Staryjump | Portfolio</title>

    <style>

        /* =========================
           RESET
        ========================= */

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        html,
        body {
            width: 100%;
            overflow-x: hidden;
        }

        body {
            font-family: Arial, Helvetica, sans-serif;
            background: #09090f;
            color: #ffffff;
            line-height: 1.6;
        }


        /* =========================
           BACKGROUND
        ========================= */

        .background {
            position: fixed;
            inset: 0;
            overflow: hidden;
            pointer-events: none;
            z-index: -1;
        }

        .blob {
            position: absolute;
            width: 350px;
            height: 350px;
            border-radius: 50%;
            filter: blur(130px);
            opacity: 0.13;
            animation: floating 12s ease-in-out infinite;
        }

        .blob.one {
            background: #7c5cff;
            top: -140px;
            left: -120px;
        }

        .blob.two {
            background: #00b7ff;
            right: -140px;
            top: 40%;
            animation-delay: -4s;
        }

        .blob.three {
            background: #ff4fd8;
            bottom: -170px;
            left: 35%;
            animation-delay: -8s;
        }

        @keyframes floating {

            0%,
            100% {
                transform: translate(0, 0) scale(1);
            }

            50% {
                transform: translate(35px, -40px) scale(1.08);
            }
        }


        /* =========================
           NAVIGATION
        ========================= */

        nav {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;

            padding: 18px 6%;

            display: flex;
            justify-content: space-between;
            align-items: center;

            background: rgba(9, 9, 15, 0.72);
            backdrop-filter: blur(18px);

            border-bottom: 1px solid rgba(255, 255, 255, 0.07);

            z-index: 1000;

            transition: 0.3s;
        }

        nav.scrolled {
            padding-top: 13px;
            padding-bottom: 13px;
            background: rgba(9, 9, 15, 0.9);
        }

        .logo {
            color: white;
            font-size: 22px;
            font-weight: 800;
        }

        .logo span {
            color: #8b6cff;
        }

        .nav-links {
            display: flex;
            gap: 25px;
        }

        .nav-links a {
            position: relative;

            color: #92929d;
            text-decoration: none;

            transition: 0.25s;
        }

        .nav-links a::after {
            content: "";

            position: absolute;

            left: 0;
            bottom: -6px;

            width: 0;
            height: 2px;

            background: #8b6cff;

            transition: 0.25s;
        }

        .nav-links a:hover {
            color: white;
        }

        .nav-links a:hover::after {
            width: 100%;
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
            max-width: 760px;
            color: #a4a4af;
            font-size: 17px;
        }


        /* =========================
           HERO
        ========================= */

        .hero {
            min-height: 100vh;

            display: flex;
            align-items: center;

            position: relative;
        }

        .hero-content {
            animation: heroAppear 1s ease forwards;
        }

        @keyframes heroAppear {

            from {
                opacity: 0;
                transform: translateY(35px);
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
            margin-bottom: 8px;
        }

        .hero h1 {
            max-width: 100%;

            font-size: clamp(55px, 11vw, 100px);
            line-height: 0.95;

            letter-spacing: -4px;

            margin-bottom: 20px;

            background: linear-gradient(
                90deg,
                #ffffff,
                #b9adff,
                #ffffff
            );

            background-size: 200% auto;

            -webkit-background-clip: text;
            background-clip: text;

            color: transparent;

            animation: titleGlow 5s linear infinite;
        }

        @keyframes titleGlow {

            0% {
                background-position: 0% center;
            }

            100% {
                background-position: 200% center;
            }
        }

        .hero h2 {
            color: #aaaab5;
            font-size: 25px;
            font-weight: normal;
        }

        .hero-text {
            max-width: 650px;

            margin-top: 20px;

            color: #858591;
            font-size: 17px;
        }

        .hero-buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;

            margin-top: 30px;
        }

        .button {
            display: inline-flex;
            align-items: center;
            gap: 8px;

            padding: 12px 21px;

            color: white;
            text-decoration: none;

            border: 1px solid #33333e;
            border-radius: 9px;

            transition:
                transform 0.3s,
                border-color 0.3s,
                box-shadow 0.3s;
        }

        .button.primary {
            background: #7657ff;
            border-color: #7657ff;
        }

        .button:hover {
            transform: translateY(-5px);

            border-color: #8b6cff;

            box-shadow:
                0 12px 35px rgba(118, 87, 255, 0.25);
        }

        .scroll-hint {
            position: absolute;

            bottom: 30px;
            left: 50%;

            transform: translateX(-50%);

            color: #666673;

            font-size: 13px;

            animation: scrollBounce 2s ease-in-out infinite;
        }

        @keyframes scrollBounce {

            0%,
            100% {
                transform: translate(-50%, 0);
            }

            50% {
                transform: translate(-50%, 8px);
            }
        }


        /* =========================
           ABOUT
        ========================= */

        .about-grid {
            display: grid;

            grid-template-columns: 260px 1fr;

            gap: 45px;

            align-items: center;
        }

        .profile {
            width: 260px;
            height: 260px;

            object-fit: cover;

            border-radius: 25px;

            background: #12121a;

            border: 1px solid #292936;

            transition:
                transform 0.4s,
                border-color 0.4s,
                box-shadow 0.4s;
        }

        .profile:hover {
            transform: rotate(-2deg) scale(1.04);

            border-color: #7657ff;

            box-shadow:
                0 20px 50px rgba(118, 87, 255, 0.18);
        }

        .facts {
            display: flex;
            flex-wrap: wrap;

            gap: 10px;

            margin-top: 25px;
        }

        .fact {
            padding: 8px 13px;

            color: #aaa;

            background: #111118;

            border: 1px solid #252530;

            border-radius: 8px;

            transition: 0.25s;
        }

        .fact:hover {
            color: white;

            border-color: #7657ff;

            transform: translateY(-3px);
        }


        /* =========================
           SKILLS
        ========================= */

        .skills {
            display: grid;

            grid-template-columns: repeat(2, 1fr);

            gap: 15px;
        }

        .skill {
            position: relative;

            padding: 24px;

            background: rgba(17, 17, 24, 0.85);

            border: 1px solid #252530;

            border-radius: 15px;

            overflow: hidden;

            transition:
                transform 0.3s,
                border-color 0.3s,
                box-shadow 0.3s;
        }

        .skill::before {
            content: "";

            position: absolute;

            top: 0;
            left: 0;

            width: 100%;
            height: 2px;

            background: linear-gradient(
                90deg,
                transparent,
                #7657ff,
                transparent
            );

            transform: translateX(-100%);

            transition: 0.5s;
        }

        .skill:hover {
            transform: translateY(-6px);

            border-color: #7657ff;

            box-shadow:
                0 14px 35px rgba(118, 87, 255, 0.12);
        }

        .skill:hover::before {
            transform: translateX(100%);
        }

        .skill-top {
            display: flex;

            align-items: center;

            gap: 12px;

            margin-bottom: 8px;
        }

        .skill-icon {
            width: 40px;
            height: 40px;

            display: flex;

            align-items: center;
            justify-content: center;

            border-radius: 10px;

            background: #1a1925;

            border: 1px solid #302d47;

            font-size: 19px;
        }

        .skill h3 {
            font-size: 19px;
        }

        .skill p {
            color: #777783;

            font-size: 14px;
        }


        /* =========================
           WORK HISTORY
        ========================= */

        .work-list {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .work-card {
            display: grid;

            grid-template-columns: 280px 1fr;

            min-height: 280px;

            overflow: hidden;

            background: #111118;

            border: 1px solid #252530;

            border-radius: 18px;

            transition:
                transform 0.35s,
                border-color 0.35s,
                box-shadow 0.35s;
        }

        .work-card:hover {
            transform: translateY(-7px);

            border-color: #7657ff;

            box-shadow:
                0 20px 45px rgba(0, 0, 0, 0.3);
        }

        .work-image-wrapper {
            width: 280px;
            height: 280px;

            overflow: hidden;

            background: #181820;
        }

        .work-image {
            width: 280px;
            height: 280px;

            object-fit: cover;

            display: block;

            transition: transform 0.5s ease;
        }

        .work-card:hover .work-image {
            transform: scale(1.07);
        }

        .work-content {
            padding: 28px;

            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        .work-company {
            font-size: 25px;

            margin-bottom: 3px;
        }

        .work-role {
            color: #8b6cff;

            font-weight: bold;

            margin-bottom: 3px;
        }

        .work-date {
            color: #666673;

            font-size: 14px;

            margin-bottom: 18px;
        }

        .work-content p {
            color: #9999a5;
        }


        /* =========================
           PROJECTS
        ========================= */

        .project-card {
            overflow: hidden;

            background: #111118;

            border: 1px solid #252530;

            border-radius: 18px;

            transition:
                transform 0.35s,
                border-color 0.35s,
                box-shadow 0.35s;
        }

        .project-card:hover {
            transform: translateY(-7px);

            border-color: #7657ff;

            box-shadow:
                0 20px 45px rgba(0, 0, 0, 0.3);
        }

        .project-image-wrapper {
            width: 100%;
            height: 360px;

            overflow: hidden;

            background: #171720;
        }

        .project-image {
            width: 100%;
            height: 360px;

            object-fit: cover;

            display: block;

            transition: transform 0.5s ease;
        }

        .project-card:hover .project-image {
            transform: scale(1.04);
        }

        .project-content {
            padding: 27px;
        }

        .project-content h3 {
            font-size: 25px;

            margin-bottom: 8px;
        }

        .project-content p {
            color: #9999a5;
        }

        .status {
            display: inline-block;

            margin-top: 16px;

            padding: 6px 11px;

            color: #9c8cff;

            background: #1a1925;

            border-radius: 7px;

            font-size: 13px;
        }


        /* =========================
           CONTACT
        ========================= */

        .contact-box {
            padding: 55px 25px;

            text-align: center;

            background: rgba(17, 17, 24, 0.85);

            border: 1px solid #252530;

            border-radius: 20px;

            transition: 0.35s;
        }

        .contact-box:hover {
            border-color: #343344;
        }

        .contact-box .text {
            margin: auto;
        }


        /* =========================
           SOCIAL BUTTONS
        ========================= */

        .socials {
            display: flex;

            justify-content: center;

            flex-wrap: wrap;

            gap: 12px;

            margin-top: 35px;
        }

        .social {
            display: inline-flex;

            align-items: center;

            gap: 10px;

            padding: 13px 20px;

            color: white;

            text-decoration: none;

            background: #111118;

            border: 1px solid #30303b;

            border-radius: 10px;

            transition:
                transform 0.25s,
                border-color 0.25s,
                background 0.25s,
                box-shadow 0.25s;
        }

        .social svg {
            width: 20px;
            height: 20px;

            fill: currentColor;
        }

        .social:hover {
            transform: translateY(-5px);

            border-color: #7657ff;

            background: #171522;

            box-shadow:
                0 10px 30px rgba(118, 87, 255, 0.12);
        }


        /* =========================
           FOOTER
        ========================= */

        footer {
            width: 100%;

            padding: 45px 20px;

            text-align: center;

            color: #666673;

            border-top: 1px solid #202027;
        }


        /* =========================
           SCROLL ANIMATION
        ========================= */

        .animate {
            opacity: 0;

            transform: translateY(35px);

            transition:
                opacity 0.8s ease,
                transform 0.8s ease;
        }

        .animate.show {
            opacity: 1;

            transform: translateY(0);
        }


        /* =========================
           MOBILE
        ========================= */

        @media (max-width: 750px) {

            nav {
                padding: 15px 20px;
            }

            .nav-links {
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

            .scroll-hint {
                display: none;
            }

            .about-grid {
                grid-template-columns: 1fr;

                gap: 30px;
            }

            .profile {
                width: 210px;
                height: 210px;
            }

            .section-title {
                font-size: 31px;
            }

            .skills {
                grid-template-columns: 1fr;
            }

            .work-card {
                grid-template-columns: 1fr;

                min-height: 0;
            }

            .work-image-wrapper {
                width: 100%;
                height: auto;

                aspect-ratio: 1 / 1;
            }

            .work-image {
                width: 100%;
                height: 100%;
            }

            .work-content {
                padding: 25px;
            }

            .project-image-wrapper {
                height: 230px;
            }

            .project-image {
                height: 230px;
            }

            .social {
                width: 100%;

                justify-content: center;
            }

        }

    </style>

</head>


<body>


    <!-- =========================
         BACKGROUND
    ========================= -->

    <div class="background">

        <div class="blob one"></div>
        <div class="blob two"></div>
        <div class="blob three"></div>

    </div>


    <!-- =========================
         NAVIGATION
    ========================= -->

    <nav id="navbar">

        <div class="logo">
            Stary<span>jump</span>
        </div>

        <div class="nav-links">

            <a href="#about">
                About
            </a>

            <a href="#skills">
                Skills
            </a>

            <a href="#experience">
                Experience
            </a>

            <a href="#projects">
                Projects
            </a>

            <a href="#contact">
                Contact
            </a>

        </div>

    </nav>


    <!-- =========================
         HOME
    ========================= -->

    <section class="hero">

        <div class="hero-content">

            <div class="hello">
                Hey, I'm
            </div>

            <h1>
                Staryjump
            </h1>

            <h2>
                Welcome to my portfolio
            </h2>

            <p class="hero-text">
                I enjoy creating things, working on projects and
                learning new skills. This is where I keep some of
                the things I've worked on.
            </p>

            <div class="hero-buttons">

                <a
                    class="button primary"
                    href="#projects"
                >
                    See my work
                </a>

                <a
                    class="button"
                    href="#contact"
                >
                    Find me online
                </a>

            </div>

        </div>

        <div class="scroll-hint">
            ↓ Scroll
        </div>

    </section>


    <!-- =========================
         ABOUT
    ========================= -->

    <section id="about" class="animate">

        <h2 class="section-title">
            About <span>Me</span>
        </h2>

        <div class="about-grid">

            <img
                class="profile"
                src="profile.png"
                alt="Staryjump"
            >

            <div>

                <p class="text">
                    Hey! I'm Staryjump. I like working on projects
                    and creating things on Roblox. I also enjoy
                    learning more about programming and web
                    development.
                </p>

                <br>

                <p class="text">
                    Outside of projects, I like playing games,
                    working on ideas and improving the things
                    I create.
                </p>

                <div class="facts">

                    <div class="fact">
                        🎮 Roblox
                    </div>

                    <div class="fact">
                        💻 Luau
                    </div>

                    <div class="fact">
                        🧱 Building
                    </div>

                    <div class="fact">
                        🌐 HTML
                    </div>

                </div>

            </div>

        </div>

    </section>


    <!-- =========================
         SKILLS
    ========================= -->

    <section id="skills" class="animate">

        <h2 class="section-title">
            My <span>Skills</span>
        </h2>

        <div class="skills">


            <!-- LUAU -->

            <div class="skill">

                <div class="skill-top">

                    <div class="skill-icon">
                        💻
                    </div>

                    <h3>
                        Luau
                    </h3>

                </div>

                <p>
                    Roblox scripting.
                </p>

            </div>


            <!-- BUILDING -->

            <div class="skill">

                <div class="skill-top">

                    <div class="skill-icon">
                        🧱
                    </div>

                    <h3>
                        Building
                    </h3>

                </div>

                <p>
                    Maps and environments.
                </p>

            </div>


            <!-- HTML / CSS -->

            <div class="skill">

                <div class="skill-top">

                    <div class="skill-icon">
                        🌐
                    </div>

                    <h3>
                        HTML / CSS
                    </h3>

                </div>

                <p>
                    Web design.
                </p>

            </div>


            <!-- JAVASCRIPT -->

            <div class="skill">

                <div class="skill-top">

                    <div class="skill-icon">
                        ⚡
                    </div>

                    <h3>
                        JavaScript
                    </h3>

                </div>

                <p>
                    Web development.
                </p>

            </div>


        </div>

    </section>


    <!-- =========================
         WORK HISTORY
    ========================= -->

    <section id="experience" class="animate">

        <h2 class="section-title">
            Work <span>History</span>
        </h2>

        <div class="work-list">


            <!-- =========================
                 FRESHLY
            ========================= -->

            <div class="work-card">

                <div class="work-image-wrapper">

                    <img
                        class="work-image"
                        src="freshly.png"
                        alt="Freshly"
                    >

                </div>

                <div class="work-content">

                    <h3 class="work-company">
                        Freshly
                    </h3>

                    <div class="work-role">
                        Store Management
                    </div>

                    <div class="work-date">
                        2026
                    </div>

                    <p>
                        Experience in store management within
                        the Roblox environment.
                    </p>

                </div>

            </div>


            <!-- =========================
                 NEXO CORPORATION
            ========================= -->

            <div class="work-card">

                <div class="work-image-wrapper">

                    <img
                        class="work-image"
                        src="nexo.png"
                        alt="Nexo Corporation"
                    >

                </div>

                <div class="work-content">

                    <h3 class="work-company">
                        Nexo Corporation
                    </h3>

                    <div class="work-role">
                        Corporate Intern
                    </div>

                    <div class="work-date">
                        2026
                    </div>

                    <p>
                        Experience as a Corporate Intern within
                        a Roblox corporate environment.
                    </p>

                </div>

            </div>

                  <!-- =========================
     EXPERIENCE 3
========================= -->

<div class="work-card">

    <div class="work-image-wrapper">

        <img
            class="work-image"
            src="experience3.png"
            alt="Company Name"
        >

    </div>

    <div class="work-content">

        <h3 class="work-company">
            Company Name
        </h3>

        <div class="work-role">
            Your Role
        </div>

        <div class="work-date">
            2026
        </div>

        <p>
            Write your experience description here.
        </p>

    </div>

</div>


<!-- =========================
     EXPERIENCE 4
========================= -->

<div class="work-card">

    <div class="work-image-wrapper">

        <img
            class="work-image"
            src="experience4.png"
            alt="Company Name"
        >

    </div>

    <div class="work-content">

        <h3 class="work-company">
            Company Name
        </h3>

        <div class="work-role">
            Your Role
        </div>

        <div class="work-date">
            2026
        </div>

        <p>
            Write your experience description here.
        </p>

    </div>

</div>


<!-- =========================
     EXPERIENCE 5
========================= -->

<div class="work-card">

    <div class="work-image-wrapper">

        <img
            class="work-image"
            src="experience5.png"
            alt="Company Name"
        >

    </div>

    <div class="work-content">

        <h3 class="work-company">
            Company Name
        </h3>

        <div class="work-role">
            Your Role
        </div>

        <div class="work-date">
            2026
        </div>

        <p>
            Write your experience description here.
        </p>

    </div>

</div> 
  

            <!-- =========================
                 ADD MORE EXPERIENCES HERE
                 
                 Copy a complete .work-card
                 and change:

                 1. image
                 2. company name
                 3. role
                 4. date
                 5. description

                 ========================= -->


        </div>

    </section>


    <!-- =========================
         PROJECTS
    ========================= -->

    <section id="projects" class="animate">

        <h2 class="section-title">
            My <span>Projects</span>
        </h2>

        <div class="project-card">

            <div class="project-image-wrapper">

                <img
                    class="project-image"
                    src="project1.png"
                    alt="Dropper Game"
                >

            </div>

            <div class="project-content">

                <h3>
                    Dropper Game
                </h3>

                <p>
                   A Roblox Dropper project created to test gameplay ideas, map design and different mechanics.
                </p>

                <span class="status">
                    Test Project
                </span>

            </div>

        </div>

    </section>


    <!-- =========================
         CONTACT
    ========================= -->

    <section id="contact" class="animate">

        <div class="contact-box">

            <h2 class="section-title">
                Find me <span>online</span>
            </h2>

            <p class="text">
                You can find me on the platforms below.
            </p>

            <div class="socials">


                <!-- DISCORD -->

                <a
                    class="social"
                    href="https://discord.com/users/1088893328994619504"
                    target="_blank"
                    rel="noopener noreferrer"
                >

                    <svg
                        viewBox="0 0 24 24"
                        aria-hidden="true"
                    >

                        <path d="M19.54 5.32A16.9 16.9 0 0 0 15.8 4.15l-.47.96a15.1 15.1 0 0 0-6.66 0l-.47-.96a16.9 16.9 0 0 0-3.74 1.17C2.1 8.84 1.46 12.25 1.78 15.62a16.9 16.9 0 0 0 5.15 2.6l1.25-1.68c-.69-.26-1.35-.59-1.97-.98l.48-.37c3.8 1.77 7.92 1.77 11.67 0l.48.37c-.62.39-1.28.72-1.97.98l1.25 1.68a16.9 16.9 0 0 0 5.15-2.6c.38-3.91-.65-7.28-3.73-10.3ZM8.68 14.08c-1.14 0-2.08-1.04-2.08-2.32s.92-2.32 2.08-2.32 2.1 1.04 2.08 2.32c0 1.28-.92 2.32-2.08 2.32Zm6.64 0c-1.14 0-2.08-1.04-2.08-2.32s.92-2.32 2.08-2.32 2.1 1.04 2.08 2.32c0 1.28-.92 2.32-2.08 2.32Z"/>

                    </svg>

                    Discord

                </a>


                <!-- GITHUB -->

                <a
                    class="social"
                    href="TON_GITHUB_LINK"
                    target="_blank"
                    rel="noopener noreferrer"
                >

                    <svg
                        viewBox="0 0 24 24"
                        aria-hidden="true"
                    >

                        <path d="M12 .5a12 12 0 0 0-3.79 23.39c.6.11.82-.26.82-.58v-2.03c-3.34.73-4.04-1.42-4.04-1.42-.55-1.39-1.34-1.76-1.34-1.76-1.09-.75.08-.74.08-.74 1.2.09 1.83 1.23 1.83 1.23 1.07 1.83 2.8 1.3 3.48.99.11-.77.42-1.3.76-1.6-2.67-.3-5.47-1.34-5.47-5.95 0-1.31.47-2.38 1.23-3.22-.12-.3-.53-1.52.12-3.17 0 0 1-.32 3.3 1.23a11.5 11.5 0 0 1 6 0c2.3-1.55 3.3-1.23 3.3-1.23.65 1.65.24 2.87.12 3.17.76.84 1.23 1.91 1.23 3.22 0 4.62-2.81 5.64-5.49 5.94.43.37.81 1.1.81 2.22v3.29c0 .32.22.69.83.57A12 12 0 0 0 12 .5Z"/>

                    </svg>

                    GitHub

                </a>


                <!-- ROBLOX -->

                <a
                    class="social"
                    href="https://www.roblox.com/share?code=dda92c69ae24364fa71dc8949b1fbd41&type=Profile&source=ProfileShare&stamp=1787535416100"
                    target="_blank"
                    rel="noopener noreferrer"
                >

                    <svg
                        viewBox="0 0 24 24"
                        aria-hidden="true"
                    >

                        <path d="m5.4 3.2 15.4 4.1-4.2 15.4-15.4-4.2L5.4 3.2Zm3.7 7.2-1.1 4 4 1.1 1.1-4-4-1.1Z"/>

                    </svg>

                    Roblox

                </a>


            </div>

        </div>

    </section>


    <!-- =========================
         FOOTER
    ========================= -->

    <footer>

        <p>
            © 2026 Staryjump
        </p>

    </footer>


    <!-- =========================
         JAVASCRIPT
    ========================= -->

    <script>

        /* =========================
           SCROLL REVEAL
        ========================= */

        const elements =
            document.querySelectorAll(".animate");

        const observer =
            new IntersectionObserver(
                (entries) => {

                    entries.forEach((entry) => {

                        if (entry.isIntersecting) {

                            entry.target.classList.add("show");

                            observer.unobserve(entry.target);

                        }

                    });

                },
                {
                    threshold: 0.12
                }
            );


        elements.forEach((element) => {

            observer.observe(element);

        });


        /* =========================
           NAVBAR ON SCROLL
        ========================= */

        const navbar =
            document.getElementById("navbar");

        window.addEventListener("scroll", () => {

            if (window.scrollY > 40) {

                navbar.classList.add("scrolled");

            } else {

                navbar.classList.remove("scrolled");

            }

        });

    </script>


</body>

</html>
