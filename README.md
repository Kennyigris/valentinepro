<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Valentine's Day Surprise</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            background-color: #ffe6f2;
            font-family: 'Arial', sans-serif;
        }

        .envelope {
            width: 200px;
            height: 120px;
            background-color: #ff6666;
            position: relative;
            cursor: pointer;
            transition: transform 0.3s;
            clip-path: polygon(0% 0%, 100% 0%, 100% 75%, 50% 100%, 0% 75%);
        }

        .envelope:hover {
            transform: scale(1.1);
        }

        .note {
            display: none;
            position: absolute;
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.2);
            text-align: center;
            max-width: 300px;
            transition: transform 0.3s ease;
            transform-origin: center;
        }

        .buttons {
            margin-top: 15px;
            display: flex;
            gap: 10px;
            justify-content: center;
        }

        button {
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        #yesBtn {
            background-color: #4CAF50;
            color: white;
            transition: transform 0.3s ease;
        }

        #noBtn {
            background-color: #f44336;
            color: white;
            position: relative;
            transition: all 0.3s ease;
        }

        #finalNote {
            display: none;
            font-size: 24px;
            color: #ff3366;
            text-align: center;
        }
    </style>
</head>
<body>
    <div class="envelope" onclick="openEnvelope()"></div>
    
    <div class="note" id="mainNote">
        <h2>💌 To my precious girl Gift 💝</h2>
        <p>Will you be my Valentine?</p>
        <p>👸🏼</p>
        <div class="buttons">
            <button id="yesBtn" onclick="respondYes()">YES</button>
            <button id="noBtn" onmousedown="moveNo()">NO</button>
        </div>
    </div>

    <div id="finalNote">
        <h2>I will always treasure you, pookie! 💖</h2>
        <p>Forever yours, Kenny</p>
    </div>

    <script>
        let yesScale = 1;
        let noteScale = 1;

        function openEnvelope() {
            document.querySelector('.envelope').style.display = 'none';
            document.getElementById('mainNote').style.display = 'block';
        }

        function moveNo() {
            const noBtn = document.getElementById('noBtn');
            // More dramatic movement
            const randomX = Math.random() * 200 - 100;
            const randomY = Math.random() * 200 - 100;
            noBtn.style.transform = `translate(${randomX}px, ${randomY}px)`;
            
            // Increase Yes button size and note size
            yesScale *= 1.2;
            noteScale *= 1.05;
            document.getElementById('yesBtn').style.transform = `scale(${yesScale})`;
            document.getElementById('mainNote').style.transform = `scale(${noteScale})`;
            
            // Reset positions after animation
            setTimeout(() => {
                noBtn.style.transform = 'translate(0, 0)';
            }, 500);
        }

        function respondYes() {
            document.getElementById('mainNote').style.display = 'none';
            document.getElementById('finalNote').style.display = 'block';
        }
    </script>
</body>
</html>

after you gave me this code I don't know how to make it finally to be shared as a link to people teach me please I need to send it as a link to someone when it's complete working 
