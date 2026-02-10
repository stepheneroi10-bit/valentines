<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Resil 💖</title>

<!-- Cute Google Font -->
<link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Poppins:wght@300;500&display=swap" rel="stylesheet">

<style>
    body {
        margin: 0;
        padding: 0;
        height: 100vh;
        overflow: hidden;
        display: flex;
        justify-content: center;
        align-items: center;
        background: linear-gradient(to bottom, #ff9a9e, #fad0c4);
        font-family: 'Poppins', sans-serif;
        color: white;
        text-align: center;
    }

    .container {
        z-index: 2;
    }

    h1 {
        font-family: 'Pacifico', cursive;
        font-size: 2.6em;
    }

    h2 {
        font-size: 1.5em;
    }

    p {
        font-size: 1.1em;
        max-width: 300px;
        margin: auto;
    }

    button {
        padding: 12px 28px;
        font-size: 1.1em;
        border-radius: 30px;
        border: none;
        cursor: pointer;
        margin: 10px;
    }

    .yes {
        background-color: #ff4d6d;
        color: white;
    }

    .no {
        background-color: #555;
        color: white;
        position: absolute;
    }

    iframe {
        margin-top: 20px;
        border-radius: 12px;
    }

    /* Heart animation */
    .heart {
        position: absolute;
        bottom: -20px;
        font-size: 20px;
        animation: floatUp 6s linear infinite;
        opacity: 0.7;
    }

    @keyframes floatUp {
        0% {
            transform: translateY(0) scale(1);
            opacity: 1;
        }
        100% {
            transform: translateY(-100vh) scale(1.5);
            opacity: 0;
        }
    }
</style>
</head>

<body>

<div class="container">
    <h1>💌 Hi Resil 💌</h1>
    <p>There’s a song that reminds me of you…</p>
    <p>And every time I hear it, I think of us.</p>

    <h2>Will you be my Valentine? 💖</h2>

    <button class="yes" onclick="yesClicked()">Yes 💕</button>
    <button class="no" id="noBtn">No 😢</button>

    <!-- Spotify Embed -->
    <iframe
        src="https://open.spotify.com/embed/track/4IYfN5KZgqYb5wXcMznQhc"
        width="300"
        height="80"
        frameborder="0"
        allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture">
    </iframe>
</div>

<script>
    // Runaway NO button
    const noBtn = document.getElementById("noBtn");

    noBtn.addEventListener("mouseover", moveButton);
    noBtn.addEventListener("touchstart", moveButton);

    function moveButton() {
        const x = Math.random() * (window.innerWidth - 100);
        const y = Math.random() * (window.innerHeight - 50);
        noBtn.style.left = x + "px";
        noBtn.style.top = y + "px";
    }

    // Yes button
    function yesClicked() {
        document.body.innerHTML = `
            <div style="text-align:center; color:white;">
                <h1 style="font-family:'Pacifico', cursive;">🥰 YAY RESIL 🥰</h1>
                <p>You just made my heart so happy 💖</p>
                <p>Happy Valentine’s Day 🌹</p>
                <p>— from someone who loves you</p>
            </div>
        `;
    }

    // Floating hearts
    setInterval(() => {
        const heart = document.createElement("div");
        heart.className = "heart";
        heart.innerHTML = "💖";
        heart.style.left = Math.random() * window.innerWidth + "px";
        heart.style.animationDuration = (4 + Math.random() * 3) + "s";
        document.body.appendChild(heart);

        setTimeout(() => {
            heart.remove();
        }, 7000);
    }, 300);
</script>

</body>
</html>
