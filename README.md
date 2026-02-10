<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday Petni</title>

<style>
    body {
        margin: 0;
        background: black;
        color: #f5f5f5;
        height: 100vh;
        display: flex;
        align-items: center;
        justify-content: center;
        font-family: "Courier New", monospace;
        text-align: center;
        padding: 20px;
    }

    h1 {
        font-size: 2.5em;
        margin-bottom: 30px;
    }

    p {
        font-size: 1.2em;
        line-height: 1.6;
        opacity: 0.9;
        max-width: 700px;
    }

    .cursor {
        display: inline-block;
        width: 8px;
        height: 1.2em;
        background: white;
        margin-left: 5px;
        animation: blink 1s infinite;
    }

    @keyframes blink {
        0%,50%,100% {opacity:1;}
        25%,75% {opacity:0;}
    }
</style>
</head>

<body>

<div>
    <!-- Fallback content (ALWAYS visible) -->
    <h1 id="title">Happy Birthday Petni</h1>
    <p id="msg">
        someday we will celebrate your birthday in a dark room and i will be whispering happy birthday
    </p>
    <span class="cursor"></span>
</div>

<script>
    // Animate only if JS runs
    const titleText = "Happy Birthday Petni";
    const messageText = "someday we will celebrate your birthday in a dark room and i will be whispering happy birthday";

    let i = 0, j = 0;
    const titleEl = document.getElementById("title");
    const msgEl = document.getElementById("msg");

    titleEl.textContent = "";
    msgEl.textContent = "";

    function typeTitle() {
        if (i < titleText.length) {
            titleEl.textContent += titleText[i++];
            setTimeout(typeTitle, 120);
        } else {
            setTimeout(typeMessage, 700);
        }
    }

    function typeMessage() {
        if (j < messageText.length) {
            msgEl.textContent += messageText[j++];
            setTimeout(typeMessage, 50);
        }
    }

    typeTitle();
</script>

</body>
</html>
