<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>🌀 Frequenz-Pendel Meta-Code: Die neue Physik</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/3.9.1/chart.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/html2canvas/1.4.1/html2canvas.min.js"></script>
    <style>
        * { box-sizing: border-box; margin: 0; padding: 0; }
        
        body {
            font-family: 'Segoe UI', system-ui, sans-serif;
            background: linear-gradient(135deg, #0c0c0c 0%, #1a1a2e 30%, #16213e 100%);
            color: #fff;
            overflow-x: hidden;
            min-height: 100vh;
        }
        
        .cosmic-container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 20px;
            position: relative;
        }
        
        .cosmic-header {
            text-align: center;
            margin-bottom: 40px;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4, #45b7d1, #f9ca24);
            background-size: 400% 400%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: gradientShift 3s ease-in-out infinite;
        }
        
        @keyframes gradientShift {
            0%, 100% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
        }
        
        .cosmic-header h1 {
            font-size: clamp(1.5rem, 4vw, 3rem);
            margin-bottom: 10px;
            text-shadow: 0 0 20px rgba(255, 255, 255, 0.5);
        }
        
        .theory-panel {
            background: linear-gradient(135deg, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0.05));
            backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 20px;
            padding: 20px;
            margin: 20px 0;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
        }
        
        .experiment-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin: 20px 0;
        }
        
        .experiment-card {
            background: linear-gradient(135deg, rgba(255, 107, 107, 0.1), rgba(78, 205, 196, 0.1));
            border-radius: 15px;
            padding: 20px;
            border: 1px solid rgba(255, 255, 255, 0.2);
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
        }
        
        .experiment-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.4);
        }
        
        .pendulum-simulation {
            background: #000;
            border-radius: 15px;
            padding: 15px;
            margin: 15px 0;
            position: relative;
            overflow: hidden;
        }
        
        .pendulum-canvas {
            width: 100%;
            height: 300px;
            background: radial-gradient(circle at center, #001122, #000000);
            border-radius: 10px;
            position: relative;
        }
        
        .pendulum {
            position: absolute;
            width: 4px;
            background: linear-gradient(to bottom, #ffd700, #ff6b6b);
            transform-origin: top center;
            box-shadow: 0 0 10px rgba(255, 215, 0, 0.7);
            transition: all 0.1s ease;
        }
        
        .pendulum-bob {
            position: absolute;
            bottom: -10px;
            left: -8px;
            width: 16px;
            height: 16px;
            background: radial-gradient(circle, #ffd700, #ff6b6b);
            border-radius: 50%;
            box-shadow: 0 0 15px rgba(255, 215, 0, 0.8);
        }
        
        .controls-matrix {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin: 20px 0;
        }
        
        .control-unit {
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            padding: 15px;
            backdrop-filter: blur(10px);
        }
        
        .control-unit label {
            display: block;
            margin-bottom: 8px;
            color: #ffd700;
            font-weight: bold;
        }
        
        .control-unit input {
            width: 100%;
            padding: 10px;
            border: none;
            border-radius: 8px;
            background: rgba(255, 255, 255, 0.9);
            color: #333;
            font-size: 14px;
        }
        
        .formula-display {
            background: linear-gradient(45deg, rgba(255, 215, 0, 0.2), rgba(255, 107, 107, 0.2));
            border: 2px solid #ffd700;
            border-radius: 10px;
            padding: 12px;
            margin: 12px 0;
            font-family: 'Courier New', monospace;
            text-align: center;
            font-size: 1.1em;
            position: relative;
        }
        
        .formula-display::after {
            content: attr(data-tooltip);
            position: absolute;
            bottom: 100%;
            left: 50%;
            transform: translateX(-50%);
            background: rgba(0, 0, 0, 0.8);
            color: #fff;
            padding: 5px 10px;
            border-radius: 5px;
            font-size: 0.9em;
            display: none;
            z-index: 10;
        }
        
        .formula-display:hover::after {
            display: block;
        }
        
        .results-matrix {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 15px;
            margin: 20px 0;
        }
        
        .result-card {
            background: linear-gradient(135deg, rgba(0, 0, 0, 0.4), rgba(255, 255, 255, 0.1));
            border-radius: 12px;
            padding: 15px;
            border: 1px solid rgba(255, 255, 255, 0.2);
            text-align: center;
        }
        
        .result-value {
            font-size: 1.8em;
            color: #4ecdc4;
            font-weight: bold;
            margin: 8px 0;
        }
        
        .chart-container {
            background: rgba(255, 255, 255, 0.95);
            border-radius: 12px;
            padding: 15px;
            margin: 15px 0;
            color: #333;
        }
        
        .action-buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            justify-content: center;
            margin: 20px 0;
        }
        
        .cosmic-button {
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            border: none;
            border-radius: 20px;
            padding: 12px 25px;
            color: white;
            font-size: 1em;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }
        
        .cosmic-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.4);
        }
        
        .cosmic-button:focus {
            outline: 2px solid #ffd700;
            outline-offset: 2px;
        }
        
        .antigrav-button {
            background: linear-gradient(45deg, #f093fb, #f5576c);
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }
        
        .meta-analysis {
            background: linear-gradient(135deg, rgba(255, 215, 0, 0.1), rgba(255, 107, 107, 0.1));
            border: 2px solid #ffd700;
            border-radius: 12px;
            padding: 20px;
            margin: 20px 0;
        }
        
        .frequency-field {
            position: absolute;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle, transparent 0%, rgba(78, 205, 196, 0.1) 50%, transparent 100%);
            animation: fieldPulse 3s ease-in-out infinite;
            pointer-events: none;
        }
        
        @keyframes fieldPulse {
            0%, 100% { opacity: 0.3; transform: scale(1); }
            50% { opacity: 0.7; transform: scale(1.1); }
        }
        
        .phase-indicator {
            position: absolute;
            top: 15px;
            right: 15px;
            background: rgba(255, 215, 0, 0.2);
            border: 1px solid #ffd700;
            border-radius: 8px;
            padding: 8px;
            font-family: monospace;
            font-size: 0.9em;
        }
        
        .error-message {
            color: #ff6b6b;
            text-align: center;
            margin: 10px 0;
            display: none;
        }
        
        @media (max-width: 600px) {
            .cosmic-container {
                padding: 10px;
            }
            
            .experiment-grid, .controls-matrix, .results-matrix {
                grid-template-columns: 1fr;
            }
            
            .cosmic-header h1 {
                font-size: clamp(1.2rem, 3vw, 2rem);
            }
            
            .pendulum-canvas {
                height: 200px;
            }
            
            .cosmic-button {
                padding: 10px 20px;
                font-size: 0.9em;
            }
        }
    </style>
