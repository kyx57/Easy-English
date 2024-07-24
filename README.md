<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="ee.css">
    <title>Home</title>
</head>
<body>
        <header>
            <a href="#" class="logo">Easy English</a>
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
