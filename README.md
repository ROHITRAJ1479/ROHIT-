<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>🚀 Math Master - 100 Level Quiz Challenge</title>
    <link rel="stylesheet" href="style.css">
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body>
    <div class="app-container">
        <!-- Particles Background -->
        <div class="particles" id="particles"></div>
        
        <!-- Game Interface -->
        <div class="game-container">
            <!-- Header -->
            <header class="game-header">
                <div class="logo-section">
                    <div class="logo">
                        <i class="fas fa-brain"></i>
                        <span>Math</span><span class="gradient-text">Master</span>
                    </div>
                    <div class="tagline">100 Level Challenge</div>
                </div>
                
                <div class="stats-grid">
                    <div class="stat-card level-stat">
                        <i class="fas fa-layer-group"></i>
                        <span class="stat-label">Level</span>
                        <span class="stat-value" id="levelNum">1</span>
                    </div>
                    <div class="stat-card score-stat">
                        <i class="fas fa-star"></i>
                        <span class="stat-label">Score</span>
                        <span class="stat-value" id="scoreNum">0</span>
                    </div>
                    <div class="stat-card streak-stat">
                        <i class="fas fa-fire"></i>
                        <span class="stat-label">Streak</span>
                        <span class="stat-value" id="streakNum">0</span>
                    </div>
                    <div class="stat-card time-stat">
                        <i class="fas fa-clock"></i>
                        <span class="stat-label">Time</span>
                        <span class="stat-value" id="timeNum">30s</span>
                    </div>
                </div>
            </header>

            <!-- Main Content -->
            <main class="main-content">
                <!-- Start Screen -->
                <div class="screen active" data-screen="start">
                    <div class="start-content">
                        <div class="hero-icon">
                            <i class="fas fa-rocket"></i>
                        </div>
                        <h1 class="main-title">Ready for the Ultimate Math Challenge?</h1>
                        <p class="subtitle">Master 100 increasingly difficult levels of addition, subtraction, multiplication & division!</p>
                        
                        <div class="difficulty-preview">
                            <div class="difficulty-item">
                                <span class="level-range">1-25</span>
                                <i class="fas fa-plus"></i>
                                <span>Addition</span>
                            </div>
                            <div class="difficulty-item">
                                <span class="level-range">26-50</span>
                                <i class="fas fa-minus"></i>
                                <span>Subtraction</span>
                            </div>
                            <div class="difficulty-item">
                                <span class="level-range">51-75</span>
                                <i class="fas fa-times"></i>
                                <span>Multiplication</span>
                            </div>
                            <div class="difficulty-item">
                                <span class="level-range">76-100</span>
                                <i class="fas fa-divide"></i>
                                <span>Division</span>
                            </div>
                        </div>
                        
                        <button class="cta-button primary" id="startGameBtn">
                            <i class="fas fa-play"></i> Start Level 1
                        </button>
                        
                        <div class="achievements-preview">
                            <i class="fas fa-trophy"></i>
                            <span>Best Score: <strong id="bestScorePreview">0</strong></span>
                        </div>
                    </div>
                </div>

                <!-- Game Screen -->
                <div class="screen" data-screen="game">
                    <div class="progress-bar-container">
                        <div class="progress-bar">
                            <div class="progress-fill" id="progressFill"></div>
                        </div>
                        <span class="progress-text" id="progressText">1 / 100</span>
                    </div>

                    <div class="question-section">
                        <div class="question-card" id="questionCard">
                            <div class="question-display" id="questionDisplay"></div>
                            <div class="question-timer">
                                <i class="fas fa-clock"></i>
                                <span id="questionTimer">30</span>
                            </div>
                        </div>
                    </div>

                    <div class="answers-section" id="answersSection">
                        <div class="answers-grid" id="answersGrid"></div>
                    </div>
                </div>

                <!-- Result Screen -->
                <div class="screen" data-screen="result">
                    <div class="result-content">
                        <div class="result-icon" id="resultIcon"></div>
                        <div class="result-title" id="resultTitle"></div>
                        <div class="result-score" id="resultScore"></div>
                        <div class="result-explanation" id="resultExplanation"></div>
                        <button class="cta-button" id="nextQuestionBtn">
                            <i class="fas fa-arrow-right"></i> Next
                        </button>
                    </div>
                </div>

                <!-- Level Complete -->
                <div class="screen" data-screen="levelComplete">
                    <div class="level-complete-content">
                        <div class="trophy-animation">
                            <i class="fas fa-trophy"></i>
                        </div>
                        <h2>🎉 Level <span id="completedLevelNum">1</span> Complete!</h2>
                        <p class="level-complete-message">You're on fire! Ready for the next challenge?</p>
                        <div class="level-stats">
                            <span>Score this level: <strong id="levelScoreNum">0</strong></span>
                        </div>
                        <button class="cta-button primary" id="nextLevelBtn">
                            Level <span id="nextLevelNum">2</span> → 
                            <i class="fas fa-arrow-right"></i>
                        </button>
                    </div>
                </div>

                <!-- Game Complete -->
                <div class="screen" data-screen="gameComplete">
                    <div class="game-complete-content">
                        <div class="fireworks">
                            <div class="firework"></div>
                            <div class="firework"></div>
                            <div class="firework"></div>
                        </div>
                        <div class="mega-trophy">
                            <i class="fas fa-crown"></i>
                        </div>
                        <h1 class="victory-title">🏆 LEGENDARY!</h1>
                        <p class="victory-subtitle">You conquered all 100 levels!</p>
                        <div class="final-stats">
                            <div class="final-stat">
                                <span>Final Score:</span>
                                <strong id="finalScoreNum">0</strong>
                            </div>
                            <div class="final-stat">
                                <span>Time Taken:</span>
                                <strong id="totalTimeTaken">0s</strong>
                            </div>
                        </div>
                        <button class="cta-button primary huge" id="playAgainBtn">
                            <i class="fas fa-redo"></i> Play Again
                        </button>
                    </div>
                </div>
            </main>

            <!-- Floating Controls -->
            <div class="floating-controls">
                <button class="control-btn" id="pauseBtn" title="Pause">
                    <i class="fas fa-pause"></i>
                </button>
                <button class="control-btn sound-control" id="soundToggle">
                    <i class="fas fa-volume-up"></i>
                </button>
            </div>
        </div>
    </div>

    <!-- Audio Elements -->
    <audio id="correctSound" preload="auto">
        <source src="data:audio/wav;base64,UklGRnoGAABXQVZFZm10IBAAAAABAAEAQB8AAEAfAAABAAgAZGF0YQoGAACBhYqFbF1fdJivrJBhNjVgodDbq2EcBj+a2/LDciUFLIHO8tiJNwgZaLvt559NEAxQp+PwtmMcBjiR1/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSq2/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSq2/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSq2/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSq2/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSq2/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSq2/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSq2/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSq2/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSq2/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSq2/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSq2/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSq2/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSq2/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSq2/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSq2/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSq2/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSq2/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSq2/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSq
