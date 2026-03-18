# Reddy
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Love Promises 💖</title>
<style>
    body {
        margin: 0;
        font-family: 'Poppins', sans-serif;
        background: radial-gradient(circle at top, #0f2027, #203a43, #2c5364);
        color: white;
        overflow: hidden;
    }

    .stars {
        position: fixed;
        width: 100%;
        height: 100%;
        background: url('https://www.transparenttextures.com/patterns/stardust.png');
        animation: moveStars 50s linear infinite;
    }

    @keyframes moveStars {
        from {background-position: 0 0;}
        to {background-position: 10000px 5000px;}
    }

    .container {
        text-align: center;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }

    h1 {
        font-size: 2.5em;
        color: #ff4b5c;
    }

    #typing {
        font-size: 1.5em;
        margin-top: 10px;
        color: #fff;
    }

    button {
        margin-top: 20px;
        padding: 10px 20px;
        border: none;
        background: #ff4b5c;
        color: white;
        border-radius: 20px;
        cursor: pointer;
        font-size: 16px;
    }

    button:hover {
        background: #ff1e38;
    }

    .popup {
        display: none;
        position: fixed;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        background: #111;
        padding: 20px;
        border-radius: 15px;
        box-shadow: 0 0 20px #ff4b5c;
        width: 80%;
        max-width: 400px;
    }

    .heart {
        position: fixed;
        color: red;
        animation: floatUp 5s linear infinite;
    }

    @keyframes floatUp {
        from {
            transform: translateY(100vh);
            opacity: 1;
        }
        to {
            transform: translateY(-10vh);
            opacity: 0;
        }
    }
</style>
</head>

<body>

<div class="stars"></div>

<div class="container">
    <h1>💖 Love Promises 💖</h1>
    <div id="typing"></div>

    <button onclick="showLove()">💌 Open Love Letter</button>
    <button onclick="unlockSecret()">🔐 Unlock Secret</button>
</div>

<div class="popup" id="popup">
    <h2>💌 My Promises</h2>
    <p>
        Dear MISS REDDY ❤️,<br><br>
        I promise to stand with you forever 💞<br>
        I promise to make you smile every day 😊<br>
        I promise to love you endlessly ♾️<br>
        I promise to never leave your side 💖<br><br>
        — Yours forever,<br>
        JITHIN CHOWDARY 💘
    </p>
    <button onclick="closePopup()">Close</button>
</div>

<script>
    // Typing Effect
    const text = "I Love You MISS REDDY ❤️";
    let i = 0;

    function typingEffect() {
        if (i < text.length) {
            document.getElementById("typing").innerHTML += text.charAt(i);
            i++;
            setTimeout(typingEffect, 80);
        }
    }
    typingEffect();

    // Popup
    function showLove() {
        document.getElementById("popup").style.display = "block";
    }

    function closePopup() {
        document.getElementById("popup").style.display = "none";
    }

    // Secret Unlock
    function unlockSecret() {
        let pass = prompt("Enter Secret Code 💖");
        if (pass === "143") {
            alert("Secret Message: I LOVE YOU FOREVER ❤️🔥");
        } else {
            alert("Wrong Code 😢");
        }
    }

    // Floating Hearts
    setInterval(() => {
        let heart = document.createElement("div");
        heart.className = "heart";
        heart.innerHTML = "❤️";
        heart.style.left = Math.random() * 100 + "vw";
        heart.style.fontSize = Math.random() * 20 + 10 + "px";
        document.body.appendChild(heart);

        setTimeout(() => {
            heart.remove();
        }, 5000);
    }, 500);
</script>

</body>
</html>
