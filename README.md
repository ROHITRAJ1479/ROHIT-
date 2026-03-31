<h1> FAMILY PICTURES </h1

     <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Snake Game</title>
    <link rel="stylesheet" href="style.css">
    <link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap" rel="stylesheet">
</head>
<body>
    <div class="game-container">
        <h1>SNAKE GAME</h1>
        <div class="score-board">
            <div class="score">Score: <span id="score">0</span></div>
            <div class="high-score">High Score: <span id="highScore">0</span></div>
        </div>
        <canvas id="gameCanvas" width="400" height="400"></canvas>
        <div class="controls">
            <button id="startBtn">START GAME</button>
            <button id="pauseBtn">PAUSE</button>
        </div>
        <div id="gameOver" class="game-over hidden">
            <h2>GAME OVER</h2>
            <p>Final Score: <span id="finalScore">0</span></p>
            <button id="restartBtn">PLAY AGAIN</button>
        </div>
    </div>
    <script src="game.js"></script>
</body>
</html>
