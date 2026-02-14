<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Veux-tu être ma Valentine ?</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #ffe4e1;
            overflow: hidden;
            text-align: center;
        }

        h1 {
            color: #d02e52;
            font-size: 2.5rem;
            margin-bottom: 20px;
        }

        .container {
            background: white;
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }

        .buttons {
            margin-top: 30px;
            display: flex;
            justify-content: center;
            gap: 20px;
        }

        button {
            padding: 15px 30px;
            font-size: 1.2rem;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            transition: transform 0.2s;
        }

        #yesBtn {
            background-color: #ff4d6d;
            color: white;
        }

        #noBtn {
            background-color: #adb5bd;
            color: white;
            position: absolute; /* Important pour le mouvement */
        }

        .gif-container img {
            width: 200px;
            border-radius: 10px;
        }
    </style>
</head>
<body>

    <div class="container">
        <div class="gif-container">
            <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExOHpueXNqZzR3bm82bm90am96eHpsbmNreWp6eHpsbmNreWp6eHpsJmVwPXYxX2ludGVybmFsX2dpZl9ieV9pZCZjdD1z/K979VpDzV8c8E9y0mP/giphy.gif" alt="Cœur mignon">
        </div>
        <h1>Veux-tu être ma Valentine ? ❤️</h1>
        <div class="buttons">
            <button id="yesBtn">Oui !</button>
            <button id="noBtn">Non</button>
        </div>
    </div>

    <script>
        const noBtn = document.getElementById('noBtn');
        const yesBtn = document.getElementById('yesBtn');

        // Fonction pour faire fuir le bouton "Non"
        noBtn.addEventListener('mouseover', () => {
            const x = Math.random() * (window.innerWidth - noBtn.offsetWidth);
            const y = Math.random() * (window.innerHeight - noBtn.offsetHeight);
            
            noBtn.style.left = `${x}px`;
            noBtn.style.top = `${y}px`;
        });

        // Action quand elle clique sur "Oui"
        yesBtn.addEventListener('click', () => {
            document.body.innerHTML = `
                <div class="container">
                    <h1>YAY ! À bientôt Valentine ! 🥰</h1>
                    <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExbWp6eHpsbmNreWp6eHpsbmNreWp6eHpsbmNreWp6eHpsJmVwPXYxX2ludGVybmFsX2dpZl9ieV9pZCZjdD1n/l41lH4ADRtAYnGsLe/giphy.gif" width="300">
                </div>
            `;
            document.body.style.backgroundColor = "#ff4d6d";
        });
    </script>
</body>
</html>
