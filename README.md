# Durga-mam-anniversary-
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Anniversary, Durga Mam! 🎉</title>

<style>
/* Background */
body {
    margin: 0;
    padding: 0;
    text-align: center;
    font-family: 'Arial', sans-serif;
    background: linear-gradient(135deg,#ff9a9e,#fecfef,#a8edea,#fed6e3);
    overflow-x: hidden;
}

/* Container */
.container {
    max-width: 850px;
    margin: 40px auto;
    padding: 25px;
    background: rgba(255,255,255,0.9);
    border-radius: 20px;
    box-shadow: 0 10px 40px rgba(0,0,0,0.25);
}

/* Heading */
h1 {
    font-size: 3rem;
    color: #ff4b5c;
    animation: bounce 1.8s infinite alternate;
}
@keyframes bounce {
    from { transform: translateY(0); }
    to { transform: translateY(-12px); }
}

/* Photo Frame */
.photo-frame {
    width: 240px;
    height: 240px;
    padding: 10px;
    margin: 10px auto;
    border-radius: 50%;
    background: radial-gradient(circle,#ffd93d,#ff4b5c);
    box-shadow: 0 0 30px gold;
    animation: glow 3s infinite alternate;
}
@keyframes glow {
    from { box-shadow: 0 0 25px gold; }
    to { box-shadow: 0 0 60px #ff4b5c; }
}

.photo {
    width: 100%;
    height: 100%;
    border-radius: 50%;
    object-fit: cover;
}

/* Message */
.message {
    font-size: 1.5rem;
    margin-top: 20px;
    animation: slideIn 1.5s ease-out;
}
@keyframes slideIn {
    from { opacity: 0; transform: translateX(-80px); }
    to { opacity: 1; transform: translateX(0); }
}

/* Buttons */
.btn {
    background: #ff4b5c;
    color: #fff;
    padding: 12px 22px;
    border-radius: 30px;
    font-size: 1.1rem;
    border: none;
    cursor: pointer;
    margin: 10px;
    transition: .3s;
}
.btn:hover {
    transform: scale(1.1);
    background: #ff2b3d;
}

/* Hearts Animation */
.hearts, .petals-container, .butterfly-container {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    pointer-events: none;
}
.heart {
    position: absolute;
    color: red;
    font-size: 22px;
    animation: float 6s linear infinite;
}
@keyframes float {
    0% { transform: translateY(100vh); opacity: 1; }
    100% { transform: translateY(-10vh); opacity: 0; }
}

/* Falling Petals */
.petal {
    position: absolute;
    width: 25px;
    animation: fall 7s linear infinite;
}
@keyframes fall {
    0% { transform: translateY(-10vh) rotate(0); }
    100% { transform: translateY(120vh) rotate(360deg); }
}

/* Fireworks */
.firework {
    position: absolute;
    width: 5px; height: 5px;
    border-radius: 50%;
    background: gold;
    animation: explode 1s linear;
}
@keyframes explode {
    0% { transform: scale(1); opacity: 1; }
    100% { transform: scale(8); opacity: 0; }
}

/* Butterflies */
.butterfly {
    position: absolute;
    font-size: 30px;
    animation: fly 10s linear infinite;
}
@keyframes fly {
    0% { transform: translateX(-10%) translateY(80%); }
    100% { transform: translateX(110%) translateY(-20%); }
}
</style>
</head>

<body>

<!-- Background Music -->
<audio id="bgm" loop>
<source src="https://cdn.pixabay.com/download/audio/2022/03/25/audio_7cbcb6e5a3.mp3?filename=raabta-soft-instrumental.mp3">
</audio>

<!-- Animations Layers -->
<div class="hearts" id="hearts"></div>
<div class="petals-container" id="petals"></div>
<div class="butterfly-container" id="butterfly"></div>

<div class="container">
    <h1>Happy Anniversary, Durga Mam! 🎉❤️</h1>

    <div class="photo-frame">
        <img src="web_photo_800.jpg" class="photo">
    </div>

    <div class="message">
        <p>You are an inspiration of kindness, strength and elegance. 🌹</p>
        <p>May your anniversary be filled with joy, blessings and love. 💖</p>
        <p><b>From: Saket ❤️</b></p>
    </div>

    <button class="btn" onclick="toggleMusic()">🎵 Play / Pause Music</button>
    <button class="btn" onclick="launchConfetti()">🎊 Confetti</button>
    <button class="btn" onclick="burstHearts()">💘 Heart Burst</button>
    <button class="btn" onclick="sharePage()">🔗 Share</button>
</div>

<script>
/* MUSIC */
const bgm = document.getElementById("bgm");
function toggleMusic() {
    bgm.paused ? bgm.play() : bgm.pause();
}

/* FLOATING HEARTS */
setInterval(() => {
    let h = document.createElement("div");
    h.className = "heart";
    h.innerHTML = "❤️";
    h.style.left = Math.random()*100 + "vw";
    h.style.fontSize = Math.random()*20+20 + "px";
    h.style.animationDuration = Math.random()*3+3 + "s";
    document.getElementById("hearts").appendChild(h);
    setTimeout(()=>h.remove(),6000);
}, 350);

/* ROSE PETALS */
setInterval(() => {
    let p = document.createElement("img");
    p.src="https://pngimg.com/uploads/rose/rose_PNG667.png";
    p.className="petal";
    p.style.left = Math.random()*100 + "vw";
    p.style.animationDuration = Math.random()*4+4 + "s";
    p.style.width = (Math.random()*20+20)+"px";
    document.getElementById("petals").appendChild(p);
    setTimeout(()=>p.remove(),7000);
}, 400);

/* BUTTERFLIES */
setInterval(() => {
    let b = document.createElement("div");
    b.className="butterfly";
    b.innerHTML="🦋";
    b.style.left = Math.random()*100 + "vw";
    document.getElementById("butterfly").appendChild(b);
    setTimeout(()=>b.remove(),10000);
}, 5000);

/* CONFETTI */
function launchConfetti() {
    for(let i=0;i<25;i++){
        let f=document.createElement("div");
        f.className="firework";
        f.style.left=Math.random()*100+"vw";
        f.style.top=Math.random()*100+"vh";
        document.body.appendChild(f);
        setTimeout(()=>f.remove(),1000);
    }
}

/* HEART BURST */
function burstHearts() {
    for(let i=0;i<20;i++){
        let h=document.createElement("div");
        h.className="heart";
        h.innerHTML="💖";
        h.style.left="50vw";
        h.style.top="50vh";
        h.style.animationDuration="1.5s";
        document.body.appendChild(h);
        setTimeout(()=>h.remove(),1500);
    }
}

/* SHARE */
function sharePage() {
    navigator.share({
        title:"Anniversary Page",
        text:"Special surprise page for Durga Mam ❤️",
        url:window.location.href
    });
}
</script>

</body>
</html>
