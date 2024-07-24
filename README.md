<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="ee.css">
    <title>Home</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
}
body {
    min-height: 100vh;
    overflow-x: hidden;
    background: linear-gradient(#2b1055, #7597de);
}
header {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    padding: 30px 100px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
header .logo {
    color: #fff;
    font-weight: 700;
    text-decoration: none;
    font-size: 2em;
    text-transform: uppercase;
    letter-spacing: 2px;
}
header ul {
    display: flex;
    justify-content: center;
    align-items: center;
}
header ul li {
    list-style: none;
    margin-left: 20px;
}
header ul li a {
    text-decoration: none;
    padding: 6px 35px;
    color: #fff;
    border-radius: 30px;
    z-index: 1000;
}
header ul li a:hover,
header ul li a.active {
    background: #fff;
    color: #2b1055;
}
section {
    position: relative;
    width: 100%;
    height: 100vh;
    padding: 100px;
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
}
section::before {
    content: '';
    position: absolute;
    bottom: 0;
    width: 100%;
    height: 100px;
    background: linear-gradient(to top, #1c0522, transparent);
    z-index: 1000;
}
section img {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    pointer-events: none;
}
section img#moon {
    mix-blend-mode: screen;
}
section img#mountains_front {
    z-index: 10;
}
#text {
    position: absolute;
    right: -350px;
    color: #fff;
    white-space: nowrap;
    font-size: 7.5vw;
    z-index: 9;
}
#btn {
    text-decoration: none;
    display: inline-block;
    padding: 8px 30px;
    border-radius: 40px;
    background: #fff;
    color: #2b1055;
    font-size: 1.5em;
    z-index: 9;
    transform: translateY(100px);
}
.sec {
    position: relative;
    padding: 100px;
    background: #1c0522;
}
.sec h2 {
    font-size: 3.5em;
    margin-bottom: 10px;
    color: #fff;
}
.sec p {
    font-size: 1em;
    color: #fff;
}
.ces {
    position: relative;
    padding: 100px;
    background: #1c0522;
    height: 70vh;
    display: flex;
}
.ces h5 {
    font-size: 2.5em;
    margin-bottom: 10px;
    color: #fff;
    align-items: center;
    justify-content: center;
}
.ces p {
    font-size: 1.5em;
    color: #fff;
}
.module_right {
    width: 50%;
    height: 50vh;
    border-radius: 20px;
    background: gray;
    opacity: 30%;
    align-items: center;
    justify-content: center;
    display: flex;
}
.module_left {
    width: 50%;
    height: 50vh;
    align-items: center;
    justify-content: center;
    overflow: hidden;
}
#sign_up {
    margin-top: -40px;
    position: absolute;
    text-decoration: none;
    display: inline-block;
    padding: 8px 30px;
    border-radius: 40px;
    background: #fff;
    color: #2b1055;
    font-size: 1.5em;
    z-index: 9;
    transform: translateY(100px);
}

    </style>
</head>
<body>
        <header>
            <a href="#" class="logo"></a>
            <ul>
                <li><a href="#" class="active">Home</a></li>
                <li><a href="about.html">About</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </header>
        <section>
            <img src="stars.png" id="stars">
            <img src="moon.png" id="moon">
            <img src="mountains_behind.png" id="mountains_behind">
            <h2 id="text"></h2>
            <a href="#" id="btn">Login</a>
            <img src="mountains_front.png" id="mountains_front">
        </section>
        <div class="sec">
            <h2>Easy English</h2>
            <p>Today, the english language is a global language that guarantees a stepping stone for one's success. Easy English consists of 2 teachers aiming to teach English to children who seek to walk side by side with the world. Enroll your child to our online class and ensure their prosperous future</p>
        </div>
    <script>
            let stars = document.getElementById('stars');
            let moon = document.getElementById('moon');
            let mountains_front = document.getElementById('mountains_front');
            let mountains_behind = document.getElementById('mountains_behind');
            let text = document.getElementById('text');
            let btn = document.getElementById('btn');
            let header = document.querySelector('header');
            window.addEventListener('scroll', function(){
                let value = window.scrollY;
                stars.style.left = value * 0.25 + 'px';
                moon.style.top = value * 1.05 + 'px';
                mountains_front.style.top = value * 0 + 'px';
                mountains_behind.style.top = value * 0.5 + 'px';
                text.style.marginRight = value * 4 + 'px';
                text.style.marginTop = value * 1.5 + 'px';
                btn.style.marginTop = value * 1.5 + 'px';
                header.style.top = value * 0.5 + 'px';
            })
        </script>
</body>
</html>
