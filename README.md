<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Math Quiz Master - 100 Levels</title>
    <link rel="stylesheet" href="style.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
</head>
<body>
    <div class="container">
        <!-- Game Header -->
        <header class="header">
            <div class="logo">
                <i class="fas fa-calculator"></i>
                <h1>Math Quiz Master</h1>
            </div>
            <div class="stats">
                <div class="stat">
                    <span class="stat-label">Level</span>
                    <span class="stat-value" id="currentLevel">1</span>
                </div>
                <div class="stat">
                    <span class="stat-label">Score</span>
                    <span class="stat-value" id="score">0</span>
                </div>
                <div class="stat">
                    <span class="stat-label">Best</span>
                    <span class="stat-value" id="bestScore">0</span>
                </div>
            </div>
        </header>

        <!-- Main Game Area -->
        <main class="game-area">
            <!-- Welcome Screen -->
            <div class="welcome-screen active" id="welcomeScreen">
                <div class="welcome-content">
                    <i class="fas fa-brain"></i>
                    <h2>Welcome to Math Quiz Master!</h2>
                    <p>Test your math skills across 100 challenging levels!</p>
                    <div class="level-info">
                        <i class="fas fa-info-circle"></i>
                        <span>Each level gets progressively harder!</span>
                    </div>
                    <button class="start-btn" id="startBtn">
                        <i class="fas fa-rocket"></i> Start Quiz
                    </button>
                </div>
            </div>

            <!-- Game Screen -->
            <div class="game-screen hidden" id="gameScreen">
                <!-- Progress Bar -->
                <div class="progress-container">
                    <div class="progress-bar">
                        <div class="progress-fill" id="progressFill"></div>
                    </div>
                    <span class="progress-text" id="progressText">Level 1/100</span>
                </div>

                <!-- Question Area -->
                <div class="question-container">
                    <div class="question-box" id="questionBox">
                        <div class="question" id="question"></div>
                        <div class="timer" id="timer">
                            <i class="fas fa-clock"></i>
                            <span id="timeLeft">30</span>s
                        </div>
                    </div>
                </div>

                <!-- Answer Options -->
                <div class="options-container" id="optionsContainer">
                    <div class="options-grid" id="optionsGrid"></div>
                </div>

                <!-- Result Feedback -->
                <div class="feedback-container hidden" id="feedbackContainer">
                    <div class="feedback-icon" id="feedbackIcon"></div>
                    <div class="feedback-message" id="feedbackMessage"></div>
                    <button class="next-btn" id="nextBtn">
                        <i class="fas fa-arrow-right"></i> Next Question
                    </button>
                </div>
            </div>

            <!-- Level Complete Screen -->
            <div class="level-complete-screen hidden" id="levelCompleteScreen">
                <div class="level-complete-content">
                    <i class="fas fa-trophy"></i>
                    <h2>Level <span id="completedLevel">1</span> Complete!</h2>
                    <p>Great job! Ready for the next challenge?</p>
                    <button class="continue-btn" id="continueBtn">Continue to Level <span id="nextLevel">2</span></button>
                </div>
            </div>

            <!-- Game Over Screen -->
            <div class="game-over-screen hidden" id="gameOverScreen">
                <div class="game-over-content">
                    <i class="fas fa-flag-checkered"></i>
                    <h2>Congratulations!</h2>
                    <p>You completed all 100 levels!</p>
                    <div class="final-stats">
                        <div class="final-stat">
                            <span>Total Score:</span>
                            <span id="finalScore">0</span>
                        </div>
                    </div>
                    <button class="restart-btn" id="restartBtn">Play Again</button>
                </div>
            </div>
        </main>

        <!-- Controls -->
        <div class="controls">
            <button class="control-btn" id="pauseBtn" title="Pause">
                <i class="fas fa-pause"></i>
            </button>
            <button class="control-btn" id="soundBtn" title="Sound">
                <i class="fas fa-volume-up"></i>
            </button>
        </div>
    </div>

    <script src="script.js"></script>
</body>
</html>
