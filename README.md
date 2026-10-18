
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Engenharia de Resistência Cosmológica Anti-BIGs — Impressora Quântica 6D</title>
    <style>
        :root {
            --bg-dark: #02040a;
            --panel-bg: rgba(6, 12, 26, 0.92);
            --border-cyan: rgba(0, 243, 255, 0.35);
            --neon-cyan: #00f3ff;
            --neon-purple: #bd00ff;
            --neon-amber: #ffaa00;
            --neon-red: #ff0055;
            --neon-green: #00ff66;
            --text-main: #d4f0ff;
            --text-sub: #7b9cc0;
            --font-code: 'Courier New', Courier, monospace;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: var(--font-code);
            user-select: none;
        }

        body {
            background-color: var(--bg-dark);
            color: var(--text-main);
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 12px;
            overflow-x: hidden;
            background-image: 
                radial-gradient(circle at 10% 15%, rgba(0, 243, 255, 0.08) 0%, transparent 40%),
                radial-gradient(circle at 90% 85%, rgba(189, 0, 255, 0.1) 0%, transparent 45%);
        }

        header {
            text-align: center;
            width: 100%;
            max-width: 1450px;
            margin-bottom: 10px;
            border-bottom: 1px solid var(--border-cyan);
            padding-bottom: 8px;
        }

        header h1 {
            font-size: 1.45rem;
            color: var(--neon-cyan);
            text-shadow: 0 0 12px rgba(0, 243, 255, 0.6);
            letter-spacing: 2px;
        }

        header p {
            font-size: 0.78rem;
            color: var(--text-sub);
            margin-top: 3px;
        }

        .badge-header {
            display: inline-block;
            background: linear-gradient(90deg, var(--neon-cyan), var(--neon-purple));
            color: #000;
            font-weight: bold;
            font-size: 0.68rem;
            padding: 2px 10px;
            border-radius: 10px;
            margin-top: 5px;
            letter-spacing: 1px;
        }

        .app-container {
            display: grid;
            grid-template-columns: 350px 1fr 340px;
            gap: 12px;
            width: 100%;
            max-width: 1450px;
            height: calc(100vh - 105px);
            min-height: 660px;
        }

        @media (max-width: 1100px) {
            .app-container {
                grid-template-columns: 1fr;
                height: auto;
            }
        }

        .panel {
            background: var(--panel-bg);
            border: 1px solid var(--border-cyan);
            border-radius: 8px;
            padding: 12px;
            display: flex;
            flex-direction: column;
            gap: 10px;
            backdrop-filter: blur(8px);
            box-shadow: 0 0 15px rgba(0, 243, 255, 0.05);
            overflow-y: auto;
        }

        .panel-title {
            font-size: 0.82rem;
            color: var(--neon-cyan);
            border-bottom: 1px solid var(--border-cyan);
            padding-bottom: 5px;
            text-transform: uppercase;
            font-weight: bold;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        /* TABS PARA OS TRÊS BIGS */
        .scenario-tabs {
            display: flex;
            flex-direction: column;
            gap: 6px;
        }

        .tab-btn {
            background: rgba(2, 8, 20, 0.85);
            border: 1px solid rgba(0, 243, 255, 0.2);
            color: var(--text-sub);
            padding: 8px 10px;
            border-radius: 6px;
            cursor: pointer;
            font-size: 0.72rem;
            font-weight: bold;
            text-align: left;
            transition: all 0.25s;
            display: flex;
            flex-direction: column;
            gap: 2px;
        }

        .tab-btn:hover {
            border-color: var(--neon-cyan);
            color: #fff;
        }

        .tab-btn.active-freeze {
            border-color: var(--neon-cyan);
            background: rgba(0, 243, 255, 0.15);
            color: var(--neon-cyan);
            box-shadow: 0 0 10px rgba(0, 243, 255, 0.25);
        }

        .tab-btn.active-rip {
            border-color: var(--neon-amber);
            background: rgba(255, 170, 0, 0.15);
            color: var(--neon-amber);
            box-shadow: 0 0 10px rgba(255, 170, 0, 0.25);
        }

        .tab-btn.active-crunch {
            border-color: var(--neon-purple);
            background: rgba(189, 0, 255, 0.18);
            color: var(--neon-purple);
            box-shadow: 0 0 10px rgba(189, 0, 255, 0.3);
        }

        .info-card {
            background: rgba(1, 4, 12, 0.85);
            border: 1px solid rgba(0, 243, 255, 0.15);
            border-radius: 6px;
            padding: 8px 10px;
            font-size: 0.68rem;
            color: var(--text-sub);
            line-height: 1.35;
        }

        .info-card h4 {
            font-size: 0.72rem;
            color: var(--neon-cyan);
            margin-bottom: 3px;
        }

        .control-group {
            display: flex;
            flex-direction: column;
            gap: 3px;
        }

        .control-label {
            font-size: 0.68rem;
            color: var(--text-sub);
            display: flex;
            justify-content: space-between;
        }

        .control-value {
            color: var(--neon-cyan);
            font-weight: bold;
        }

        input[type="range"] {
            appearance: none;
            -webkit-appearance: none;
            width: 100%;
            height: 4px;
            background: #0a182e;
            border-radius: 2px;
            outline: none;
        }

        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background: var(--neon-cyan);
            cursor: pointer;
            box-shadow: 0 0 8px var(--neon-cyan);
        }

        .btn-action {
            background: transparent;
            border: 1px solid var(--neon-cyan);
            color: var(--neon-cyan);
            padding: 8px;
            border-radius: 5px;
            font-weight: bold;
            font-size: 0.72rem;
            cursor: pointer;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: all 0.3s;
        }

        .btn-action:hover {
            background: var(--neon-cyan);
            color: #000;
            box-shadow: 0 0 12px var(--neon-cyan);
        }

        .btn-action.purple {
            border-color: var(--neon-purple);
            color: var(--neon-purple);
        }

        .btn-action.purple:hover {
            background: var(--neon-purple);
            color: #fff;
            box-shadow: 0 0 12px var(--neon-purple);
        }

        /* CANVAS CONTAINER */
        .canvas-area {
            position: relative;
            background: #010206;
            border: 1px solid var(--border-cyan);
            border-radius: 8px;
            overflow: hidden;
            display: flex;
            flex-direction: column;
        }

        canvas {
            display: block;
            width: 100%;
            height: 100%;
        }

        .canvas-tag {
            position: absolute;
            top: 8px;
            left: 10px;
            background: rgba(0, 0, 0, 0.82);
            border: 1px solid var(--border-cyan);
            padding: 3px 8px;
            font-size: 0.65rem;
            color: var(--neon-cyan);
            border-radius: 4px;
            pointer-events: none;
            letter-spacing: 1px;
        }

        .canvas-hud {
            position: absolute;
            bottom: 8px;
            right: 10px;
            background: rgba(0, 0, 0, 0.85);
            border: 1px solid rgba(189, 0, 255, 0.4);
            padding: 5px 10px;
            font-size: 0.65rem;
            color: #b0d8ff;
            border-radius: 4px;
            pointer-events: none;
            text-align: right;
            line-height: 1.3;
        }

        /* LOG TERMINAL */
        .terminal {
            background: #010308;
            border: 1px solid rgba(0, 243, 255, 0.2);
            border-radius: 5px;
            padding: 8px;
            height: 130px;
            overflow-y: auto;
            font-size: 0.65rem;
            color: #88c5ff;
            display: flex;
            flex-direction: column;
            gap: 3px;
        }

        .log-line { line-height: 1.25; }
        .log-line.cyan { color: var(--neon-cyan); }
        .log-line.amber { color: var(--neon-amber); }
        .log-line.purple { color: var(--neon-purple); }
        .log-line.green { color: var(--neon-green); }
        .log-line.red { color: var(--neon-red); }

        .stat-grid {
            display: flex;
            flex-direction: column;
            gap: 4px;
            font-size: 0.66rem;
        }

        .stat-row {
            display: flex;
            justify-content: space-between;
        }
    </style>
