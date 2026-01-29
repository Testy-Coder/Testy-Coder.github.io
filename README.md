<!DOCTYPE html>
<html lang="ru" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TestyLemonad | Портфолио</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;700&family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --lemon-yellow: #facc15;
            --deep-orange: #f97316;
            --dark-bg: #0c0701; 
            --card-bg: rgba(28, 17, 4, 0.7);
        }

        body {
            font-family: 'Inter', sans-serif;
            background: var(--dark-bg);
            color: #fff7ed;
            overflow-x: hidden;
            -webkit-font-smoothing: antialiased;
        }

        .mono { font-family: 'JetBrains Mono', monospace; }

        .noise::before {
            content: "";
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            opacity: 0.03;
            z-index: 100;
            pointer-events: none;
            background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noiseFilter'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.65' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noiseFilter)'/%3E%3C/svg%3E");
        }

        .bg-glow {
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: 
                radial-gradient(circle at 50% -20%, #4c2b0a 0%, transparent 50%),
                radial-gradient(circle at 0% 100%, #1e1305 0%, transparent 40%);
            z-index: -1;
        }

        .blob {
            position: fixed;
            width: 400px;
            height: 400px;
            background: var(--deep-orange);
            filter: blur(120px);
            opacity: 0.05;
            border-radius: 50%;
            z-index: -1;
            animation: move 20s infinite alternate;
        }

        @keyframes move {
            from { transform: translate(-10%, -10%); }
            to { transform: translate(100%, 50%); }
        }

        .gradient-text {
            background: linear-gradient(135deg, var(--lemon-yellow) 10%, var(--deep-orange) 90%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            filter: drop-shadow(0 2px 10px rgba(250, 204, 21, 0.2));
        }

        .glass-card {
            background: var(--card-bg);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid rgba(251, 191, 36, 0.08);
            box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
            transition: all 0.5s cubic-bezier(0.23, 1, 0.32, 1);
        }

        .glass-card:hover {
            transform: translateY(-12px);
            border-color: rgba(251, 191, 36, 0.3);
            box-shadow: 0 20px 40px -10px rgba(0, 0, 0, 0.5), 0 0 20px rgba(249, 115, 22, 0.1);
        }

        .scroll-progress {
            position: fixed;
            top: 0; left: 0; width: 0%; height: 3px;
            background: linear-gradient(90deg, var(--lemon-yellow), var(--deep-orange));
            z-index: 100;
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

        #particles-canvas {
            position: fixed;
            top: 0; left: 0;
            pointer-events: none;
            z-index: 0;
            opacity: 0.6;
        }

        .btn-glow:hover {
            box-shadow: 0 0 20px rgba(250, 204, 21, 0.4);
        }
    </style>
</head>
<body class="min-h-screen flex flex-col noise">
    <div class="scroll-progress" id="scroll-bar"></div>
    <div class="blob"></div>
    <canvas id="particles-canvas"></canvas>
    <div class="bg-glow"></div>

    <!-- Навигация -->
    <nav class="sticky top-0 z-50 w-full px-6 py-5 backdrop-blur-xl border-b border-white/5">
        <div class="max-w-7xl mx-auto flex justify-between items-center">
            <div class="text-xl font-bold mono gradient-text tracking-tighter">
                testy-coder.github.io
            </div>
            <div class="space-x-8 flex items-center">
                <a href="#" class="text-sm font-medium hover:text-yellow-400 transition-colors duration-300 relative group">
                    Главная
                    <span class="absolute -bottom-1 left-0 w-0 h-0.5 bg-yellow-400 transition-all group-hover:w-full"></span>
                </a>
                <a href="#projects" class="text-sm font-medium hover:text-yellow-400 transition-colors duration-300 relative group">
                    Проекты
                    <span class="absolute -bottom-1 left-0 w-0 h-0.5 bg-yellow-400 transition-all group-hover:w-full"></span>
                </a>
                <a href="https://github.com/testy-coder" target="_blank" class="text-sm font-medium bg-white/5 px-4 py-1.5 rounded-full hover:bg-white/10 transition">
                    GitHub
                </a>
            </div>
        </div>
    </nav>

    <!-- Герой-секция -->
    <header class="relative flex-grow flex flex-col justify-center items-center text-center px-4 py-20 md:py-32 z-10 overflow-hidden">
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
        
        <div class="absolute bottom-10 left-1/2 -translate-x-1/2 animate-bounce opacity-20">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3"></path></svg>
        </div>
    </header>

    <!-- Секция проектов -->
    <section id="projects" class="relative w-full px-6 py-24 z-10">
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
                            <div class="absolute inset-0 opacity-20" style="background-image: radial-gradient(circle at 2px 2px, white 1px, transparent 0); background-size: 20px 20px;"></div>
                            <span class="relative text-4xl font-black text-white drop-shadow-2xl">Miheytale</span>
                        </div>
                        <div class="px-3 pb-4 flex flex-col flex-grow">
                            <h3 class="text-2xl font-bold mb-3 text-white">Miheytale</h3>
                            <p class="text-orange-100/50 text-base mb-6 flex-grow leading-relaxed">
                                Увлекательный игровой проект, созданный с душой. Погрузитесь в мир приключений прямо в браузере.
                            </p>
                            <div class="flex flex-wrap gap-2 mb-8">
                                <span class="bg-white/5 text-yellow-500/80 border border-yellow-500/10 px-3 py-1 rounded-full text-xs font-bold mono">HTML5</span>
                                <span class="bg-white/5 text-yellow-500/80 border border-yellow-500/10 px-3 py-1 rounded-full text-xs font-bold mono">CSS</span>
                                <span class="bg-white/5 text-yellow-500/80 border border-yellow-500/10 px-3 py-1 rounded-full text-xs font-bold mono">GameDev</span>
                            </div>
                            <a href="/Miheytale.html" class="flex items-center justify-center bg-white text-black px-6 py-3 rounded-xl font-bold hover:bg-yellow-400 transition-all duration-300">
                                Играть
                                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 ml-2 group-hover:translate-x-1 transition-transform" viewBox="0 0 20 20" fill="currentColor">
                                    <path fill-rule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clip-rule="evenodd" />
                                </svg>
                            </a>
                        </div>
                    </div>
                </div>

                <!-- Проект: Генератор дзен - цитат -->
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
                            <div class="flex flex-wrap gap-2 mb-8">
                                <span class="bg-white/5 text-yellow-500/80 border border-yellow-500/10 px-3 py-1 rounded-full text-xs font-bold mono">HTML5</span>
                                <span class="bg-white/5 text-yellow-500/80 border border-yellow-500/10 px-3 py-1 rounded-full text-xs font-bold mono">CSS</span>
                            </div>
                            <a href="/Dzen.html" class="flex items-center justify-center bg-white text-black px-6 py-3 rounded-xl font-bold hover:bg-yellow-400 transition-all duration-300">
                                Запустить
                                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 ml-2 group-hover:translate-x-1 transition-transform" viewBox="0 0 20 20" fill="currentColor">
                                    <path fill-rule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clip-rule="evenodd" />
                                </svg>
                            </a>
                        </div>
                    </div>
                </div>

                <!-- Заглушка -->
                <div class="border-2 border-dashed border-orange-900/50 p-8 rounded-[2rem] flex flex-col justify-center items-center text-center opacity-60 min-h-[400px] hover:opacity-100 transition-all duration-500 group">
                    <div class="w-14 h-14 bg-orange-900/30 rounded-full flex items-center justify-center mb-4 transition-transform duration-300">
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
    <footer class="w-full px-6 py-12 border-t border-white/5 text-center mt-auto bg-black/40 backdrop-blur-md">
        <div class="max-w-7xl mx-auto flex flex-col items-center gap-4">
            <div class="w-12 h-px bg-gradient-to-r from-transparent via-orange-500 to-transparent mb-4"></div>
            <p class="mono text-xs sm:text-sm text-orange-100/40 tracking-widest uppercase">
                &copy; 2026 testylemonad. сделано с помощью кода и лимонада.
            </p>
        </div>
    </footer>

    <script>
        window.onscroll = function() {
            const winScroll = document.body.scrollTop || document.documentElement.scrollTop;
            const height = document.documentElement.scrollHeight - document.documentElement.clientHeight;
            const scrolled = (winScroll / height) * 100;
            document.getElementById("scroll-bar").style.width = scrolled + "%";
        };

        const canvas = document.getElementById('particles-canvas');
        const ctx = canvas.getContext('2d');
        let particles = [];

        function initCanvas() {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
        }

        class Particle {
            constructor() {
                this.reset();
            }
            reset() {
                this.x = Math.random() * canvas.width;
                this.y = Math.random() * canvas.height;
                this.size = Math.random() * 1.5 + 0.5;
                this.speedX = (Math.random() - 0.5) * 0.3;
                this.speedY = (Math.random() - 0.5) * 0.3;
                this.opacity = Math.random() * 0.5 + 0.1;
                this.color = Math.random() > 0.5 ? '#facc15' : '#f97316';
            }
            update() {
                this.x += this.speedX;
                this.y += this.speedY;
                if (this.x < 0 || this.x > canvas.width || this.y < 0 || this.y > canvas.height) {
                    this.reset();
                }
            }
            draw() {
                ctx.globalAlpha = this.opacity;
                ctx.fillStyle = this.color;
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
                ctx.fill();
            }
        }

        function createParticles() {
            particles = [];
            const count = Math.min(Math.floor(window.innerWidth / 12), 120);
            for (let i = 0; i < count; i++) {
                particles.push(new Particle());
            }
        }

        function animate() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            particles.forEach(p => {
                p.update();
                p.draw();
            });
            requestAnimationFrame(animate);
        }

        window.addEventListener('resize', () => {
            initCanvas();
            createParticles();
        });

        initCanvas();
        createParticles();
        animate();
    </script>
</body>
</html>
