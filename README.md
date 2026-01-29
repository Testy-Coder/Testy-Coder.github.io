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
            --dark-bg: #1a0f02;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: var(--dark-bg);
            color: #fff7ed;
            overflow-x: hidden;
        }

        .mono { font-family: 'JetBrains Mono', monospace; }

        /* Анимированный градиентный фон */
        .bg-glow {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at 50% -20%, #4c2b0a 0%, var(--dark-bg) 70%);
            z-index: -1;
        }

        .gradient-text {
            background: linear-gradient(135deg, var(--lemon-yellow), var(--deep-orange));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .glass-card {
            background: rgba(45, 26, 5, 0.6);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(251, 191, 36, 0.1);
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        .glass-card:hover {
            transform: translateY(-8px) scale(1.02);
            border-color: rgba(251, 146, 60, 0.4);
            box-shadow: 0 20px 40px -15px rgba(249, 115, 22, 0.2);
        }

        /* Анимация появления */
        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .animate-fade-in {
            animation: fadeInUp 0.8s ease-out forwards;
        }

        /* Кастомный скроллбар */
        ::-webkit-scrollbar { width: 8px; }
        ::-webkit-scrollbar-track { background: var(--dark-bg); }
        ::-webkit-scrollbar-thumb { 
            background: #432609; 
            border-radius: 10px;
        }
        ::-webkit-scrollbar-thumb:hover { background: var(--deep-orange); }

        #particles-canvas {
            position: fixed;
            top: 0;
            left: 0;
            pointer-events: none;
            z-index: 0;
        }
    </style>
</head>
<body class="min-h-screen flex flex-col">
    <canvas id="particles-canvas"></canvas>
    <div class="bg-glow"></div>

    <!-- Навигация -->
    <nav class="sticky top-0 z-50 w-full px-4 sm:px-6 lg:px-8 py-6 backdrop-blur-md border-b border-orange-900/20">
        <div class="max-w-7xl mx-auto flex justify-between items-center">
            <div class="text-lg sm:text-xl font-bold mono gradient-text truncate">
                testy-coder.github.io
            </div>
            <div class="space-x-4 sm:space-x-6 flex items-center">
                <a href="#" class="text-sm sm:text-base hover:text-yellow-400 transition">Главная</a>
                <a href="#projects" class="text-sm sm:text-base hover:text-yellow-400 transition">Проекты</a>
                <a href="https://github.com/testy-coder" target="_blank" class="text-sm sm:text-base hover:text-yellow-400 transition hidden xs:inline">GitHub</a>
            </div>
        </div>
    </nav>

    <!-- Герой-секция -->
    <header class="relative flex-grow flex flex-col justify-center items-center text-center px-4 py-12 md:py-24 z-10">
        <div class="animate-fade-in max-w-4xl mx-auto">
            <h1 class="text-4xl sm:text-5xl md:text-7xl font-extrabold mb-6 tracking-tight text-white">
                Привет, я <span class="gradient-text">TestyLemonad</span>
            </h1>
            <p class="text-orange-100/70 text-base sm:text-lg md:text-xl max-w-2xl mx-auto mb-10 leading-relaxed">
                Добро пожаловать в мой цифровой уголок. Здесь я собираю свои эксперименты в коде и игровые проекты.
            </p>
            <div class="flex flex-col sm:flex-row gap-4 justify-center">
                <a href="#projects" class="w-full sm:w-auto bg-yellow-400 hover:bg-yellow-300 text-orange-950 px-8 py-3 rounded-full font-bold transition shadow-lg shadow-yellow-500/20 text-center">
                    Посмотреть проекты
                </a>
            </div>
        </div>
    </header>

    <!-- Секция проектов -->
    <section id="projects" class="relative w-full px-4 sm:px-6 lg:px-8 py-16 md:py-24 z-10 bg-black/10">
        <div class="max-w-7xl mx-auto">
            <h2 class="text-2xl sm:text-3xl font-bold mb-12 flex items-center gap-4 text-orange-100">
                <span class="h-px bg-orange-900 flex-grow"></span>
                Мои проекты
                <span class="h-px bg-orange-900 flex-grow"></span>
            </h2>

            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 md:gap-8">
                <!-- Проект: Miheytale -->
                <div class="glass-card p-5 sm:p-6 rounded-2xl flex flex-col h-full group">
                    <div class="w-full aspect-video bg-gradient-to-br from-yellow-500 to-orange-600 rounded-xl mb-6 flex items-center justify-center overflow-hidden relative">
                        <div class="absolute inset-0 opacity-10 group-hover:scale-110 transition-transform duration-500" style="background-image: radial-gradient(circle at 2px 2px, white 1px, transparent 0); background-size: 15px 15px;"></div>
                        <span class="relative text-3xl sm:text-4xl font-bold text-white drop-shadow-md">Miheytale</span>
                    </div>
                    <h3 class="text-xl sm:text-2xl font-bold mb-3 text-white">Miheytale</h3>
                    <p class="text-orange-100/60 text-sm sm:text-base mb-6 flex-grow leading-relaxed">
                        Увлекательный игровой проект, созданный с душой. Погрузитесь в мир приключений прямо в браузере.
                    </p>
                    <div class="flex flex-wrap gap-2 mb-6">
                        <span class="bg-orange-900/40 text-yellow-200 px-3 py-1 rounded-md text-xs font-medium">HTML5</span>
                        <span class="bg-orange-900/40 text-yellow-200 px-3 py-1 rounded-md text-xs font-medium">CSS</span>
                        <span class="bg-orange-900/40 text-yellow-200 px-3 py-1 rounded-md text-xs font-medium">GameDev</span>
                    </div>
                    <a href="/Miheytale.html" class="inline-flex items-center justify-center bg-orange-100 text-orange-950 px-6 py-2.5 rounded-lg font-bold hover:bg-yellow-200 transition w-full">
                        Играть
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 ml-2" viewBox="0 0 20 20" fill="currentColor">
                            <path fill-rule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clip-rule="evenodd" />
                        </svg>
                    </a>
                </div>

                <!-- Проект: Генератор дзен - цитат -->
                <div class="glass-card p-5 sm:p-6 rounded-2xl flex flex-col h-full group">
                    <div class="w-full aspect-video bg-gradient-to-br from-orange-400 to-yellow-500 rounded-xl mb-6 flex items-center justify-center overflow-hidden relative">
                        <span class="text-3xl sm:text-4xl font-bold text-white drop-shadow-md">Dzen</span>
                    </div>
                    <h3 class="text-xl sm:text-2xl font-bold mb-3 text-white">Генератор дзен - цитат</h3>
                    <p class="text-orange-100/60 text-sm sm:text-base mb-6 flex-grow leading-relaxed">
                        Генератор дзен - цитат, сделанный по приколу. Получите несколько философских цитат не выходя из браузера.
                    </p>
                    <div class="flex flex-wrap gap-2 mb-6">
                        <span class="bg-orange-900/40 text-yellow-200 px-3 py-1 rounded-md text-xs font-medium">HTML5</span>
                        <span class="bg-orange-900/40 text-yellow-200 px-3 py-1 rounded-md text-xs font-medium">CSS</span>
                    </div>
                    <a href="/Dzen.html" class="inline-flex items-center justify-center bg-orange-100 text-orange-950 px-6 py-2.5 rounded-lg font-bold hover:bg-yellow-200 transition w-full">
                        Запустить
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 ml-2" viewBox="0 0 20 20" fill="currentColor">
                            <path fill-rule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clip-rule="evenodd" />
                        </svg>
                    </a>
                </div>

                <!-- Заглушка -->
                <div class="border-2 border-dashed border-orange-900/50 p-6 rounded-2xl flex flex-col justify-center items-center text-center opacity-60 min-h-[300px] hover:opacity-100 transition-opacity">
                    <div class="w-14 h-14 bg-orange-900/30 rounded-full flex items-center justify-center mb-4">
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
    <footer class="w-full px-4 sm:px-6 lg:px-8 py-10 border-t border-orange-900/30 text-center text-orange-400/50 mt-auto bg-black/20 z-10">
        <div class="max-w-7xl mx-auto">
            <p class="mono text-xs sm:text-sm">&copy; 2026 TestyLemonad. Сделано с помощью кода и лимонада.</p>
        </div>
    </footer>

    <script>
        // Анимация частиц на фоне
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
                this.size = Math.random() * 2;
                this.speedX = (Math.random() - 0.5) * 0.4;
                this.speedY = (Math.random() - 0.5) * 0.4;
                this.opacity = Math.random() * 0.5;
            }
            update() {
                this.x += this.speedX;
                this.y += this.speedY;
                if (this.x < 0 || this.x > canvas.width || this.y < 0 || this.y > canvas.height) {
                    this.reset();
                }
            }
            draw() {
                ctx.fillStyle = `rgba(250, 204, 21, ${this.opacity})`;
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
                ctx.fill();
            }
        }

        function createParticles() {
            particles = [];
            const count = Math.min(Math.floor(window.innerWidth / 10), 100);
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