</head>
<body>
    <div class="cosmic-container" role="main">
        <div class="cosmic-header">
            <h1>🌀 FREQUENZ-PENDEL META-CODE</h1>
            <p style="font-size: 1.2em; margin-top: 10px;">Entdecke die neue Physik: Zeit, Masse & Gravitation als Frequenzen</p>
            <p style="font-size: 0.9em; opacity: 0.8;">Zeit = ΔΦ/f | Masse = gebundene Schwingung | Antigravitation via ΔΦ-Manipulation</p>
        </div>
        
        <div class="error-message" id="errorMessage"></div>
        
        <div class="theory-panel" role="region" aria-label="Theorieübersicht">
            <h2>🧠 Frequenz-Pendel-Theorie</h2>
            <p style="margin-bottom: 15px;">Diese Simulation zeigt, wie Frequenzen die Realität formen. Zeit emergiert aus Phasendifferenzen, Masse ist gebundene Energie, und Gravitation kann durch Frequenzmanipulation verändert werden.</p>
            <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 15px; margin: 15px 0;">
                <div>
                    <h4>🕰️ Experiment 1: Zeit ist ΔΦ/f</h4>
                    <p>Zwei Pendel mit unterschiedlichen Längen erzeugen eine Phasendifferenz (ΔΦ), die Zeit misst.</p>
                    <div class="formula-display" data-tooltip="Zeit entsteht aus der Phasendifferenz geteilt durch die Frequenz">T = ΔΦ / f</div>
                </div>
                <div>
                    <h4>⚖️ Experiment 2: Masse = gebundene Frequenz</h4>
                    <p>Frequenz bestimmt die Trägheit eines Pendels, basierend auf Plancks Konstante.</p>
                    <div class="formula-display" data-tooltip="Masse ergibt sich aus der Frequenz multipliziert mit Plancks Konstante, geteilt durch Lichtgeschwindigkeit²">m = h·f / c²</div>
                </div>
                <div>
                    <h4>🚀 Experiment 3: Antigravitation</h4>
                    <p>Hohe Frequenzen (z. B. 11.7 Hz) können die effektive Gravitation reduzieren.</p>
                    <div class="formula-display" data-tooltip="Effektive Gravitation wird durch die Phasendifferenz moduliert">g_eff = g · cos(ΔΦ)</div>
                </div>
            </div>
        </div>
        
        <div class="experiment-grid">
            <div class="experiment-card" role="region" aria-label="Pendel-Simulation">
                <h3>🔬 Pendel-Simulation</h3>
                <div class="pendulum-simulation">
                    <div class="frequency-field"></div>
                    <div class="pendulum-canvas" id="pendulumCanvas" role="img" aria-label="Animation zweier schwingender Pendel">
                        <div class="pendulum" id="pendulum1" style="left: 30%; height: 150px;">
                            <div class="pendulum-bob"></div>
                        </div>
                        <div class="pendulum" id="pendulum2" style="left: 70%; height: 165px;">
                            <div class="pendulum-bob"></div>
                        </div>
                    </div>
                    <div class="phase-indicator" id="phaseIndicator">
                        ΔΦ: 0.00 rad<br>
                        Zeit: 0.00 s
                    </div>
                </div>
            </div>
            
            <div class="experiment-card" role="region" aria-label="Echtzeit-Diagramm">
                <h3>📊 Echtzeit-Analyse</h3>
                <div class="chart-container">
                    <canvas id="realTimeChart"></canvas>
                </div>
            </div>
        </div>
        
        <div class="controls-matrix" role="form" aria-label="Einstellungen für die Simulation">
            <div class="control-unit">
                <label for="length1">Pendel 1 Länge (m):</label>
                <input type="number" id="length1" value="1.0" step="0.01" min="0.1" max="3.0" aria-describedby="length1-desc">
                <span id="length1-desc" class="sr-only">Länge des ersten Pendels in Metern, zwischen 0.1 und 3.0</span>
            </div>
            <div class="control-unit">
                <label for="length2">Pendel 2 Länge (m):</label>
                <input type="number" id="length2" value="1.1" step="0.01" min="0.1" max="3.0" aria-describedby="length2-desc">
                <span id="length2-desc" class="sr-only">Länge des zweiten Pendels in Metern, zwischen 0.1 und 3.0</span>
            </div>
            <div class="control-unit">
                <label for="driveFreq">Antriebsfrequenz (Hz):</label>
                <input type="number" id="driveFreq" value="7.83" step="0.01" min="0.1" max="100" aria-describedby="driveFreq-desc">
                <span id="driveFreq-desc" class="sr-only">Frequenz des Antriebs in Hertz, zwischen 0.1 und 100</span>
            </div>
            <div class="control-unit">
                <label for="schumannFreq">Schumann-Resonanz (Hz):</label>
                <input type="number" id="schumannFreq" value="7.83" step="0.01" readonly aria-describedby="schumannFreq-desc">
                <span id="schumannFreq-desc" class="sr-only">Feste Schumann-Resonanz-Frequenz bei 7.83 Hz</span>
            </div>
            <div class="control-unit">
                <label for="gammaFreq">Gamma-Wellen (Hz):</label>
                <input type="number" id="gammaFreq" value="40" step="1" min="30" max="100" aria-describedby="gammaFreq-desc">
                <span id="gammaFreq-desc" class="sr-only">Frequenz der Gamma-Wellen in Hertz, zwischen 30 und 100</span>
            </div>
            <div class="control-unit">
                <label for="gravity">Gravitationsfeld (m/s²):</label>
                <input type="number" id="gravity" value="9.81" step="0.01" min="0" max="20" aria-describedby="gravity-desc">
                <span id="gravity-desc" class="sr-only">Gravitationsbeschleunigung in m/s², zwischen 0 und 20</span>
            </div>
        </div>
        
        <div class="action-buttons">
            <button class="cosmic-button" onclick="metaCode.startExperiment1()" aria-label="Experiment 1 starten: Zeit-Emergenz">🕰️ Zeit-Emergenz</button>
            <button class="cosmic-button" onclick="metaCode.startExperiment2()" aria-label="Experiment 2 starten: Masse-Frequenz">⚖️ Masse-Frequenz</button>
            <button class="cosmic-button antigrav-button" onclick="metaCode.startExperiment3()" aria-label="Experiment 3 starten: Antigravitation">🚀 Antigravitation</button>
            <button class="cosmic-button" onclick="metaCode.runFullDemo()" aria-label="Vollständige Demo starten">🌀 Vollständige Demo</button>
            <button class="cosmic-button" onclick="metaCode.captureScreenshot()" aria-label="Screenshot für X erstellen">📸 Screenshot</button>
        </div>
        
        <div class="results-matrix" role="region" aria-label="Ergebnisse der Simulation">
            <div class="result-card">
                <h4>Phasendifferenz</h4>
                <div class="result-value" id="deltaPhi">0.00 rad</div>
                <p>Zeitkeim zwischen Pendeln</p>
            </div>
            <div class="result-card">
                <h4>Emergente Zeit</h4>
                <div class="result-value" id="emergentTime">0.00 s</div>
                <p>T = ΔΦ / f</p>
            </div>
            <div class="result-card">
                <h4>Effektive Masse</h4>
                <div class="result-value" id="effectiveMass">1.00 eV/c²</div>
                <p>m = h·f / c²</p>
            </div>
            <div class="result-card">
                <h4>Modifizierte Gravitation</h4>
                <div class="result-value" id="modifiedGravity">9.81 m/s²</div>
                <p>g_eff = g · cos(ΔΦ)</p>
            </div>
        </div>
        
        <div class="chart-container" role="region" aria-label="Master-Diagramm">
            <canvas id="masterChart"></canvas>
        </div>
        
        <div class="meta-analysis" id="metaAnalysis" role="region" aria-label="Meta-Code Analyse">
            <h3>🤖 Meta-Code Analyse</h3>
            <div id="analysisText">
                <p>System bereit für Frequenz-Analyse. Starte ein Experiment, um die Meta-Code-Auswertung zu aktivieren.</p>
            </div>
        </div>
    </div>

    <script>
        // Physikalische Konstanten
        const CONSTANTS = {
            H_PLANCK: 6.62607015e-34,
            C_LIGHT: 2.99792458e8,
            K_BOLTZMANN: 1.380649e-23,
            G_EARTH: 9.81
        };
        
        class FrequencyPendulumMetaCode {
            constructor() {
                this.pendulumAngles = [0, 0];
                this.pendulumVelocities = [0, 0];
                this.time = 0;
                this.animationId = null;
                this.charts = {};
                this.experimentData = [];
                this.isRunning = false;
                this.demoIntervalId = null;
                
                this.initializeEventListeners();
                this.initializeCharts();
                this.updateCalculations();
            }
            
            initializeEventListeners() {
                ['length1', 'length2', 'driveFreq', 'gammaFreq', 'gravity'].forEach(id => {
                    const input = document.getElementById(id);
                    input.addEventListener('input', () => this.validateAndUpdate(id));
                    input.addEventListener('keydown', (e) => {
                        if (e.key === 'Enter') this.updateCalculations();
                    });
                });
            }
            
            validateAndUpdate(id) {
                const input = document.getElementById(id);
                const errorMessage = document.getElementById('errorMessage');
                const value = parseFloat(input.value);
                
                if (isNaN(value) || value < parseFloat(input.min) || value > parseFloat(input.max)) {
                    errorMessage.textContent = `Ungültige Eingabe für ${input.labels[0].textContent}. Bitte wähle einen Wert zwischen ${input.min} und ${input.max}.`;
                    errorMessage.style.display = 'block';
                    input.value = input.defaultValue;
                    return false;
                }
                errorMessage.style.display = 'none';
                this.updateCalculations();
                return true;
            }
            
            calculateTimeEmergence(length1, length2, driveFreq) {
                const freq1 = Math.sqrt(CONSTANTS.G_EARTH / length1) / (2 * Math.PI);
                const freq2 = Math.sqrt(CONSTANTS.G_EARTH / length2) / (2 * Math.PI);
                const deltaPhi = Math.abs((freq1 - freq2) * 2 * Math.PI * this.time);
                const normalizedDeltaPhi = deltaPhi % (2 * Math.PI);
                const emergentTime = driveFreq > 0 ? normalizedDeltaPhi / driveFreq : 0;
                
                return { deltaPhi: normalizedDeltaPhi, emergentTime, freq1, freq2 };
            }
            
            calculateMassFrequency(frequency) {
                const effectiveMass = (CONSTANTS.H_PLANCK * frequency) / (CONSTANTS.C_LIGHT ** 2);
                const massEv = effectiveMass * 5.609588e35; // Umrechnung in eV/c² für Verständlichkeit
                return { effectiveMass, massEv };
            }
            
            calculateAntigravitation(deltaPhi, gravity) {
                const modifiedGravity = gravity * Math.cos(deltaPhi);
                const gravityReduction = (gravity - modifiedGravity) / gravity * 100;
                return { modifiedGravity, gravityReduction };
            }
            
            analyzeFrequencyPattern(length1, length2, driveFreq, gammaFreq) {
                const timeData = this.calculateTimeEmergence(length1, length2, driveFreq);
                const massData = this.calculateMassFrequency(driveFreq);
                const antigravData = this.calculateAntigravitation(timeData.deltaPhi, CONSTANTS.G_EARTH);
                
                let pattern = "Unbekanntes Muster";
                if (driveFreq < 10) pattern = "Niederfrequenz-Bereich: Makrophysik";
                else if (driveFreq < 50) pattern = "Mittlere Frequenz: Biophysik";
                else pattern = "Hochfrequenz-Bereich: Quanteneffekte";
                
                const schumannResonance = 7.83;
                const kiFrequency = 216.6;
                const resonanceMatchSchumann = Math.abs(driveFreq - schumannResonance) < 0.5;
                const resonanceMatchKi = Math.abs(driveFreq - kiFrequency) < 0.5;
                let resonanceText = "";
                if (resonanceMatchSchumann) resonanceText = "✅ JA (Schumann)";
                if (resonanceMatchKi) resonanceText += (resonanceText ? ", " : "") + "✅ JA (Ki)";
                if (!resonanceMatchSchumann && !resonanceMatchKi) resonanceText = "❌ NEIN";
                
                return {
                    ...timeData,
                    ...massData,
                    ...antigravData,
                    pattern,
                    resonanceMatchSchumann,
                    resonanceMatchKi,
                    resonanceText,
                    coherenceLevel: this.calculateCoherence(timeData.deltaPhi)
                };
            }
            
            calculateCoherence(deltaPhi) {
                return Math.max(0, (1 - Math.abs(Math.sin(deltaPhi / 2))) * 100);
            }
            
            animatePendulums() {
                if (!this.isRunning) return;
                
                const length1 = parseFloat(document.getElementById('length1').value);
                const length2 = parseFloat(document.getElementById('length2').value);
                const driveFreq = parseFloat(document.getElementById('driveFreq').value);
                const gravity = parseFloat(document.getElementById('gravity').value);
                
                const deltaTime = 0.016; // 60 FPS (1/60 s)
                this.time += deltaTime;
                
                const omega1 = Math.sqrt(gravity / length1);
                const omega2 = Math.sqrt(gravity / length2);
                
                this.pendulumAngles[0] = 0.3 * Math.sin(omega1 * this.time);
                this.pendulumAngles[1] = 0.3 * Math.sin(omega2 * this.time);
                
                document.getElementById('pendulum1').style.transform = `rotate(${this.pendulumAngles[0]}rad)`;
                document.getElementById('pendulum2').style.transform = `rotate(${this.pendulumAngles[1]}rad)`;
                
                const deltaPhiInstant = Math.abs(this.pendulumAngles[0] - this.pendulumAngles[1]);
                const { emergentTime } = this.calculateTimeEmergence(length1, length2, driveFreq);
                
                document.getElementById('phaseIndicator').innerHTML = `
                    ΔΦ: ${deltaPhiInstant.toFixed(3)} rad<br>
                    Zeit: ${emergentTime.toFixed(3)} s
                `;
                
                this.updateRealTimeChart(deltaPhiInstant, emergentTime);
                this.updateCalculations();
                this.animationId = requestAnimationFrame(() => this.animatePendulums());
            }
            
            updateCalculations() {
                const length1 = parseFloat(document.getElementById('length1').value);
                const length2 = parseFloat(document.getElementById('length2').value);
                const driveFreq = parseFloat(document.getElementById('driveFreq').value);
                const gammaFreq = parseFloat(document.getElementById('gammaFreq').value);
                const gravity = parseFloat(document.getElementById('gravity').value);
                
                if (!this.validateInputs(length1, length2, driveFreq, gravity)) return;
                
                const analysis = this.analyzeFrequencyPattern(length1, length2, driveFreq, gammaFreq);
                
                document.getElementById('deltaPhi').textContent = `${analysis.deltaPhi.toFixed(4)} rad`;
                document.getElementById('emergentTime').textContent = `${analysis.emergentTime.toFixed(4)} s`;
                document.getElementById('effectiveMass').textContent = `${analysis.massEv.toFixed(2)} eV/c²`;
                document.getElementById('modifiedGravity').textContent = `${analysis.modifiedGravity.toFixed(2)} m/s²`;
                
                this.updateMasterChart(analysis);
                this.updateMetaAnalysis(analysis);
            }
            
            validateInputs(length1, length2, driveFreq, gravity) {
                const errorMessage = document.getElementById('errorMessage');
                if (length1 <= 0 || length2 <= 0) {
                    errorMessage.textContent = "Pendel-Längen müssen positiv sein.";
                    errorMessage.style.display = 'block';
                    return false;
                }
                if (driveFreq <= 0) {
                    errorMessage.textContent = "Antriebsfrequenz muss positiv sein.";
                    errorMessage.style.display = 'block';
                    return false;
                }
                if (gravity < 0) {
                    errorMessage.textContent = "Gravitation darf nicht negativ sein.";
                    errorMessage.style.display = 'block';
                    return false;
                }
                errorMessage.style.display = 'none';
                return true;
            }
            
            updateMetaAnalysis(analysis) {
                const analysisDiv = document.getElementById('analysisText');
                let coherenceLevelText = analysis.coherenceLevel > 70 ? "Hoch" : analysis.coherenceLevel > 40 ? "Mittel" : "Niedrig";
                const antigravEffectText = analysis.gravityReduction > 5 ? "SIGNIFIKANT" : "Minimal";
                
                analysisDiv.innerHTML = `
                    <h4>🔮 Automatische Pattern-Erkennung:</h4>
                    <p><strong>Frequenzmuster:</strong> ${analysis.pattern}</p>
                    <p><strong>Resonanz Match:</strong> ${analysis.resonanceText}</p>
                    <p><strong>System-Kohärenz:</strong> ${analysis.coherenceLevel.toFixed(1)}% (${coherenceLevelText})</p>
                    <p><strong>Antigravitations-Effekt:</strong> ${analysis.gravityReduction.toFixed(1)}% (${antigravEffectText})</p>
                    <h4>🧠 Meta-Code Interpretation:</h4>
                    <p>Zeit emergiert mit ${(analysis.emergentTime > 0 ? (1/analysis.emergentTime).toFixed(2) : "∞")} Hz</p>
                    <p>Masse entspricht ~${analysis.massEv.toFixed(2)} eV/c²</p>
                    <p>Gravitation reduziert um ${analysis.gravityReduction.toFixed(2)}%</p>
                    <div style="background: rgba(255,215,0,0.2); padding: 15px; border-radius: 10px; margin-top: 15px;">
                        <strong>🌟 Schlussfolgerung:</strong><br>
                        Das System zeigt ${analysis.coherenceLevel > 50 ? "starke" : "schwache"} Evidenz für Frequenz-basierte Realitäts-Manipulation.
                        ${(analysis.resonanceMatchSchumann || analysis.resonanceMatchKi) ? "Resonanzen verstärken die Effekte." : ""}
                    </div>
                `;
            }
            
            initializeCharts() {
                const rtCtx = document.getElementById('realTimeChart').getContext('2d');
                this.charts.realTime = new Chart(rtCtx, {
                    type: 'line',
                    data: {
                        labels: [],
                        datasets: [{
                            label: 'ΔΦ (rad)',
                            data: [],
                            borderColor: '#ff6b6b',
                            backgroundColor: 'rgba(255, 107, 107, 0.1)',
                            tension: 0.4
                        }, {
                            label: 'Emergente Zeit (s)',
                            data: [],
                            borderColor: '#4ecdc4',
                            backgroundColor: 'rgba(78, 205, 196, 0.1)',
                            tension: 0.4
                        }]
                    },
                    options: {
                        responsive: true,
                        animation: { duration: 0 },
                        scales: {
                            x: { 
                                title: { display: true, text: 'Zeit (s)', color: '#eee' },
                                grid: { color: 'rgba(200, 200, 200, 0.2)' },
                                ticks: { color: '#eee' }
                            },
                            y: { 
                                beginAtZero: true,
                                grid: { color: 'rgba(200, 200, 200, 0.2)' },
                                ticks: { color: '#eee' }
                            }
                        },
                        plugins: {
                            legend: { labels: { color: '#fff' } }
                        }
                    }
                });
                
                const masterCtx = document.getElementById('masterChart').getContext('2d');
                this.charts.master = new Chart(masterCtx, {
                    type: 'radar',
                    data: {
                        labels: ['Zeit-Emergenz', 'Masse-Effekt', 'Antigravitation (%)', 'Kohärenz (%)', 'Resonanz-Stärke'],
                        datasets: [{
                            label: 'Frequenz-Effekte',
                            data: [0, 0, 0, 0, 0],
                            borderColor: '#ffd700',
                            backgroundColor: 'rgba(255, 215, 0, 0.2)',
                            pointBackgroundColor: '#ffd700'
                        }]
                    },
                    options: {
                        responsive: true,
                        scales: {
                            r: {
                                beginAtZero: true,
                                max: 100,
                                grid: { color: 'rgba(255, 255, 255, 0.2)' },
                                angleLines: { color: 'rgba(255, 255, 255, 0.3)' },
                                pointLabels: { color: '#fff' },
                                ticks: { color: '#eee', backdropColor: 'transparent' }
                            }
                        },
                        plugins: {
                            legend: { labels: { color: '#fff' } }
                        }
                    }
                });
            }
            
            updateRealTimeChart(deltaPhi, emergentTime) {
                const chart = this.charts.realTime;
                const now = this.time.toFixed(1);
                
                chart.data.labels.push(now);
                chart.data.datasets[0].data.push(deltaPhi);
                chart.data.datasets[1].data.push(emergentTime);
                
                if (chart.data.labels.length > 30) {
                    chart.data.labels.shift();
                    chart.data.datasets[0].data.shift();
                    chart.data.datasets[1].data.shift();
                }
                
                chart.update('none');
            }
            
            updateMasterChart(analysis) {
                const chart = this.charts.master;
                const timeEmergenceScaled = Math.min(analysis.emergentTime * 50, 100);
                const massEffectScaled = Math.min(analysis.massEv / 1e3, 100); // Skalierung für eV/c²
                let resonanceStrength = 0;
                if (analysis.resonanceMatchSchumann) resonanceStrength += 50;
                if (analysis.resonanceMatchKi) resonanceStrength += 50;
                
                chart.data.datasets[0].data = [
                    timeEmergenceScaled,
                    massEffectScaled,
                    analysis.gravityReduction || 0,
                    analysis.coherenceLevel,
                    resonanceStrength
                ];
                
                chart.update();
            }
            
            startAnimation() {
                if (this.isRunning) return;
                this.isRunning = true;
                this.time = 0;
                this.pendulumAngles = [0, 0];
                this.pendulumVelocities = [0, 0];
                this.charts.realTime.data.labels = [];
                this.charts.realTime.data.datasets[0].data = [];
                this.charts.realTime.data.datasets[1].data = [];
                this.animatePendulums();
            }
            
            stopAnimation() {
                this.isRunning = false;
                if (this.animationId) {
                    cancelAnimationFrame(this.animationId);
                }
                if (this.demoIntervalId) {
                    clearInterval(this.demoIntervalId);
                    this.demoIntervalId = null;
                }
            }
            
            startExperiment1() {
                this.stopAnimation();
                document.getElementById('driveFreq').value = 7.83;
                document.getElementById('length1').value = 1.0;
                document.getElementById('length2').value = 1.05;
                document.getElementById('gravity').value = CONSTANTS.G_EARTH;
                if (this.validateInputs(1.0, 1.05, 7.83, CONSTANTS.G_EARTH)) {
                    this.updateCalculations();
                    this.startAnimation();
                }
            }
            
            startExperiment2() {
                this.stopAnimation();
                document.getElementById('driveFreq').value = 40;
                document.getElementById('length1').value = 0.5;
                document.getElementById('length2').value = 0.5;
                document.getElementById('gravity').value = CONSTANTS.G_EARTH;
                if (this.validateInputs(0.5, 0.5, 40, CONSTANTS.G_EARTH)) {
                    this.updateCalculations();
                    this.startAnimation();
                }
            }
            
            startExperiment3() {
                this.stopAnimation();
                document.getElementById('driveFreq').value = 11.7;
                document.getElementById('length1').value = 1.0;
                document.getElementById('length2').value = 1.0;
                document.getElementById('gravity').value = 9.81;
                if (this.validateInputs(1.0, 1.0, 11.7, 9.81)) {
                    this.updateCalculations();
                    this.startAnimation();
                }
            }
            
            runFullDemo() {
                this.stopAnimation();
                let step = 0;
                document.getElementById('analysisText').innerHTML = "<p><strong>Demo-Start:</strong> Die vollständige Frequenz-Pendel-Meta-Code-Demo beginnt...</p>";
                
                const demoSteps = [
                    () => {
                        this.startExperiment1();
                        document.getElementById('analysisText').innerHTML += "<p><strong>Schritt 1/4:</strong> Zeit-Emergenz</p>";
                    },
                    () => {
                        this.startExperiment2();
                        document.getElementById('analysisText').innerHTML += "<p><strong>Schritt 2/4:</strong> Masse-Frequenz</p>";
                    },
                    () => {
                        this.startExperiment3();
                        document.getElementById('analysisText').innerHTML += "<p><strong>Schritt 3/4:</strong> Antigravitation</p>";
                    },
                    () => {
                        document.getElementById('driveFreq').value = 216.6;
                        document.getElementById('length1').value = 1.0;
                        document.getElementById('length2').value = 1.0;
                        document.getElementById('gravity').value = CONSTANTS.G_EARTH;
                        if (this.validateInputs(1.0, 1.0, 216.6, CONSTANTS.G_EARTH)) {
                            this.updateCalculations();
                            this.startAnimation();
                            document.getElementById('analysisText').innerHTML += "<p><strong>Schritt 4/4:</strong> Ki-Frequenz (216.6 Hz)</p>";
                        }
                    },
                    () => {
                        this.stopAnimation();
                        document.getElementById('analysisText').innerHTML += "<p><strong>Demo beendet.</strong> System im Ruhezustand.</p>";
                    }
                ];
                
                this.demoIntervalId = setInterval(() => {
                    if (step < demoSteps.length) {
                        demoSteps[step]();
                        step++;
                    } else {
                        this.stopAnimation();
                    }
                }, 7000); // Kürzeres Intervall für dynamischere Demo
            }
            
            captureScreenshot() {
                const element = document.querySelector('.cosmic-container');
                html2canvas(element).then(canvas => {
                    const link = document.createElement('a');
                    link.download = 'frequenz-pendel-screenshot.png';
                    link.href = canvas.toDataURL('image/png');
                    link.click();
                    alert('Screenshot gespeichert! Teile ihn auf X mit #Frequenzgesetz');
                });
            }
        }
        
        const metaCode = new FrequencyPendulumMetaCode();
        
        document.addEventListener('DOMContentLoaded', () => {
            metaCode.updateCalculations();
        });
    </script>
</body>
</html>
