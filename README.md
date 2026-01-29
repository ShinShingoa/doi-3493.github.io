<html lang="en">
<head>
    
    <!-- Remove the blue website name/title from browser tabs and search results -->
    <meta name="theme-color" content="#310000">
    <link rel="icon" href="data:,">
    
    <!-- Font Imports -->
    <link rel="stylesheet" href="https://scp-wiki.wdfiles.com/local--files/theme:isolated-terminal/terminus.css">
    <link rel="stylesheet" href="https://scp-wiki.wdfiles.com/local--files/theme:isolated-terminal/profontwindows.css">
    <link rel="stylesheet" href="https://scp-wiki.wdfiles.com/local--files/theme:isolated-terminal/vga8.css">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=K2D">
    
    <style>
        /* ==========================================
           ROOT VARIABLES
           ========================================== */
        :root {
            /* Terminal Theme Colors (Red variant) */
            --accentColor: 153, 0, 0;
            --darkColor: 40, 8, 8;
            
            /* Base measurements */
            --header-height-on-desktop: 12.4rem;
            --header-height-on-mobile: 12rem;
            --header-h1-font-size: 3.3rem;
            --base-font-size: 1.1rem;
            
            /* Typefaces */
            --body-font: 'terminus_ttfmedium', sans-serif;
            --header-font: 'mxplus_ibm_vga_8x16regular', sans-serif;
            --title-font: 'mxplus_ibm_vga_8x16regular', sans-serif;
            --mono-font: 'profontwindowsregular', monospace;
            
            /* Original Terminal Theme Colors */
            --black-monochrome: 246, 196, 3;
            --gray-monochrome: 40, 26, 8;
            --white-monochrome: 40, 26, 8;
            
            /* Background */
            --background-color: 40, 8, 8;
        }
        
        /* ==========================================
           GLOBAL RESET & BASE STYLES
           ========================================== */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        html {
            background: rgb(var(--darkColor));
        }
        
        body {
            font-family: var(--body-font);
            font-size: var(--base-font-size);
            color: rgba(255, 128, 128, 0.85);
            background: #310000;
            line-height: 1.6;
            position: relative;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 2rem;
        }
        
        /* ==========================================
           TERMINAL CONTAINER
           ========================================== */
        .terminal {
            border: solid 3px #990000;
            border-radius: 16px;
            background-color: #310000;
            background-image: radial-gradient(ellipse 1000% 100% at 50% 90%, transparent, #210000);
            background-position: center;
            display: block;
            box-shadow: inset 0 0 10em 1em rgba(0, 0, 0, 0.5);
            overflow: hidden;
            max-width: 800px;
            width: 100%;
            min-height: 600px;
            position: relative;
        }
        
        .terminal blockquote {
            background-color: black;
            border: double 3px #FF8080;
            padding: 1rem;
            margin: 1rem 0;
        }
        
        /* ==========================================
           LOGIN FORM
           ========================================== */
        .log-form {
            font-family: Verdana;
            text-align: center;
            padding: 2rem;
            padding-top: 4rem;
        }
        
        .log-form .logint {
            font-size: 420%;
            font-family: 'K2D', sans-serif;
            color: rgba(255, 128, 128, 0.85);
            margin-bottom: 2rem;
        }
        
        .login-container {
            max-width: 450px;
            margin: 2rem auto;
            padding: 0 2rem;
        }
        
        .input-group {
            margin-bottom: 1.5rem;
            text-align: left;
        }
        
        .input-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: #FF9999;
            font-family: var(--mono-font);
        }
        
        .input-group input {
            width: 100%;
            padding: 10px;
            outline: none;
            border: 1px solid #990000;
            background-color: rgba(0, 0, 0, 0.3);
            color: #FF9999;
            font-family: var(--mono-font);
            border-radius: 3px;
        }
        
        .input-group input:focus {
            padding: 9px;
            border: 2px solid maroon;
        }
        
        .input-group input[type="password"] {
            -webkit-text-security: disc;
            text-security: disc;
        }
        
        .login-btn {
            display: inline-block;
            width: 50%;
            max-width: 160px;
            background-color: Maroon;
            color: red;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
            opacity: 0.9;
            transition: 0.8s;
            border-radius: 3px;
            font-family: var(--mono-font);
            font-size: 1rem;
            margin-top: 1rem;
        }
        
        .login-btn:hover {
            opacity: 1;
            transition: 0.8s;
            box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.7);
        }
        
        .login-btn:active {
            transition: 0.09s;
            transform: translateY(1px);
            box-shadow: 0 0px 0px 0 rgba(0, 0, 0, 0);
        }
        
        /* ==========================================
           EMAIL CONTENT
           ========================================== */
        .email-content {
            display: none;
            padding: 2rem;
            text-align: center;
            animation: fadeIn 0.5s;
        }
        
        .email-content.active {
            display: block;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        .email-title {
            font-size: 1.5rem;
            font-weight: bold;
            margin-bottom: 2rem;
            color: #FF9999;
        }
        
        .email {
            background-color: rgba(0, 0, 0, 0.5);
            border: 2px solid #990000;
            padding: 1.5rem;
            text-align: left;
            margin: 1rem 0;
            border-radius: 5px;
        }
        
        .tofrom {
            margin-bottom: 1rem;
            font-family: var(--mono-font);
            line-height: 1.8;
        }
        
        .tofrom strong {
            color: #FF8080;
        }
        
        .email hr {
            background-color: #990000;
            height: 2px;
            border: none;
            margin: 1rem 0;
        }
        
        .email p {
            margin: 1rem 0;
            line-height: 1.6;
        }
        
        /* ==========================================
           TERMINAL TEXT STYLING
           ========================================== */
        .text a {
            color: #FF9999;
            text-decoration: none;
            background: transparent;
            padding: 0.2em 0.4em;
            transition: all 0.2s;
        }
        
        .text a:hover {
            color: #310000;
            text-decoration: underline;
            background-color: #FF8080;
        }
        
        .text a:hover::before {
            content: "> ";
        }
        
        .logout-btn {
            display: inline-block;
            background-color: #990000;
            color: #FF9999;
            padding: 8px 16px;
            border: 1px solid #FF8080;
            cursor: pointer;
            opacity: 0.9;
            transition: 0.3s;
            border-radius: 3px;
            font-family: var(--mono-font);
            margin-top: 2rem;
        }
        
        .logout-btn:hover {
            opacity: 1;
            background-color: #FF8080;
            color: #310000;
        }
        
        /* ==========================================
           SCANLINE MONITOR EFFECT
           ========================================== */
        #scanline-overlay {
            position: fixed;
            width: 100vw;
            height: 100vh;
            pointer-events: none;
            background: repeating-linear-gradient(180deg, rgba(0, 0, 0, 0), rgba(0, 0, 0, .15) 50%, rgba(0, 0, 0, 0));
            background-size: auto 8px;
            opacity: 0.7;
            z-index: 100;
        }
        
        #scanline-moving {
            position: fixed;
            width: 100vw;
            height: 1rem;
            top: 0;
            pointer-events: none;
            background: linear-gradient(to bottom, rgba(255, 0, 0, 0) 0%, rgba(255, 250, 250, 1) 50%, rgba(255, 255, 255, 0.98) 51%, rgba(255, 0, 0, 0) 100%);
            opacity: .1;
            animation: scanm 6s linear infinite;
            z-index: 101;
        }
        
        @keyframes scanm {
            0% { top: -1rem; opacity: .05; }
            25% { top: 50%; opacity: .03; }
            37.5% { top: 75%; opacity: 0.06; }
            50% { top: 100%; opacity: .03; }
            100% { top: 100%; }
        }
        
        #vignette {
            position: fixed;
            width: 100vw;
            height: 100vh;
            pointer-events: none;
            background-image: radial-gradient(circle, rgb(230, 210, 200) 0%, rgb(177, 158, 152) 60%, rgb(55, 28, 30) 100%);
            opacity: 0.25;
            mix-blend-mode: color-dodge;
            background-repeat: no-repeat;
            background-size: cover;
            z-index: 102;
        }
        
        /* Disable on Safari due to bug */
        @supports (-webkit-hyphens:none) {
            #vignette {
                display: none;
            }
        }
        
        /* ==========================================
           RESPONSIVE DESIGN
           ========================================== */
        @media (max-width: 400px) {
            .log-form .logint {
                font-size: 285% !important;
            }
        }

        @media (min-width: 400px) and (max-width: 450px) {
            .log-form .logint {
                font-size: 330% !important;
            }
        }

        @media (min-width: 450px) and (max-width: 767px) {
            .log-form .logint {
                font-size: 365% !important;
            }
        }

        @media (max-width: 767px) {
            body {
                padding: 1rem;
            }
            
            .terminal {
                min-height: 400px;
            }
            
            .log-form,
            .email-content {
                padding: 1rem;
            }
        }
    </style>
