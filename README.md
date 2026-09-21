<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CRITICAL_EXCEPTION_0x8F</title>
    <style>
        :root {
            --neon-green: #00ff66;
            --terminal-dark: #050b05;
            --alert-red: #ff3333;
            --font-mono: 'Courier New', Courier, monospace;
        }
        body {
            background-color: var(--terminal-dark);
            color: var(--neon-green);
            font-family: var(--font-mono);
            padding: 2rem;
            max-width: 800px;
            margin: 0 auto;
            overflow-x: hidden;
        }
        .glitch-header {
            font-size: 2.5rem;
            font-weight: bold;
            text-transform: uppercase;
            border-bottom: 2px solid var(--neon-green);
            padding-bottom: 10px;
            text-shadow: 0 0 10px var(--neon-green);
            animation: flicker 0.15s infinite;
        }
        .warning-box {
            border: 1px dashed var(--alert-red);
            background: rgba(255, 51, 51, 0.05);
            color: var(--alert-red);
            padding: 1.5rem;
            border-radius: 4px;
            margin: 2rem 0;
            font-weight: bold;
            box-shadow: 0 0 15px rgba(255, 51, 51, 0.1);
        }
        .terminal-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1.5rem;
            margin: 2rem 0;
        }
        @media (max-width: 600px) { .terminal-grid { grid-template-columns: 1fr; } }
        .data-card {
            background: rgba(0, 255, 102, 0.02);
            border: 1px solid rgba(0, 255, 102, 0.2);
            padding: 1.2rem;
            border-radius: 4px;
        }
        .data-value {
            font-size: 1.8rem;
            color: #ffffff;
            text-shadow: 0 0 5px #fff;
            margin-top: 0.5rem;
        }
        .log-stream {
            background: #000;
            border: 1px solid #113311;
            padding: 1rem;
            height: 180px;
            overflow-y: auto;
            font-size: 0.9rem;
            color: #88ff88;
            border-radius: 4px;
        }
        .log-line { margin-bottom: 4px; }
        .interactive-btn {
            background: transparent;
            border: 1px solid var(--neon-green);
            color: var(--neon-green);
            padding: 10px 20px;
            font-family: var(--font-mono);
            font-size: 1rem;
            cursor: pointer;
            width: 100%;
            margin-top: 1rem;
            transition: all 0.2s ease;
        }
        .interactive-btn:hover {
            background: var(--neon-green);
            color: var(--terminal-dark);
            box-shadow: 0 0 15px var(--neon-green);
        }
        @keyframes flicker {
            0% { opacity: 0.98; }
            50% { opacity: 1; }
            100% { opacity: 0.99; }
        }
    </style>
</head>
<body>

    <!-- Self-Aware Terminal Header -->
    <div class="glitch-header">⚠️ CAUTION: MEMORY_LEAK</div>

    <!-- Shock Element Warning Box -->
    <div class="warning-box">
        [!] UNEXPECTED HOST OVERRIDE DETECTED.<br>
        This README file has executed an asynchronous isolation protocol. Your browser runtime environment is currently simulating an isolated hardware container.
    </div>

    <p>The metrics below are actively streaming from a simulated background matrix loop. Do not refresh this page while synchronization is active.</p>

    <!-- Real-time Random Data Fields -->
    <div class="terminal-grid">
        <div class="data-card">
            <div>Quantum Entropy Delta</div>
            <div class="data-value" id="entropy-val">0.0000</div>
        </div>
        <div class="data-card">
            <div>Simulated Threat Index</div>
            <div class="data-value" id="threat-val" style="color: var(--alert-red);">0.0%</div>
        </div>
    </div>

    <!-- Live Updating Terminal Activity Feed -->
    <h3>🛰️ Live Sub-Layer Log Stream</h3>
    <div class="log-stream" id="terminal-log">
        <div class="log-line">[SYS] Core virtualization layer spinning up...</div>
        <div class="log-line">[SYS] Successfully mounted sandbox environment.</div>
    </div>

    <!-- The Climax Interactive Trigger -->
    <button class="interactive-btn" onclick="triggerMeltdown()">MANUALLY PURGE BUFFER CACHE</button>

    <script>
        // Continuously generate unique, chaotic random metrics to shock the viewer
        setInterval(() => {
            document.getElementById('entropy-val').innerText = (Math.random() * 9.9999).toFixed(4);
            document.getElementById('threat-val').innerText = (Math.random() * 100).toFixed(1) + '%';
            
            const logBox = document.getElementById('terminal-log');
            const processes = ['NET_PING', 'MEM_ALLOC', 'HEX_DUMP', 'CYC_CHECK', 'SIG_INT'];
            const hex = Math.floor(Math.random()*16777215).toString(16).toUpperCase();
            
            const newLine = document.createElement('div');
            newLine.className = 'log-line';
            newLine.innerText = `[${processes[Math.floor(Math.random()*processes.length)]}] Processing memory block 0x${hex}... OK`;
            
            logBox.appendChild(newLine);
            logBox.scrollTop = logBox.scrollHeight;
            
            if(logBox.children.length > 20) {
                logBox.removeChild(logBox.children[0]);
            }
        }, 900);

        // Sudden, dramatic payload effect when clicked
        function triggerMeltdown() {
            alert("⚠️ SYSTEM HALT\n\nBuffer purge initiated. The matrix simulator will now intentionally crash this mock interface thread.");
            document.body.innerHTML = `
                <div style="color: #ff3333; text-align: center; margin-top: 20vh; font-family: monospace;">
                    <h1 style="font-size: 4rem; margin-bottom: 0;">FATAL CORRUPTION</h1>
                    <p style="font-size: 1.5rem;">The local environment structure has collapsed entirely.</p>
                    <p style="color: #666;">(Refresh the preview frame to reconstruct reality.)</p>
                </div>
            `;
            document.body.style.backgroundColor = "#000000";
        }
    </script>

</body>
</html>
