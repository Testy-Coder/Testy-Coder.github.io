<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Генератор Случайных Слов</title>
    <!-- Подключение Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Установка шрифта Inter для всего документа */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f3f4f6; /* Светло-серый фон */
        }
    </style>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        'primary': '#4f46e5',
                        'secondary': '#6366f1',
                    },
                }
            }
        }
    </script>
</head>
<body class="min-h-screen flex items-center justify-center p-4">

    <!-- Основной контейнер приложения, центрированный и адаптивный -->
    <div class="w-full max-w-lg bg-white p-8 rounded-xl shadow-2xl border border-gray-100">
        <h1 class="text-3xl font-extrabold text-primary mb-6 text-center tracking-tight">
            Случайное Слово
        </h1>
        
        <!-- Область для отображения слова -->
        <div id="wordDisplay" class="min-h-24 flex items-center justify-center text-4xl sm:text-5xl font-bold text-gray-800 bg-gray-50 p-6 mb-8 rounded-lg border-2 border-dashed border-gray-300 transition duration-300 ease-in-out">
            Нажмите кнопку
        </div>

        <!-- Кнопка генерации -->
        <button id="generateButton" 
                class="w-full py-3 px-4 bg-primary text-white font-semibold rounded-lg shadow-md hover:bg-secondary 
                       focus:outline-none focus:ring-4 focus:ring-indigo-500 focus:ring-opacity-50 
                       active:bg-indigo-700 transition duration-150 ease-in-out transform hover:scale-[1.02]">
            Сгенерировать Слово
        </button>

        <!-- Описание списка -->
        <p class="text-xs text-gray-500 mt-4 text-center" id="listSizeInfo">
            *Список содержит более 1000 наиболее употребляемых русских слов.
        </p>

    </div>

    <script>
        // Инициализация элементов DOM
        const generateButton = document.getElementById('generateButton');
        const wordDisplay = document.getElementById('wordDisplay');
        const listSizeInfo = document.getElementById('listSizeInfo');

        // ОЧЕНЬ РАСШИРЕННЫЙ СПИСОК СЛОВ (более 1000 существительных и прилагательных)
