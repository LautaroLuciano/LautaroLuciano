<!DOCTYPE html>
<html lang="es" class="dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lautaro Castro - GitHub Profile README Generator</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        brand: {
                            purple: '#AA9BEF',
                            dark: '#0d1117',
                            card: '#161b22',
                            border: '#30363d',
                            accent: '#58a6ff'
                        }
                    },
                    fontFamily: {
                        mono: ['JetBrains Mono', 'Fira Code', 'Consolas', 'monospace'],
                        sans: ['Inter', 'system-ui', 'sans-serif']
                    }
                }
            }
        }
    </script>
    <!-- Google Fonts & Icons -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        body {
            background-color: #0d1117;
            color: #c9d1d9;
            font-family: 'Inter', sans-serif;
        }

        /* Custom scrollbar for webkit */
        ::-webkit-scrollbar {
            width: 8px;
            height: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #0d1117;
        }
        ::-webkit-scrollbar-thumb {
            background: #30363d;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #58a6ff;
        }

        .code-editor {
            font-family: 'JetBrains Mono', monospace;
            tab-size: 2;
        }

        .markdown-body h1, .markdown-body h2 {
            border-bottom: 1px solid #30363d;
            padding-bottom: 0.3em;
        }
    </style>
</head>
<body class="min-h-screen flex flex-col bg-brand-dark text-slate-200">

    <header class="border-b border-brand-border bg-brand-card/80 backdrop-blur sticky top-0 z-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-16 flex items-center justify-between">
            <div class="flex items-center space-x-3">
                <i class="fab fa-github text-2xl text-brand-purple"></i>
                <div>
                    <h1 class="text-sm font-bold text-white font-mono tracking-tight">PROFILE.MD GENERATOR</h1>
                    <p class="text-xs text-slate-400">Lautaro Castro &bull; Hazard Forecaster</p>
                </div>
            </div>
            
            <div class="flex items-center space-x-3">
                <button id="copyBtn" class="bg-brand-purple hover:bg-purple-400 text-slate-950 font-semibold px-4 py-2 rounded-lg text-xs font-mono transition-all flex items-center space-x-2 shadow-lg shadow-brand-purple/20 active:scale-95">
                    <i class="fas fa-copy"></i>
                    <span>COPIAR CÓDIGO</span>
                </button>
            </div>
        </div>
    </header>

    <main class="flex-grow max-w-7xl w-full mx-auto px-4 sm:px-6 lg:px-8 py-6 grid grid-cols-1 lg:grid-cols-12 gap-6">
        
        <!-- Left Sidebar: Controls & Live Animation canvas -->
        <div class="lg:col-span-5 flex flex-col space-y-6">
            
            <!-- Animated Constellation Canvas Container -->
            <div class="bg-brand-card border border-brand-border rounded-xl p-4 flex flex-col relative overflow-hidden">
                <div class="flex items-center justify-between mb-3">
                    <span class="text-xs font-mono font-semibold text-brand-purple flex items-center">
                        <i class="fas fa-atom mr-2 animate-spin" style="animation-duration: 8s;"></i> VECTOR CONSTELLATION
                    </span>
                    <span class="text-[10px] font-mono text-slate-500">CANVAS 2D &bull; INTERACTIVE</span>
                </div>
                
                <div class="relative w-full h-[280px] bg-black/60 rounded-lg border border-brand-border/60 overflow-hidden flex items-center justify-center">
                    <canvas id="faceCanvas" class="w-full h-full cursor-crosshair"></canvas>
                    <div class="absolute bottom-2 left-2 text-[10px] font-mono text-slate-400 bg-brand-dark/80 px-2 py-1 rounded border border-brand-border">
                        Puntero: Dispersión | Clic: Fragmentación
                    </div>
                </div>
            </div>

            <!-- Customization Form -->
            <div class="bg-brand-card border border-brand-border rounded-xl p-5 space-y-4">
                <h3 class="text-xs font-mono font-semibold text-slate-300 uppercase tracking-wider flex items-center">
                    <i class="fas fa-sliders-h mr-2 text-brand-purple"></i> Parámetros del Perfil
                </h3>

                <div class="space-y-3 font-mono text-xs">
                    <div>
                        <label class="block text-slate-400 mb-1">GitHub Username</label>
                        <input type="text" id="inputGithub" value="lautarocastro" class="w-full bg-brand-dark border border-brand-border rounded-lg px-3 py-2 text-slate-200 focus:outline-none focus:border-brand-purple transition-colors">
                    </div>
                    
                    <div>
                        <label class="block text-slate-400 mb-1">LinkedIn Username</label>
                        <input type="text" id="inputLinkedin" value="lautaro-castro" class="w-full bg-brand-dark border border-brand-border rounded-lg px-3 py-2 text-slate-200 focus:outline-none focus:border-brand-purple transition-colors">
                    </div>

                    <div>
                        <label class="block text-slate-400 mb-1">X (Twitter) Username</label>
                        <input type="text" id="inputX" value="lautarocastro" class="w-full bg-brand-dark border border-brand-border rounded-lg px-3 py-2 text-slate-200 focus:outline-none focus:border-brand-purple transition-colors">
                    </div>

                    <div>
                        <label class="block text-slate-400 mb-1">Email de contacto</label>
                        <input type="text" id="inputEmail" value="contacto@lautarocastro.com" class="w-full bg-brand-dark border border-brand-border rounded-lg px-3 py-2 text-slate-200 focus:outline-none focus:border-brand-purple transition-colors">
                    </div>

                    <div>
                        <label class="block text-slate-400 mb-1">URL Foto Animada (Avatar)</label>
                        <input type="text" id="inputAvatar" value="https://raw.githubusercontent.com/lautarocastro/lautarocastro/main/assets/constellation-avatar.gif" class="w-full bg-brand-dark border border-brand-border rounded-lg px-3 py-2 text-slate-200 focus:outline-none focus:border-brand-purple transition-colors">
                    </div>
                </div>
            </div>

        </div>

        <!-- Right Column: Code Editor & Live Preview -->
        <div class="lg:col-span-7 flex flex-col space-y-4">
            
            <!-- View Tabs -->
            <div class="flex items-center justify-between border-b border-brand-border pb-2">
                <div class="flex space-x-2">
                    <button id="tabCode" class="px-4 py-2 bg-brand-card text-brand-purple border border-brand-border rounded-t-lg font-mono text-xs font-semibold flex items-center space-x-2">
                        <i class="fas fa-code"></i>
                        <span>CÓDIGO MARKDOWN</span>
                    </button>
                    <button id="tabPreview" class="px-4 py-2 bg-transparent text-slate-400 hover:text-slate-200 rounded-t-lg font-mono text-xs font-semibold flex items-center space-x-2 transition-colors">
                        <i class="fas fa-eye"></i>
                        <span>VISTA PREVIA</span>
                    </button>
                </div>
            </div>

            <!-- Code Editor View -->
            <div id="codeContainer" class="flex-grow flex flex-col bg-brand-card border border-brand-border rounded-xl overflow-hidden min-h-[500px]">
                <div class="bg-brand-dark/50 px-4 py-2 border-b border-brand-border flex items-center justify-between font-mono text-xs text-slate-500">
                    <span>README.md</span>
                    <span>UTF-8</span>
                </div>
                <textarea id="markdownOutput" class="w-full flex-grow bg-transparent p-4 text-slate-200 code-editor text-xs leading-relaxed focus:outline-none resize-none border-none" readonly></textarea>
            </div>

            <!-- Live Preview View (Hidden by default) -->
            <div id="previewContainer" class="hidden flex-grow bg-brand-card border border-brand-border rounded-xl p-6 overflow-y-auto max-h-[600px] space-y-6 text-sm">
                
                <div class="text-center space-y-4">
                    <img id="prevAvatar" src="" alt="Avatar" class="w-32 h-32 rounded-full mx-auto border-2 border-brand-purple/40 shadow-xl object-cover bg-black">
                    
                    <div>
                        <h2 class="text-xl font-bold font-mono text-brand-purple">Lautaro Castro</h2>
                        <p class="text-xs font-mono text-slate-400 mt-1">Hazard Forecaster &bull; Early Warning Systems &bull; Data & Risk Analysis</p>
                    </div>

                    <div class="flex justify-center space-x-2 pt-2">
                        <span class="bg-blue-600/20 text-blue-400 border border-blue-500/30 text-xs px-3 py-1 rounded font-mono"><i class="fab fa-linkedin mr-1"></i> LinkedIn</span>
                        <span class="bg-slate-800 text-slate-300 border border-slate-700 text-xs px-3 py-1 rounded font-mono"><i class="fab fa-x-twitter mr-1"></i> X</span>
                        <span class="bg-purple-900/20 text-purple-300 border border-purple-500/30 text-xs px-3 py-1 rounded font-mono"><i class="fas fa-envelope mr-1"></i> Email</span>
                    </div>
                </div>

                <hr class="border-brand-border">

                <div class="space-y-3">
                    <h3 class="font-bold text-base text-white">This is me :)</h3>
                    <p class="text-slate-300 leading-relaxed">
                        Hi, I'm <strong>Lautaro Castro</strong>, Hazard Forecaster. I specialize in severe weather prediction, natural hazards, and modeling impact to protect communities and critical infrastructure.
                    </p>
                    <ul class="list-disc list-inside space-y-1 text-slate-300">
                        <li>🌩️ <strong>Hazard Forecaster:</strong> Analyzing meteorological, seismic, and hydrological data to deliver precise early warnings.</li>
                        <li>📊 <strong>Predictive Impact Modeling & Risk Assessment:</strong> Quantifying potential impacts before disaster strikes.</li>
                        <li>🗺️ <strong>GIS & Geospatial Analysis:</strong> Turning raw spatial data into actionable intelligence.</li>
                    </ul>
                </div>

                <hr class="border-brand-border">

                <div class="text-center space-y-3">
                    <h3 class="font-mono text-xs font-semibold uppercase text-slate-400">My Stack</h3>
                    <div class="flex flex-wrap justify-center gap-2 font-mono text-xs text-brand-purple">
                        <span class="bg-brand-dark px-3 py-1 rounded border border-brand-border">Python</span>
                        <span class="bg-brand-dark px-3 py-1 rounded border border-brand-border">R</span>
                        <span class="bg-brand-dark px-3 py-1 rounded border border-brand-border">PostGIS</span>
                        <span class="bg-brand-dark px-3 py-1 rounded border border-brand-border">QGIS</span>
                        <span class="bg-brand-dark px-3 py-1 rounded border border-brand-border">Docker</span>
                        <span class="bg-brand-dark px-3 py-1 rounded border border-brand-border">AWS</span>
                    </div>
                </div>

            </div>

        </div>

    </main>

    <!-- Notification Toast -->
    <div id="toast" class="fixed bottom-6 right-6 bg-emerald-500 text-slate-950 px-4 py-2.5 rounded-lg font-mono text-xs font-bold shadow-2xl transition-all opacity-0 translate-y-4 pointer-events-none flex items-center space-x-2">
        <i class="fas fa-check-circle"></i>
        <span id="toastMsg">¡Código copiado al portapapeles!</span>
    </div>

    <script>
        // --- 1. CANVAS CONSTELLATION ANIMATION LOGIC ---
        const canvas = document.getElementById('faceCanvas');
        const ctx = canvas.getContext('2d');

        function resizeCanvas() {
            canvas.width = canvas.parentElement.clientWidth;
            canvas.height = canvas.parentElement.clientHeight;
        }
        resizeCanvas();
        window.addEventListener('resize', resizeCanvas);

        let mouse = { x: -1000, y: -1000, radius: 80 };

        canvas.addEventListener('mousemove', (e) => {
            const rect = canvas.getBoundingClientRect();
            mouse.x = e.clientX - rect.left;
            mouse.y = e.clientY - rect.top;
        });

        canvas.addEventListener('mouseleave', () => {
            mouse.x = -1000;
            mouse.y = -1000;
        });

        // Generate Nodes forming face outline
        let nodes = [];
        function initNodes() {
            nodes = [];
            const cx = canvas.width / 2;
            const cy = canvas.height / 2 - 10;
            const scale = Math.min(canvas.width, canvas.height) * 0.65;

            function addP(nx, ny, isFragment = false) {
                nodes.push({
                    baseX: cx + nx * scale,
                    baseY: cy + ny * scale,
                    x: cx + nx * scale + (Math.random() - 0.5) * 20,
                    y: cy + ny * scale + (Math.random() - 0.5) * 20,
                    vx: 0,
                    vy: 0,
                    isFragment: isFragment,
                    driftX: isFragment ? (Math.random() * 0.8 + 0.2) : 0,
                    driftY: isFragment ? (Math.random() - 0.5) * 0.4 : 0
                });
            }

            // Head contour
            for (let a = 0; a < Math.PI * 2; a += 0.12) {
                let rx = 0.22 * Math.cos(a);
                let ry = 0.30 * Math.sin(a);
                addP(rx, ry);
            }
            // Eyes
            [-0.08, 0.08].forEach(ex => {
                for (let a = 0; a < Math.PI * 2; a += 0.5) {
                    addP(ex + Math.cos(a) * 0.04, -0.05 + Math.sin(a) * 0.02);
                }
            });
            // Nose & Mouth
            for (let y = -0.03; y <= 0.05; y += 0.02) addP(0, y);
            for (let x = -0.06; x <= 0.06; x += 0.02) addP(x, 0.14);

            // Dissolving Particles to right
            for (let i = 0; i < 90; i++) {
                addP(0.1 + Math.random() * 0.35, (Math.random() - 0.5) * 0.6, true);
            }
        }
        initNodes();

        canvas.addEventListener('click', () => {
            nodes.forEach(n => {
                n.vx += (Math.random() - 0.5) * 20;
                n.vy += (Math.random() - 0.5) * 20;
            });
        });

        function animateCanvas() {
            ctx.fillStyle = 'rgba(13, 17, 23, 0.3)';
            ctx.fillRect(0, 0, canvas.width, canvas.height);

            nodes.forEach(n => {
                // Fragment drifting
                if (n.isFragment) {
                    n.baseX += n.driftX;
                    n.baseY += n.driftY;
                    if (n.baseX > canvas.width + 20) n.baseX = canvas.width / 2;
                }

                // Mouse Repulsion
                let dx = n.x - mouse.x;
                let dy = n.y - mouse.y;
                let dist = Math.sqrt(dx * dx + dy * dy);
                if (dist < mouse.radius && dist > 0) {
                    let force = (1 - dist / mouse.radius) * 8;
                    let angle = Math.atan2(dy, dx);
                    n.vx += Math.cos(angle) * force;
                    n.vy += Math.sin(angle) * force;
                }

                // Return force
                n.vx += (n.baseX - n.x) * 0.05;
                n.vy += (n.baseY - n.y) * 0.05;

                n.vx *= 0.85;
                n.vy *= 0.85;

                n.x += n.vx;
                n.y += n.vy;

                // Draw node
                ctx.fillStyle = '#AA9BEF';
                ctx.beginPath();
                ctx.arc(n.x, n.y, 1.5, 0, Math.PI * 2);
                ctx.fill();
            });

            // Draw connecting lines
            ctx.lineWidth = 0.5;
            for (let i = 0; i < nodes.length; i++) {
                for (let j = i + 1; j < nodes.length; j++) {
                    let dx = nodes[i].x - nodes[j].x;
                    let dy = nodes[i].y - nodes[j].y;
                    let dist = Math.sqrt(dx * dx + dy * dy);

                    if (dist < 22) {
                        let alpha = (1 - dist / 22) * 0.4;
                        ctx.strokeStyle = `rgba(170, 155, 239, ${alpha})`;
                        ctx.beginPath();
                        ctx.moveTo(nodes[i].x, nodes[i].y);
                        ctx.lineTo(nodes[j].x, nodes[j].y);
                        ctx.stroke();
                    }
                }
            }

            requestAnimationFrame(animateCanvas);
        }
        animateCanvas();

        const inputGithub = document.getElementById('inputGithub');
        const inputLinkedin = document.getElementById('inputLinkedin');
        const inputX = document.getElementById('inputX');
        const inputEmail = document.getElementById('inputEmail');
        const inputAvatar = document.getElementById('inputAvatar');
        const markdownOutput = document.getElementById('markdownOutput');
        const prevAvatar = document.getElementById('prevAvatar');

        function generateMarkdown() {
            const gh = inputGithub.value.trim() || 'lautarocastro';
            const li = inputLinkedin.value.trim() || 'lautaro-castro';
            const x = inputX.value.trim() || 'lautarocastro';
            const email = inputEmail.value.trim() || 'contacto@lautarocastro.com';
            const avatar = inputAvatar.value.trim();

            prevAvatar.src = avatar;

            const md = `<div align="center">

<!-- ANIMATED CONSTELLATION PORTRAIT AVATAR -->
<a href="https://github.com/${gh}">
  <img src="${avatar}" width="180" height="180" style="border-radius: 50%; border: 2px solid #AA9BEF;" alt="Lautaro Castro Vector Constellation">
</a>

<br><br>

<!-- NAME & TYPING HEADER -->
<a href="https://github.com/${gh}">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=26&duration=2600&pause=900&color=AA9BEF&center=true&vCenter=true&width=880&lines=Lautaro+Castro+-+Hazard+Forecaster;Early+Warning+Systems+%26+Risk+Analysis;Data+%2B+Weather+%2B+Impact+Modeling" alt="Lautaro Castro Header">
</a>

<br>

<!-- SOCIAL BADGES -->
<a href="https://www.linkedin.com/in/${li}"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>&nbsp;&nbsp;
<a href="https://x.com/${x}"><img src="https://img.shields.io/badge/X-0d1117?style=for-the-badge&logo=x&logoColor=aa9bef" alt="X"></a>&nbsp;&nbsp;
<a href="mailto:${email}"><img src="https://img.shields.io/badge/Email-0d1117?style=for-the-badge&logo=gmail&logoColor=aa9bef" alt="Email"></a>

<br>

<img src="https://komarev.com/ghpvc/?username=${gh}&style=flat&color=aa9bef&label=profile+views" alt="profile views">

</div>

---

## This is me :)

Hi, I'm **Lautaro Castro**, Hazard Forecaster.
I specialize in predicting severe weather, natural hazards, and modeling impact to protect communities and infrastructure.

- 🌩️ **Hazard Forecaster:** analyzing meteorological data, climate trends, and risk scenarios to deliver actionable early warnings.
- 📊 **Predictive Impact Modeling & Risk Assessment:** building models that quantify potential impact, not just forecast conditions.
- 🗺️ **GIS & Geospatial Analysis:** unapologetically obsessed with data visualization. Mix that with predictive models and you get actionable intelligence.
- 🌱 **My mission:** bridging the gap between weather science and disaster risk reduction through technology.
- 💬 Talk to me about **meteorology, hazard modeling, early warning systems, or GIS**.
<br>

<div align="center">

## my toolkit

<img src="https://skillicons.dev/icons?i=python,r,postgres,docker,aws,git,github,vscode&perline=7" alt="tech stack">

</div>

---

<div align="center">

## Numbers matter? ohhh yes.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api?username=${gh}&show_icons=true&theme=dark&title_color=aa9bef&icon_color=aa9bef&text_color=c9d1d9&bg_color=0d1117">
  <img src="https://github-readme-stats.vercel.app/api?username=${gh}&show_icons=true&theme=dark" width="480" alt="GitHub statistics">
</picture>

<br>

<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=${gh}&layout=compact&theme=dark&title_color=aa9bef&text_color=c9d1d9&bg_color=0d1117" alt="most used languages">

</div>`;

            markdownOutput.value = md;
        }

        [inputGithub, inputLinkedin, inputX, inputEmail, inputAvatar].forEach(input => {
            input.addEventListener('input', generateMarkdown);
        });

        generateMarkdown();

        const tabCode = document.getElementById('tabCode');
        const tabPreview = document.getElementById('tabPreview');
        const codeContainer = document.getElementById('codeContainer');
        const previewContainer = document.getElementById('previewContainer');

        tabCode.addEventListener('click', () => {
            tabCode.className = "px-4 py-2 bg-brand-card text-brand-purple border border-brand-border rounded-t-lg font-mono text-xs font-semibold flex items-center space-x-2";
            tabPreview.className = "px-4 py-2 bg-transparent text-slate-400 hover:text-slate-200 rounded-t-lg font-mono text-xs font-semibold flex items-center space-x-2 transition-colors";
            codeContainer.classList.remove('hidden');
            previewContainer.classList.add('hidden');
        });

        tabPreview.addEventListener('click', () => {
            tabPreview.className = "px-4 py-2 bg-brand-card text-brand-purple border border-brand-border rounded-t-lg font-mono text-xs font-semibold flex items-center space-x-2";
            tabCode.className = "px-4 py-2 bg-transparent text-slate-400 hover:text-slate-200 rounded-t-lg font-mono text-xs font-semibold flex items-center space-x-2 transition-colors";
            previewContainer.classList.remove('hidden');
            codeContainer.classList.add('hidden');
        });
