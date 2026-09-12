# index.html1
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For My Moonpie ❤️</title>

<style>
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: "Trebuchet MS", Arial, sans-serif;
    overflow-x: hidden;
    color: white;
}

.screen {
    min-height: 100vh;
    width: 100%;
    display: none;
    position: relative;
    overflow: hidden;
}

.screen.active {
    display: flex;
}

/* =========================
   WELCOME SCREEN
========================= */

#welcome {
    justify-content: center;
    align-items: center;
    text-align: center;
    background:
        radial-gradient(circle at 20% 20%, rgba(255,255,255,.15), transparent 20%),
        radial-gradient(circle at 80% 70%, rgba(255,0,150,.18), transparent 25%),
        linear-gradient(135deg, #09001f, #170044, #32005f, #08001d);
}

.stars {
    position: absolute;
    inset: 0;
    background-image:
        radial-gradient(white 1px, transparent 1px),
        radial-gradient(white 1px, transparent 1px);
    background-size: 70px 70px, 110px 110px;
    background-position: 0 0, 30px 40px;
    opacity: .4;
    animation: starsMove 15s linear infinite;
}

@keyframes starsMove {
    from { transform: translateY(0); }
    to { transform: translateY(-70px); }
}

.welcome-content {
    position: relative;
    z-index: 2;
    padding: 30px;
    animation: fadeIn 1.5s ease;
}

.game-title {
    font-size: clamp(60px, 12vw, 120px);
    font-weight: 900;
    letter-spacing: 5px;
    text-shadow:
        0 0 10px #fff,
        0 0 25px #ff4fc3,
        0 0 50px #ff1493;
    margin-bottom: 25px;
}

.welcome-text {
    font-size: clamp(20px, 4vw, 32px);
    line-height: 1.5;
    max-width: 800px;
    margin: auto;
}

