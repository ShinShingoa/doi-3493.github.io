<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Isolated Terminal Theme - GitHub Pages</title>
    
    <!-- Font Imports -->
    <link rel="stylesheet" href="https://scp-wiki.wdfiles.com/local--files/theme:isolated-terminal/terminus.css">
    <link rel="stylesheet" href="https://scp-wiki.wdfiles.com/local--files/theme:isolated-terminal/profontwindows.css">
    <link rel="stylesheet" href="https://scp-wiki.wdfiles.com/local--files/theme:isolated-terminal/vga8.css">
    
    <style>
        /* ==========================================
           ROOT VARIABLES
           ========================================== */
        :root {
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
            
            /* Colors */
            --accentColor: 246, 196, 3;
            --darkColor: 40, 26, 8;
            --black-monochrome: 246, 196, 3;
            --gray-monochrome: 40, 26, 8;
            --white-monochrome: 40, 26, 8;
            
            /* Background */
            --background-color: 40, 26, 8;
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
            background: rgb(var(--background-color));
        }
        
        body {
            font-family: var(--body-font);
            font-size: var(--base-font-size);
            color: rgb(var(--accentColor));
            background: rgb(var(--background-color));
            line-height: 1.6;
            position: relative;
            min-height: 100vh;
        }
        
        /* ==========================================
           HEADER
           ========================================== */
        header {
            height: var(--header-height-on-desktop);
            background: rgb(var(--background-color));
            display: flex;
            align-items: flex-end;
            justify-content: center;
            position: relative;
            padding-bottom: 1rem;
        }
        
        header::before {
            content: "";
            position: absolute;
            top: 0;
            left: 50%;
            transform: translateX(-50%);
            width: calc(var(--header-height-on-desktop) - var(--header-h1-font-size) - 1rem);
            height: calc(var(--header-height-on-desktop) - var(--header-h1-font-size) - 1rem);
            background-color: rgb(var(--black-monochrome));
            -webkit-mask-image: url("data:image/svg+xml;charset=utf8,%3Csvg xmlns='http://www.w3.org/2000/svg' version='1.0' width='1040' height='1040'%3E%3Cpath d='M437 969v-10h-73v-18h-36v-18h-36v-18h-36v-18h-56v18h-72v-36h-18v-36H92v-37H74v-36H55v-36H37v-36H19v-56h18v-18h18v-18h19V451h18v-72h18v-38h18v-36h18v-36h18v-18h18v-18h18v-19h20v-18h18v-18h18v-18h36v-18h36v-18h18v-18h18V50h19V32h272v18h19v56h18v18h18v18h36v18h36v18h18v18h20v18h18v19h18v18h18v18h18v36h18v36h18v38h18v72h18v145h19v18h18v18h18v56h-18v36h-18v36h-19v36h-18v37h-18v36h-18v36h-72v-18h-56v18h-36v18h-36v18h-36v18h-73v20H437v-10zm146-37v-9h72v-18h37v-18h36v-18h18v-18h92v18h54v-36h18v-37h18v-36h18v-36h18v-36h19v-38h-19v-18h-18v-18h-18V469h-18v-72h-18v-38h-18v-36h-18v-18h-18v-36h-18v-18h-20v-18h-18v-19h-36v-18h-18v-18h-36v-18h-18v-18h-19v-36h-18V70H401v36h-18v36h-19v18h-18v18h-36v18h-18v18h-36v19h-18v18h-18v18h-20v36h-18v18h-18v36h-18v38h-18v72h-18v145H92v18H74v18H55v38h19v36h18v36h18v36h18v37h18v36h54v-18h92v18h18v18h36v18h37v18h72v18h128v-9z'/%3E%3Cpath d='M437 805v-9h-54v-18h-37v-18h-18v-18h-18v-18h-18v-18h-36v18h-36v18h-20v-18h-18v-36h38v-18h18v-20h18v-18h-18v-72h-18v-73h18v-72h18v-36h18v-38h18v-18h18v-18h18v-18h18v-18h37v-18h36v-18h72v-55h56v55h72v18h36v18h37v18h18v18h18v18h18v18h18v38h18v36h18v72h20v73h-20v72h-18v18h18v20h20v18h36v36h-18v18h-18v-18h-38v-18h-36v18h-18v18h-18v18h-18v18h-37v18h-54v18H437v-9zm164-54v-9h36v-18h37v-18h18v-18h18v-18h-18v-20h-37v-18h-18v38h-18v-20h-18v-36h-18v-18h-18v-18h-18v-36h90v18h55v18h-18v18h18v18h36v18h18v-54h18V469h-18v-54h-18v-36h-18v-20h-18v-18h-18v-18h-37v-18h-36v-18h-54v92h36v36h-18v36h-18v36h-18v18h-20v-18h-18v-36h-18v-36h-18v-36h36v-92h-54v18h-36v18h-37v18h-18v18h-18v20h-18v36h-18v54h-18v109h18v54h18v-18h36v-18h18v-18h-18v-18h55v-18h90v36h-18v18h-18v18h-18v36h-18v20h-18v-38h-18v18h-37v20h-18v18h18v18h18v18h37v18h36v18h164v-9z'/%3E%3C/svg%3E");
            mask-image: url("data:image/svg+xml;charset=utf8,%3Csvg xmlns='http://www.w3.org/2000/svg' version='1.0' width='1040' height='1040'%3E%3Cpath d='M437 969v-10h-73v-18h-36v-18h-36v-18h-36v-18h-56v18h-72v-36h-18v-36H92v-37H74v-36H55v-36H37v-36H19v-56h18v-18h18v-18h19V451h18v-72h18v-38h18v-36h18v-36h18v-18h18v-18h18v-19h20v-18h18v-18h18v-18h36v-18h36v-18h18v-18h18V50h19V32h272v18h19v56h18v18h18v18h36v18h36v18h18v18h20v18h18v19h18v18h18v18h18v36h18v36h18v38h18v72h18v145h19v18h18v18h18v56h-18v36h-18v36h-19v36h-18v37h-18v36h-18v36h-72v-18h-56v18h-36v18h-36v18h-36v18h-73v20H437v-10zm146-37v-9h72v-18h37v-18h36v-18h18v-18h92v18h54v-36h18v-37h18v-36h18v-36h18v-36h19v-38h-19v-18h-18v-18h-18V469h-18v-72h-18v-38h-18v-36h-18v-18h-18v-36h-18v-18h-20v-18h-18v-19h-36v-18h-18v-18h-36v-18h-18v-18h-19v-36h-18V70H401v36h-18v36h-19v18h-18v18h-36v18h-18v18h-36v19h-18v18h-18v18h-20v36h-18v18h-18v36h-18v38h-18v72h-18v145H92v18H74v18H55v38h19v36h18v36h18v36h18v37h18v36h54v-18h92v18h18v18h36v18h37v18h72v18h128v-9z'/%3E%3Cpath d='M437 805v-9h-54v-18h-37v-18h-18v-18h-18v-18h-18v-18h-36v18h-36v18h-20v-18h-18v-36h38v-18h18v-20h18v-18h-18v-72h-18v-73h18v-72h18v-36h18v-38h18v-18h18v-18h18v-18h18v-18h37v-18h36v-18h72v-55h56v55h72v18h36v18h37v18h18v18h18v18h18v18h18v38h18v36h18v72h20v73h-20v72h-18v18h18v20h20v18h36v36h-18v18h-18v-18h-38v-18h-36v18h-18v18h-18v18h-18v18h-37v18h-54v18H437v-9zm164-54v-9h36v-18h37v-18h18v-18h18v-18h-18v-20h-37v-18h-18v38h-18v-20h-18v-36h-18v-18h-18v-18h-18v-36h90v18h55v18h-18v18h18v18h36v18h18v-54h18V469h-18v-54h-18v-36h-18v-20h-18v-18h-18v-18h-37v-18h-36v-18h-54v92h36v36h-18v36h-18v36h-18v18h-20v-18h-18v-36h-18v-36h-18v-36h36v-92h-54v18h-36v18h-37v18h-18v18h-18v20h-18v36h-18v54h-18v109h18v54h18v-18h36v-18h18v-18h-18v-18h55v-18h90v36h-18v18h-18v18h-18v36h-18v20h-18v-38h-18v18h-37v20h-18v18h18v18h18v18h37v18h36v18h164v-9z'/%3E%3C/svg%3E");
            -webkit-mask-size: 100%;
            mask-size: 100%;
            -webkit-mask-repeat: no-repeat;
            mask-repeat: no-repeat;
        }
        
        h1 {
            font-family: var(--header-font);
            font-size: var(--header-h1-font-size);
            color: rgb(var(--black-monochrome));
            letter-spacing: 0.1rem;
            text-shadow: none;
            position: relative;
            z-index: 1;
        }
        
        /* ==========================================
           NAVIGATION
           ========================================== */
        nav {
            background: rgb(var(--accentColor));
            padding: 0.5rem 2rem;
            display: flex;
            gap: 1.5rem;
            justify-content: center;
            flex-wrap: wrap;
        }
        
        nav a {
            color: rgb(var(--white-monochrome));
            text-decoration: none;
            font-family: var(--mono-font);
            padding: 0.3rem 0.8rem;
            transition: all 0.2s;
        }
        
        nav a:hover {
            background: rgb(var(--white-monochrome));
            color: rgb(var(--accentColor));
        }
        
        /* ==========================================
           MAIN CONTENT
           ========================================== */
        main {
            max-width: 90rem;
            margin: 2rem auto;
            padding: 0 2rem;
        }
        
        /* Typography */
        h2, h3, h4, h5, h6 {
            font-family: var(--header-font);
            color: rgb(var(--accentColor));
            margin-top: 1.5em;
            margin-bottom: 0.5em;
        }
        
        p {
            margin-bottom: 1em;
        }
        
        /* Links */
        a {
            font-weight: bold;
            color: rgb(var(--gray-monochrome));
            padding: 0.115em;
            background-color: rgb(var(--black-monochrome));
            text-decoration: none;
            transition: box-shadow 0.2s;
        }
        
        a:hover {
            box-shadow: 0 0 0.7em 0.1em rgba(var(--black-monochrome), 0.3);
        }
        
        /* Code */
        code, pre {
            font-family: var(--mono-font);
            background-color: #f4f4f4;
            color: #000;
            padding: 0.2em 0.4em;
        }
        
        pre {
            padding: 1em;
            overflow-x: auto;
            margin: 1em 0;
        }
        
        /* Blockquote */
        blockquote {
            background-color: rgba(var(--accentColor), 0.06);
            border-left: 0.5rem solid rgb(var(--accentColor));
            padding: 1rem 2rem;
            margin: 1.5em 0;
        }
        
        /* Horizontal Rule */
        hr {
            background-color: rgb(var(--accentColor));
            height: 0.6rem;
            border: none;
            margin: 1.5em 0;
        }
        
        /* Images */
        img {
            max-width: 100%;
            height: auto;
        }
        
        .image-block {
            margin: 1rem 0;
        }
        
        .image-caption {
            color: rgb(var(--white-monochrome));
            background-color: rgb(var(--accentColor));
            border: 2px solid rgb(var(--accentColor));
            padding: 0.15rem;
            margin-top: 6px;
            text-align: center;
        }
        
        /* Custom Blocks */
        .expoblock {
            box-sizing: border-box;
            border: solid 0.7rem rgb(var(--black-monochrome));
            padding: 1rem;
            margin: 1.5rem 0;
        }
        
        .hilighter {
            background-color: rgb(var(--black-monochrome));
            color: rgb(var(--gray-monochrome));
            font-weight: bold;
            padding: 0.2em;
            font-size: 108%;
            line-height: 1.2;
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
        @media only screen and (max-width: 56.25rem) {
            :root {
                --header-h1-font-size: 2.64rem;
            }
            
            header {
                height: var(--header-height-on-mobile);
            }
            
            nav {
                padding: 0.5rem 1rem;
                gap: 1rem;
            }
            
            main {
                padding: 0 1rem;
            }
        }
    </style>
</head>
<body>
    <!-- Scanline effects -->
    <div id="scanline-overlay"></div>
    <div id="scanline-moving"></div>
    <div id="vignette"></div>
    
    <!-- Header -->
    <header>
        <h1>SCP FOUNDATION</h1>
    </header>
    
    <!-- Navigation -->
    <nav>
        <a href="#home">HOME</a>
        <a href="#about">ABOUT</a>
        <a href="#articles">ARTICLES</a>
        <a href="#archive">ARCHIVE</a>
        <a href="#contact">CONTACT</a>
    </nav>
    
    <!-- Main Content -->
    <main>
        <h2>Welcome to the Terminal</h2>
        <p>This is a GitHub Pages adaptation of the <strong>Isolated Terminal Theme</strong> from the SCP Wiki. The retro terminal aesthetic has been preserved with scanline effects and vintage typography.</p>
        
        <div class="expoblock">
            <h3>Featured Content</h3>
            <p>This is an example of an <span class="hilighter">exposition block</span> with custom styling. You can use this for important callouts or special sections.</p>
        </div>
        
        <blockquote>
            <p>"The Foundation operates to secure and contain anomalous objects, entities, and phenomena."</p>
        </blockquote>
        
        <hr>
        
        <h3>Code Example</h3>
        <pre><code>function initialize() {
    console.log("Terminal initialized...");
    return true;
}</code></pre>
        
        <div class="image-block">
            <img src="https://via.placeholder.com/800x400/281a08/f6c403?text=TERMINAL+DISPLAY" alt="Terminal Display">
            <div class="image-caption">Figure 1.1 - Terminal Interface Display</div>
        </div>
        
        <h3>Links and Navigation</h3>
        <p>All <a href="#example">hyperlinks</a> maintain the terminal aesthetic with highlighted backgrounds. The scanline effect creates an authentic CRT monitor appearance.</p>
        
        <h4>Features</h4>
        <ul>
            <li>Retro terminal fonts (Terminus, VGA8, ProFont)</li>
            <li>Scanline CRT monitor effects</li>
            <li>Vintage color palette (amber on dark)</li>
            <li>Fully responsive design</li>
            <li>Custom styled blocks and elements</li>
        </ul>
    </main>
</body>
</html>
