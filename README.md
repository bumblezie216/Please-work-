<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Lola ♡</title>
<style>
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}
html {
    scroll-behavior: smooth;
}
body {
    font-family: Georgia, "Times New Roman", serif;
    background:
        radial-gradient(circle at 20% 20%, rgba(120,190,255,.18), transparent 25%),
        radial-gradient(circle at 80% 70%, rgba(100,150,255,.12), transparent 30%),
        #05091c;
    color: #eef7ff;
    overflow-x: hidden;
}
body::before {
    content: "";
    position: fixed;
    inset: 0;
    pointer-events: none;
    background-image:
        radial-gradient(circle, white 1px, transparent 1.5px),
        radial-gradient(circle, rgba(180,220,255,.8) 1px, transparent 1.5px);
    background-size: 90px 90px, 140px 140px;
    background-position: 10px 20px, 50px 70px;
    opacity: .45;
    z-index: -1;
}
.hero {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 40px 25px;
}
.tiny {
    color: #a9dfff;
    text-transform: uppercase;
    letter-spacing: 4px;
    font-size: 12px;
    margin-bottom: 18px;
}
h1 {
    font-size: clamp(60px, 16vw, 130px);
    color: #d8f3ff;
    text-shadow:
        0 0 15px rgba(140,210,255,.8),
        0 0 50px rgba(80,170,255,.5);
    margin-bottom: 15px;
}
h2 {
    font-size: clamp(32px, 8vw, 58px);
    color: #ccecff;
    margin-bottom: 22px;
}
h3 {
    color: #d9f3ff;
    margin-bottom: 10px;
}
p {
    line-height: 1.8;
    color: #d4e6f3;
}
.subtitle {
    font-size: 25px;
    color: #a9dcff;
}
.intro {
    max-width: 600px;
    margin: 20px auto 30px;
    font-size: 18px;
}
button {
    border: none;
    cursor: pointer;
    font-family: inherit;
}
.enter,
.final-btn {
    padding: 15px 25px;
    border-radius: 40px;
    background: #bde8ff;
    color: #071021;
    font-weight: bold;
    box-shadow: 0 0 25px rgba(120,210,255,.4);
    transition: .3s;
}
.enter:hover,
.final-btn:hover {
    transform: translateY(-3px) scale(1.03);
    box-shadow: 0 0 40px rgba(120,210,255,.7);
}
.section {
    max-width: 1000px;
    margin: auto;
    padding: 100px 25px;
    text-align: center;
}
.eyebrow {
    color: #9fdcff;
    text-transform: uppercase;
    letter-spacing: 3px;
    font-size: 12px;
    margin-bottom: 18px;
}
.reason-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(130px, 1fr));
    gap: 15px;
    margin-top: 35px;
}
.star {
    min-height: 110px;
    padding: 18px;
    border-radius: 20px;
    background: rgba(150,210,255,.08);
    border: 1px solid rgba(170,225,255,.2);
    color: #dff5ff;
    transition: .3s;
}
.star:hover {
    transform: translateY(-5px);
    background: rgba(150,210,255,.16);
    box-shadow: 0 0 25px rgba(120,210,255,.2);
}
.star-number {
    display: block;
    font-size: 25px;
    color: #aee3ff;
    margin-bottom: 8px;
}
.cards {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 20px;
    margin-top: 35px;
}
.card {
    padding: 30px 22px;
    border-radius: 25px;
    background: rgba(255,255,255,.055);
    border: 1px solid rgba(180,225,255,.15);
    transition: .3s;
}
.card:hover {
    transform: translateY(-5px);
    background: rgba(255,255,255,.09);
}
.emoji {
    font-size: 45px;
    margin-bottom: 15px;
}
.timeline {
    display: grid;
    gap: 20px;
    margin-top: 35px;
}
.timeline-item {
    text-align: left;
    padding: 25px;
    border-left: 2px solid #9bdcff;
    background: rgba(255,255,255,.045);
    border-radius: 0 20px 20px 0;
}
.gallery {
    margin-top: 20px;
}
.gallery-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 18px;
    margin-top: 35px;
}
.photo {
    min-height: 220px;
    border-radius: 25px;
    border: 1px dashed rgba(180,225,255,.35);
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 20px;
    background: rgba(255,255,255,.04);
    overflow: hidden;
}
.photo img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 20px;
}
.letter-buttons {
    display: grid;
    gap: 15px;
    max-width: 500px;
    margin: 35px auto;
}
.letter-buttons button {
    padding: 18px;
    border-radius: 20px;
    background: rgba(170,220,255,.1);
    color: #e8f8ff;
    border: 1px solid rgba(170,220,255,.25);
    font-size: 16px;
}
.letter-buttons button:hover {
    background: rgba(170,220,255,.2);
}
.future-list {
    display: grid;
    gap: 15px;
    max-width: 650px;
    margin: 30px auto;
}
.future-item {
    padding: 20px;
    border-radius: 18px;
    background: rgba(255,255,255,.05);
    display: flex;
    justify-content: space-between;
    gap: 15px;
    text-align: left;
}
.future-item span {
    color: #9fcce4;
}
.final-card {
    padding: 60px 30px;
    border-radius: 35px;
    background: linear-gradient(
        145deg,
        rgba(130,205,255,.13),
        rgba(255,255,255,.04)
    );
    border: 1px solid rgba(180,225,255,.25);
    box-shadow: 0 0 60px rgba(80,160,255,.12);
}
.signature {
    margin: 30px 0;
    color: #b9e7ff;
}
.hidden {
    display: none;
}
#finalMessage {
    max-width: 650px;
    margin: 30px auto 0;
    font-size: 20px;
    color: #e5f7ff;
}
footer {
    text-align: center;
    padding: 50px 20px;
    color: #8fb5ca;
}
@media (max-width: 600px) {
    .gallery-grid {
        grid-template-columns: 1fr;
    }
    .future-item {
        flex-direction: column;
    }
    .section {
        padding: 75px 20px;
    }
}
</style>
</head>
<body>
<header class="hero">
    <div class="tiny">A little universe made for</div>
    <h1>Lola ♡</h1>
    <p class="subtitle">Twenty-seven years of you.</p>
    <p class="intro">
        And somehow, in all the billions of people in this world,
        I got lucky enough to find you.
    </p>
    <button class="enter"
    onclick="document.getElementById('birthday').scrollIntoView({behavior:'smooth'})">
        Enter my little universe ↓
    </button>
