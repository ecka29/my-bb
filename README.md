<html>
<head>
<meta charset="UTF-8">
<title>to my ebeb 💖</title>
<style>
/* 🌸 Soft Pink Gradient Background */
body {
    margin:0;
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    font-family: 'Arial', sans-serif;
    background: linear-gradient(135deg, #ffe6f0, #ffd1dc);
    overflow:hidden;
    text-align:center;
    color:#ff4d6d;
}

.container {
    position:relative;
    z-index:2;
}

h1 {
    font-size:2.8rem;
    margin-bottom:0.5rem;
}

p {
    font-size:1.2rem;
    margin-bottom:20px;
}

button {
    padding:15px 35px;
    font-size:1.2rem;
    margin:10px;
    border:none;
    border-radius:50px;
    cursor:pointer;
    box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    transition:0.3s;
    font-weight:bold;
}

/* Buttons Specific */
#yesBtn {
    background:white;
    color:#ff4d6d;
}

#noBtn {
    background:#ff4d6d;
    color:white;
    position:relative; /* changed from absolute for proper flow */
}

/* Images */
img {
    width:180px;
    border-radius:20px;
    margin:10px;
    box-shadow:0 10px 20px rgba(0,0,0,0.2);
}

.celebrate {
    font-size:3rem;
    animation: pop 0.5s ease-in-out forwards;
}

@keyframes pop {
    0% { transform:scale(0); }
    100% { transform:scale(1); }
}

.heart {
    position: absolute;
    width: 20px;
    height: 20px;
    background: #ff4d6d;
    opacity: 0.8;
    transform: rotate(45deg);
    animation: float 5s linear infinite;
    z-index:1;
}

.heart:before,
.heart:after {
    content:"";
    position:absolute;
    width:20px;
    height:20px;
    background:#ff4d6d;
    border-radius:50%;
}

.heart:before { top:-10px; left:0; }
.heart:after { left:10px; top:0; }

@keyframes float {
    0% { transform: translateY(0) rotate(45deg); opacity:0.8; }
    50% { opacity:1; }
    100% { transform: translateY(-700px) rotate(45deg); opacity:0; }
}
</style>
</head>
<body>

<div class="container">
    <h1 id="question">Will You Be My Galentine BB? 💖</h1>
    <p>I hope you're my bestfriend in every universe</p>

    <!-- GitHub Raw Image URLs -->
    <img src="https://raw.githubusercontent.com/ecka29/my-bb/ca4d37f50ae7b247e98b78b8aa87c30a16db9c2e/bestie1.jpg">
    <img src="https://raw.githubusercontent.com/ecka29/my-bb/ca4d37f50ae7b247e98b78b8aa87c30a16db9c2e/bestie2.jpg">

    <br>

    <div style="margin-top:20px;">
        <button id="yesBtn">OFC MY BB</button>
        <button id="noBtn">NO!!!</button>
    </div>
</div>

<script>
function createHeart() {
    const heart = document.createElement('div');
    heart.className = 'heart';
    heart.style.left = Math.random() * window.innerWidth + 'px';
    heart.style.animationDuration = (4 + Math.random() * 3) + 's';
    document.body.appendChild(heart);
    setTimeout(() => { heart.remove(); }, 7000);
}
setInterval(createHeart, 300);

const noBtn = document.getElementById("noBtn");
const yesBtn = document.getElementById("yesBtn");
const question = document.getElementById("question");

// Make the "NO!!!" button run away
noBtn.addEventListener("mouseover", () => {
    const x = Math.random() * (window.innerWidth - 120);
    const y = Math.random() * (window.innerHeight - 80);
    noBtn.style.position = "absolute"; // set absolute dynamically
    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";
});

// When "OFC MY BB" is clicked
yesBtn.addEventListener("click", () => {
    question.innerHTML = "I wuv you BB 💖✨";
    document.body.style.background = "linear-gradient(135deg, #ffb6c1, #ff69b4)";
    noBtn.style.display = "none";
    yesBtn.style.display = "none";

    const celebration = document.createElement("div");
    celebration.className = "celebrate";
    celebration.innerHTML = "💖✨";
    document.body.appendChild(celebration);
});
</script>

</body>
</html>