</head>
<body>
    <!-- Scanline effects -->
    <div id="scanline-overlay"></div>
    <div id="scanline-moving"></div>
    <div id="vignette"></div>
    
    <!-- Terminal Container -->
    <div class="terminal">
        <!-- Login Form -->
        <div class="log-form" id="loginForm">
            <div class="logint">SCiPNET</div>
            <div class="login-container">
                <div class="input-group">
                    <label for="username">USERNAME:</label>
                    <input type="text" id="username" placeholder="Enter username" value="P.Crenshaw" readonly>
                </div>
                <div class="input-group">
                    <label for="password">PASSWORD:</label>
                    <input type="password" id="password" placeholder="Enter password" value="Password123" readonly>
                </div>
                <button class="login-btn" onclick="login()">Login</button>
            </div>
        </div>
        
        <!-- Email Content (Hidden Initially) -->
        <div class="email-content text" id="emailContent">
            <div class="email-title">Access SCiPNET Email? One (1) new message!</div>
            
            <div class="email">
                <div class="tofrom">
                    <strong>To:</strong> <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ" target="_blank">P.Crenshaw@scip.net</a><br>
                    <strong>From:</strong> Site-72 Department of Administration, Records Department.<br>
                    <strong>Subject:</strong> Senior Agent "Insight"
                </div>
                
                <hr>
                
                <p>Your request for Information, regarding <strong>'Insight'</strong> of the Site-72 Department of Investigations, has been approved.</p>
                
                <blockquote>
                    <strong>[Attachments:]</strong><br>
                    <a href="3493-unredacted.html">Department Of Investigations | S.A. 3493, 'Insight'.</a>
                </blockquote>
            </div>
            
            <button class="logout-btn" onclick="logout()">Logout</button>
        </div>
    </div>
    
    <script>
        function login() {
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;
            
            // Simple validation (in real scenario, this would be server-side)
            if (username === 'P.Crenshaw' && password === 'Password123') {
                document.getElementById('loginForm').style.display = 'none';
                document.getElementById('emailContent').classList.add('active');
            } else {
                alert('Invalid credentials. Try: P.Crenshaw / Password123');
            }
        }
        
        function logout() {
            document.getElementById('loginForm').style.display = 'block';
            document.getElementById('emailContent').classList.remove('active');
            // Keep password filled on logout (no clearing)
        }
        
        // Allow Enter key to submit
        document.getElementById('password').addEventListener('keypress', function(e) {
            if (e.key === 'Enter') {
                login();
            }
        });
    </script>
</body>
</html>
