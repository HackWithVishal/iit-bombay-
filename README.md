# iit-bombay-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Techfest, IIT Bombay | College Ambassador Program (Cyborg Edition)</title>
    <!-- Google Fonts for High-Tech Typography -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Rajdhani:wght@500;600;700&display=swap" rel="stylesheet">
    <!-- FontAwesome for Cyber-style Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        /* --- CYBERPUNK CODES & THEME VARIABLES --- */
        :root {
            --bg-dark: #060814;
            --bg-card: rgba(10, 16, 36, 0.7);
            --neon-blue: #00f3ff;
            --neon-purple: #b500ff;
            --text-main: #e2e8f0;
            --text-dim: #8a99ad;
            --glow: drop-shadow(0 0 8px rgba(0, 243, 255, 0.6));
            --glow-purple: drop-shadow(0 0 8px rgba(181, 0, 255, 0.6));
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Rajdhani', sans-serif;
        }

        body {
            background-color: var(--bg-dark);
            color: var(--text-main);
            overflow-x: hidden;
            background-image: 
                radial-gradient(at 80% 20%, rgba(181, 0, 255, 0.15) 0px, transparent 50%),
                radial-gradient(at 20% 80%, rgba(0, 243, 255, 0.1) 0px, transparent 50%),
                linear-gradient(rgba(6, 8, 20, 0.95) 2px, transparent 2px), 
                linear-gradient(90deg, rgba(6, 8, 20, 0.95) 2px, transparent 2px);
            background-size: 100% 100%, 100% 100%, 40px 40px, 40px 40px;
        }

        /* --- GLOWING CIRCUIT PATTERN HEADER --- */
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 6%;
            border-bottom: 1px solid rgba(0, 243, 255, 0.2);
            background: rgba(6, 8, 20, 0.8);
            backdrop-filter: blur(10px);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }

        .logo-container {
            display: flex;
            flex-direction: column;
        }

        .logo-main {
            font-family: 'Orbitron', sans-serif;
            font-weight: 900;
            font-size: 1.8rem;
            letter-spacing: 2px;
            background: linear-gradient(45deg, var(--neon-blue), var(--neon-purple));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            filter: var(--glow);
        }

        .logo-sub {
            font-size: 0.75rem;
            text-transform: uppercase;
            letter-spacing: 4px;
            color: var(--neon-purple);
            font-weight: bold;
        }

        nav {
            display: flex;
            gap: 25px;
            background: rgba(255, 255, 255, 0.03);
            padding: 8px 24px;
            border-radius: 30px;
            border: 1px solid rgba(255, 255, 255, 0.08);
        }

        nav a {
            color: var(--text-main);
            text-decoration: none;
            font-size: 1.1rem;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: 0.3s;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        nav a i {
            font-size: 0.9rem;
            color: var(--neon-blue);
        }

        nav a:hover, nav a.active {
            color: var(--neon-blue);
            filter: var(--glow);
        }

        .cta-header-btn {
            font-family: 'Orbitron', sans-serif;
            background: linear-gradient(45deg, transparent 10%, var(--neon-purple) 10%, var(--neon-purple) 90%, var(--neon-blue) 90%);
            border: none;
            color: white;
            padding: 10px 20px;
            font-weight: bold;
            letter-spacing: 1px;
            cursor: pointer;
            clip-path: polygon(0 0, 92% 0, 100% 30%, 100% 100%, 8% 100%, 0 70%);
            transition: 0.3s;
        }

        .cta-header-btn:hover {
            filter: var(--glow-purple);
            box-shadow: 0 0 15px rgba(181, 0, 255, 0.4);
        }

        /* --- HERO SECTION --- */
        .hero-container {
            max-width: 1400px;
            margin: 120px auto 0 auto;
            min-height: calc(100vh - 120px);
            display: grid;
            grid-template-columns: 1.2fr 0.8fr;
            padding: 40px 6%;
            align-items: center;
            gap: 40px;
        }

        .hero-left h2 {
            font-family: 'Orbitron', sans-serif;
            font-size: 1.3rem;
            color: var(--neon-blue);
            letter-spacing: 5px;
            margin-bottom: 10px;
            text-transform: uppercase;
        }

        .hero-left h1 {
            font-family: 'Orbitron', sans-serif;
            font-size: 4.2rem;
            font-weight: 900;
            line-height: 1.1;
            text-transform: uppercase;
            margin-bottom: 20px;
            background: linear-gradient(to right, #ffffff 40%, #c1ccff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero-left h1 span {
            display: block;
            background: linear-gradient(90deg, var(--neon-blue), var(--neon-purple));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            filter: var(--glow);
        }

        .hero-description {
            font-size: 1.3rem;
            color: var(--text-dim);
            line-height: 1.6;
            margin-bottom: 35px;
            max-width: 600px;
            border-left: 3px solid var(--neon-purple);
            padding-left: 15px;
        }

        /* --- INTERACTIVE ACTION BUTTONS --- */
        .hero-actions {
            display: flex;
            align-items: center;
            gap: 30px;
            margin-bottom: 50px;
        }

        .btn-prime {
            font-family: 'Orbitron', sans-serif;
            font-size: 1.1rem;
            padding: 16px 35px;
            background: transparent;
            border: 2px solid var(--neon-blue);
            color: var(--neon-blue);
            font-weight: bold;
            letter-spacing: 2px;
            cursor: pointer;
            position: relative;
            clip-path: polygon(0 0, 85% 0, 100% 30%, 100% 100%, 15% 100%, 0 70%);
            transition: 0.3s;
        }

        .btn-prime:hover {
            background: var(--neon-blue);
            color: var(--bg-dark);
            box-shadow: 0 0 25px rgba(0, 243, 255, 0.5);
            filter: var(--glow);
        }

        .btn-sec {
            font-family: 'Orbitron', sans-serif;
            font-size: 1rem;
            color: var(--text-main);
            text-decoration: none;
            letter-spacing: 1px;
            display: flex;
            align-items: center;
            gap: 10px;
            transition: 0.3s;
        }

        .btn-sec:hover {
            color: var(--neon-purple);
            filter: var(--glow-purple);
        }

        /* --- MISSION MODULES GRID (CARDS) --- */
        .modules-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
        }

        .module-card {
            background: var(--bg-card);
            border: 1px solid rgba(255, 255, 255, 0.05);
            border-top: 3px solid var(--neon-blue);
            padding: 20px;
            border-radius: 4px;
            display: flex;
            gap: 15px;
            align-items: flex-start;
            transition: transform 0.3s, border 0.3s;
        }

        .module-card:nth-child(even) {
            border-top-color: var(--neon-purple);
        }

        .module-card:hover {
            transform: translateY(-5px);
            border-color: var(--neon-blue);
            box-shadow: 0 5px 20px rgba(0, 243, 255, 0.1);
        }

        .module-icon {
            background: rgba(0, 243, 255, 0.1);
            padding: 12px;
            border-radius: 4px;
            color: var(--neon-blue);
            font-size: 1.4rem;
        }

        .module-card:nth-child(even) .module-icon {
            background: rgba(181, 0, 255, 0.1);
            color: var(--neon-purple);
        }

        .module-info h3 {
            font-family: 'Orbitron', sans-serif;
            font-size: 1.2rem;
            margin-bottom: 5px;
            letter-spacing: 1px;
        }

        .module-info p {
            color: var(--text-dim);
            font-size: 0.95rem;
            line-height: 1.4;
        }

        /* --- HERO RIGHT: CYBORG & DEPLOYMENT VISUALIZER --- */
        .hero-right {
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        /* Pure CSS HUD Cyber interface matrix background representation */
        .hud-interface {
            width: 100%;
            aspect-ratio: 1/1;
            border: 2px dashed rgba(0, 243, 255, 0.2);
            border-radius: 50%;
            position: relative;
            animation: spin 40s linear infinite;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        @keyframes spin { 100% { transform: rotate(360deg); } }

        .hud-inner {
            width: 80%;
            height: 80%;
            border: 1px solid rgba(181, 0, 255, 0.3);
            border-radius: 50%;
            border-left-width: 4px;
            border-right-width: 4px;
            animation: spin-reverse 20s linear infinite;
        }

        @keyframes spin-reverse { 100% { transform: rotate(-360deg); } }

        /* Floating Code Terminal Module representing the prompt's cyborg asset style */
        .code-terminal {
            position: absolute;
            background: rgba(5, 9, 23, 0.9);
            border: 1px solid var(--neon-blue);
            border-radius: 8px;
            padding: 20px;
            width: 90%;
            font-family: monospace;
            box-shadow: 0 0 30px rgba(0, 243, 255, 0.15);
            backdrop-filter: blur(5px);
        }

        .terminal-header {
            display: flex;
            gap: 6px;
            margin-bottom: 12px;
            border-bottom: 1px solid rgba(255,255,255,0.1);
            padding-bottom: 8px;
        }

        .dot { width: 10px; height: 10px; border-radius: 50%; background: #ff5f56; }
        .dot:nth-child(2) { background: #ffbd2e; }
        .dot:nth-child(3) { background: #27c93f; }
        .terminal-title { margin-left: 10px; font-size: 0.75rem; color: var(--text-dim); font-family: 'Orbitron'; }

        .code-snippet {
            font-family: 'Consolas', monospace;
            font-size: 0.85rem;
            line-height: 1.5;
            color: #a9b7c6;
        }

        .code-keyword { color: var(--neon-purple); font-weight: bold; }
        .code-string { color: var(--neon-blue); }
        .code-var { color: #ffc66d; }

        /* --- DATA TELEMETRY BAR (FOOTER AREA) --- */
        .telemetry-bar {
            max-width: 1400px;
            margin: 60px auto 0 auto;
            padding: 25px 6%;
            border-top: 1px solid rgba(255, 255, 255, 0.05);
            display: grid;
            grid-template-columns: 1fr 1fr;
            align-items: center;
        }

        .telemetry-stats {
            display: flex;
            gap: 40px;
        }

        .stat-item {
            display: flex;
            flex-direction: column;
        }

        .stat-label {
            font-size: 0.8rem;
            text-transform: uppercase;
            color: var(--text-dim);
            letter-spacing: 2px;
            margin-bottom: 4px;
        }

        .stat-value {
            font-family: 'Orbitron', sans-serif;
            font-size: 1.6rem;
            color: var(--neon-blue);
            font-weight: 700;
        }

        .social-matrix {
            justify-self: end;
            display: flex;
            gap: 15px;
            background: rgba(181, 0, 255, 0.1);
            padding: 8px 20px;
            border-radius: 20px;
            border: 1px solid rgba(181, 0, 255, 0.3);
        }

        .social-matrix a {
            color: var(--text-main);
            font-size: 1.1rem;
            transition: 0.3s;
        }

        .social-matrix a:hover {
            color: var(--neon-blue);
            filter: var(--glow);
            transform: scale(1.1);
        }

        /* --- RESPONSIVE OPTIMIZATION --- */
        @media (max-width: 1024px) {
            .hero-container {
                grid-template-columns: 1fr;
                margin-top: 100px;
                text-align: center;
            }
            .hero-description { margin: 0 auto 35px auto; border-left: none; border-bottom: 3px solid var(--neon-purple); padding-bottom: 10px;}
            .hero-actions { justify-content: center; }
            .hero-right { order: -1; min-height: 300px; }
            .code-terminal { width: 70%; }
            .telemetry-bar { grid-template-columns: 1fr; gap: 20px; justify-items: center; }
        }

        @media (max-width: 600px) {
            header { padding: 15px 4%; }
            nav { display: none; } /* Kept clean for single-file mobile presentation */
            .hero-left h1 { font-size: 2.6rem; }
            .modules-grid { grid-template-columns: 1fr; }
            .code-terminal { width: 100%; }
        }
    </style>
</head>
<body>

    <!-- --- GLOWING CIRCUIT HEADER --- -->
    <header>
        <div class="logo-container">
            <span class="logo-main">TECHFEST</span>
            <span class="logo-sub">IIT BOMBAY</span>
        </div>
        
        <nav>
            <a href="#" class="active"><i class="fa-solid fa-house"></i> Home</a>
            <a href="#"><i class="fa-solid fa-list-check"></i> Tasks</a>
            <a href="#"><i class="fa-solid fa-trophy"></i> Rewards</a>
            <a href="#"><i class="fa-solid fa-network-wired"></i> Projects</a>
        </nav>

        <button class="cta-header-btn">SECURE OFFER LETTER</button>
    </header>

    <!-- --- CYBORG HERO CONTENT CONTAINER --- -->
    <main class="hero-container">
        
        <!-- Left Matrix Data Column -->
        <section class="hero-left">
            <h2>NEXUS DEPLOYMENT PROTOCOL</h2>
            <h1>COLLEGE AMBASSADOR <span>PROGRAM</span></h1>
            
            <p class="hero-description">
                Be the computational node of Asia's largest Science & Technology Festival at your sector. Represent, synchronize execution vectors, and inspire the organic entities around you.
            </p>

            <!-- Action Modules -->
            <div class="hero-actions">
                <button class="btn-prime" onclick="alert('Initiating Registration Node Protocol...')">INITIALIZE PROTOCOL</button>
                <a href="#" class="btn-sec">EXPLORE SUBSYSTEMS <i class="fa-solid fa-arrow-right-long"></i></a>
            </div>

            <!-- Quad-Core Mission Modules -->
            <div class="modules-grid">
                <div class="module-card">
                    <div class="module-icon"><i class="fa-solid fa-rocket"></i></div>
                    <div class="module-info">
                        <h3>Full-Stack Leadership</h3>
                        <p>Command operations and scale regional community engagement strategies.</p>
                    </div>
                </div>
                <div class="module-card">
                    <div class="module-icon"><i class="fa-solid fa-microchip"></i></div>
                    <div class="module-info">
                        <h3>AI & Automation Core</h3>
                        <p>Integrate cutting-edge Techfest digital ecosystems at your university base.</p>
                    </div>
                </div>
                <div class="module-card">
                    <div class="module-icon"><i class="fa-solid fa-shield-halved"></i></div>
                    <div class="module-info">
                        <h3>Secure Networking</h3>
                        <p>Architect robust connections with technology enthusiasts nationwide.</p>
                    </div>
                </div>
                <div class="module-card">
                    <div class="module-icon"><i class="fa-solid fa-terminal"></i></div>
                    <div class="module-info">
                        <h3>Quantum Process</h3>
                        <p>Execute structured technical tasks to earn premium cryptographic rewards.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Right Cyborg UI Render Column -->
        <section class="hero-right">
            <div class="hud-interface">
                <div class="hud-inner"></div>
            </div>
            
            <!-- Dynamic Reactive Coding UI Component Overlay -->
            <div class="code-terminal">
                <div class="terminal-header">
                    <div class="dot"></div>
                    <div class="dot"></div>
                    <div class="dot"></div>
                    <span class="terminal-title">iitb_ambassador_node.js</span>
                </div>
                <div class="code-snippet">
                    <p><span class="code-keyword">const</span> <span class="code-var">Techfest</span> = require(<span class="code-string">'@iitb/core'</span>);</p>
                    <p><span class="code-keyword">const</span> <span class="code-var">Ambassador</span> = require(<span class="code-string">'./cyborgUser'</span>);</p>
                    <br>
                    <p><span class="code-keyword">function</span> <span class="code-var">initializeNode</span>() {</p>
                    <p>&nbsp;&nbsp;Techfest.<span class="code-var">connectNode</span>({</p>
                    <p>&nbsp;&nbsp;&nbsp;&nbsp;id: <span class="code-string">"IITB-CA-2026"</span>,</p>
                    <p>&nbsp;&nbsp;&nbsp;&nbsp;power: <span class="code-string">"MAX_CAPACITY"</span>,</p>
                    <p>&nbsp;&nbsp;&nbsp;&nbsp;skills: [<span class="code-string">"React"</span>, <span class="code-string">"Node.js"</span>, <span class="code-string">"AI Automation"</span>]</p>
                    <p>&nbsp;&nbsp;});</p>
                    <p>&nbsp;&nbsp;return <span class="code-string">"SYSTEMS ONLINE"</span>;</p>
                    <p>}</p>
                    <br>
                    <p><span class="code-keyword">export default</span> initializeNode;</p>
                </div>
            </div>
        </section>

    </main>

    <!-- --- TELEMETRY AND MATRIX METRICS FOOTER --- -->
    <footer class="telemetry-bar">
        <div class="telemetry-stats">
            <div class="stat-item">
                <span class="stat-label"><i class="fa-solid fa-bolt"></i> Synapse Speed</span>
                <span class="stat-value">165 ms</span>
            </div>
            <div class="stat-item">
                <span class="stat-label"><i class="fa-solid fa-bullseye"></i> Sync Precision</span>
                <span class="stat-value">1,404 Nodes</span>
            </div>
            <div class="stat-item">
                <span class="stat-label"><i class="fa-solid fa-lightbulb"></i> Quantum Innov.</span>
                <span class="stat-value">1,130 %</span>
            </div>
        </div>

        <div class="social-matrix">
            <a href="#" title="Instagram"><i class="fa-brands fa-instagram"></i></a>
            <a href="#" title="X (Twitter)"><i class="fa-brands fa-x-twitter"></i></a>
            <a href="#" title="LinkedIn"><i class="fa-brands fa-linkedin-in"></i></a>
            <a href="#" title="Facebook"><i class="fa-brands fa-facebook-f"></i></a>
            <a href="#" title="WhatsApp"><i class="fa-brands fa-whatsapp"></i></a>
            <a href="#" title="YouTube"><i class="fa-brands fa-youtube"></i></a>
        </div>
    </footer>

</body>
</html>
