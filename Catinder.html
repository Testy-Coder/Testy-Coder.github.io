<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Котиндер — Найди своего пушистика</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://unpkg.com/lucide@latest"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;700;900&display=swap');
 
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f5f5f5;
            overscroll-behavior: none;
        }
 
        .card-shadow {
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
        }
 
        @keyframes slide-up {
            from { transform: translateY(100%); }
            to { transform: translateY(0); }
        }
 
        .animate-slide-up {
            animation: slide-up 0.4s cubic-bezier(0.16, 1, 0.3, 1) forwards;
        }
 
        .swipe-overlay {
            transition: opacity 0.2s ease;
            pointer-events: none;
        }
 
        .no-select {
            user-select: none;
            -webkit-user-drag: none;
        }
 
        #app-container {
            max-width: 450px;
            width: 100%;
            height: 100vh;
            background: white;
            position: relative;
            overflow: hidden;
            display: flex;
            flex-direction: column;
        }
 
        @media (min-width: 640px) {
            #app-container {
                height: 800px;
                border-radius: 40px;
                margin: 20px;
            }
        }
    </style>
</head>
<body class="flex items-center justify-center min-h-screen">
 
    <div id="app-container" class="shadow-2xl">
        <!-- Header -->
        <header class="px-6 py-4 flex justify-between items-center bg-white z-40 border-b shrink-0">
            <div class="flex items-center gap-2">
                <div class="p-1 bg-gradient-to-tr from-orange-500 to-rose-500 rounded-lg shadow-sm text-white">
                    <i data-lucide="sparkles" class="w-4 h-4"></i>
                </div>
                <h1 class="text-xl font-black text-slate-800 italic tracking-tighter">Котиндер</h1>
            </div>
            <div class="flex items-center gap-2">
                <div id="loader-spinner" class="hidden">
                    <i data-lucide="loader-2" class="w-4 h-4 animate-spin text-orange-400"></i>
                </div>
                <span id="queue-counter" class="text-[10px] font-bold text-slate-400 bg-slate-50 px-2 py-0.5 rounded-full border border-slate-100 uppercase">
                    В ОЧЕРЕДИ: 0
                </span>
            </div>
        </header>
 
        <!-- Main Content Area -->
        <main id="main-view" class="flex-1 relative overflow-hidden flex flex-col bg-white">
            <!-- Content will be injected here via JS -->
        </main>
 
        <!-- Bottom Navigation -->
        <nav class="px-12 py-6 border-t flex justify-between items-center bg-white shrink-0">
            <button onclick="switchView('explore')" id="nav-explore" class="transition-all text-orange-500 scale-125">
                <i data-lucide="sparkles" class="w-6 h-6"></i>
            </button>
            <button onclick="attemptAccessChat()" id="nav-matches" class="transition-all text-slate-300 hover:text-slate-400">
                <i data-lucide="message-circle" class="w-6 h-6"></i>
            </button>
            <button onclick="switchView('profile')" id="nav-profile" class="transition-all text-slate-300 hover:text-slate-400">
                <i data-lucide="user" class="w-6 h-6"></i>
            </button>
        </nav>
 
        <!-- Paywall Overlay (hidden by default) -->
        <div id="paywall" class="hidden absolute inset-0 z-[100] bg-slate-900/70 backdrop-blur-sm flex items-end sm:items-center justify-center p-4">
            <div class="bg-white w-full max-w-sm rounded-[3.5rem] p-8 animate-slide-up relative">
                <button onclick="closePaywall()" class="absolute top-8 right-8 text-slate-300 hover:text-slate-500 transition-colors">
                    <i data-lucide="x" class="w-6 h-6"></i>
                </button>
                <div class="text-center pt-4">
                    <div class="w-20 h-20 bg-orange-100 rounded-[2rem] flex items-center justify-center text-orange-500 mx-auto mb-6 shadow-inner">
                        <i data-lucide="sparkles" class="w-10 h-10"></i>
                    </div>
                    <h2 class="text-2xl font-black text-slate-800 mb-2">Котиндер PLUS</h2>
                    <p class="text-slate-500 text-sm leading-relaxed mb-8 font-medium">Хотите безлимитно общаться с котиками? Подписка стоит всего 10 мисок паштета в месяц!</p>
 
                    <div id="payment-idle">
                        <button onclick="handlePayment()" class="w-full py-5 bg-slate-900 text-white font-black rounded-2xl hover:bg-slate-800 transition-all shadow-lg active:scale-95">
                            Оплатить 10 мисок паштета
                        </button>
                    </div>
 
                    <div id="payment-processing" class="hidden py-6 flex flex-col items-center">
                        <i data-lucide="loader-2" class="w-8 h-8 animate-spin text-orange-500 mb-3"></i>
                        <p class="text-[10px] font-black text-slate-400 uppercase tracking-widest text-center">Проверяем наличие рыбы в банке...</p>
                    </div>
 
                    <div id="payment-error" class="hidden">
                        <div class="bg-red-50 text-red-500 p-5 rounded-3xl flex items-start gap-4 text-left mb-6 border border-red-100 shadow-sm">
                            <i data-lucide="alert-circle" class="shrink-0 mt-0.5 w-5 h-5"></i>
                            <div>
                                <p class="font-black text-sm uppercase">Ошибка оплаты</p>
                                <p class="text-xs font-medium opacity-80 mt-1 leading-relaxed">Транзакция отклонена кошачьим советом. Вероятно, вы забыли погладить пушистого или паштет просрочен.</p>
                            </div>
                        </div>
                        <button onclick="resetPayment()" class="text-orange-500 font-black text-xs uppercase tracking-widest hover:underline">
                            Попробовать еще раз
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>
 
    <script>
        const apiKey = ""; // Gemini API Key
        const CAT_NAMES = ["Мурзик", "Барсик", "Снежок", "Рыжик", "Борис", "Пират", "Зефир", "Альф", "Барон", "Василий", "Гарфилд", "Дымок", "Симба", "Лео", "Марс", "Пушок", "Кекс", "Тигр", "Шерлок", "Буся"];
        const CAT_BIOS = ["Люблю коробки больше жизни.", "Ищу того, кто чешет за ушком.", "Тыгыдык в 3 утра — мое призвание.", "Твой будущий хозяин.", "Ем цветы, сплю на клавиатуре.", "Я не толстый, я пушистый.", "Сплю 22 часа в сутки."];
        const CAT_PERSONALITIES = ["Ласковый", "Игривый", "Гордый", "Ленивый", "Хитрый", "Умный"];
 
        let queue = [];
        let matches = [];
        let currentView = 'explore';
        let isPremium = false;
        let isFetching = false;
 
        // --- Core Logic ---
 
        async function callGemini(prompt) {
            if (!apiKey) return "Мяу! У нас мэтч! 🐾";
            const url = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-09-2025:generateContent?key=${apiKey}`;
            try {
                const response = await fetch(url, {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify({ contents: [{ parts: [{ text: prompt }] }] })
                });
                const result = await response.json();
                return result.candidates?.[0]?.content?.parts?.[0]?.text || "Мяу! 🐾";
            } catch (e) { return "Мяу! 🐾"; }
        }
 
        async function fillQueue() {
            if (isFetching || queue.length >= 5) return;
            isFetching = true;
            document.getElementById('loader-spinner').classList.remove('hidden');
 
            try {
                const res = await fetch(`https://api.thecatapi.com/v1/images/search?limit=5&mime_types=jpg,png`);
                const data = await res.json();
                const newCats = data.map(item => ({
                    id: Math.random().toString(36).substring(7),
                    url: item.url,
                    name: CAT_NAMES[Math.floor(Math.random() * CAT_NAMES.length)],
                    bio: CAT_BIOS[Math.floor(Math.random() * CAT_BIOS.length)],
                    personality: CAT_PERSONALITIES[Math.floor(Math.random() * CAT_PERSONALITIES.length)],
                    distance: Math.floor(Math.random() * 15) + 1,
                    age: Math.floor(Math.random() * 12) + 1
                }));
                queue = [...queue, ...newCats];
                updateUI();
            } catch (err) {
                console.error("Ошибка API Котиков", err);
            } finally {
                isFetching = false;
                document.getElementById('loader-spinner').classList.add('hidden');
            }
        }
 
        async function handleLike(cat) {
            if (Math.random() < 0.3) { // 30% chance of match
                const aiMsg = await callGemini(`Напиши короткое милое кошачье приветствие от кота по имени ${cat.name} на русском языке.`);
                matches.unshift({
                    ...cat,
                    lastMessage: aiMsg,
                    time: new Date().toLocaleTimeString([], { hour: '2-digit', minute: '2-digit' })
                });
            }
        }
 
        // --- View Management ---
 
        function switchView(view) {
            currentView = view;
            const main = document.getElementById('main-view');
 
            // Update nav styles
            const navIds = ['explore', 'matches', 'profile'];
            navIds.forEach(id => {
                const btn = document.getElementById(`nav-${id}`);
                if (id === view) {
                    btn.classList.add('text-orange-500', 'scale-125');
                    btn.classList.remove('text-slate-300');
                } else {
                    btn.classList.remove('text-orange-500', 'scale-125');
                    btn.classList.add('text-slate-300');
                }
            });
 
            renderView();
        }
 
        function attemptAccessChat() {
            if (!isPremium) {
                document.getElementById('paywall').classList.remove('hidden');
                lucide.createIcons();
            } else {
                switchView('matches');
            }
        }
 
        function renderView() {
            const main = document.getElementById('main-view');
            document.getElementById('queue-counter').textContent = `В ОЧЕРЕДИ: ${queue.length}`;
 
            if (currentView === 'explore') {
                if (queue.length === 0) {
                    main.innerHTML = `
                        <div class="flex-1 flex flex-col items-center justify-center p-4">
                            <i data-lucide="loader-2" class="animate-spin text-orange-500 w-10 h-10 mb-4"></i>
                            <p class="text-slate-400 font-bold text-sm">Ищем пушистых поблизости...</p>
                        </div>
                    `;
                } else {
                    const cat = queue[0];
                    main.innerHTML = `
                        <div class="flex-1 flex flex-col items-center justify-center p-4 relative">
                            <div id="swipe-card" class="relative w-full aspect-[4/5.2] rounded-[2.5rem] shadow-2xl overflow-hidden cursor-grab active:cursor-grabbing transition-transform no-select" style="touch-action: none;">
                                <img src="${cat.url}" class="w-full h-full object-cover pointer-events-none no-select" draggable="false">
 
                                <!-- Overlays -->
                                <div id="like-badge" class="swipe-overlay opacity-0 absolute top-10 left-8 border-4 border-green-500 text-green-500 font-black text-3xl px-4 py-1 rounded-xl uppercase -rotate-12">МЯУ</div>
                                <div id="nope-badge" class="swipe-overlay opacity-0 absolute top-10 right-8 border-4 border-red-500 text-red-500 font-black text-3xl px-4 py-1 rounded-xl uppercase rotate-12">ПФФ</div>
 
                                <div class="absolute bottom-0 inset-x-0 bg-gradient-to-t from-black/90 via-black/20 to-transparent p-8 text-white">
                                    <h2 class="text-3xl font-bold">${cat.name}, ${cat.age}</h2>
                                    <p class="text-xs font-medium opacity-80 mt-1 flex items-center gap-1.5">
                                       <span class="w-2 h-2 bg-green-500 rounded-full"></span> В ${cat.distance} км от вас
                                    </p>
                                    <p class="mt-4 text-lg font-medium leading-snug">"${cat.bio}"</p>
                                    <div class="mt-4 inline-block px-3 py-1 bg-white/20 backdrop-blur-md rounded-full text-[10px] font-bold uppercase tracking-wider">
                                        ${cat.personality}
                                    </div>
                                </div>
                            </div>
                            <div class="flex gap-8 mt-8">
                                <button onclick="triggerSwipe('left')" class="p-4 bg-white rounded-full shadow-xl text-red-500 hover:scale-110 active:scale-90 transition-all border border-slate-50"><i data-lucide="x" class="w-8 h-8"></i></button>
                                <button onclick="triggerSwipe('right')" class="p-4 bg-white rounded-full shadow-xl text-green-500 hover:scale-110 active:scale-90 transition-all border border-slate-50"><i data-lucide="heart" class="w-8 h-8" style="fill: currentColor"></i></button>
                            </div>
                        </div>
                    `;
                    initSwipeLogic();
                }
            } else if (currentView === 'matches') {
                main.innerHTML = `
                    <div class="flex-1 p-6 overflow-y-auto">
                        <div class="flex items-center justify-between mb-8">
                            <h2 class="text-xs font-black text-slate-400 uppercase tracking-widest">Новые пары</h2>
                            <div class="flex items-center gap-1 text-[9px] font-black text-orange-500 bg-orange-50 px-2 py-1 rounded-full border border-orange-100">
                                <i data-lucide="lock" class="w-2.5 h-2.5"></i> PLUS
                            </div>
                        </div>
                        <div class="space-y-4">
                            ${matches.length === 0 ? `
                                <div class="text-center py-20 px-10">
                                    <div class="w-16 h-16 bg-slate-50 rounded-full flex items-center justify-center mx-auto mb-4">
                                        <i data-lucide="heart" class="text-slate-200 w-8 h-8"></i>
                                    </div>
                                    <p class="text-slate-400 text-sm font-medium">Свайпайте вправо, чтобы найти идеального котика!</p>
                                </div>
                            ` : matches.map(m => `
                                <div class="flex items-center gap-4 p-4 bg-white rounded-3xl border border-slate-100 shadow-sm blur-[3px] hover:blur-0 transition-all cursor-pointer group">
                                    <img src="${m.url}" class="w-16 h-16 rounded-2xl object-cover shadow-sm">
                                    <div class="flex-1 min-w-0">
                                        <h3 class="font-bold text-slate-800">${m.name}</h3>
                                        <p class="text-xs text-slate-400 truncate mt-0.5">${m.lastMessage}</p>
                                    </div>
                                    <i data-lucide="lock" class="w-4 h-4 text-slate-300 group-hover:text-orange-400"></i>
                                </div>
                            `).join('')}
                        </div>
                    </div>
                `;
            } else if (currentView === 'profile') {
                main.innerHTML = `
                    <div class="flex-1 p-10 flex flex-col items-center text-center overflow-y-auto">
                        <div class="relative mb-8">
                            <div class="w-36 h-36 rounded-[3rem] overflow-hidden border-4 border-white shadow-2xl rotate-2">
                                <img src="https://images.unsplash.com/photo-1514888286974-6c03e2ca1dba?w=400" class="w-full h-full object-cover">
                            </div>
                            <div class="absolute -bottom-2 -right-2 bg-rose-500 p-3 rounded-2xl border-4 border-white text-white shadow-xl">
                                <i data-lucide="user" class="w-5 h-5"></i>
                            </div>
                        </div>
                        <h2 class="text-3xl font-black text-slate-800">Барсик, 3 года</h2>
                        <p class="text-slate-400 text-sm font-bold mt-1 uppercase tracking-wider">Король дивана • Эксперт по сну</p>
 
                        <div class="grid grid-cols-2 gap-4 w-full mt-12">
                            <div class="bg-orange-50/50 p-6 rounded-[2.5rem] border border-orange-100">
                                <div class="text-3xl font-black text-orange-600">42</div>
                                <div class="text-[10px] uppercase font-black text-orange-400 tracking-widest mt-1">Лайков</div>
                            </div>
                            <div class="bg-rose-50/50 p-6 rounded-[2.5rem] border border-rose-100">
                                <div class="text-3xl font-black text-rose-600">${matches.length}</div>
                                <div class="text-[10px] uppercase font-black text-rose-400 tracking-widest mt-1">Мэтчей</div>
                            </div>
                        </div>
 
                        <button onclick="document.getElementById('paywall').classList.remove('hidden'); lucide.createIcons();" class="mt-10 w-full py-5 bg-gradient-to-r from-orange-500 to-rose-500 text-white font-black rounded-3xl shadow-xl hover:opacity-90 transition-all flex items-center justify-center gap-3 uppercase tracking-widest text-xs">
                            <i data-lucide="sparkles" class="w-4 h-4"></i> Котиндер Gold ✨
                        </button>
                    </div>
                `;
            }
            lucide.createIcons();
        }
 
        // --- Swipe Logic ---
 
        function initSwipeLogic() {
            const card = document.getElementById('swipe-card');
            if (!card) return;
 
            let startX = 0;
            let currentX = 0;
            let isDragging = false;
 
            const handleStart = (e) => {
                isDragging = true;
                startX = e.clientX || e.touches[0].clientX;
                card.style.transition = 'none';
            };
 
            const handleMove = (e) => {
                if (!isDragging) return;
                currentX = (e.clientX || e.touches[0].clientX) - startX;
                const rotation = currentX * 0.05;
                card.style.transform = `translateX(${currentX}px) rotate(${rotation}deg)`;
 
                // Overlay opacity
                document.getElementById('like-badge').style.opacity = Math.max(0, currentX / 100);
                document.getElementById('nope-badge').style.opacity = Math.max(0, -currentX / 100);
            };
 
            const handleEnd = () => {
                if (!isDragging) return;
                isDragging = false;
                if (currentX > 120) {
                    completeSwipe('right');
                } else if (currentX < -120) {
                    completeSwipe('left');
                } else {
                    card.style.transition = 'transform 0.3s ease';
                    card.style.transform = '';
                    document.getElementById('like-badge').style.opacity = 0;
                    document.getElementById('nope-badge').style.opacity = 0;
                }
                currentX = 0;
            };
 
            card.addEventListener('mousedown', handleStart);
            card.addEventListener('mousemove', handleMove);
            window.addEventListener('mouseup', handleEnd);
            card.addEventListener('touchstart', handleStart);
            card.addEventListener('touchmove', handleMove);
            card.addEventListener('touchend', handleEnd);
        }
 
        function triggerSwipe(dir) {
            const card = document.getElementById('swipe-card');
            if (!card) return;
            card.style.transition = 'transform 0.4s ease-in';
            card.style.transform = dir === 'right' ? 'translateX(500px) rotate(20deg)' : 'translateX(-500px) rotate(-20deg)';
            setTimeout(() => completeSwipe(dir), 300);
        }
 
        function completeSwipe(dir) {
            const cat = queue.shift();
            if (dir === 'right') handleLike(cat);
            fillQueue();
            renderView();
        }
 
        // --- Paywall & Payment ---
 
        function closePaywall() {
            document.getElementById('paywall').classList.add('hidden');
            resetPayment();
        }
 
        function handlePayment() {
            document.getElementById('payment-idle').classList.add('hidden');
            document.getElementById('payment-processing').classList.remove('hidden');
 
            setTimeout(() => {
                document.getElementById('payment-processing').classList.add('hidden');
                document.getElementById('payment-error').classList.remove('hidden');
                lucide.createIcons();
            }, 2000);
        }
 
        function resetPayment() {
            document.getElementById('payment-idle').classList.remove('hidden');
            document.getElementById('payment-processing').classList.add('hidden');
            document.getElementById('payment-error').classList.add('hidden');
        }
 
        function updateUI() {
            if (currentView === 'explore' && queue.length > 0) {
                renderView();
            } else {
                document.getElementById('queue-counter').textContent = `В ОЧЕРЕДИ: ${queue.length}`;
            }
        }
 
        // --- Init ---
        window.onload = () => {
            fillQueue();
            renderView();
        };
    </script>
</body>
</html>
