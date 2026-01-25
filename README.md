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
    </style>
</head>
<body class="min-h-screen flex flex-col">

    <!-- Навигация -->
    <nav class="p-6 flex justify-between items-center max-w-6xl mx-auto w-full">
        <div class="text-xl font-bold mono gradient-text">testy-coder.github.io</div>
        <div class="space-x-6 hidden md:flex">
            <a href="#" class="hover:text-sky-400 transition">Главная</a>
            <a href="#projects" class="hover:text-sky-400 transition">Проекты</a>
            <a href="https://github.com/testy-coder" target="_blank" class="hover:text-sky-400 transition">GitHub</a>
        </div>
    </nav>

    <!-- Герой-секция -->
    <header class="flex-grow flex flex-col justify-center items-center text-center px-4 py-20">
        <h1 class="text-5xl md:text-7xl font-extrabold mb-6"> Привет, я <span class="gradient-text">TestyLemonad</span></h1>
        <p class="text-slate-400 text-lg md:text-xl max-w-2xl mb-10">
            Добро пожаловать в мой цифровой уголок. Здесь я собираю свои эксперименты в коде и игровые проекты.
        </p>
        <a href="#projects" class="bg-sky-500 hover:bg-sky-400 text-white px-8 py-3 rounded-full font-semibold transition shadow-lg shadow-sky-500/20">
            Посмотреть проекты
        </a>
    </header>

    <!-- Секция проектов -->
    <section id="projects" class="max-w-6xl mx-auto w-full px-6 py-20">
        <h2 class="text-3xl font-bold mb-12 flex items-center gap-4">
            <span class="h-px bg-slate-700 flex-grow"></span>
            Мои проекты
            <span class="h-px bg-slate-700 flex-grow"></span>
        </h2>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            
            <!-- Проект: Miheytale -->
            <div class="project-card bg-slate-800/50 p-6 rounded-2xl flex flex-col h-full">
                <div class="w-full h-48 bg-gradient-to-br from-indigo-500 to-purple-600 rounded-xl mb-6 flex items-center justify-center">
                    <span class="text-4xl font-bold text-white drop-shadow-md">Miheytale</span>
                </div>
                <h3 class="text-2xl font-bold mb-3">Miheytale</h3>
                <p class="text-slate-400 mb-6 flex-grow">
                    Увлекательный игровой проект, созданный с душой. Погрузитесь в мир приключений прямо в браузере.
                </p>
                <div class="flex flex-wrap gap-2 mb-6">
                    <span class="bg-slate-700 text-slate-300 px-3 py-1 rounded-md text-sm">HTML5</span>
                    <span class="bg-slate-700 text-slate-300 px-3 py-1 rounded-md text-sm">CSS</span>
                    <span class="bg-slate-700 text-slate-300 px-3 py-1 rounded-md text-sm">GameDev</span>
                </div>
                <a href="/Miheytale.html" class="inline-flex items-center justify-center bg-white text-slate-900 px-6 py-2 rounded-lg font-bold hover:bg-sky-100 transition">
                    Запустить игру
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 ml-2" viewBox="0 0 20 20" fill="currentColor">
                        <path fill-rule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clip-rule="evenodd" />
                    </svg>
                </a>
            </div>

            <!-- Заглушка для будущего проекта -->
            <div class="border-2 border-dashed border-slate-700 p-6 rounded-2xl flex flex-col justify-center items-center text-center opacity-50">
                <div class="w-16 h-16 bg-slate-800 rounded-full flex items-center justify-center mb-4">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-slate-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4v16m8-8H4" />
                    </svg>
                </div>
                <p class="text-slate-500 font-medium">Здесь скоро появится новый проект...</p>
            </div>

        </div>
    </section>

    <!-- Футер -->
    <footer class="p-10 border-t border-slate-800 text-center text-slate-500 mt-20">
        <p class="mono text-sm">&copy; 2024 testy-coder. Сделано с помощью кода и кофе.</p>
    </footer>

</body>
</html>
