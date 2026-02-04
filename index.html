<html lang="ru" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TestyLemonad | Портфолио</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;700&family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
    <style>
        :root {
            /* --- НАСТРОЙКИ БЛЮРА И ЦВЕТОВ --- */
            --bg-blur: 2px;           /* Базовый уровень блюра фона */
            --lemon-yellow: #facc15;
            --deep-orange: #f97316;
            --dark-bg: #050200; 
            --card-bg: rgba(20, 10, 5, 0.4);
        }

        body {
            font-family: 'Inter', sans-serif;
            background: var(--dark-bg);
            color: #fff7ed;
            overflow-x: hidden;
            -webkit-font-smoothing: antialiased;
            margin: 0;
        }

        .mono { font-family: 'JetBrains Mono', monospace; }

        /* Контейнер для 3D с блюром */
        #canvas-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 0;
            filter: blur(var(--bg-blur)); 
            transition: filter 0.4s ease-out;
            will-change: filter, transform;
        }

        .vignette {
            position: fixed;
            inset: 0;
            z-index: 1;
            pointer-events: none;
            background: radial-gradient(circle, transparent 30%, rgba(0,0,0,0.9) 100%);
        }

        .noise::before {
            content: "";
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            opacity: 0.03;
            z-index: 2;
            pointer-events: none;
            background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noiseFilter'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.65' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noiseFilter)'/%3E%3C/svg%3E");
        }

        #loader {
            position: fixed;
            inset: 0;
            background: #050200;
            z-index: 100;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: opacity 1.5s cubic-bezier(0.4, 0, 0.2, 1);
            color: #ff9900;
            font-family: 'JetBrains Mono', monospace;
            letter-spacing: 4px;
            text-transform: uppercase;
            font-size: 12px;
        }

        .content-wrapper {
            position: relative;
            z-index: 10;
        }

        .gradient-text {
            background: linear-gradient(135deg, var(--lemon-yellow) 10%, var(--deep-orange) 90%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .glass-card {
            background: var(--card-bg);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid rgba(251, 191, 36, 0.08);
            transition: all 0.5s cubic-bezier(0.23, 1, 0.32, 1);
        }

        .glass-card:hover {
            transform: translateY(-8px);
            border-color: rgba(251, 191, 36, 0.3);
            box-shadow: 0 20px 40px -10px rgba(0, 0, 0, 0.5);
            background: rgba(30, 15, 5, 0.5);
        }

        .scroll-progress {
            position: fixed;
            top: 0; left: 0; width: 0%; height: 3px;
            background: linear-gradient(90deg, var(--lemon-yellow), var(--deep-orange));
            z-index: 110;
        }

        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .animate-fade-in {
            animation: fadeInUp 1.2s cubic-bezier(0.2, 0.8, 0.2, 1) forwards;
        }

        ::-webkit-scrollbar { width: 6px; }
        ::-webkit-scrollbar-track { background: var(--dark-bg); }
        ::-webkit-scrollbar-thumb { 
            background: #2d1a05; 
            border-radius: 10px;
        }
        ::-webkit-scrollbar-thumb:hover { background: var(--lemon-yellow); }

        .btn-glow:hover {
            box-shadow: 0 0 20px rgba(250, 204, 21, 0.4);
        }
    </style>
</head>
<body class="noise">
    <div id="loader">Инициализация квантового ядра...</div>
    <div class="scroll-progress" id="scroll-bar"></div>
    <div class="vignette"></div>
    <div id="canvas-container"></div>

    <div class="content-wrapper min-h-screen flex flex-col">
        <!-- Навигация -->
        <nav class="sticky top-0 z-50 w-full px-6 py-5 backdrop-blur-xl border-b border-white/5">
            <div class="max-w-7xl mx-auto flex justify-between items-center">
                <div class="text-xl font-bold mono gradient-text tracking-tighter">
                    testy-coder.github.io
                </div>
                <div class="space-x-8 flex items-center text-white/80">
                    <a href="#" class="text-sm font-medium hover:text-yellow-400 transition-colors duration-300 relative group">
                        Главная
                        <span class="absolute -bottom-1 left-0 w-0 h-0.5 bg-yellow-400 transition-all group-hover:w-full"></span>
                    </a>
                    <a href="#projects" class="text-sm font-medium hover:text-yellow-400 transition-colors duration-300 relative group">
                        Проекты
                        <span class="absolute -bottom-1 left-0 w-0 h-0.5 bg-yellow-400 transition-all group-hover:w-full"></span>
                    </a>
                    <a href="https://github.com/testy-coder" target="_blank" class="text-sm font-medium bg-white/5 px-4 py-1.5 rounded-full hover:bg-white/10 transition border border-white/5">
                        GitHub
                    </a>
                </div>
            </div>
        </nav>

        <!-- Герой-секция -->
        <header class="relative flex-grow flex flex-col justify-center items-center text-center px-4 py-20 md:py-32 overflow-hidden">
            <div class="animate-fade-in max-w-4xl mx-auto">
                <h1 class="text-5xl sm:text-6xl md:text-8xl font-extrabold mb-8 tracking-tighter text-white leading-tight">
                    Привет, я <span class="gradient-text">TestyLemonad</span>
                </h1>
                <p class="text-orange-100/60 text-lg md:text-2xl max-w-2xl mx-auto mb-12 leading-relaxed font-light">
                    Добро пожаловать в мой цифровой уголок. Здесь я собираю свои эксперименты в коде и игровые проекты.
                </p>
                <div class="flex flex-col sm:flex-row gap-6 justify-center">
                    <a href="#projects" class="btn-glow w-full sm:w-auto bg-yellow-400 hover:bg-yellow-300 text-orange-950 px-10 py-4 rounded-2xl font-bold transition-all duration-300 transform hover:scale-105 text-center">
                        Посмотреть проекты
                    </a>
                </div>
            </div>
        </header>

        <!-- Секция проектов -->
        <section id="projects" class="relative w-full px-6 py-24">
            <div class="max-w-7xl mx-auto">
                <div class="flex items-center gap-6 mb-16">
                    <h2 class="text-3xl sm:text-4xl font-black text-white whitespace-nowrap">
                        Мои проекты
                    </h2>
                    <div class="h-px bg-gradient-to-r from-orange-500/50 to-transparent flex-grow"></div>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <!-- Проект: Miheytale -->
                    <div class="glass-card p-2 rounded-[2rem] group">
                        <div class="p-4 flex flex-col h-full">
                            <div class="w-full aspect-video bg-gradient-to-br from-yellow-500/20 to-orange-600/20 rounded-[1.5rem] mb-6 flex items-center justify-center overflow-hidden relative border border-white/5">
                                <div class="absolute inset-0 bg-gradient-to-br from-yellow-500 to-orange-600 opacity-80 group-hover:scale-110 transition-transform duration-700"></div>
                                <span class="relative text-4xl font-black text-white drop-shadow-2xl">Miheytale</span>
                            </div>
                            <div class="px-3 pb-4 flex flex-col flex-grow">
                                <h3 class="text-2xl font-bold mb-3 text-white">Miheytale</h3>
                                <p class="text-orange-100/50 text-base mb-6 flex-grow leading-relaxed">
                                    Увлекательный игровой проект, созданный с душой. Погрузитесь в мир приключений прямо в браузере.
                                </p>
                                <a href="/Miheytale.html" class="flex items-center justify-center bg-white text-black px-6 py-3 rounded-xl font-bold hover:bg-yellow-400 transition-all duration-300">
                                    Играть
                                </a>
                            </div>
                        </div>
                    </div>

                    <!-- Проект: Dzen -->
                    <div class="glass-card p-2 rounded-[2rem] group">
                        <div class="p-4 flex flex-col h-full">
                            <div class="w-full aspect-video bg-gradient-to-br from-orange-400/20 to-yellow-500/20 rounded-[1.5rem] mb-6 flex items-center justify-center overflow-hidden relative border border-white/5">
                                <div class="absolute inset-0 bg-gradient-to-br from-orange-400 to-yellow-500 opacity-80 group-hover:scale-110 transition-transform duration-700"></div>
                                <span class="relative text-4xl font-black text-white drop-shadow-2xl">Dzen</span>
                            </div>
                            <div class="px-3 pb-4 flex flex-col flex-grow">
                                <h3 class="text-2xl font-bold mb-3 text-white">Генератор дзен - цитат</h3>
                                <p class="text-orange-100/50 text-base mb-6 flex-grow leading-relaxed">
                                    Генератор дзен - цитат, сделанный по приколу. Получите несколько философских цитат не выходя из браузера.
                                </p>
                                <a href="/Dzen.html" class="flex items-center justify-center bg-white text-black px-6 py-3 rounded-xl font-bold hover:bg-yellow-400 transition-all duration-300">
                                    Запустить
                                </a>
                            </div>
                        </div>
                    </div>

                    <!-- Заглушка (ВОССТАНОВЛЕНО) -->
                    <div class="border-2 border-dashed border-orange-900/30 p-8 rounded-[2rem] flex flex-col justify-center items-center text-center opacity-40 min-h-[400px] hover:opacity-100 transition-all duration-500 group">
                        <div class="w-14 h-14 bg-orange-900/20 rounded-full flex items-center justify-center mb-4">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-7 w-7 text-orange-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4v16m8-8H4" />
                            </svg>
                        </div>
                        <p class="text-orange-400/80 font-medium">Здесь скоро появится новый проект...</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Футер -->
        <footer class="w-full px-6 py-12 border-t border-white/5 text-center mt-auto bg-black/80 backdrop-blur-xl">
            <div class="max-w-7xl mx-auto flex flex-col items-center gap-4">
                <div class="w-12 h-px bg-gradient-to-r from-transparent via-orange-500 to-transparent mb-4"></div>
                <p class="mono text-xs sm:text-sm text-orange-100/40 tracking-widest uppercase">
                    &copy; 2026 testylemonad. сделано с помощью кода и лимонада.
                </p>
            </div>
        </footer>
    </div>

    <script>
        const rootStyle = getComputedStyle(document.documentElement);
        const BASE_BLUR = parseFloat(rootStyle.getPropertyValue('--bg-blur')) || 2;
        
        let scrollPercent = 0;

        window.onscroll = function() {
            const winScroll = document.body.scrollTop || document.documentElement.scrollTop;
            const height = document.documentElement.scrollHeight - document.documentElement.clientHeight;
            scrollPercent = (winScroll / height);
            
            document.getElementById("scroll-bar").style.width = (scrollPercent * 100) + "%";

            const additionalBlur = winScroll / 200;
            const finalBlur = BASE_BLUR + additionalBlur;
            document.getElementById('canvas-container').style.filter = `blur(${Math.min(finalBlur, 12)}px)`;
        };

        let scene, camera, renderer, particles, mesh, glowMesh;
        const container = document.getElementById('canvas-container');
        const THEME_COLOR = 0xff9900;

        function initThree() {
            scene = new THREE.Scene();
            camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
            camera.position.z = 8;

            renderer = new THREE.WebGLRenderer({ antialias: true, alpha: true });
            renderer.setSize(window.innerWidth, window.innerHeight);
            renderer.setPixelRatio(Math.min(window.devicePixelRatio, 2));
            container.appendChild(renderer.domElement);

            const geometry = new THREE.IcosahedronGeometry(2.5, 15);
            const material = new THREE.MeshBasicMaterial({
                color: THEME_COLOR,
                wireframe: true,
                transparent: true,
                opacity: 0.15
            });
            mesh = new THREE.Mesh(geometry, material);
            scene.add(mesh);

            const glowGeometry = new THREE.IcosahedronGeometry(2.4, 10);
            const glowMaterial = new THREE.MeshBasicMaterial({
                color: THEME_COLOR,
                transparent: true,
                opacity: 0.04,
                blending: THREE.AdditiveBlending
            });
            glowMesh = new THREE.Mesh(glowGeometry, glowMaterial);
            scene.add(glowMesh);

            const particleCount = 5000;
            const posArray = new Float32Array(particleCount * 3);
            for(let i = 0; i < particleCount; i++) {
                const r = 3 + Math.random() * 10;
                const theta = Math.random() * Math.PI * 2;
                const phi = Math.acos(2 * Math.random() - 1);
                posArray[i * 3] = r * Math.sin(phi) * Math.cos(theta);
                posArray[i * 3 + 1] = r * Math.sin(phi) * Math.sin(theta);
                posArray[i * 3 + 2] = r * Math.cos(phi);
            }
            const pGeometry = new THREE.BufferGeometry();
            pGeometry.setAttribute('position', new THREE.BufferAttribute(posArray, 3));
            const pMaterial = new THREE.PointsMaterial({
                size: 0.015,
                color: THEME_COLOR,
                transparent: true,
                opacity: 0.3,
                blending: THREE.AdditiveBlending,
                sizeAttenuation: true
            });
            particles = new THREE.Points(pGeometry, pMaterial);
            scene.add(particles);

            window.addEventListener('resize', onWindowResize, false);
            document.addEventListener('mousemove', onMouseMove);
            
            setTimeout(() => {
                const loader = document.getElementById('loader');
                if (loader) {
                    loader.style.opacity = '0';
                    setTimeout(() => loader.remove(), 1500);
                }
            }, 1000);

            animate();
        }

        let mouseX = 0, mouseY = 0;
        let targetX = 0, targetY = 0;

        function onMouseMove(event) {
            mouseX = (event.clientX - window.innerWidth / 2) / 250;
            mouseY = (event.clientY - window.innerHeight / 2) / 250;
        }

        function onWindowResize() {
            camera.aspect = window.innerWidth / window.innerHeight;
            camera.updateProjectionMatrix();
            renderer.setSize(window.innerWidth, window.innerHeight);
        }

        function animate() {
            const time = Date.now() * 0.001;
            requestAnimationFrame(animate);

            const scrollRotationBoost = scrollPercent * 0.05;
            mesh.rotation.x += 0.0002 + scrollRotationBoost;
            mesh.rotation.y += 0.0004 + scrollRotationBoost;
            glowMesh.rotation.y -= 0.0003 + scrollRotationBoost;
            
            const scrollScaleFactor = 1 - (scrollPercent * 0.3);
            const pulseScale = 1 + Math.sin(time * 1.2) * 0.02;
            const finalScale = pulseScale * scrollScaleFactor;
            
            mesh.scale.set(finalScale, finalScale, finalScale);
            glowMesh.scale.set(finalScale * 1.05, finalScale * 1.05, finalScale * 1.05);

            particles.rotation.y -= 0.0001 + scrollRotationBoost;

            targetX += (mouseX - targetX) * 0.04;
            targetY += (mouseY - targetY) * 0.04;
            camera.position.x = targetX;
            camera.position.y = -targetY;
            camera.lookAt(scene.position);

            renderer.render(scene, camera);
        }

        window.onload = initThree;
    </script>
</body>
</html>