</header>
<main id="birthday">
<section class="section">
    <p class="eyebrow">♡ Your special day</p>
    <h2>Happy 27th Birthday, my love.</h2>
    <p>
        Today isn't just about another year passing.
        It's about celebrating the person who makes my world
        softer simply by existing in it.
    </p>
    <br>
    <p>
        So I made you a tiny universe.
        Every little corner is here because it reminds me of you.
    </p>
</section>
<section class="section">
    <h2>27 little reasons I love you</h2>
    <p>Tap through the stars and remember how loved you are. ♡</p>
    <div class="reason-grid" id="reasons"></div>
</section>
<section class="section">
    <h2>Our little story</h2>
    <div class="timeline">
        <div class="timeline-item">
            <h3>01 · Then there was you.</h3>
            <p>
                Somewhere along the way, I found you.
                And somehow you became one of the most important
                people in my entire universe.
            </p>
        </div>
        <div class="timeline-item">
            <h3>02 · The distance.</h3>
            <p>
                Different countries, different skies,
                different days and nights.
                But somehow you still became home.
            </p>
        </div>
        <div class="timeline-item">
            <h3>03 · All the little things.</h3>
            <p>
                Your voice. Your hazel eyes.
                Your little habits. Your laugh.
                All the tiny things that make you you.
            </p>
        </div>
        <div class="timeline-item">
            <h3>04 · And now you're 27.</h3>
            <p>
                Another chapter begins,
                and I hope it is gentle, beautiful
                and filled with everything you deserve.
            </p>
        </div>
    </div>
</section>
<section class="section">
    <h2>Lola's little world</h2>
    <p>All the tiny things that make me think of you.</p>
    <div class="cards">
        <div class="card">
            <div class="emoji">🩵</div>
            <h3>Baby blue</h3>
            <p>Your favourite colour. Soft, peaceful and completely you.</p>
        </div>
        <div class="card">
            <div class="emoji">🦦</div>
            <h3>Otters</h3>
            <p>Because obviously there had to be an otter corner.</p>
        </div>
        <div class="card">
            <div class="emoji">☕</div>
            <h3>Black coffee</h3>
            <p>For the girl who somehow makes bitter things beautiful.</p>
        </div>
        <div class="card">
            <div class="emoji">🍣</div>
            <h3>Sushi</h3>
            <p>Your favourite. Even though I still don't understand the obsession.</p>
        </div>
        <div class="card">
            <div class="emoji">🌊</div>
            <h3>The ocean</h3>
            <p>
                One day I want you to see it properly,
                and I want to be there beside you.
            </p>
        </div>
        <div class="card">
            <div class="emoji">🌌</div>
            <h3>Stars</h3>
            <p>
                A whole sky full of them still wouldn't be enough
                to describe what you mean to me.
            </p>
        </div>
        <div class="card">
            <div class="emoji">👁️</div>
            <h3>Your hazel eyes</h3>
            <p>
                Two little pieces of magic I could probably
                get lost in forever.
            </p>
        </div>
        <div class="card">
            <div class="emoji">🎂</div>
            <h3>27</h3>
            <p>
                Twenty-seven years of Lola existing in this world.
                Lucky world.
            </p>
        </div>
    </div>
