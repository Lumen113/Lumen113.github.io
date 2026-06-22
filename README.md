# Lumen113.github.io
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LUMEN SMP — Правила</title>
    <style>
        /* ===== ТЁМНО-СИНИЙ ФОН + ФИОЛЕТОВАЯ ПУЛЬСАЦИЯ ===== */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: 'Segoe UI', Roboto, system-ui, sans-serif;
            padding: 30px 20px;
            background: #0a1628; /* ТЁМНО-СИНИЙ БАЗОВЫЙ */
            color: #e0e6ed;
            position: relative;
            overflow-x: hidden;
        }

        /* ФИОЛЕТОВАЯ ПУЛЬСИРУЮЩАЯ ПОДЛОЖКА */
        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at 50% 50%, rgba(160, 80, 255, 0.25), rgba(0, 0, 0, 0) 80%);
            animation: purplePulse 5s ease-in-out infinite alternate;
            pointer-events: none;
            z-index: 0;
        }

        @keyframes purplePulse {
            0%   { opacity: 0.2; transform: scale(0.95); }
            100% { opacity: 0.9; transform: scale(1.3); }
        }

        /* ===== КОНТЕЙНЕР ===== */
        .container {
            max-width: 900px;
            width: 100%;
            background: rgba(12, 22, 42, 0.92);
            backdrop-filter: blur(4px);
            padding: 30px 35px;
            border-radius: 28px;
            box-shadow: 0 12px 40px rgba(0, 0, 0, 0.9), 0 0 40px rgba(160, 80, 255, 0.08);
            border: 1px solid rgba(160, 80, 255, 0.12);
            position: relative;
            z-index: 1;
        }

        /* ===== СИНИЙ ЗАГОЛОВОК ===== */
        .main-title {
            font-size: 3rem;
            font-weight: 800;
            color: #3b82f6;
            text-shadow: 0 0 20px rgba(59, 130, 246, 0.4);
            letter-spacing: 2px;
            margin-bottom: 4px;
            text-align: center;
        }

        .rules-heading {
            color: #b0c4de;
            font-size: 1.2rem;
            font-weight: 600;
            text-align: center;
            border-bottom: 2px solid #1e2a4a;
            padding-bottom: 12px;
            margin-bottom: 28px;
            letter-spacing: 1px;
        }

        /* ===== СЕКЦИИ С ОБВОДКАМИ ===== */
        .section {
            margin-bottom: 32px;
            padding: 18px 20px;
            border-radius: 16px;
            border: 3px solid transparent;
            background: rgba(0, 0, 0, 0.30);
        }

        .section-red    { border-color: #dc2626; box-shadow: 0 0 18px rgba(220, 38, 38, 0.10); }
        .section-orange { border-color: #f97316; box-shadow: 0 0 18px rgba(249, 115, 22, 0.10); }
        .section-black  { border-color: #555555; box-shadow: 0 0 18px rgba(85, 85, 85, 0.08); }
        .section-blue   { border-color: #3b82f6; box-shadow: 0 0 18px rgba(59, 130, 246, 0.10); }

        .section-title {
            font-size: 1.5rem;
            font-weight: 700;
            color: #ffffff;
            margin-bottom: 14px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        .section-title span {
            background: #1f2c3a;
            padding: 0 14px;
            border-radius: 40px;
            font-size: 0.9rem;
            color: #8aa9d9;
        }

        /* ===== ПУНКТЫ ПРАВИЛ ===== */
        .rule-item {
            background: rgba(20, 30, 50, 0.6);
            padding: 10px 16px;
            margin-bottom: 8px;
            border-radius: 10px;
            border-left: 4px solid #3b6a9c;
        }
        .rule-item strong {
            color: #b8d0f0;
            font-weight: 600;
        }

        .ban  { color: #ff8a80; }
        .mute { color: #ffcc80; }
        .perm { color: #ef5350; font-weight: 700; }
/* ===== ПОДВАЛ ===== */
        .footer {
            margin-top: 30px;
            padding-top: 18px;
            border-top: 1px solid #1e2a4a;
            text-align: center;
            font-size: 1rem;
        }
        .footer a {
            color: #a78bfa;
            text-decoration: none;
            font-weight: 600;
        }
        .footer a:hover {
            text-decoration: underline;
        }

        /* ===== АДАПТАЦИЯ ===== */
        @media (max-width: 640px) {
            .container { padding: 18px 14px; }
            .main-title { font-size: 2.2rem; }
            .section { padding: 12px 12px; }
        }
    </style>
</head>
<body>
<div class="container">

    <!-- ЗАГОЛОВОК -->
    <div class="main-title">LUMEN_SMP</div>
    <div class="rules-heading">✦ Правила сервера:</div>

    <!-- ПУНКТ 1 — КРАСНАЯ ОБВОДКА -->
    <div class="section section-red">
        <div class="section-title">❶ Постороннее ПО</div>
        <div class="rule-item"><strong>1.1</strong> игра с читами (если спалил античит 15 дней) — <span class="ban">бан 30 дней</span></div>
        <div class="rule-item"><strong>1.2</strong> Ресурс пак или мод X-Ray — <span class="ban">бан 7 дней</span></div>
        <div class="rule-item"><strong>1.3</strong> Killaura, trigger bot или всё что есть в читах (визуальные функции и автосвап не считается) — <span class="ban">бан 30 дней</span></div>
        <div class="rule-item"><strong>1.4</strong> Моды по типу freeCam или replay mod (позволяют видеть то, что не должны) — <span class="ban">бан 1 день</span></div>
        <div class="rule-item"><strong>1.5</strong> использование Rival visuals, Luminar visuals (из-за присутствия freecam и других запрещённых функций) — <span class="ban">бан 7 дней</span></div>
    </div>

    <!-- ПУНКТ 2 — ОРАНЖЕВАЯ ОБВОДКА -->
    <div class="section section-orange">
        <div class="section-title">❷ Муты</div>
        <div class="rule-item"><strong>2.1</strong> оскорбление игроков — <span class="mute">мут 15 мин</span></div>
        <div class="rule-item"><strong>2.2</strong> оскорбление родственников игрока — <span class="mute">мут 1 день</span></div>
        <div class="rule-item"><strong>2.3</strong> оскорбление администрации (от Modera до Ownera) — <span class="mute">мут 15 дней</span></div>
        <div class="rule-item"><strong>2.4</strong> оскорбление родственников администрации — <span class="mute">мут 30 дней</span></div>
        <div class="rule-item"><strong>2.5</strong> предложение построения лаг машин — <span class="ban">бан 1 день</span></div>
        <div class="rule-item"><strong>2.6</strong> палить пароль игрока который вам доверил свой пароль аккаунта — <span class="perm">мут навсегда</span></div>
        <div class="rule-item"><strong>2.7</strong> разговоры о сексуальных действиях — <span class="mute">мут 10 мин</span></div>
    </div>

    <!-- ПУНКТ 3 — ЧЁРНАЯ ОБВОДКА -->
    <div class="section section-black">
        <div class="section-title">❸ Лаг машины и тому подобное</div>
        <div class="rule-item"><strong>3.1</strong> постройка лаг машины (если не успел запустить) — <span class="ban">бан 15 дней</span></div>
        <div class="rule-item"><strong>3.2</strong> постройка лаг машины (если запустил её) — <span class="ban">бан 20 дней</span></div>
        <div class="rule-item"><strong>3.3</strong> если построил запустил и она крашнула сервер до отката — <span class="perm">бан навсегда</span></div>
        <div class="rule-item"><strong>3.4</strong> если что то построил такое по случайности и оно крашнуло сервер — <span class="ban">бан 7 дней</span></div>
    </div>

    <!-- ПУНКТ 4 — СИНЯЯ ОБВОДКА -->
    <div class="section section-blue">
        <div class="section-title">❹ Для администрации</div>
        <div class="rule-item"><strong>4.1</strong> оскорбление игрока — <span class="mute">снятие 1 час</span></div>
<div class="rule-item"><strong>4.2</strong> подкуп от игрока и бан в пвп режиме — <span class="ban">снятие 3 недели</span></div>
        <div class="rule-item"><strong>4.3</strong> оскорбление администратора выше по званию — <span class="mute">снятие 1 час</span></div>
        <div class="rule-item"><strong>4.4</strong> не забанить игрока за читы или другое нарушение — <span class="ban">снятие 5 дней</span></div>
        <div class="rule-item"><strong>4.5</strong> бан за просто так: если бан на 1 день — <span class="ban">снятие 10 дней</span> / 7-20 — <span class="ban">снятие 30 дней</span> / 20-любое число — <span class="perm">снятие навсегда</span></div>
    </div>

    <!-- ПОДВАЛ -->
    <div class="footer">
        📩 <strong>Подавать заявки на администрацию или медиа сюда:</strong><br>
        <a href="https://t.me/mrtip52" target="_blank">@mrtip52</a>
    </div>

</div>
</body>
</html>
