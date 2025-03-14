<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>I'm Sorry</title>
    <style>
        body {
            background-color: #ffdab9; /* Peach color */
            text-align: center;
            font-family: cursive;
            overflow: hidden;
            position: relative;
        }
        .container {
            margin-top: 100px;
        }
        h1 {
            color: #d81b60;
        }
        p {
            font-size: 20px;
            color: #880e4f;
        }
        .heart {
            font-size: 50px;
            color: red;
            animation: heartbeat 1s infinite alternate;
        }
        @keyframes heartbeat {
            0% { transform: scale(1); }
            100% { transform: scale(1.2); }
        }
        button {
            padding: 10px 20px;
            font-size: 18px;
            background-color: #d81b60;
            color: white;
            border: none;
            cursor: pointer;
            border-radius: 5px;
        }
        button:hover {
            background-color: #ad1457;
        }
        .emoji {
            position: absolute;
            font-size: 30px;
            animation: fall 5s linear;
        }
        @keyframes fall {
            from { transform: translateY(-100px); opacity: 1; }
            to { transform: translateY(100vh); opacity: 0; }
        }
        .popup {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 0px 15px rgba(0,0,0,0.3);
            font-size: 18px;
        }
    </style>
</head>
<body>
    <script>
        function createEmojiRain(type, count, duration) {
            for (let i = 0; i < count; i++) {
                setTimeout(() => {
                    const emoji = document.createElement("div");
                    emoji.classList.add("emoji");
                    emoji.innerText = type;
                    emoji.style.left = Math.random() * 100 + "vw";
                    emoji.style.animationDuration = duration + "s";
                    document.body.appendChild(emoji);
                    setTimeout(() => { emoji.remove(); }, duration * 1000);
                }, Math.random() * 5000);
            }
        }
        window.onload = function() {
            createEmojiRain("🥺", 100, 5);
        };
    </script>
    
    <div class="container">
        <h1>I'm Really Sorry!</h1>
        <p>Dear Bestie, I never meant to hurt you. Please forgive me?</p>
        <div class="heart">❤️</div>
        <br>
        <button onclick="acceptApology()">Accept Apology</button>
    </div>
    
    <div id="popup" class="popup">
        <p>Thank you for being my bestie! You are the best one I ever met! ❤️</p>
        <button onclick="closePopup()">Close</button>
    </div>
    
    <script>
        function acceptApology() {
            document.getElementById("popup").style.display = "block";
            createEmojiRain("😘", 100, 10); // Slower falling kisses
        }
        function closePopup() {
            document.getElementById("popup").style.display = "none";
        }
    </script>
</body>
</html>

function createEmojiRain(type, count, duration) {
    for (let i = 0; i < count; i++) {
        setTimeout(() => {
            const emoji = document.createElement("div");
            emoji.classList.add("emoji");
            emoji.innerText = type;
            emoji.style.left = Math.random() * 100 + "vw";
            emoji.style.animationDuration = duration + "s";
            document.body.appendChild(emoji);
            setTimeout(() => { emoji.remove(); }, duration * 1000);
        }, Math.random() * 5000);
    }
}

// Trigger falling 🥺 emojis on page load
window.onload = function() {
    createEmojiRain("🥺", 100, 5);
};

function acceptApology() {
    document.getElementById("popup").style.display = "block";
    createEmojiRain("😘", 100, 10); // Slower falling kisses
}

function closePopup() {
    document.getElementById("popup").style.display = "none";
}


body {
    background-color: #ffdab9; /* Peach color */
    text-align: center;
    font-family: cursive;
    overflow: hidden;
    position: relative;
}

.container {
    margin-top: 100px;
}

h1 {
    color: #d81b60;
}

p {
    font-size: 20px;
    color: #880e4f;
}

.heart {
    font-size: 50px;
    color: red;
    animation: heartbeat 1s infinite alternate;
}

@keyframes heartbeat {
    0% { transform: scale(1); }
    100% { transform: scale(1.2); }
}

button {
    padding: 10px 20px;
    font-size: 18px;
    background-color: #d81b60;
    color: white;
    border: none;
    cursor: pointer;
    border-radius: 5px;
}

button:hover {
    background-color: #ad1457;
}

.emoji {
    position: absolute;
    font-size: 30px;
    animation: fall 5s linear;
}

@keyframes fall {
    from { transform: translateY(-100px); opacity: 1; }
    to { transform: translateY(100vh); opacity: 0; }
}

.popup {
    display: none;
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background: white;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0px 0px 15px rgba(0,0,0,0.3);
    font-size: 18px;
}
