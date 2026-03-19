<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>InstaClone - Instagram Like App</title>
    <link rel="stylesheet" href="style.css">
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
</head>
<body>
    <!-- Login/Register Modal -->
    <div class="modal-overlay" id="modalOverlay">
        <div class="modal-container">
            <!-- Login Form -->
            <div class="modal-content active" id="loginForm">
                <div class="modal-header">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2a/Instagram_logo.svg/1280px-Instagram_logo.svg.png" alt="Instagram" class="logo">
                    <h2>Log in</h2>
                </div>
                <form id="loginFormElement">
                    <input type="email" id="loginEmail" placeholder="Email or Phone" required>
                    <input type="password" id="loginPassword" placeholder="Password" required>
                    <button type="submit" class="login-btn">Log in</button>
                </form>
                <div class="divider">
                    <span>OR</span>
                </div>
                <button class="facebook-login">
                    <i class="fab fa-facebook-f"></i>
                    Log in with Facebook
                </button>
                <div class="modal-footer">
                    <p>Forgot password? <a href="#" id="forgotPassword">Reset it</a></p>
                    <p>Don't have an account? <a href="#" id="showRegister">Sign up</a></p>
                </div>
            </div>

            <!-- Register Form -->
            <div class="modal-content" id="registerForm">
                <div class="modal-header">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2a/Instagram_logo.svg/1280px-Instagram_logo.svg.png" alt="Instagram" class="logo">
                    <h2>Sign up</h2>
                </div>
                <form id="registerFormElement">
                    <input type="email" id="regEmail" placeholder="Email" required>
                    <input type="text" id="regFullname" placeholder="Full Name" required>
                    <input type="text" id="regUsername" placeholder="Username" required>
                    <input type="password" id="regPassword" placeholder="Password" required>
                    <button type="submit" class="signup-btn">Sign up</button>
                </form>
                <div class="modal-footer">
                    <p>Have an account? <a href="#" id="showLogin">Log in</a></p>
                </div>
            </div>
        </div>
    </div>

    <!-- Main App (Hidden until login) -->
    <div class="app-container hidden" id="appContainer">
        <!-- Header -->
        <header class="header">
            <div class="header-left">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2a/Instagram_logo.svg/1280px-Instagram_logo.svg.png" alt="Instagram" class="logo-small">
            </div>
            <div class="header-center">
                <input type="text" placeholder="Search" class="search-bar">
            </div>
            <div class="header-right">
                <i class="fas fa-home"></i>
                <i class="far fa-comment"></i>
                <i class="far fa-bell"></i>
                <div class="profile-pic" id="profilePic">
                    <i class="fas fa-user"></i>
                </div>
            </div>
        </header>

        <!-- Stories Section -->
        <div class="stories">
            <div class="story active">
                <div class="story-avatar">
                    <i class="fas fa-plus"></i>
                </div>
                <span>Your Story</span>
            </div>
            <div class="story">
                <img src="https://via.placeholder.com/60" class="story-avatar" alt="User">
                <span>user1</span>
            </div>
            <div class="story">
                <img src="https://via.placeholder.com/60" class="story-avatar" alt="User">
                <span>user2</span>
            </div>
        </div>

        <!-- Posts Feed -->
        <div class="feed" id="feed">
            <!-- Posts will be dynamically loaded here -->
        </div>

        <!-- Profile Dropdown -->
        <div class="profile-dropdown hidden" id="profileDropdown">
            <div class="dropdown-item" id="profileLink">
                <i class="fas fa-user"></i>
                Profile
            </div>
            <div class="dropdown-item" id="logoutBtn">
                <i class="fas fa-sign-out-alt"></i>
                Log out
            </div>
        </div>
    </div>

    <script src="script.js"></script>
</body>
</html>