</head>
<body>

    <header>
        <h1>SISTEMA DE RESISTÊNCIA COSMOLÓGICA ANTI-BIGs</h1>
        <p>Estabilização do Espaço-Tempo & Ancoragem Dimensional Multiversal via MHD, SAMS, SROS e Impressora 6D</p>
        <span class="badge-header" id="headerModeTag">CENÁRIO 1: BIG FREEZE — ESTABILIZAÇÃO POR SÓIS DE SINGULARIDADE</span>
    </header>

    <div class="app-container">
        <!-- PAINEL ESQUERDO: SELEÇÃO DE AMEAÇA COSMOLÓGICA -->
        <div class="panel">
            <div class="panel-title">
                <span>1. TIPO DE AMEAÇA CÓSMICA</span>
            </div>

            <div class="scenario-tabs">
                <div class="tab-btn active-freeze" id="tabFreeze" onclick="selectScenario('freeze')">
                    <span>❄️ 1. BIG FREEZE (Morte Térmica)</span>
                    <span style="font-size:0.6rem; opacity:0.8;">Zero Absoluto, Estrelas Mortas & Entropia Máxima</span>
                </div>

                <div class="tab-btn" id="tabRip" onclick="selectScenario('rip')">
                    <span>💥 2. BIG RIP (O Grande Rasgo)</span>
                    <span style="font-size:0.6rem; opacity:0.8;">Expansão Acelerada & Esfarelamento Subatômico</span>
                </div>

                <div class="tab-btn" id="tabCrunch" onclick="selectScenario('crunch')">
                    <span>🌌 3. BIG CRUNCH (O Grande Colapso)</span>
                    <span style="font-size:0.6rem; opacity:0.8;">Gravidade Total, Implosão & Singularidade Quente</span>
                </div>
            </div>

            <div class="info-card">
                <h4 id="infoTitle">SISTEMA ATIVO: SÓIS DE SINGULARIDADE 6D</h4>
                <p id="infoDesc">
                    A Impressora 6D imprime Sóis Artificiais de Singularidade. O Reator HD-MHD excita o vácuo quântico, alimentando cidades protegidas pela bolha térmica SAMS sem depender de estrelas moribundas.
                </p>
            </div>

            <div class="panel-title" style="margin-top: 4px;">
                <span>MODULADORES MÉTRICOS</span>
            </div>

            <div class="control-group">
                <div class="control-label">
                    <span id="slider1Label">Excitação do Vácuo Quântico:</span>
                    <span class="control-value" id="valSlider1">85.0%</span>
                </div>
                <input type="range" id="slider1" min="1" max="100" value="85">
            </div>

            <div class="control-group">
                <div class="control-label">
                    <span id="slider2Label">Confinamento de Bolha SAMS:</span>
                    <span class="control-value" id="valSlider2">99.9%</span>
                </div>
                <input type="range" id="slider2" min="1" max="100" value="99">
            </div>

            <button class="btn-action" id="btnToggleShield" onclick="toggleActiveDefense()">ATIVAR DEFESA ATIVA (ESTABILIZAÇÃO)</button>
            <button class="btn-action purple" id="btnMultiverseSalt" onclick="triggerMultiverseEscape()" style="display:none;">EJETAR CIVILIZAÇÃO VIA SROS MULTIVERSO</button>
        </div>

        <!-- PAINEL CENTRAL: VISUALIZADOR CANVAS 2D -->
        <div class="canvas-area">
            <div class="canvas-tag" id="canvasTagText">VISOR MÉTRICO — BIG FREEZE: SÓIS ARTIFICIAIS & BOLHA TÉRMICA SAMS</div>
            <canvas id="cosmoCanvas"></canvas>
            <div class="canvas-hud" id="hudText">
                ENTROPIA EXTERNA: MÁXIMA (0.0001 K)<br>
                ENERGIA DO VÁCUO HD-MHD: 12.8 YottaWatts<br>
                ISOLAMENTO DA BOLHA SAMS: ESTÁVEL
            </div>
        </div>

        <!-- PAINEL DIREITO: TELEMETRIA & TELECONVERSÃO SROS -->
        <div class="panel">
            <div class="panel-title">
                <span>TELEMETRIA DA BOLHA SAMS</span>
            </div>

            <div class="info-card">
                <h4>STATUS DA CIVILIZAÇÃO</h4>
                <div class="stat-grid">
                    <div class="stat-row">
                        <span>Temperatura Interna:</span>
                        <span id="statTemp" style="color:var(--neon-cyan)">298.15 K (25°C)</span>
                    </div>
                    <div class="stat-row">
                        <span>Tensão Espaço-Tempo:</span>
                        <span id="statTension" style="color:var(--neon-green)">1.0000 Norm</span>
                    </div>
                    <div class="stat-row">
                        <span>Ancoragem de Brana:</span>
                        <span id="statBrane" style="color:var(--neon-purple)">6D Hilbert Sync</span>
                    </div>
                    <div class="stat-row">
                        <span>Taxa de Sobrevivência:</span>
                        <span id="statSurvive" style="color:var(--neon-green)">100.0%</span>
                    </div>
                </div>
            </div>

            <div class="panel-title" style="margin-top: 8px;">
                <span>LOGS DA IMPRESSORA 6D & SROS</span>
            </div>

            <div class="terminal" id="terminalLog">
                <div class="log-line cyan">> Sistema de Análise Cosmológica ativado.</div>
                <div class="log-line green">> Bolha de Ruído Quântico Zero estabelecida pelo SAMS.</div>
            </div>
        </div>
    </div>

    <script>
        const canvas = document.getElementById('cosmoCanvas');
        const ctx = canvas.getContext('2d');

        // ELEMENTOS DO DOM
        const tabFreeze = document.getElementById('tabFreeze');
        const tabRip = document.getElementById('tabRip');
        const tabCrunch = document.getElementById('tabCrunch');

        const headerModeTag = document.getElementById('headerModeTag');
        const infoTitle = document.getElementById('infoTitle');
        const infoDesc = document.getElementById('infoDesc');
        const canvasTagText = document.getElementById('canvasTagText');
        const hudText = document.getElementById('hudText');

        const slider1 = document.getElementById('slider1');
        const slider2 = document.getElementById('slider2');
        const slider1Label = document.getElementById('slider1Label');
        const slider2Label = document.getElementById('slider2Label');
        const valSlider1 = document.getElementById('valSlider1');
        const valSlider2 = document.getElementById('valSlider2');

        const btnToggleShield = document.getElementById('btnToggleShield');
        const btnMultiverseSalt = document.getElementById('btnMultiverseSalt');

        const statTemp = document.getElementById('statTemp');
        const statTension = document.getElementById('statTension');
        const statBrane = document.getElementById('statBrane');
        const statSurvive = document.getElementById('statSurvive');
        const terminalLog = document.getElementById('terminalLog');

        // ESTADO INTERNO DA SIMULAÇÃO
        let currentScenario = 'freeze'; // 'freeze', 'rip', 'crunch'
        let isDefenseActive = true;
        let isMultiverseEscaped = false;

        let particles = [];
        let stars = [];
        let ripGridLines = [];
        let crunchRadius = 0;

        function resizeCanvas() {
            canvas.width = canvas.parentElement.clientWidth;
            canvas.height = canvas.parentElement.clientHeight;
            initElements();
        }
        window.addEventListener('resize', resizeCanvas);

        function logMsg(msg, colorClass = 'cyan') {
            const entry = document.createElement('div');
            entry.className = `log-line ${colorClass}`;
            const time = new Date().toLocaleTimeString();
            entry.textContent = `[${time}] ${msg}`;
            terminalLog.appendChild(entry);
            terminalLog.scrollTop = terminalLog.scrollHeight;
        }

        // SLIDERS LISTENERS
        slider1.addEventListener('input', (e) => {
            if (currentScenario === 'freeze') valSlider1.textContent = e.target.value + '.0%';
            else if (currentScenario === 'rip') valSlider1.textContent = (e.target.value * 12.5).toFixed(1) + ' Tesla-SAMS';
            else valSlider1.textContent = (e.target.value * 0.1).toFixed(1) + ' Energy-Casimir';
        });

        slider2.addEventListener('input', (e) => {
            valSlider2.textContent = (e.target.value * 0.99 + 1).toFixed(1) + '%';
        });

        function initElements() {
            stars = [];
            for (let i = 0; i < 120; i++) {
                stars.push({
                    x: Math.random() * canvas.width,
                    y: Math.random() * canvas.height,
                    size: Math.random() * 2 + 0.5,
                    alpha: Math.random()
                });
            }
            crunchRadius = canvas.width * 0.48;
        }

        // TROCA DE CENÁRIO
        function selectScenario(scen) {
            currentScenario = scen;
            isMultiverseEscaped = false;

            tabFreeze.className = 'tab-btn' + (scen === 'freeze' ? ' active-freeze' : '');
            tabRip.className = 'tab-btn' + (scen === 'rip' ? ' active-rip' : '');
            tabCrunch.className = 'tab-btn' + (scen === 'crunch' ? ' active-crunch' : '');

            btnMultiverseSalt.style.display = scen === 'crunch' ? 'block' : 'none';

            if (scen === 'freeze') {
                headerModeTag.textContent = 'CENÁRIO 1: BIG FREEZE — ESTABILIZAÇÃO POR SÓIS DE SINGULARIDADE';
                infoTitle.textContent = 'SÓIS ARTIFICIAIS DE SINGULARIDADE 6D';
                infoDesc.innerHTML = 'A Impressora 6D imprime "Sóis de Singularidade". O Reator HD-MHD excita o vácuo quântico, alimentando a colônia protegida pelo SAMS térmico na escuridão eterna do cosmos.';
                canvasTagText.textContent = 'VISOR MÉTRICO — BIG FREEZE: SÓIS ARTIFICIAIS & BOLHA TÉRMICA SAMS';
                slider1Label.textContent = 'Excitação do Vácuo Quântico:';
                slider2Label.textContent = 'Confinamento de Bolha SAMS:';

                statTemp.textContent = '298.15 K (25°C)';
                statTemp.style.color = 'var(--neon-cyan)';
                statTension.textContent = '1.0000 Norm';
                statTension.style.color = 'var(--neon-green)';
                statBrane.textContent = '6D Hilbert Sync';
                statSurvive.textContent = '100.0%';

                logMsg('Ameaça Selecionada: Big Freeze (Morte Térmica). Reator HD-MHD extraindo energia do vácuo quântico.', 'cyan');
            } else if (scen === 'rip') {
                headerModeTag.textContent = 'CENÁRIO 2: BIG RIP — REMENDO MÉTRICO & ATRACTOR SAMS';
                infoTitle.textContent = 'GRAVIDADE POSITIVA EXTREMA (ATRACTOR A)';
                infoDesc.innerHTML = 'O SAMS Dimensional lê a aceleração do tecido e ativa os piezoelétricos SAMS em frequência oposta. A Nave Atractor segura a bolha métrica enquanto o tecido externo esfarela.';
                canvasTagText.textContent = 'VISOR MÉTRICO — BIG RIP: ESTICAMENTO SUBATÔMICO & RETENÇÃO DE BOLHA';
                slider1Label.textContent = 'Tensão Gravitacional Atractor:';
                slider2Label.textContent = 'Remendo Métrico SAMS:';

                statTemp.textContent = '295.00 K';
                statTension.textContent = '0.0001 (Nulo na Bolha)';
                statTension.style.color = 'var(--neon-amber)';
                statBrane.textContent = '4D Lock Local';
                statSurvive.textContent = '100.0%';

                logMsg('Ameaça Selecionada: Big Rip (O Grande Rasgo). Tensão de confinamento SAMS ativada.', 'amber');
            } else {
                headerModeTag.textContent = 'CENÁRIO 3: BIG CRUNCH — ENERGIA NEGATIVA & EJEÇÃO MULTIVERSAL';
                infoTitle.textContent = 'EXPANSÃO FORÇADA & SROS MULTIVERSO';
                infoDesc.innerHTML = 'A Nave Expansora (B) projeta Energia Negativa para empurrar o super-colapso. Se o esmagamento for inevitável, consciências e memórias saltam para uma nova Brana do Multiverso.';
                canvasTagText.textContent = 'VISOR MÉTRICO — BIG CRUNCH: AMORTECEDOR CASIMIR & SALTO DIMENSIONAL';
                slider1Label.textContent = 'Injeção de Energia Negativa:';
                slider2Label.textContent = 'Frequência de Salto SROS:';

                statTemp.textContent = '310.00 K';
                statTension.textContent = '999.8 TPa (Contido)';
                statTension.style.color = 'var(--neon-purple)';
                statBrane.textContent = 'Brana Salto Pronta';
                statSurvive.textContent = '100.0%';

                logMsg('Ameaça Selecionada: Big Crunch (O Grande Colapso). Geradores Casimir preparados.', 'purple');
            }
        }

        function toggleActiveDefense() {
            isDefenseActive = !isDefenseActive;
            btnToggleShield.textContent = isDefenseActive ? 'DESATIVAR DEFESA ATIVA (ESTABILIZAÇÃO)' : 'ATIVAR DEFESA ATIVA (ESTABILIZAÇÃO)';
            btnToggleShield.style.borderColor = isDefenseActive ? 'var(--neon-cyan)' : 'var(--neon-red)';
            btnToggleShield.style.color = isDefenseActive ? 'var(--neon-cyan)' : 'var(--neon-red)';

            logMsg(`Defesa Ativa Métrica: ${isDefenseActive ? 'ATIVADA' : 'DESATIVADA'}`, isDefenseActive ? 'green' : 'red');
        }

        function triggerMultiverseEscape() {
            isMultiverseEscaped = true;
            logMsg('DISPARO DE EJEÇÃO: Consciências e Matriz de Dados SROS saltando através do buraco de minhoca para universo jovem!', 'green');
        }

        // DESENHO DO CENÁRIO 1: BIG FREEZE
        function drawFreeze() {
            const w = canvas.width;
            const h = canvas.height;
            const cx = w / 2;
            const cy = h / 2;

            // Fundo Frio/Escuro com pouquíssimas estrelas
            stars.forEach(s => {
                ctx.fillStyle = `rgba(100, 180, 255, ${s.alpha * 0.3})`;
                ctx.fillRect(s.x, s.y, s.size, s.size);
            });

            // Bolha SAMS da Cidade Humanidade
            const bubbleRadius = 140;

            if (isDefenseActive) {
                // Sol Artificial de Singularidade no Centro
                const time = Date.now() * 0.003;
                ctx.save();
                ctx.translate(cx, cy);

                // Brilho Térmico / Plasma do Vácuo
                ctx.shadowColor = '#00f3ff';
                ctx.shadowBlur = 35;
                ctx.fillStyle = '#00f3ff';
                ctx.beginPath();
                ctx.arc(0, 0, 22, 0, Math.PI * 2);
                ctx.fill();

                // Anéis de Lasers Full Duplex do SROS
                ctx.strokeStyle = '#ffffff';
                ctx.lineWidth = 1.5;
                for (let i = 0; i < 3; i++) {
                    ctx.beginPath();
                    ctx.ellipse(0, 0, 45 + i * 15, 18 + i * 5, time * (i % 2 === 0 ? 1 : -1), 0, Math.PI * 2);
                    ctx.stroke();
                }

                // Cidade / Estrutura Humana
                ctx.fillStyle = '#ffffff';
                for (let a = 0; a < 8; a++) {
                    const ang = (a * Math.PI / 4) + time * 0.2;
                    const bx = Math.cos(ang) * 85;
                    const by = Math.sin(ang) * 85;
                    ctx.fillRect(bx - 4, by - 4, 8, 8);
                }

                ctx.restore();

                // Borda da Bolha Térmica SAMS
                ctx.strokeStyle = '#00ff66';
                ctx.lineWidth = 3;
                ctx.shadowColor = '#00ff66';
                ctx.shadowBlur = 20;
                ctx.beginPath();
                ctx.arc(cx, cy, bubbleRadius, 0, Math.PI * 2);
                ctx.stroke();
                ctx.shadowBlur = 0;
            } else {
                // Sem Defesa: Congelamento Total
                ctx.fillStyle = 'rgba(0, 100, 255, 0.4)';
                ctx.font = '16px Courier New';
                ctx.fillText('BOLHA COLAPSADA: CONGELAMENTO TÉRMICO', cx - 180, cy);
            }

            hudText.innerHTML = `
                ENTROPIA EXTERNA: <span style="color:#00f3ff;">MÁXIMA (0.0001 K)</span><br>
                SÓIS DE SINGULARIDADE: ${isDefenseActive ? 'ATIVOS (EXCITAÇÃO DO VÁCUO)' : 'INATIVOS'}<br>
                TEMPERATURA DA BOLHA: ${isDefenseActive ? '298.15 K (ESTÁVEL)' : '0.001 K'}
            `;
        }

        // DESENHO DO CENÁRIO 2: BIG RIP
        function drawRip() {
            const w = canvas.width;
            const h = canvas.height;
            const cx = w / 2;
            const cy = h / 2;
            const time = Date.now() * 0.002;

            // Malha do Espaço-Tempo Sendo Esticada
            ctx.strokeStyle = 'rgba(255, 170, 0, 0.25)';
            ctx.lineWidth = 1;
            const ripStretch = (Math.sin(time) + 1) * 20;

            for (let x = 0; x < w; x += 35 + ripStretch) {
                ctx.beginPath(); ctx.moveTo(x, 0); ctx.lineTo(x, h); ctx.stroke();
            }

            // Bolha Métrica Estabilizada pelo Atractor (Nave A)
            if (isDefenseActive) {
                // Bolha Central Não Esticada
                ctx.save();
                ctx.translate(cx, cy);

                // Campo do Atractor (Gravidade Positiva Extrema)
                ctx.shadowColor = '#ffaa00';
                ctx.shadowBlur = 25;
                ctx.strokeStyle = '#ffaa00';
                ctx.lineWidth = 3;
                ctx.beginPath();
                ctx.arc(0, 0, 110, 0, Math.PI * 2);
                ctx.stroke();

                // Terra / Colônia em Segurança
                ctx.fillStyle = '#00f3ff';
                ctx.beginPath(); ctx.arc(0, 0, 30, 0, Math.PI * 2); ctx.fill();

                ctx.restore();
            }

            hudText.innerHTML = `
                TAXA DE EXPANSÃO (ENERGIA ESCURA): <span style="color:#ffaa00;">CRÍTICA ($\infty$)</span><br>
                REMENDO MÉTRICO SAMS: ${isDefenseActive ? 'RETENDO TECIDO LOCAL' : 'RASGADO'}<br>
                INTEGRIDADE SUBATÔMICA: ${isDefenseActive ? '100.0% (INTACTA)' : 'DESINTEGRANDO'}
            `;
        }

        // DESENHO DO CENÁRIO 3: BIG CRUNCH
        function drawCrunch() {
            const w = canvas.width;
            const h = canvas.height;
            const cx = w / 2;
            const cy = h / 2;

            if (!isMultiverseEscaped) {
                // Colapso Gravitacional Entrando
                crunchRadius = Math.max(90, crunchRadius - 0.2);
            }

            // Anel do Colapso Cósmico
            ctx.strokeStyle = '#ff0055';
            ctx.lineWidth = 4;
            ctx.shadowColor = '#ff0055';
            ctx.shadowBlur = 30;
            ctx.beginPath();
            ctx.arc(cx, cy, crunchRadius, 0, Math.PI * 2);
            ctx.stroke();
            ctx.shadowBlur = 0;

            // Se Ejetado para o Multiverso
            if (isMultiverseEscaped) {
                // Fenda de Buraco de Minhoca Aberta na 6ª Dimensão
                ctx.strokeStyle = '#bd00ff';
                ctx.lineWidth = 3;
                ctx.shadowColor = '#bd00ff';
                ctx.shadowBlur = 30;
                ctx.beginPath();
                ctx.arc(cx, cy, 45, 0, Math.PI * 2);
                ctx.stroke();

                ctx.fillStyle = '#ffffff';
                ctx.font = '12px Courier New';
                ctx.fillText('CIVILIZAÇÃO SEGURA EM NOVO UNIVERSO (6D)', cx - 140, cy + 85);
            } else if (isDefenseActive) {
                // Amortecedores Casimires de Energia Negativa (Nave B Expansora)
                ctx.strokeStyle = '#bd00ff';
                ctx.lineWidth = 2;
                ctx.beginPath();
                ctx.arc(cx, cy, 75, 0, Math.PI * 2);
                ctx.stroke();

                ctx.fillStyle = '#bd00ff';
                ctx.beginPath(); ctx.arc(cx, cy, 18, 0, Math.PI * 2); ctx.fill();
            }

            hudText.innerHTML = `
                DENSIDADE COSMOLÓGICA: <span style="color:#bd00ff;">MÁXIMA (SINGULARIDADE)</span><br>
                ZONA DE EXPANSÃO FORÇADA: ${isDefenseActive ? 'ATIVA (ENERGIA NEGATIVA)' : 'INATIVA'}<br>
                STATUS MULTIVERSO: ${isMultiverseEscaped ? '<span style="color:#00ff66;">EJETADO COM SUCESSO</span>' : 'AGUARDANDO SALTO'}
            `;
        }

        // LOOP PRINCIPAL DE RENDERIZAÇÃO
        function render() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);

            if (currentScenario === 'freeze') drawFreeze();
            else if (currentScenario === 'rip') drawRip();
            else drawCrunch();

            requestAnimationFrame(render);
        }

        // INICIALIZAÇÃO
        resizeCanvas();
        render();
    </script>
</body>
</html>