</section>
<section class="section">
    <h2>Us, in another universe</h2>
    <p>
        Your anime pictures can go here when we add them.
        ♡
    </p>
    <div class="gallery-grid">
        <div class="photo">
            <span>🌌<br><br>Our first picture</span>
        </div>
        <div class="photo">
            <span>🩵<br><br>Our second picture</span>
        </div>
        <div class="photo">
            <span>🌙<br><br>Our third picture</span>
        </div>
        <div class="photo">
            <span>✨<br><br>Our fourth picture</span>
        </div>
    </div>
</section>
<section class="section">
    <h2>Open when...</h2>
    <div class="letter-buttons">
        <button onclick="openLetter('miss')">
            💌 You miss me
        </button>
        <button onclick="openLetter('sad')">
            🌧️ You're sad
        </button>
        <button onclick="openLetter('sleep')">
            🌙 You can't sleep
        </button>
        <button onclick="openLetter('loved')">
            🩵 You need to feel loved
        </button>
    </div>
</section>
<section class="section">
    <h2>A song for you 🎵</h2>
    <p>
        The One That Got Away has always felt like a song
        that belongs somewhere inside our story.
    </p>
    <br>
    <p>
        When you have an audio file you're legally allowed
        to use, we can add it here.
    </p>
</section>
<section class="section">
    <h2>Places we haven't been yet</h2>
    <div class="future-list">
        <div class="future-item">
            <b>🌊 The ocean</b>
            <span>One day.</span>
        </div>
        <div class="future-item">
            <b>🌅 A sunrise together</b>
            <span>Not through a screen.</span>
        </div>
        <div class="future-item">
            <b>✈️ Somewhere new</b>
            <span>Just us.</span>
        </div>
        <div class="future-item">
            <b>🏠 A little place of our own</b>
            <span>Something that feels like home.</span>
        </div>
        <div class="future-item">
            <b>🌌 A sky full of stars</b>
            <span>Both of us looking up.</span>
        </div>
    </div>
</section>
<section class="section">
    <div class="final-card">
        <div class="tiny">For my Lola</div>
        <h2>
            Until I can give you these things in person...
        </h2>
        <p>
            let this little universe hold them for me.
        </p>
        <p class="signature">
            Love always,<br>
            <strong>Bree / Putiputi ♡</strong>
        </p>
        <button class="final-btn" onclick="revealFinal()">
            One last thing...
        </button>
        <p id="finalMessage" class="hidden">
            If I could give you anything for your birthday,
            it would be the ability to see yourself through my eyes.
            Maybe then you'd finally understand why I love you so much.
            <br><br>
            Happy 27th birthday, my love. 🩵
        </p>
    </div>
</section>
</main>
<footer>
    Made with an unreasonable amount of love by Putiputi ♡
</footer>
<script>
const reasons = [
    "Your hazel eyes.",
    "Your voice.",
    "The way you make me feel at home.",
    "Your little laugh.",
    "Your beautiful heart.",
    "Your softness.",
    "Your strength.",
    "Your love for otters.",
    "Your baby blue world.",
    "Your black coffee.",
    "The way you make me smile.",
    "The way you listen.",
    "Your little habits.",
    "Your beautiful soul.",
    "The way you calm me.",
    "The way you make ordinary moments special.",
    "Your kindness.",
    "Your patience.",
    "Your silly side.",
    "Your beautiful mind.",
    "The way you make distance feel smaller.",
    "The way you became my home.",
    "The way you make me feel understood.",
    "Your dreams.",
    "Your courage.",
    "The person you are becoming.",
    "Simply because you're Lola."
];
const reasonContainer = document.getElementById("reasons");
reasons.forEach((reason, index) => {
    const button = document.createElement("button");
    button.className = "star";
    button.innerHTML =
        '<span class="star-number">✦ ' +
        (index + 1) +
        '</span>' +
        '<span>Tap me</span>';
    button.onclick = function() {
        alert(reason);
    };
    reasonContainer.appendChild(button);
});
function openLetter(type) {
    const messages = {
        miss:
        "If you miss me, look at the sky. Somewhere beneath that same sky is a girl who is missing you too. Distance doesn't change where my heart belongs. 🩵",
        sad:
        "If you're sad, you don't have to pretend to be okay. Come exactly as you are. You can be messy, tired, quiet or broken. I'll still love you through every version of you.",
        sleep:
        "If you can't sleep, imagine me beside you. No distance. No screens. Just quiet, warm and safe. Close your eyes and imagine my hand in yours.",
        loved:
        "If you need to feel loved, remember this: you are loved beyond the kilometres between us, beyond the days we spend apart and beyond anything words could ever properly explain."
    };
    alert(messages[type]);
}
function revealFinal() {
    const message = document.getElementById("finalMessage");
    message.classList.remove("hidden");
    message.scrollIntoView({
        behavior: "smooth",
        block: "center"
    });
}
</script>
</body>
</html>
