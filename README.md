# Reddy
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Love Promises ❤️</title>

<style>
body {
    margin: 0;
    font-family: 'Courier New', monospace;
    background: black;
    color: #ff4d6d;
    text-align: center;
    overflow: hidden;
}

/* 🌌 Stars Background */
.stars {
    width: 100%;
    height: 100%;
    position: fixed;
    background: black;
    overflow: hidden;
    z-index: -1;
}

.star {
    position: absolute;
    width: 2px;
    height: 2px;
    background: white;
    animation: moveStars linear infinite;
}

@keyframes moveStars {
    from { transform: translateY(0); }
    to { transform: translateY(100vh); }
}

h1 {
    margin-top: 40px;
    text-shadow: 0 0 10px #ff4d6d;
}

#typing {
    font-size: 26px;
    color: white;
}

/* Box */
.box {
    margin: 30px auto;
    width: 80%;
    padding: 20px;
    border-radius: 20px;
    background: rgba(255, 77, 109, 0.1);
    box-shadow: 0 0 20px #ff4d6d;
}

/* 💌 Love Letter Popup */
.popup {
    display: none;
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%) scale(0);
    background: #111;
    padding: 25px;
    border-radius: 20px;
    box-shadow: 0 0 25px #ff4d6d;
    color: white;
    width: 80%;
    max-width: 400px;
    transition: 0.5s;
}

.popup.show {
    display: block;
    transform: translate(-50%, -50%) scale(1);
}

/* Buttons */
button {
    padding: 10px 15px;
    border-radius: 10px;
    border: none;
    background: #ff4d6d;
    color: white;
    cursor: pointer;
    margin-top: 10px;
}

#secretMessage {
    display: none;
    margin-top: 15px;
    color: #00ffcc;
}
</style>
</head>

<body>

<!-- 🌌 Background -->
<div class="stars" id="stars"></div>

<h1>JITHIN CHOWDARY ❤️ MISS REDDY</h1>
<div id="typing"></div>

<div class="box">
    <p>💖 I promise to love you forever</p>
    <p>💖 I promise to stay with you always</p>
    <p>💖 I promise to protect your smile</p>
</div>

<!-- 🔐 Unlock -->
<input type="password" id="pass" placeholder="Enter password">
<br>
<button onclick="unlock()">Unlock Love 💖</button>

<div id="secretMessage">
    💌 Secret Unlocked!
    <br>
    <button onclick="openLetter()">Read Love Letter 💌</button>
</div>

<!-- 💌 Popup -->
<div class="popup" id="letter">
    <h2>💌 My Love Letter</h2>
    <p>
        MISS REDDY ❤️<br><br>
        From the moment you came into my life, everything became beautiful.<br>
        You are my happiness, my strength, my forever.<br><br>
        I promise to love you endlessly... 💖<br><br>
        — Yours, JITHIN CHOWDARY
    </p>
    <button onclick="closeLetter()">Close</button>
</div>

<!-- Music -->
<audio autoplay loop>
    <source src="anitha-o-anitha.mp3" type="audio/mp3">
</audio>

<script>
// Typing Effect
const text = "I Love You MISS REDDY ❤️";
let i = 0;
(function typeWriter() {
    if (i < text.length) {
        document.getElementById("typing").innerHTML += text[i++];
        setTimeout(typeWriter, 100);
    }
})();

// 🔐 Unlock
function unlock() {
    let pass = document.getElementById("pass").value;
    if (pass === "reddy") {
        document.getElementById("secretMessage").style.display = "block";
    } else {
        alert("Wrong password 😢");
    }
}

// 💌 Popup control
function openLetter() {
    document.getElementById("letter").classList.add("show");
}

function closeLetter() {
    document.getElementById("letter").classList.remove("show");
}

// 🌌 Create stars
const starsContainer = document.getElementById("stars");

for (let i = 0; i < 100; i++) {
    let star = document.createElement("div");
    star.classList.add("star");

    star.style.left = Math.random() * 100 + "vw";
    star.style.top = Math.random() * 100 + "vh";
    star.style.animationDuration = (Math.random() * 5 + 5) + "s";

    starsContainer.appendChild(star);
}
</script>

</body>
</html>
