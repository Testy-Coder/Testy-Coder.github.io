<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TestyLemonad | Портфолио</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;700&family=Inter:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #0f172a;
            color: #f8fafc;
            overflow-x: hidden;
        }
        .mono {
            font-family: 'JetBrains Mono', monospace;
        }
        .gradient-text {
            background: linear-gradient(90deg, #38bdf8, #818cf8);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        .project-card {
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px -5px rgba(56, 189, 248, 0.2);
            border-color: rgba(56, 189, 248, 0.4);
        }
        /* Дополнительная плавная прокрутка */
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="min-h-screen flex flex-col">

    <!-- Навигация -->
    <nav class="w-full px-4 sm:px-6 lg:px-8 py-6">
        <div class="max-w-7xl mx-auto flex justify-between items-center">
            <div class="text-lg sm:text-xl font-bold mono gradient-text truncate">testy-coder.github.io</div>
            <div class="space-x-4 sm:space-x-6 flex">
                <a href="#" class="text-sm sm:text-base hover:text-sky-400 transition">Главная</a>
                <a href="#projects" class="text-sm sm:text-base hover:text-sky-400 transition">Проекты</a>
                <a href="https://github.com/testy-coder" target="_blank" class="text-sm sm:text-base hover:text-sky-400 transition hidden xs:inline">GitHub</a>
            </div>
        </div>
    </nav>

    <!-- Герой-секция -->
    <header class="flex-grow flex flex-col justify-center items-center text-center px-4 py-12 md:py-24">
        <div class="max-w-4xl mx-auto">
            <h1 class="text-4xl sm:text-5xl md:text-7xl font-extrabold mb-6 tracking-tight">
                Привет, я <span class="gradient-text">TestyLemonad</span>
            </h1>
            <p class="text-slate-400 text-base sm:text-lg md:text-xl max-w-2xl mx-auto mb-10 leading-relaxed">
                Добро пожаловать в мой цифровой уголок. Здесь я собираю свои эксперименты в коде и игровые проекты.
            </p>
            <div class="flex flex-col sm:flex-row gap-4 justify-center">
                <a href="#projects" class="w-full sm:w-auto bg-sky-500 hover:bg-sky-400 text-white px-8 py-3 rounded-full font-semibold transition shadow-lg shadow-sky-500/20 text-center">
                    Посмотреть проекты
                </a>
            </div>
        </div>
    </header>

    <!-- Секция проектов -->
    <section id="projects" class="w-full px-4 sm:px-6 lg:px-8 py-16 md:py-24 bg-slate-900/30">
        <div class="max-w-7xl mx-auto">
            <h2 class="text-2xl sm:text-3xl font-bold mb-12 flex items-center gap-4">
                <span class="h-px bg-slate-700 flex-grow"></span>
                Мои проекты
                <span class="h-px bg-slate-700 flex-grow"></span>
            </h2>

            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 md:gap-8">
                
                <!-- Проект: Miheytale -->
                <div class="project-card bg-slate-800/50 p-5 sm:p-6 rounded-2xl flex flex-col h-full">
                    <div class="w-full aspect-video bg-gradient-to-br from-indigo-500 to-purple-600 rounded-xl mb-6 flex items-center justify-center">
                        <span class="text-3xl sm:text-4xl font-bold text-white drop-shadow-md">Miheytale</span>
                    </div>
                    <h3 class="text-xl sm:text-2xl font-bold mb-3">Miheytale</h3>
                    <p class="text-slate-400 text-sm sm:text-base mb-6 flex-grow leading-relaxed">
                        Увлекательный игровой проект, созданный с душой. Погрузитесь в мир приключений прямо в браузере.
                    </p>
                    <div class="flex flex-wrap gap-2 mb-6">
                        <span class="bg-slate-700/50 text-sky-300 px-3 py-1 rounded-md text-xs font-medium">HTML5</span>
                        <span class="bg-slate-700/50 text-sky-300 px-3 py-1 rounded-md text-xs font-medium">CSS</span>
                        <span class="bg-slate-700/50 text-sky-300 px-3 py-1 rounded-md text-xs font-medium">GameDev</span>
                    </div>
                    <a href="/Miheytale.html" class="inline-flex items-center justify-center bg-white text-slate-900 px-6 py-2.5 rounded-lg font-bold hover:bg-sky-100 transition w-full">
                        Играть
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 ml-2" viewBox="0 0 20 20" fill="currentColor">
                            <path fill-rule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clip-rule="evenodd" />
                        </svg>
                    </a>
                </div>

                <!-- Проект: Генератор дзен - цитат -->
                <div class="project-card bg-slate-800/50 p-5 sm:p-6 rounded-2xl flex flex-col h-full">
                    <div class="w-full aspect-video bg-gradient-to-br from-indigo-500 to-purple-600 rounded-xl mb-6 flex items-center justify-center">
                        <span class="text-3xl sm:text-4xl font-bold text-white drop-shadow-md">Dzen</span>
                    </div>
                    <h3 class="text-xl sm:text-2xl font-bold mb-3">Генератор дзен - цитат</h3>
                    <p class="text-slate-400 text-sm sm:text-base mb-6 flex-grow leading-relaxed">
                        Генератор дзен - цитат, созданный по приколу. Получите несколько философских цитат не выходя из браузера.
                    </p>
                    <div class="flex flex-wrap gap-2 mb-6">
                        <span class="bg-slate-700/50 text-sky-300 px-3 py-1 rounded-md text-xs font-medium">HTML5</span>
                        <span class="bg-slate-700/50 text-sky-300 px-3 py-1 rounded-md text-xs font-medium">CSS</span>
                    </div>
                    <a href="/Dzen.html" class="inline-flex items-center justify-center bg-white text-slate-900 px-6 py-2.5 rounded-lg font-bold hover:bg-sky-100 transition w-full">
                        Запустить
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 ml-2" viewBox="0 0 20 20" fill="currentColor">
                            <path fill-rule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clip-rule="evenodd" />
                        </svg>
                    </a>
                </div>

                <!-- Заглушка для будущего проекта -->
                <div class="border-2 border-dashed border-slate-700 p-6 rounded-2xl flex flex-col justify-center items-center text-center opacity-60 min-h-[300px]">
                    <div class="w-14 h-14 bg-slate-800 rounded-full flex items-center justify-center mb-4">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-7 w-7 text-slate-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4v16m8-8H4" />
                        </svg>
                    </div>
                    <p class="text-slate-500 font-medium">Здесь скоро появится новый проект...</p>
                </div>

            </div>
        </div>
    </section>

    <!-- Футер -->
    <footer class="w-full px-4 sm:px-6 lg:px-8 py-10 border-t border-slate-800/50 text-center text-slate-500 mt-auto">
        <div class="max-w-7xl mx-auto">
            <p class="mono text-xs sm:text-sm">&copy; 2026 TestyLemonad. Сделано с помощью кода и кофе.</p>
        </div>
    </footer>

</body>
</html>