.start-btn {
    margin-top: 40px;
    padding: 18px 55px;
    border: 2px solid white;
    border-radius: 50px;
    background: linear-gradient(90deg, #ff1493, #9b00ff);
    color: white;
    font-size: 22px;
    font-weight: bold;
    cursor: pointer;
    box-shadow: 0 0 20px #ff1493;
    transition: .3s;
}

.start-btn:hover {
    transform: scale(1.1);
    box-shadow: 0 0 40px #ff1493;
}

/* =========================
   COMMON QUIZ
========================= */

.quiz-screen {
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 25px;
}

.quiz-card {
    position: relative;
    z-index: 5;
    width: min(90%, 700px);
    padding: 40px 30px;
    border-radius: 30px;
    background: rgba(255,255,255,.12);
    backdrop-filter: blur(12px);
    border: 1px solid rgba(255,255,255,.3);
    box-shadow: 0 20px 60px rgba(0,0,0,.4);
    animation: cardIn .8s ease;
}

.level {
    display: inline-block;
    padding: 8px 20px;
    border-radius: 30px;
    background: rgba(255,255,255,.2);
    margin-bottom: 25px;
    font-weight: bold;
    letter-spacing: 2px;
}

.question {
    font-size: clamp(27px, 5vw, 45px);
    margin-bottom: 35px;
    line-height: 1.3;
}

.options {
    display: flex;
    flex-direction: column;
    gap: 16px;
}

.option {
    padding: 16px 20px;
    border-radius: 15px;
    border: 2px solid rgba(255,255,255,.5);
    background: rgba(255,255,255,.12);
    color: white;
    font-size: 19px;
    font-weight: bold;
    cursor: pointer;
    transition: .25s;
}

.option:hover {
    transform: scale(1.04);
    background: rgba(255,255,255,.25);
}

/* =========================
   LEVEL 1
========================= */

#level1 {
    background: linear-gradient(135deg, #081b29, #123b55, #08141f);
}

.question-mark {
    position: absolute;
    color: rgba(255,255,255,.08);
    font-size: 80px;
    font-weight: bold;
    animation: floatQuestion 8s ease-in-out infinite;
}

.q1 { top: 5%; left: 8%; }
.q2 { top: 25%; right: 8%; animation-delay: 1s; }
.q3 { bottom: 10%; left: 15%; animation-delay: 2s; }
.q4 { bottom: 20%; right: 15%; animation-delay: 3s; }
.q5 { top: 50%; left: 3%; animation-delay: 4s; }
.q6 { top: 8%; right: 30%; animation-delay: 5s; }

@keyframes floatQuestion {
    0%,100% { transform: translateY(0) rotate(0deg); }
    50% { transform: translateY(-30px) rotate(15deg); }
}

/* =========================
   LEVEL 2
========================= */

#level2 {
    background: linear-gradient(135deg, #50002f, #a0005c, #350020);
}

.heart {
    position: absolute;
    font-size: 45px;
    opacity: .25;
    animation: heartFloat 6s ease-in-out infinite;
}

.h1 { top: 10%; left: 8%; }
.h2 { top: 20%; right: 10%; animation-delay: 1s; }
.h3 { bottom: 15%; left: 15%; animation-delay: 2s; }
.h4 { bottom: 10%; right: 15%; animation-delay: 3s; }
.h5 { top: 50%; left: 5%; animation-delay: 4s; }
.h6 { top: 5%; right: 40%; animation-delay: 2.5s; }
.h7 { bottom: 35%; right: 5%; animation-delay: 1.5s; }

@keyframes heartFloat {
    0%,100% {
        transform: translateY(0) scale(1);
    }
    50% {
        transform: translateY(-40px) scale(1.2);
    }
}

/* =========================
   LEVEL 3
========================= */

#level3 {
    background:
        linear-gradient(rgba(40,0,25,.75), rgba(40,0,25,.8)),
        radial-gradient(circle at 50% 30%, #ff709d, #320018 65%);
}

.date-decoration {
    position: absolute;
    font-size: 60px;
    opacity: .18;
    animation: dateFloat 7s ease-in-out infinite;
}

.d1 { top: 8%; left: 7%; }
.d2 { top: 15%; right: 8%; animation-delay: 1s; }
.d3 { bottom: 10%; left: 10%; animation-delay: 2s; }
.d4 { bottom: 15%; right: 10%; animation-delay: 3s; }
.d5 { top: 45%; left: 4%; animation-delay: 4s; }
.d6 { top: 40%; right: 4%; animation-delay: 2s; }

@keyframes dateFloat {
    0%,100% { transform: translateY(0) rotate(-5deg); }
    50% { transform: translateY(-25px) rotate(5deg); }
}

/* =========================
   FINAL GIFT SCREEN
========================= */

#final {
    min-height: 100vh;
    background:
        radial-gradient(circle at center, #ff5e9c 0%, #8c1452 40%, #240018 100%);
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 20px;
}

.final-title {
    position: relative;
    z-index: 10;
    text-align: center;
    font-size: clamp(35px, 7vw, 65px);
    margin-bottom: 10px;
    text-shadow: 0 0 20px rgba(255,255,255,.8);
}

.final-subtitle {
    position: relative;
    z-index: 10;
    font-size: 19px;
    margin-bottom: 20px;
}

.gift-area {
    position: relative;
    z-index: 5;
    width: min(95vw, 950px);
    height: min(65vh, 620px);
    min-height: 450px;
}

/* Gift box */

.gift {
    position: absolute;
    width: 75px;
    height: 75px;
    cursor: pointer;
    transition: transform .3s ease, filter .3s ease;
    animation: giftFloat 3s ease-in-out infinite;
}

.gift:hover {
    transform: scale(1.18) rotate(5deg);
    filter: brightness(1.3);
    z-index: 20;
}

.box {
    position: absolute;
    bottom: 0;
    width: 75px;
    height: 58px;
    border-radius: 5px;
    background: linear-gradient(135deg, #ff477e, #b8004e);
    border: 2px solid rgba(255,255,255,.5);
    box-shadow: 0 8px 15px rgba(0,0,0,.35);
}

.box::before {
    content: "";
    position: absolute;
    width: 12px;
    height: 100%;
    left: 31px;
    background: rgba(255,225,100,.9);
}

.box::after {
    content: "";
    position: absolute;
    height: 11px;
    width: 100%;
    left: 0;
    top: 22px;
    background: rgba(255,225,100,.9);
}

.lid {
    position: absolute;
    width: 85px;
    height: 16px;
    top: 7px;
    left: -5px;
    border-radius: 5px;
    background: linear-gradient(135deg, #ff6192, #c90058);
    border: 2px solid rgba(255,255,255,.5);
}

.lid::before {
    content: "";
    position: absolute;
    width: 12px;
    height: 16px;
    left: 32px;
    top: -1px;
    background: rgba(255,225,100,.9);
}

.gift-number {
    position: absolute;
    z-index: 3;
    top: 25px;
    left: 0;
    width: 100%;
    text-align: center;
    font-size: 20px;
    font-weight: 900;
    text-shadow: 1px 2px 3px black;
}

@keyframes giftFloat {
    0%,100% { transform: translateY(0); }
    50% { transform: translateY(-8px); }
}

/* =========================
   POPUP
========================= */

.popup {
    position: fixed;
    inset: 0;
    z-index: 100;
    display: none;
    justify-content: center;
    align-items: center;
    background: rgba(0,0,0,.7);
    padding: 20px;
}

.popup.show {
    display: flex;
}

.popup-card {
    width: min(90%, 600px);
    max-height: 90vh;
    overflow-y: auto;
    padding: 40px;
    border-radius: 30px;
    text-align: center;
    background: linear-gradient(135deg, #ff4f91, #8f0050);
    border: 2px solid white;
    box-shadow: 0 0 50px rgba(255,80,160,.7);
    animation: popupIn .5s ease;
}

.popup-card h2 {
    font-size: 35px;
    margin-bottom: 20px;
}

.popup-card p {
    font-size: 20px;
    line-height: 1.6;
}

.popup-btn {
    margin-top: 25px;
    padding: 12px 30px;
    border: none;
    border-radius: 30px;
    background: white;
    color: #a00058;
    font-size: 17px;
    font-weight: bold;
    cursor: pointer;
}

@keyframes popupIn {
    from {
        opacity: 0;
        transform: scale(.6);
    }
    to {
        opacity: 1;
        transform: scale(1);
    }
}

@keyframes fadeIn {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
}

@keyframes cardIn {
    from { opacity: 0; transform: scale(.8); }
    to { opacity: 1; transform: scale(1); }
}

/* =========================
   CONFETTI
========================= */

.confetti {
    position: fixed;
    top: -20px;
    width: 10px;
    height: 18px;
    z-index: 200;
    animation: confettiFall linear forwards;
}

@keyframes confettiFall {
    to {
        transform: translateY(110vh) rotate(720deg);
        opacity: 0;
    }
}

/* =========================
   FINAL MESSAGE
========================= */

.love-message {
    text-align: left;
    white-space: pre-line;
}

.birthday-heading {
    font-size: clamp(30px, 6vw, 50px);
}

/* =========================
   MOBILE
========================= */

@media (max-width: 600px) {

    .quiz-card {
        padding: 30px 20px;
    }

    .option {
        font-size: 17px;
        padding: 14px;
    }

    .gift-area {
        width: 100%;
        height: 65vh;
        min-height: 430px;
    }

    .gift {
        width: 55px;
        height: 55px;
    }

    .box {
        width: 55px;
        height: 43px;
    }

    .lid {
        width: 63px;
        height: 13px;
        left: -4px;
    }

    .box::before {
        width: 9px;
        left: 23px;
    }

    .box::after {
        height: 8px;
        top: 17px;
    }

    .lid::before {
        width: 9px;
        left: 23px;
        height: 13px;
    }

    .gift-number {
        top: 20px;
        font-size: 15px;
    }

    .popup-card {
        padding: 28px 20px;
    }

    .popup-card p {
        font-size: 17px;
    }
}
</style>
</head>

<body>

<!-- =========================
     WELCOME
========================= -->

<section id="welcome" class="screen active">

    <div class="stars"></div>

    <div class="welcome-content">

        <div class="game-title">
            WELCOME
        </div>

        <div class="welcome-text">
            To get the final reward, you have to clear all the levels. ❤️
        </div>

        <button class="start-btn" onclick="startGame()">
            START GAME ❤️
        </button>

    </div>

</section>


<!-- =========================
     LEVEL 1
========================= -->

<section id="level1" class="screen quiz-screen">

    <div class="question-mark q1">?</div>
    <div class="question-mark q2">?</div>
    <div class="question-mark q3">?</div>
    <div class="question-mark q4">?</div>
    <div class="question-mark q5">?</div>
    <div class="question-mark q6">?</div>

    <div class="quiz-card">

        <div class="level">
            LEVEL 1 🎮
        </div>

        <div class="question">
            Whats manu favourite food? ❤️
        </div>

        <div class="options">

            <button class="option" onclick="level1Correct()">
                Savoury food
            </button>

            <button class="option" onclick="wrongAnswer()">
                Sweet food
            </button>

            <button class="option" onclick="wrongAnswer()">
                Spicy food
            </button>

        </div>

    </div>

</section>


<!-- =========================
     LEVEL 2
========================= -->

<section id="level2" class="screen quiz-screen">

    <div class="heart h1">❤️</div>
    <div class="heart h2">💕</div>
    <div class="heart h3">💗</div>
    <div class="heart h4">❤️</div>
    <div class="heart h5">💖</div>
    <div class="heart h6">💕</div>
    <div class="heart h7">💗</div>

    <div class="quiz-card">

        <div class="level">
            LEVEL 2 💕
        </div>

        <div class="question">
            When was our first date? 🥰
        </div>

        <div class="options">

            <button class="option" onclick="level2Correct()">
                27 Oct
            </button>

            <button class="option" onclick="wrongAnswer()">
                27 Sept
            </button>

            <button class="option" onclick="wrongAnswer()">
                26 Oct
            </button>

        </div>

    </div>

</section>


<!-- =========================
     LEVEL 3
========================= -->

<section id="level3" class="screen quiz-screen">

    <div class="date-decoration d1">🌹</div>
    <div class="date-decoration d2">🍷</div>
    <div class="date-decoration d3">❤️</div>
    <div class="date-decoration d4">🌹</div>
    <div class="date-decoration d5">✨</div>
    <div class="date-decoration d6">🥂</div>

    <div class="quiz-card">

        <div class="level">
            LEVEL 3 🌹
        </div>

        <div class="question">
            Which date with your bf you liked the most? ❤️
        </div>

        <div class="options">

            <button class="option" onclick="wrongAnswer()">
                Mahalaxami
            </button>

            <button class="option" onclick="wrongAnswer()">
                Lower parel
            </button>

            <button class="option" onclick="level3Correct()">
                Dadar ❤️
            </button>

        </div>

    </div>

</section>


<!-- =========================
     FINAL PAGE
========================= -->

<section id="final" class="screen">

    <h1 class="final-title">
        🎁 YOUR FINAL REWARD 🎁
    </h1>

    <p class="final-subtitle">
        Find the right box... ❤️
    </p>

    <div class="gift-area" id="giftArea"></div>

</section>


<!-- =========================
     POPUP
========================= -->

<div class="popup" id="popup">

    <div class="popup-card">

        <h2 id="popupTitle">
            ❤️
        </h2>

        <p id="popupText">
        </p>

        <button class="popup-btn" onclick="closePopup()">
            Continue ❤️
        </button>

    </div>

</div>


<script>

/* =========================
   SCREEN MANAGEMENT
========================= */

function showScreen(id) {

    document.querySelectorAll(".screen").forEach(screen => {
        screen.classList.remove("active");
    });

    document.getElementById(id).classList.add("active");

    window.scrollTo(0, 0);
}


/* =========================
   START GAME
========================= */

function startGame() {
    showScreen("level1");
}


/* =========================
   POPUP
========================= */

function showPopup(title, message, callback) {

    document.getElementById("popupTitle").innerHTML = title;
    document.getElementById("popupText").innerHTML = message;

    document.getElementById("popup").classList.add("show");

    window.popupCallback = callback || null;
}

function closePopup() {

    document.getElementById("popup").classList.remove("show");

    if (window.popupCallback) {

        const callback = window.popupCallback;

        window.popupCallback = null;

        callback();
    }
}


/* =========================
   WRONG ANSWER
========================= */

function wrongAnswer() {

    showPopup(
        "Oops! 😜",
        "Wrong answer! Try again ❤️"
    );
}


/* =========================
   LEVEL 1
========================= */

function level1Correct() {

    showPopup(
        "🎉 Congratulations! 🎉",
        "Congrats on clearing lvl 1! ❤️<br><br>Now onto the next level! 💕",
        function() {
            showScreen("level2");
        }
    );
}


/* =========================
   LEVEL 2
========================= */

function level2Correct() {

    showPopup(
        "💕 Next Level 💕",
        "You remembered our first date! 🥰<br><br>Let's go to the next level! ❤️",
        function() {
            showScreen("level3");
        }
    );
}


/* =========================
   LEVEL 3
========================= */

function level3Correct() {

    showScreen("final");

    createGifts();

    setTimeout(function() {

        showPopup(
            "🎁 Choose the right box 🎁",
            "One of these 20 gifts has something special waiting for you... ❤️<br><br>Choose wisely, my love! 🥰"
        );

    }, 500);
}


/* =========================
   CREATE 20 RANDOM GIFTS
========================= */

function createGifts() {

    const giftArea = document.getElementById("giftArea");

    giftArea.innerHTML = "";

    let numbers = [];

    for (let i = 1; i <= 20; i++) {
        numbers.push(i);
    }

    /* Fisher-Yates shuffle */

    for (let i = numbers.length - 1; i > 0; i--) {

        const j = Math.floor(Math.random() * (i + 1));

        [numbers[i], numbers[j]] = [numbers[j], numbers[i]];
    }


    /*
       Create positions.
       These are randomized every time.
    */

    const positions = [];

    for (let i = 0; i < 20; i++) {

        let x, y, valid;

        do {

            x = Math.random() * 88;
            y = Math.random() * 80;

            valid = true;

            for (const pos of positions) {

                const dx = x - pos.x;
                const dy = y - pos.y;

                if (Math.sqrt(dx * dx + dy * dy) < 13) {
                    valid = false;
                    break;
                }
            }

        } while (!valid);

        positions.push({x, y});
    }


    numbers.forEach((number, index) => {

        const gift = document.createElement("div");

        gift.className = "gift";

        gift.style.left = positions[index].x + "%";
        gift.style.top = positions[index].y + "%";

        gift.style.animationDelay =
            (Math.random() * 2) + "s";


        gift.innerHTML = `
            <div class="lid"></div>
            <div class="box"></div>
            <div class="gift-number">${number}</div>
        `;


        gift.onclick = function() {

            if (number === 13) {

                openCorrectGift(gift);

            } else {

                showPopup(
                    "🎁 Not this one! 😜",
                    "This isn't the right gift, my love!<br><br>Keep looking... ❤️"
                );

            }

        };


        giftArea.appendChild(gift);

    });

}


/* =========================
   CORRECT GIFT
========================= */

function openCorrectGift(gift) {

    gift.style.transform =
        "scale(1.4) rotate(10deg)";

    gift.style.zIndex = "50";

    createConfetti();

    setTimeout(function() {

        showPopup(

            "Happiest Birthday my Love! 🎂❤️✨",

            `<div class="love-message">
Happy birthday my moonpie. 🌙❤️

Enjoy your day. You're such a nice person. I love u soo much. 🥹❤️

I bother u so much, still you're with me. Me tuja aikat nhi, teri pn tu maja aikat and ragvat nhi. 🥹❤️

Mala yevde gifts tar dete, thank u again. 🎁❤️

Yevda vait vagto, tula trass deto, tula radavto, tula paije tesa vagat nhi, det nhi tri tu maja sathi yevda kerte. 🥺❤️

I love sitting beside you in auto and in classroom. 🥰

I like it when we are spending time together alone, even if we are in clg. ❤️

I annoy you to take your attention. 😭😂❤️

When you beat me, touch my face, I enjoy that. 🥹❤️

I wanna stay with youu. ❤️

I want you everyday, everytime. 🫶🏻

You look so good that I can't look at other girls. I only see you as a diva. 👑❤️

May this bday bring you happiness and joy to your life. ✨

Stay happy and positive forever. ❤️

Love youuu and miss you, my truffle. 🥹❤️🍫

I LOVE YOUUUU ❤️❤️❤️
</div>`,

            null

        );

    }, 700);

}


/* =========================
   CONFETTI
========================= */

function createConfetti() {

    const emojis = [
        "❤️",
        "💕",
        "💗",
        "💖",
        "✨",
        "🎉",
        "🎊",
        "🥰",
        "🌹",
        "🎁"
    ];

    for (let i = 0; i < 120; i++) {

        const piece = document.createElement("div");

        piece.className = "confetti";

        piece.innerHTML =
            emojis[Math.floor(Math.random() * emojis.length)];

        piece.style.left =
            Math.random() * 100 + "vw";

        piece.style.fontSize =
            (12 + Math.random() * 18) + "px";

        piece.style.animationDuration =
            (2 + Math.random() * 4) + "s";

        piece.style.animationDelay =
            Math.random() * 1.5 + "s";

        document.body.appendChild(piece);


        setTimeout(function() {
            piece.remove();
        }, 7000);

    }
}

</script>

</body>
</html>
