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

