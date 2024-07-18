<!DOCTYPE html>
<html lang="en">
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
    body {
        background-color: #fcf6f6;
        margin: 0;
        font-family: Arial, Helvetica, sans-serif;
        position: relative;
        overflow-x: hidden;
    }

    .topnav {
        height: 50px;
        overflow: hidden;
        background: linear-gradient(90deg, rgba(223, 219, 219, 1) 0%, rgba(200, 200, 200, 1) 100%);
        margin: 5px;
        display: flex;
        align-items: center;
        box-shadow: 2px 2px 30px rgba(0, 0, 0, 0.2);
        justify-content: space-between;
        border-radius: 10px;
        transition: all 0.3s ease-in-out;
        position: relative;
    }

    #logo {
        margin-left: 20px;
        display: flex;
        align-items: center;
    }

    #logo img {
        width: 40px;
        height: 40px;
        transition: transform 0.3s ease-in-out;
    }

    #logo img:hover {
        transform: rotate(360deg);
    }

    #logo-text {
        color: #000000;
        margin-left: 10px;
        font-size: 24px;
        font-weight: bold;
        transition: color 0.3s ease-in-out;
    }

    .navtags {
        display: flex;
        flex-grow: 1;
        justify-content: flex-start;
        margin-left: 19%;
        position: relative;
    }

    .navtags a {
        color: #000000;
        text-align: center;
        padding: 14px 16px;
        text-decoration: none;
        font-size: 17px;
        margin: 0 10px;
        position: relative;
        overflow: hidden;
        transition: color 0.3s ease-in-out;
    }

    .navtags a:before {
        content: '';
        position: absolute;
        width: 100%;
        height: 0;
        bottom: 0;
        left: 0;
        background-color: rgba(0, 0, 0, 0.2);
        z-index: -1;
        transition: height 0.3s ease-in-out;
    }

    .navtags a:hover:before {
        height: 100%;
    }

    .navtags a:hover {
        color: #ffffff;
    }

    #I {
        color: cadetblue;
    }

    #nno {
        color: darkolivegreen;
    }

    #vex {
        color: rgb(130, 59, 59);
    }

    #Hub {
        color: goldenrod;
    }

    .picture {
        position: fixed;
        top: 50%;
        right: 5%;
        transform: translateY(-50%);
        z-index: 10;
    }

    .picture img {
        width: 100%; /* Adjust to fill the available width */
        max-width: 300px; /* Limit maximum width */
        height: auto;
        box-shadow: 2px 2px 20px rgba(0, 0, 0, 0.3);
        border-radius: 10px;
        transition: transform 0.5s ease-in-out;
    }

    .picture img:hover {
        transform: scale(1.05); /* Scale up slightly on hover */
    }

    .background-image {
        margin-top: 45px;
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 200vh;
        background-color: #000000;
        background-size: cover;
        background-position: center;
        z-index: 1;
        opacity: 0;
        transition: opacity 1s ease-in-out;
    }

    body.scrolled .background-image {
        opacity: 1;
    }

    #h {
        font-size: larger;
        margin-left: 20px;
        margin-top: 80px;
        z-index: 2;
        position: absolute;
        bottom: 10px;
        left: 10px;
        color: #ffffff;
        text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        transform: translateY(100%);
        transition: transform 0.5s ease-in-out;
    }

    #h.show {
        transform: translateY(0);
    }

    #p {
        z-index: 2;
        position: relative;
        max-width: 600px;
        margin-top: 50px;
        margin-left: 200px;
        padding: 20px;
        background-color: #f0f0f0;
        border-radius: 10px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        font-family: Arial, sans-serif;
        line-height: 1.6;
    }

    .topnav .icon {
        display: none;
    }

    @media screen and (max-width: 768px) {
        .navtags {
            display: none;
            flex-direction: column;
            justify-content: flex-start;
            margin-left: 0;
        }

        .topnav.responsive .navtags {
            display: flex;
            position: absolute;
            top: 50px;
            left: 0;
            width: 100%;
            background-color: #dfdbdb;
            z-index: 2;
        }

        .navtags a {
            padding: 14px;
            width: 100%;
            text-align: left;
        }

        .topnav .icon {
            display: block;
            cursor: pointer;
            padding: 14px;
        }

        #h {
            margin-left: 20px;
            margin-top: 80px;
            text-align: center;
            font-size: 24px;
            position: relative;
            bottom: auto;
            left: auto;
            transform: translateY(0);
            color: #000000;
            text-shadow: none;
            transition: none;
        }

        #p {
            margin-top: 20px;
            margin-left: 20px;
            text-align: center;
            padding: 10px;
        }

        .background-image {
            background-image: url('./images/phone-background.jpg'); /* Replace with actual phone background image */
            height: 100vh; /* Adjust height for smaller screens */
            position: relative; /* Adjust position */
        }
    }

    @media screen and (max-width: 480px) {
        #logo-text {
            font-size: 16px;
        }

        #h {
            margin-left: 10px;
            margin-top: 60px;
            font-size: 20px;
        }

        #p {
            margin-left: 10px;
            padding: 10px;
        }

        .picture img {
            width: 200px; /* Adjust size for smaller screens */
            max-width: 100%; /* Ensure it doesn't exceed screen width */
        }

        .background-image {
            background-image: url('./images/phone-background.jpg'); /* Replace with actual phone background image */
            height: 100vh; /* Adjust height for smaller screens */
            position: relative; /* Adjust position */
        }
    }
</style>
</head>
<body>
<div class="topnav" id="myTopnav">
    <div id="logo">
        <img src="./images/innovex.png" alt="Logo">
        <div id="logo-text"><span id="I">I</span><span id="nno">nno</span><span id="vex">vex</span><span id="Hub">Hub</span></div>
    </div>
    <div class="navtags" id="navtags">
        <a class="active" href="#">Home</a>
        <a href="#">About Us</a>
        <a href="#">Our Approach</a>
        <a href="#">Join Us</a>
    </div>
    <a href="javascript:void(0);" class="icon" onclick="toggleMenu()">
        &#9776;
    </a>
</div>

<div class="picture">
    <img src="./images/innovex.png" alt="Front Image">
</div>

<div class="background-image"></div>

<div id="h" class="show">
    <h1>Hello!</h1>
    <h1>Innovation starts here</h1>
</div>

<div id="p">
    <p>Welcome to Innovex Hub! <br> We're dedicated to investing in and nurturing groundbreaking startup ideas. Our mission is to support visionary entrepreneurs with the resources, mentorship, and funding they need to succeed. <br> As we embark on launching new ideas, we're actively seeking skilled programmers and full-stack app developers to join us in driving innovation and building a brighter future together.</p>
</div>

<script>
function toggleMenu() {
    var x = document.getElementById("myTopnav");
    if (x.className === "topnav") {
        x.className += " responsive";
    } else {
        x.className = "topnav";
    }
}
document.addEventListener('scroll', () =>
