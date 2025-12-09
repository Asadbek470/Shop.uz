# Shop.uz
Shop
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Asadbek IT Services | Профессиональные IT-услуги в Узбекистане</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #2A5C8A;
            --secondary: #F7B731;
            --accent: #E74C3C;
            --dark: #2C3E50;
            --light: #ECF0F1;
            --success: #27AE60;
            --marketplace-bg: #F8F9FA;
            --card-shadow: 0 8px 30px rgba(0, 0, 0, 0.08);
            --hover-shadow: 0 15px 40px rgba(0, 0, 0, 0.15);
            --border-radius: 16px;
            --transition: all 0.3s ease;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
        }
        
        body {
            background-color: var(--marketplace-bg);
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header */
        .header {
            background: linear-gradient(135deg, var(--dark) 0%, var(--primary) 100%);
            color: white;
            padding: 20px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .logo h1 {
            font-size: 28px;
            font-weight: 700;
            background: linear-gradient(to right, #fff, var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .logo-icon {
            background: var(--secondary);
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            color: var(--dark);
        }
        
        .user-panel {
            display: flex;
            align-items: center;
            gap: 25px;
        }
        
        .user-balance {
            display: flex;
            align-items: center;
            gap: 10px;
            background: rgba(255, 255, 255, 0.15);
            padding: 10px 20px;
            border-radius: 50px;
            backdrop-filter: blur(10px);
        }
        
        .coins {
            font-weight: 700;
            color: var(--secondary);
        }
        
        .vip-badge {
            background: linear-gradient(45deg, #FFD700, #FFA500);
            color: #000;
            padding: 8px 20px;
            border-radius: 50px;
            font-weight: 700;
            display: flex;
            align-items: center;
            gap: 8px;
            box-shadow: 0 4px 15px rgba(255, 165, 0, 0.3);
        }
        
        .whatsapp-header {
            background: var(--success);
            color: white;
            padding: 12px 25px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 10px;
            transition: var(--transition);
        }
        
        .whatsapp-header:hover {
            background: #1E8449;
            transform: translateY(-2px);
            box-shadow: 0 8px 20px rgba(39, 174, 96, 0.3);
        }
        
        /* Language Switcher */
        .language-switcher {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-left: 20px;
        }
        
        .lang-btn {
            background: rgba(255, 255, 255, 0.2);
            border: none;
            color: white;
            padding: 8px 15px;
            border-radius: 20px;
            cursor: pointer;
            font-weight: 600;
            transition: var(--transition);
        }
        
        .lang-btn.active {
            background: var(--secondary);
            color: var(--dark);
        }
        
        .lang-btn:hover:not(.active) {
            background: rgba(255, 255, 255, 0.3);
        }
        
        /* Developer Section */
        .developer-section {
            padding: 80px 0 40px;
            background: white;
            border-radius: 0 0 var(--border-radius) var(--border-radius);
            margin-bottom: 40px;
            box-shadow: var(--card-shadow);
        }
        
        .developer-card {
            display: flex;
            gap: 40px;
            align-items: center;
        }
        
        .developer-avatar {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--primary), var(--dark));
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 70px;
            color: white;
            box-shadow: 0 15px 35px rgba(42, 92, 138, 0.2);
            flex-shrink: 0;
        }
        
        .developer-info h2 {
            font-size: 36px;
            color: var(--dark);
            margin-bottom: 10px;
        }
        
        .developer-title {
            color: var(--primary);
            font-size: 20px;
            margin-bottom: 20px;
            font-weight: 600;
        }
        
        .developer-bio {
            color: #555;
            margin-bottom: 25px;
            font-size: 17px;
            max-width: 800px;
        }
        
        .experience-badges {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
        }
        
        .badge {
            background: var(--light);
            padding: 10px 20px;
            border-radius: 50px;
            font-weight: 600;
            color: var(--dark);
            display: flex;
            align-items: center;
            gap: 8px;
            border: 2px solid transparent;
            transition: var(--transition);
        }
        
        .badge:hover {
            border-color: var(--secondary);
            transform: translateY(-3px);
        }
        
        /* Services Section */
        .section-title {
            font-size: 32px;
            color: var(--dark);
            margin-bottom: 10px;
            position: relative;
            display: inline-block;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 60px;
            height: 4px;
            background: var(--secondary);
            border-radius: 2px;
        }
        
        .section-subtitle {
            color: #666;
            margin-bottom: 40px;
            font-size: 18px;
        }
        
        .services-section {
            padding: 60px 0;
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 30px;
        }
        
        .service-card {
            background: white;
            border-radius: var(--border-radius);
            padding: 30px;
            box-shadow: var(--card-shadow);
            transition: var(--transition);
            border: 1px solid #eee;
            position: relative;
            overflow: hidden;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--hover-shadow);
        }
        
        .service-icon {
            width: 70px;
            height: 70px;
            border-radius: 16px;
            background: linear-gradient(135deg, var(--primary), #3A7BB8);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 28px;
            color: white;
            margin-bottom: 20px;
        }
        
        .service-card h3 {
            font-size: 22px;
            color: var(--dark);
            margin-bottom: 15px;
        }
        
        .service-description {
            color: #666;
            margin-bottom: 25px;
            min-height: 60px;
        }
        
        .price-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
        }
        
        .original-price {
            font-size: 18px;
            color: #999;
            text-decoration: line-through;
        }
        
        .current-price {
            font-size: 28px;
            font-weight: 700;
            color: var(--primary);
        }
        
        .vip-discount {
            background: linear-gradient(45deg, #FFD700, #FFA500);
            color: #000;
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 14px;
            font-weight: 700;
            position: absolute;
            top: 20px;
            right: 20px;
        }
        
        .buy-button {
            width: 100%;
            background: var(--primary);
            color: white;
            border: none;
            padding: 15px;
            border-radius: 12px;
            font-weight: 600;
            font-size: 16px;
            cursor: pointer;
            transition: var(--transition);
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
        }
        
        .buy-button:hover {
            background: var(--dark);
            transform: translateY(-2px);
        }
        
        .buy-button.vip-only {
            background: linear-gradient(45deg, #FFD700, #FFA500);
            color: #000;
        }
        
        .vip-note {
            font-size: 12px;
            color: #999;
            margin-top: 10px;
            text-align: center;
        }
        
        /* Custom Price Section */
        .custom-price-section {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            padding: 60px 0;
            border-radius: var(--border-radius);
            margin: 40px 0;
            color: white;
            text-align: center;
        }
        
        .custom-price-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .custom-price-title {
            font-size: 36px;
            margin-bottom: 20px;
        }
        
        .custom-price-description {
            font-size: 18px;
            margin-bottom: 30px;
            opacity: 0.9;
        }
        
        .price-calculator {
            background: rgba(255, 255, 255, 0.1);
            padding: 30px;
            border-radius: var(--border-radius);
            backdrop-filter: blur(10px);
        }
        
        .price-slider {
            width: 100%;
            margin: 20px 0;
        }
        
        .calculated-price {
            font-size: 32px;
            font-weight: bold;
            color: var(--secondary);
            margin: 20px 0;
        }
        
        /* Friday Raffle Section */
        .friday-section {
            padding: 80px 0;
            background: linear-gradient(135deg, var(--dark) 0%, #1a2c42 100%);
            color: white;
            border-radius: var(--border-radius);
            margin: 40px 0;
            position: relative;
            overflow: hidden;
        }
        
        .friday-section::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" preserveAspectRatio="none"><path d="M0,0 L100,0 L100,100 Z" fill="rgba(255,255,255,0.03)"/></svg>');
            background-size: cover;
        }
        
        .friday-content {
            display: flex;
            align-items: center;
            gap: 60px;
            position: relative;
            z-index: 1;
        }
        
        .friday-text {
            flex: 1;
        }
        
        .friday-text h2 {
            font-size: 42px;
            margin-bottom: 20px;
            color: white;
        }
        
        .friday-text h2 span {
            color: var(--secondary);
        }
        
        .friday-description {
            font-size: 18px;
            margin-bottom: 30px;
            opacity: 0.9;
        }
        
        .countdown {
            background: rgba(255, 255, 255, 0.1);
            padding: 25px;
            border-radius: var(--border-radius);
            backdrop-filter: blur(10px);
            margin-bottom: 30px;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .countdown-title {
            font-size: 20px;
            margin-bottom: 15px;
            color: var(--secondary);
        }
        
        .countdown-timer {
            font-size: 36px;
            font-weight: 700;
            font-family: monospace;
            color: white;
        }
        
        .spin-button {
            background: linear-gradient(45deg, var(--secondary), #FF9F43);
            color: #000;
            border: none;
            padding: 18px 40px;
            border-radius: 50px;
            font-size: 20px;
            font-weight: 700;
            cursor: pointer;
            transition: var(--transition);
            display: inline-flex;
            align-items: center;
            gap: 15px;
        }
        
        .spin-button:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(255, 183, 49, 0.4);
        }
        
        .spin-button:disabled {
            opacity: 0.6;
            cursor: not-allowed;
        }
        
        .roulette-container {
            flex: 1;
            display: flex;
            justify-content: center;
        }
        
        .roulette {
            width: 300px;
            height: 300px;
            border-radius: 50%;
            background: conic-gradient(
                from 0deg,
                #e94560 0deg 30deg,
                #0f3460 30deg 60deg,
                #f9a826 60deg 90deg,
                #1f4068 90deg 120deg,
                #ff6b9d 120deg 150deg,
                #16213e 150deg 180deg,
                #e94560 180deg 210deg,
                #0f3460 210deg 240deg,
                #f9a826 240deg 270deg,
                #1f4068 270deg 300deg,
                #ff6b9d 300deg 330deg,
                #16213e 330deg 360deg
            );
            position: relative;
            transition: transform 3s cubic-bezier(0.2, 0.8, 0.3, 1);
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.3);
            border: 8px solid white;
        }
        
        .roulette-pointer {
            position: absolute;
            top: -25px;
            left: 50%;
            transform: translateX(-50%);
            width: 50px;
            height: 50px;
            background: var(--secondary);
            clip-path: polygon(50% 0%, 0% 100%, 100% 100%);
            z-index: 10;
            filter: drop-shadow(0 5px 10px rgba(0, 0, 0, 0.3));
        }
        
        /* Reviews Section */
        .reviews-section {
            padding: 80px 0;
            background: white;
            border-radius: var(--border-radius);
            margin: 40px 0;
            box-shadow: var(--card-shadow);
        }
        
        .reviews-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }
        
        .review-card {
            background: var(--light);
            padding: 30px;
            border-radius: var(--border-radius);
            box-shadow: var(--card-shadow);
            transition: var(--transition);
            border-left: 5px solid var(--secondary);
        }
        
        .review-card:hover {
            transform: translateY(-5px);
            box-shadow: var(--hover-shadow);
        }
        
        .review-text {
            font-style: italic;
            margin-bottom: 25px;
            color: #555;
            line-height: 1.8;
        }
        
        .review-author {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .review-avatar {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: var(--primary);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
        }
        
        .author-info h4 {
            color: var(--dark);
            margin-bottom: 5px;
        }
        
        .author-location {
            color: #777;
            font-size: 14px;
            display: flex;
            align-items: center;
            gap: 5px;
        }
        
        /* Contact Section */
        .contact-section {
            padding: 80px 0;
            background: linear-gradient(135deg, var(--primary) 0%, #1a4a7a 100%);
            color: white;
            border-radius: var(--border-radius);
            margin: 40px 0;
            text-align: center;
        }
        
        .contact-section .section-title {
            color: white;
        }
        
        .contact-section .section-title::after {
            background: var(--secondary);
        }
        
        .whatsapp-contact {
            background: var(--success);
            color: white;
            padding: 20px 40px;
            border-radius: 50px;
            text-decoration: none;
            font-size: 24px;
            font-weight: 700;
            display: inline-flex;
            align-items: center;
            gap: 15px;
            margin: 40px 0;
            transition: var(--transition);
            box-shadow: 0 10px 30px rgba(39, 174, 96, 0.3);
        }
        
        .whatsapp-contact:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(39, 174, 96, 0.5);
            background: #1E8449;
        }
        
        .contact-info {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 40px;
            flex-wrap: wrap;
        }
        
        .contact-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 10px;
        }
        
        .contact-icon {
            width: 60px;
            height: 60px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
        }
        
        /* Footer */
        .footer {
            background: var(--dark);
            color: white;
            padding: 40px 0;
            text-align: center;
            margin-top: 60px;
        }
        
        .footer-logo {
            font-size: 24px;
            font-weight: 700;
            margin-bottom: 20px;
            color: var(--secondary);
        }
        
        .country-badge {
            background: var(--accent);
            color: white;
            padding: 10px 25px;
            border-radius: 50px;
            display: inline-block;
            margin: 20px 0;
            font-weight: 600;
        }
        
        .copyright {
            margin-top: 30px;
            color: #aaa;
            font-size: 14px;
        }
        
        /* Modal Windows */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            z-index: 2000;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }
        
        .modal-content {
            background: white;
            padding: 40px;
            border-radius: var(--border-radius);
            max-width: 500px;
            width: 100%;
            box-shadow: 0 30px 60px rgba(0, 0, 0, 0.3);
            animation: modalAppear 0.5s ease;
            position: relative;
        }
        
        @keyframes modalAppear {
            from { opacity: 0; transform: translateY(-50px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .modal-close {
            position: absolute;
            top: 20px;
            right: 20px;
            background: none;
            border: none;
            font-size: 24px;
            cursor: pointer;
            color: #999;
            transition: var(--transition);
        }
        
        .modal-close:hover {
            color: var(--accent);
        }
        
        .modal-title {
            color: var(--dark);
            font-size: 28px;
            margin-bottom: 20px;
            text-align: center;
        }
        
        .modal-text {
            text-align: center;
            color: #666;
            margin-bottom: 30px;
        }
        
        /* Responsive */
        @media (max-width: 992px) {
            .friday-content {
                flex-direction: column;
                text-align: center;
            }
            
            .developer-card {
                flex-direction: column;
                text-align: center;
            }
            
            .header-content {
                flex-wrap: wrap;
                gap: 20px;
            }
            
            .user-panel {
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .language-switcher {
                margin-left: 0;
            }
        }
        
        @media (max-width: 768px) {
            .services-grid, .reviews-grid {
                grid-template-columns: 1fr;
            }
            
            .friday-text h2 {
                font-size: 32px;
            }
            
            .developer-avatar {
                width: 150px;
                height: 150px;
                font-size: 60px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="header">
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <div class="logo-icon">
                        <i class="fas fa-code"></i>
                    </div>
                    <h1 id="site-title">Asadbek IT Services</h1>
                </div>
                <div class="user-panel">
                    <div class="user-balance">
                        <i class="fas fa-coins" style="color: var(--secondary);"></i>
                        <span class="coins" id="coins-text">Монетки: <span id="coins">1,250</span></span>
                    </div>
                    <div class="vip-badge" id="premium-badge" style="display: none;">
                        <i class="fas fa-crown"></i>
                        <span id="vip-text">VIP ПРЕМИУМ</span>
                    </div>
                    <div class="language-switcher">
                        <button class="lang-btn active" id="lang-ru">RU</button>
                        <button class="lang-btn" id="lang-uz">UZ</button>
                    </div>
                    <a href="https://wa.me/998999100097" class="whatsapp-header" target="_blank">
                        <i class="fab fa-whatsapp"></i>
                        <span id="whatsapp-text">WhatsApp +998 99 910-00-97</span>
                    </a>
                </div>
            </div>
        </div>
    </header>

    <!-- Developer Section -->
    <section class="developer-section">
        <div class="container">
            <div class="developer-card">
                <div class="developer-avatar">
                    <i class="fas fa-user-tie"></i>
                </div>
                <div class="developer-info">
                    <h2 id="dev-name">Асадбек</h2>
                    <div class="developer-title" id="dev-title">Full-Stack Разработчик & IT-Специалист</div>
                    <div class="developer-bio" id="dev-bio">
                        Профессиональный IT-специалист с 2-летним опытом в создании современных веб-решений, 
                        разработке Telegram ботов, дизайне и автоматизации бизнес-процессов. Специализируюсь 
                        на создании качественных IT-продуктов для бизнеса в Узбекистане.
                    </div>
                    <div class="experience-badges">
                        <div class="badge">
                            <i class="fas fa-calendar-alt"></i>
                            <span id="exp-1">2+ года опыта</span>
                        </div>
                        <div class="badge">
                            <i class="fas fa-project-diagram"></i>
                            <span id="exp-2">50+ завершенных проектов</span>
                        </div>
                        <div class="badge">
                            <i class="fas fa-users"></i>
                            <span id="exp-3">35+ довольных клиентов</span>
                        </div>
                        <div class="badge">
                            <i class="fas fa-star"></i>
                            <span id="exp-4">Рейтинг 4.8/5</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section class="services-section">
        <div class="container">
            <h2 class="section-title" id="services-title">Мои Услуги</h2>
            <p class="section-subtitle" id="services-subtitle">Профессиональные IT-услуги для вашего бизнеса в Узбекистане</p>
            
            <div class="services-grid">
                <!-- Веб-дизайн -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-paint-brush"></i>
                    </div>
                    <h3 id="service-1">Веб-дизайн</h3>
                    <div class="service-description" id="desc-1">
                        Создание современного адаптивного дизайна для сайтов любой сложности с учетом UX/UI принципов
                    </div>
                    <div class="price-container">
                        <div>
                            <div class="original-price">769,000 UZS</div>
                            <div class="current-price">500,000 UZS</div>
                        </div>
                        <div class="vip-discount">-35% с VIP</div>
                    </div>
                    <button class="buy-button" data-service="Веб-дизайн">
                        <i class="fas fa-shopping-cart"></i>
                        <span id="buy-btn">Заказать через WhatsApp</span>
                    </button>
                </div>
                
                <!-- Telegram боты -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fab fa-telegram"></i>
                    </div>
                    <h3 id="service-2">Telegram боты (2 способа)</h3>
                    <div class="service-description" id="desc-2">
                        Разработка автоматизированных ботов для бизнеса: рассылки, автоответчик, интеграции, магазины
                    </div>
                    <div class="price-container">
                        <div>
                            <div class="original-price">461,000 UZS</div>
                            <div class="current-price">300,000 UZS</div>
                        </div>
                        <div class="vip-discount">-35% с VIP</div>
                    </div>
                    <button class="buy-button" data-service="Telegram боты">
                        <i class="fas fa-shopping-cart"></i>
                        <span id="buy-btn-2">Заказать через WhatsApp</span>
                    </button>
                </div>
                
                <!-- QR-коды -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-qrcode"></i>
                    </div>
                    <h3 id="service-3">QR-код (обычный)</h3>
                    <div class="service-description" id="desc-3">
                        Создание стандартных QR-кодов для ссылок, контактов, WiFi, мероприятий и других целей
                    </div>
                    <div class="price-container">
                        <div>
                            <div class="original-price">46,000 UZS</div>
                            <div class="current-price">30,000 UZS</div>
                        </div>
                        <div class="vip-discount">-35% с VIP</div>
                    </div>
                    <button class="buy-button" data-service="QR-код обычный">
                        <i class="fas fa-shopping-cart"></i>
                        <span id="buy-btn-3">Заказать через WhatsApp</span>
                    </button>
                </div>
                
                <!-- QR-коды с дизайном -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-palette"></i>
                    </div>
                    <h3 id="service-4">QR-код с дизайном</h3>
                    <div class="service-description" id="desc-4">
                        Создание уникальных дизайнерских QR-кодов с логотипом, цветами и креативным оформлением
                    </div>
                    <div class="price-container">
                        <div>
                            <div class="original-price">77,000 UZS</div>
                            <div class="current-price">50,000 UZS</div>
                        </div>
                        <div class="vip-discount">-35% с VIP</div>
                    </div>
                    <button class="buy-button" data-service="QR-код с дизайном">
                        <i class="fas fa-shopping-cart"></i>
                        <span id="buy-btn-4">Заказать через WhatsApp</span>
                    </button>
                </div>
                
                <!-- Обложки для YouTube -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fab fa-youtube"></i>
                    </div>
                    <h3 id="service-5">Обложки для YouTube</h3>
                    <div class="service-description" id="desc-5">
                        Дизайн привлекательных обложек для YouTube-каналов с учетом трендов и тематики канала
                    </div>
                    <div class="price-container">
                        <div>
                            <div class="original-price">154,000 UZS</div>
                            <div class="current-price">100,000 UZS</div>
                        </div>
                        <div class="vip-discount">-35% с VIP</div>
                    </div>
                    <button class="buy-button" data-service="Обложки для YouTube">
                        <i class="fas fa-shopping-cart"></i>
                        <span id="buy-btn-5">Заказать через WhatsApp</span>
                    </button>
                </div>
                
                <!-- Обложки для Instagram -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fab fa-instagram"></i>
                    </div>
                    <h3 id="service-6">Обложки для Instagram</h3>
                    <div class="service-description" id="desc-6">
                        Дизайн стильных обложек для Instagram аккаунтов, сторис и профилей
                    </div>
                    <div class="price-container">
                        <div>
                            <div class="original-price">154,000 UZS</div>
                            <div class="current-price">100,000 UZS</div>
                        </div>
                        <div class="vip-discount">-35% с VIP</div>
                    </div>
                    <button class="buy-button" data-service="Обложки для Instagram">
                        <i class="fas fa-shopping-cart"></i>
                        <span id="buy-btn-6">Заказать через WhatsApp</span>
                    </button>
                </div>
                
                <!-- Обложки для Facebook -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fab fa-facebook"></i>
                    </div>
                    <h3 id="service-7">Обложки для Facebook</h3>
                    <div class="service-description" id="desc-7">
                        Дизайн профессиональных обложек для Facebook страниц и групп
                    </div>
                    <div class="price-container">
                        <div>
                            <div class="original-price">154,000 UZS</div>
                            <div class="current-price">100,000 UZS</div>
                        </div>
                        <div class="vip-discount">-35% с VIP</div>
                    </div>
                    <button class="buy-button" data-service="Обложки для Facebook">
                        <i class="fas fa-shopping-cart"></i>
                        <span id="buy-btn-7">Заказать через WhatsApp</span>
                    </button>
                </div>
                
                <!-- Аватарки для Telegram -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-user-circle"></i>
                    </div>
                    <h3 id="service-8">Аватарки для Telegram</h3>
                    <div class="service-description" id="desc-8">
                        Создание уникальных аватарок для Telegram каналов, ботов и профилей
                    </div>
                    <div class="price-container">
                        <div>
                            <div class="original-price">77,000 UZS</div>
                            <div class="current-price">50,000 UZS</div>
                        </div>
                        <div class="vip-discount">-35% с VIP</div>
                    </div>
                    <button class="buy-button" data-service="Аватарки для Telegram">
                        <i class="fas fa-shopping-cart"></i>
                        <span id="buy-btn-8">Заказать через WhatsApp</span>
                    </button>
                </div>
                
                <!-- Создание сайтов -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-laptop-code"></i>
                    </div>
                    <h3 id="service-9">Создание сайтов</h3>
                    <div class="service-description" id="desc-9">
                        Разработка полнофункциональных сайтов: от лендингов до корпоративных порталов
                    </div>
                    <div class="price-container">
                        <div>
                            <div class="original-price">1,077,000 UZS</div>
                            <div class="current-price">700,000 UZS</div>
                        </div>
                        <div class="vip-discount">-35% с VIP</div>
                    </div>
                    <button class="buy-button" data-service="Создание сайтов">
                        <i class="fas fa-shopping-cart"></i>
                        <span id="buy-btn-9">Заказать через WhatsApp</span>
                    </button>
                </div>
                
                <!-- Интернет-магазины -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-shopping-cart"></i>
                    </div>
                    <h3 id="service-10">Интернет-магазины</h3>
                    <div class="service-description" id="desc-10">
                        Создание полноценных интернет-магазинов с корзиной, оплатой и управлением товарами
                    </div>
                    <div class="price-container">
                        <div>
                            <div class="original-price">1,538,000 UZS</div>
                            <div class="current-price">1,000,000 UZS</div>
                        </div>
                        <div class="vip-discount">-35% с VIP</div>
                    </div>
                    <button class="buy-button" data-service="Интернет-магазины">
                        <i class="fas fa-shopping-cart"></i>
                        <span id="buy-btn-10">Заказать через WhatsApp</span>
                    </button>
                </div>
                
                <!-- Секретные файлы (VIP) -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-lock"></i>
                    </div>
                    <h3 id="service-11">Секретные файлы</h3>
                    <div class="service-description" id="desc-11">
                        Эксклюзивные материалы, инструменты и файлы для автоматизации и оптимизации бизнеса
                    </div>
                    <div class="price-container">
                        <div>
                            <div class="original-price">ТОЛЬКО VIP</div>
                            <div class="current-price">VIP доступ</div>
                        </div>
                        <div class="vip-discount">VIP ONLY</div>
                    </div>
                    <button class="buy-button vip-only" id="secret-files-btn" disabled>
                        <i class="fas fa-crown"></i>
                        <span id="vip-only-btn">Требуется VIP доступ</span>
                    </button>
                    <div class="vip-note">Активируйте VIP для доступа к этой услуге</div>
                </div>
                
                <!-- Фальшивые документы (VIP) -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-file-contract"></i>
                    </div>
                    <h3 id="service-12">Фальшивые документы</h3>
                    <div class="service-description" id="desc-12">
                        Создание документов для образовательных, развлекательных и демонстрационных целей
                    </div>
                    <div class="price-container">
                        <div>
                            <div class="original-price">ТОЛЬКО VIP</div>
                            <div class="current-price">VIP доступ</div>
                        </div>
                        <div class="vip-discount">VIP ONLY</div>
                    </div>
                    <button class="buy-button vip-only" id="fake-docs-btn" disabled>
                        <i class="fas fa-crown"></i>
                        <span id="vip-only-btn-2">Требуется VIP доступ</span>
                    </button>
                    <div class="vip-note">Активируйте VIP для доступа к этой услуге</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Для студентов Section -->
    <section class="services-section" id="for-students">
        <div class="container">
            <h2 class="section-title" id="students-title">Для студентов</h2>
            <p class="section-subtitle" id="students-subtitle">Специальные услуги для студентов Узбекистана</p>
            
            <div class="services-grid">
                <!-- Создание доклада -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-file-alt"></i>
                    </div>
                    <h3 id="student-service-1">Создание доклада</h3>
                    <div class="service-description" id="student-desc-1">
                        Профессиональное создание докладов на любую тему для студентов, презентаций и научных работ
                    </div>
                    <div class="price-container">
                        <div>
                            <div class="original-price">150,000 UZS</div>
                            <div class="current-price">100,000 UZS</div>
                        </div>
                        <div class="vip-discount">-35% с VIP</div>
                    </div>
                    <button class="buy-button" data-service="Создание доклада">
                        <i class="fas fa-shopping-cart"></i>
                        <span class="buy-btn-text">Заказать через WhatsApp</span>
                    </button>
                </div>
                
                <!-- Создание красивых картинок -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-images"></i>
                    </div>
                    <h3 id="student-service-2">Создание красивых картинок</h3>
                    <div class="service-description" id="student-desc-2">
                        Создание 3D изображений, Pixart, картинок разного формата для проектов и презентаций
                    </div>
                    <div class="price-container">
                        <div>
                            <div class="original-price">200,000 UZS</div>
                            <div class="current-price">150,000 UZS</div>
                        </div>
                        <div class="vip-discount">-35% с VIP</div>
                    </div>
                    <button class="buy-button" data-service="Создание красивых картинок">
                        <i class="fas fa-shopping-cart"></i>
                        <span class="buy-btn-text">Заказать через WhatsApp</span>
                    </button>
                </div>
                
                <!-- 6-секундное видео -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-video"></i>
                    </div>
                    <h3 id="student-service-3">Создание 6-секундного видео</h3>
                    <div class="service-description" id="student-desc-3">
                        Создание коротких 6-секундных видеороликов для TikTok, Instagram Reels, YouTube Shorts
                    </div>
                    <div class="price-container">
                        <div>
                            <div class="original-price">250,000 UZS</div>
                            <div class="current-price">180,000 UZS</div>
                        </div>
                        <div class="vip-discount">-35% с VIP</div>
                    </div>
                    <button class="buy-button" data-service="Создание 6-секундного видео">
                        <i class="fas fa-shopping-cart"></i>
                        <span class="buy-btn-text">Заказать через WhatsApp</span>
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Настройка цены Section -->
    <section class="custom-price-section">
        <div class="container">
            <div class="custom-price-content">
                <h2 class="custom-price-title" id="custom-price-title">Настройка цены</h2>
                <p class="custom-price-description" id="custom-price-desc">
                    Вы можете самостоятельно настроить цену за услугу в зависимости от сложности и сроков выполнения
                </p>
                
                <div class="price-calculator">
                    <h3 id="calculator-title">Калькулятор цены</h3>
                    <p id="calculator-desc">Выберите сложность услуги:</p>
                    
                    <div style="margin: 20px 0;">
                        <label for="complexity" id="complexity-label">Сложность:</label>
                        <select id="complexity" style="padding: 10px; border-radius: 8px; width: 100%; margin-top: 10px;">
                            <option value="1" id="opt-1">Простая (базовая услуга)</option>
                            <option value="2" id="opt-2">Средняя (стандартная услуга)</option>
                            <option value="3" id="opt-3">Сложная (премиум услуга)</option>
                            <option value="4" id="opt-4">Очень сложная (индивидуальная разработка)</option>
                        </select>
                    </div>
                    
                    <div style="margin: 20px 0;">
                        <label for="deadline" id="deadline-label">Срок выполнения (дней):</label>
                        <input type="range" id="deadline" min="1" max="30" value="7" class="price-slider">
                        <span id="deadline-value">7 дней</span>
                    </div>
                    
                    <div class="calculated-price">
                        <span id="final-price">~ 350,000 UZS</span>
                    </div>
                    
                    <button class="spin-button" id="order-custom-price">
                        <i class="fas fa-calculator"></i>
                        <span id="order-custom-btn">Заказать по этой цене</span>
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Friday Raffle Section -->
    <section class="friday-section">
        <div class="container">
            <div class="friday-content">
                <div class="friday-text">
                    <h2>🎉 <span id="friday-title">Удачная Пятница</span> 🎉</h2>
                    <div class="friday-description" id="friday-desc">
                        Каждую пятницу разыгрываем БЕСПЛАТНУЮ услугу среди всех посетителей! 
                        Участвуйте в розыгрыше и получите шанс выиграть любую услугу из каталога совершенно бесплатно!
                    </div>
                    
                    <div class="countdown">
                        <div class="countdown-title" id="countdown-title">До следующего розыгрыша осталось:</div>
                        <div class="countdown-timer" id="countdown">5 дней 00:00:00</div>
                    </div>
                    
                    <button class="spin-button" id="spin-button">
                        <i class="fas fa-redo"></i>
                        <span id="spin-btn-text">Крутить рулетку удачи!</span>
                    </button>
                    <div id="raffle-message" style="margin-top: 20px; font-size: 18px; opacity: 0.9;">
                        Сегодня не пятница. Приходите в пятницу для участия в розыгрыше!
                    </div>
                </div>
                
                <div class="roulette-container">
                    <div class="roulette-pointer"></div>
                    <div class="roulette" id="roulette"></div>
                </div>
            </div>
        </div>
    </section>

    <!-- Reviews Section -->
    <section class="reviews-section">
        <div class="container">
            <h2 class="section-title" id="reviews-title">Отзывы клиентов</h2>
            <p class="section-subtitle" id="reviews-subtitle">Что говорят клиенты о моих услугах</p>
            
            <div class="reviews-grid">
                <div class="review-card">
                    <div class="review-text" id="review-1">
                        "Заказывал у Асадбека Telegram-бота для моего магазина. Сделал все быстро и качественно, 
                        бот работает без сбоев уже 8 месяцев. Клиенты довольны удобством заказа через бота!"
                    </div>
                    <div class="review-author">
                        <div class="review-avatar">Ш</div>
                        <div class="author-info">
                            <h4>Шахзод Рахимов</h4>
                            <div class="author-location">
                                <i class="fas fa-map-marker-alt"></i>
                                <span>Ташкент</span>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="review-card">
                    <div class="review-text" id="review-2">
                        "Асадбек создал для меня интернет-магазин за 2 недели. Сайт получился современный и удобный, 
                        интеграция с платежными системами работает идеально. Продажи выросли на 40% после запуска!"
                    </div>
                    <div class="review-author">
                        <div class="review-avatar">Н</div>
                        <div class="author-info">
                            <h4>Нодира Алимова</h4>
                            <div class="author-location">
                                <i class="fas fa-map-marker-alt"></i>
                                <span>Самарканд</span>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="review-card">
                    <div class="review-text" id="review-3">
                        "Заказал у Асадбека аватарку для Telegram-канала и обложку для YouTube. 
                        Результат превзошел все ожидания - дизайн современный, уникальный и привлекает внимание!"
                    </div>
                    <div class="review-author">
                        <div class="review-avatar">А</div>
                        <div class="author-info">
                            <h4>Азиз Нурматов</h4>
                            <div class="author-location">
                                <i class="fas fa-map-marker-alt"></i>
                                <span>Фергана</span>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="review-card">
                    <div class="review-text" id="review-4">
                        "Выиграл в 'Удачной пятнице' бесплатный QR-код для рекламы моего кафе. 
                        Асадбек сделал красивый дизайнерский QR-код, который теперь висит у входа. Клиенты сканируют с удовольствием!"
                    </div>
                    <div class="review-author">
                        <div class="review-avatar">Ф</div>
                        <div class="author-info">
                            <h4>Фарход Исмаилов</h4>
                            <div class="author-location">
                                <i class="fas fa-map-marker-alt"></i>
                                <span>Наманган</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact-section">
        <div class="container">
            <h2 class="section-title" id="contact-title">Свяжитесь со мной</h2>
            <p class="section-subtitle" id="contact-subtitle" style="color: rgba(255,255,255,0.9);">
                Все заказы оформляются через WhatsApp. Отвечаю в течение 15 минут в рабочее время
            </p>
            
            <a href="https://wa.me/998999100097" class="whatsapp-contact" target="_blank">
                <i class="fab fa-whatsapp"></i>
                <span id="whatsapp-contact-text">Написать в WhatsApp: +998 99 910-00-97</span>
            </a>
            
            <div class="contact-info">
                <div class="contact-item">
                    <div class="contact-icon">
                        <i class="fas fa-clock"></i>
                    </div>
                    <div>
                        <h4 id="work-hours-title">Режим работы</h4>
                        <p id="work-hours">Пн-Вс: 9:00 - 22:00</p>
                    </div>
                </div>
                
                <div class="contact-item">
                    <div class="contact-icon">
                        <i class="fas fa-shipping-fast"></i>
                    </div>
                    <div>
                        <h4 id="delivery-title">Сроки выполнения</h4>
                        <p id="delivery-time">От 1 до 14 дней</p>
                    </div>
                </div>
                
                <div class="contact-item">
                    <div class="contact-icon">
                        <i class="fas fa-headset"></i>
                    </div>
                    <div>
                        <h4 id="support-title">Поддержка</h4>
                        <p id="support-text">Пожизненная консультация</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <div class="footer-logo" id="footer-logo">Asadbek IT Services</div>
            <div class="country-badge">
                <i class="fas fa-map-marker-alt"></i>
                <span id="country-badge-text">ТОЛЬКО ДЛЯ УЗБЕКИСТАНА</span>
            </div>
            <p id="footer-text">Профессиональные IT-услуги для вашего бизнеса</p>
            <p id="footer-friday-text">Удачная пятница каждую неделю! Не пропустите шанс получить услугу БЕСПЛАТНО!</p>
            <div class="copyright">
                <span id="copyright-text">© 2024 Asadbek IT Services. Все права защищены. Все услуги предоставляются в ознакомительных целях.</span>
            </div>
        </div>
    </footer>

    <!-- Modals -->
    <div class="modal" id="prize-modal">
        <div class="modal-content">
            <button class="modal-close" onclick="closeModal()">&times;</button>
            <h2 class="modal-title" id="congrats-title">🎊 ПОЗДРАВЛЯЕМ! 🎊</h2>
            <p class="modal-text" id="congrats-text">Вы выиграли БЕСПЛАТНУЮ услугу:</p>
            <h3 id="prize-service" style="text-align: center; color: var(--primary); font-size: 28px; margin: 20px 0;">Веб-дизайн</h3>
            <p class="modal-text" id="activate-text">Свяжитесь со мной в WhatsApp для активации вашего приза!</p>
            <a href="https://wa.me/998999100097?text=Выиграл услугу в Удачной пятнице!" class="whatsapp-contact" target="_blank" style="font-size: 18px; padding: 15px 30px; margin: 20px auto; display: inline-block;">
                <i class="fab fa-whatsapp"></i>
                <span id="whatsapp-modal-text">Написать в WhatsApp</span>
            </a>
        </div>
    </div>
    
    <div class="modal" id="vip-modal">
        <div class="modal-content">
            <button class="modal-close" onclick="closeVipModal()">&times;</button>
            <h2 class="modal-title" id="vip-modal-title">⭐ VIP ДОСТУП АКТИВИРОВАН ⭐</h2>
            <p class="modal-text" id="vip-modal-text">Теперь вам доступны эксклюзивные привилегии:</p>
            <ul style="text-align: left; margin: 30px; color: #555;">
                <li style="margin-bottom: 15px; padding-left: 10px;"><span id="vip-benefit-1">Скидка <strong>35%</strong> на все услуги</span></li>
                <li style="margin-bottom: 15px; padding-left: 10px;"><span id="vip-benefit-2">Доступ к созданию фальшивых документов</span></li>
                <li style="margin-bottom: 15px; padding-left: 10px;"><span id="vip-benefit-3">Эксклюзивные секретные файлы</span></li>
                <li style="margin-bottom: 15px; padding-left: 10px;"><span id="vip-benefit-4">Приоритетная поддержка 24/7</span></li>
            </ul>
            <p class="modal-text" id="vip-order-text">Для оформления VIP услуг свяжитесь в WhatsApp:</p>
            <a href="https://wa.me/998999100097?text=Хочу купить VIP доступ за $2" class="whatsapp-contact" target="_blank" style="font-size: 18px; padding: 15px 30px; margin: 20px auto; display: inline-block;">
                <i class="fab fa-whatsapp"></i>
                <span id="vip-whatsapp-text">Купить VIP доступ ($2/мес)</span>
            </a>
        </div>
    </div>

    <script>
        // Language switching
        const translations = {
            ru: {
                // Header
                'site-title': 'Asadbek IT Services',
                'coins-text': 'Монетки:',
                'vip-text': 'VIP ПРЕМИУМ',
                'whatsapp-text': 'WhatsApp +998 99 910-00-97',
                
                // Developer section
                'dev-name': 'Асадбек',
                'dev-title': 'Full-Stack Разработчик & IT-Специалист',
                'dev-bio': 'Профессиональный IT-специалист с 2-летним опытом в создании современных веб-решений, разработке Telegram ботов, дизайне и автоматизации бизнес-процессов. Специализируюсь на создании качественных IT-продуктов для бизнеса в Узбекистане.',
                'exp-1': '2+ года опыта',
                'exp-2': '50+ завершенных проектов',
                'exp-3': '35+ довольных клиентов',
                'exp-4': 'Рейтинг 4.8/5',
                
                // Services
                'services-title': 'Мои Услуги',
                'services-subtitle': 'Профессиональные IT-услуги для вашего бизнеса в Узбекистане',
                'service-1': 'Веб-дизайн',
                'desc-1': 'Создание современного адаптивного дизайна для сайтов любой сложности с учетом UX/UI принципов',
                'service-2': 'Telegram боты (2 способа)',
                'desc-2': 'Разработка автоматизированных ботов для бизнеса: рассылки, автоответчик, интеграции, магазины',
                'service-3': 'QR-код (обычный)',
                'desc-3': 'Создание стандартных QR-кодов для ссылок, контактов, WiFi, мероприятий и других целей',
                'service-4': 'QR-код с дизайном',
                'desc-4': 'Создание уникальных дизайнерских QR-кодов с логотипом, цветами и креативным оформлением',
                'service-5': 'Обложки для YouTube',
                'desc-5': 'Дизайн привлекательных обложек для YouTube-каналов с учетом трендов и тематики канала',
                'service-6': 'Обложки для Instagram',
                'desc-6': 'Дизайн стильных обложек для Instagram аккаунтов, сторис и профилей',
                'service-7': 'Обложки для Facebook',
                'desc-7': 'Дизайн профессиональных обложек для Facebook страниц и групп',
                'service-8': 'Аватарки для Telegram',
                'desc-8': 'Создание уникальных аватарок для Telegram каналов, ботов и профилей',
                'service-9': 'Создание сайтов',
                'desc-9': 'Разработка полнофункциональных сайтов: от лендингов до корпоративных порталов',
                'service-10': 'Интернет-магазины',
                'desc-10': 'Создание полноценных интернет-магазинов с корзиной, оплатой и управлением товарами',
                'service-11': 'Секретные файлы',
                'desc-11': 'Эксклюзивные материалы, инструменты и файлы для автоматизации и оптимизации бизнеса',
                'service-12': 'Фальшивые документы',
                'desc-12': 'Создание документов для образовательных, развлекательных и демонстрационных целей',
                'buy-btn': 'Заказать через WhatsApp',
                'vip-only-btn': 'Требуется VIP доступ',
                'vip-only-btn-2': 'Требуется VIP доступ',
                
                // Для студентов
                'students-title': 'Для студентов',
                'students-subtitle': 'Специальные услуги для студентов Узбекистана',
                'student-service-1': 'Создание доклада',
                'student-desc-1': 'Профессиональное создание докладов на любую тему для студентов, презентаций и научных работ',
                'student-service-2': 'Создание красивых картинок',
                'student-desc-2': 'Создание 3D изображений, Pixart, картинок разного формата для проектов и презентаций',
                'student-service-3': 'Создание 6-секундного видео',
                'student-desc-3': 'Создание коротких 6-секундных видеороликов для TikTok, Instagram Reels, YouTube Shorts',
                
                // Настройка цены
                'custom-price-title': 'Настройка цены',
                'custom-price-desc': 'Вы можете самостоятельно настроить цену за услугу в зависимости от сложности и сроков выполнения',
                'calculator-title': 'Калькулятор цены',
                'calculator-desc': 'Выберите сложность услуги:',
                'complexity-label': 'Сложность:',
                'opt-1': 'Простая (базовая услуга)',
                'opt-2': 'Средняя (стандартная услуга)',
                'opt-3': 'Сложная (премиум услуга)',
                'opt-4': 'Очень сложная (индивидуальная разработка)',
                'deadline-label': 'Срок выполнения (дней):',
                'order-custom-btn': 'Заказать по этой цене',
                
                // Friday Raffle
                'friday-title': 'Удачная Пятница',
                'friday-desc': 'Каждую пятницу разыгрываем БЕСПЛАТНУЮ услугу среди всех посетителей! Участвуйте в розыгрыше и получите шанс выиграть любую услугу из каталога совершенно бесплатно!',
                'countdown-title': 'До следующего розыгрыша осталось:',
                'spin-btn-text': 'Крутить рулетку удачи!',
                
                // Reviews
                'reviews-title': 'Отзывы клиентов',
                'reviews-subtitle': 'Что говорят клиенты о моих услугах',
                'review-1': '"Заказывал у Асадбека Telegram-бота для моего магазина. Сделал все быстро и качественно, бот работает без сбоев уже 8 месяцев. Клиенты довольны удобством заказа через бота!"',
                'review-2': '"Асадбек создал для меня интернет-магазин за 2 недели. Сайт получился современный и удобный, интеграция с платежными системами работает идеально. Продажи выросли на 40% после запуска!"',
                'review-3': '"Заказал у Асадбека аватарку для Telegram-канала и обложку для YouTube. Результат превзошел все ожидания - дизайн современный, уникальный и привлекает внимание!"',
                'review-4': '"Выиграл в \'Удачной пятнице\' бесплатный QR-код для рекламы моего кафе. Асадбек сделал красивый дизайнерский QR-код, который теперь висит у входа. Клиенты сканируют с удовольствием!"',
                
                // Contact
                'contact-title': 'Свяжитесь со мной',
                'contact-subtitle': 'Все заказы оформляются через WhatsApp. Отвечаю в течение 15 минут в рабочее время',
                'whatsapp-contact-text': 'Написать в WhatsApp: +998 99 910-00-97',
                'work-hours-title': 'Режим работы',
                'work-hours': 'Пн-Вс: 9:00 - 22:00',
                'delivery-title': 'Сроки выполнения',
                'delivery-time': 'От 1 до 14 дней',
                'support-title': 'Поддержка',
                'support-text': 'Пожизненная консультация',
                
                // Footer
                'footer-logo': 'Asadbek IT Services',
                'country-badge-text': 'ТОЛЬКО ДЛЯ УЗБЕКИСТАНА',
                'footer-text': 'Профессиональные IT-услуги для вашего бизнеса',
                'footer-friday-text': 'Удачная пятница каждую неделю! Не пропустите шанс получить услугу БЕСПЛАТНО!',
                'copyright-text': '© 2024 Asadbek IT Services. Все права защищены. Все услуги предоставляются в ознакомительных целях.',
                
                // Modals
                'congrats-title': '🎊 ПОЗДРАВЛЯЕМ! 🎊',
                'congrats-text': 'Вы выиграли БЕСПЛАТНУЮ услугу:',
                'activate-text': 'Свяжитесь со мной в WhatsApp для активации вашего приза!',
                'whatsapp-modal-text': 'Написать в WhatsApp',
                'vip-modal-title': '⭐ VIP ДОСТУП АКТИВИРОВАН ⭐',
                'vip-modal-text': 'Теперь вам доступны эксклюзивные привилегии:',
                'vip-benefit-1': 'Скидка <strong>35%</strong> на все услуги',
                'vip-benefit-2': 'Доступ к созданию фальшивых документов',
                'vip-benefit-3': 'Эксклюзивные секретные файлы',
                'vip-benefit-4': 'Приоритетная поддержка 24/7',
                'vip-order-text': 'Для оформления VIP услуг свяжитесь в WhatsApp:',
                'vip-whatsapp-text': 'Купить VIP доступ ($2/мес)'
            },
            uz: {
                // Header
                'site-title': 'Asadbek IT Xizmatlari',
                'coins-text': 'Tangalar:',
                'vip-text': 'VIP PREMIUM',
                'whatsapp-text': 'WhatsApp +998 99 910-00-97',
                
                // Developer section
                'dev-name': 'Asadbek',
                'dev-title': 'Full-Stack Dasturchi & IT Mutaxassis',
                'dev-bio': '2 yillik tajribaga ega professional IT mutaxassis, zamonaviy veb-yechimlar, Telegram botlari, dizayn va biznes jarayonlarini avtomatlashtirish bo\'yicha mutaxassis. O\'zbekistonda biznes uchun sifatli IT mahsulotlar yaratishga ixtisoslashgan.',
                'exp-1': '2+ yillik tajriba',
                'exp-2': '50+ tugatilgan loyiha',
                'exp-3': '35+ mamnun mijoz',
                'exp-4': 'Reyting 4.8/5',
                
                // Services
                'services-title': 'Mening Xizmatlarim',
                'services-subtitle': 'O\'zbekistondagi biznesingiz uchun professional IT xizmatlar',
                'service-1': 'Veb-dizayn',
                'desc-1': 'Har qanday murakkablikdagi saytlar uchun zamonaviy adaptiv dizayn yaratish, UX/UI tamoyillari hisobga olinadi',
                'service-2': 'Telegram botlari (2 usul)',
                'desc-2': 'Biznes uchun avtomatlashtirilgan botlarni ishlab chiqish: yuborishlar, avtomatik javob beruvchi, integratsiyalar, do\'konlar',
                'service-3': 'QR-kod (oddiy)',
                'desc-3': 'Havolalar, kontaktlar, WiFi, tadbirlar va boshqa maqsadlar uchun standart QR-kodlar yaratish',
                'service-4': 'Dizaynli QR-kod',
                'desc-4': 'Logotip, ranglar va ijodiy bezak bilan noyob dizayner QR-kodlarini yaratish',
                'service-5': 'YouTube uchun muqovalar',
                'desc-5': 'YouTube kanallari uchun jozibador muqovalar dizayni, trendlar va mavzu hisobga olinadi',
                'service-6': 'Instagram uchun muqovalar',
                'desc-6': 'Instagram akkauntlari, storiylar va profil uchun zamonaviy muqovalar dizayni',
                'service-7': 'Facebook uchun muqovalar',
                'desc-7': 'Facebook sahifalari va guruhlari uchun professional muqovalar dizayni',
                'service-8': 'Telegram uchun avatar',
                'desc-8': 'Telegram kanallari, botlari va profillari uchun noyob avatar yaratish',
                'service-9': 'Sayt yaratish',
                'desc-9': 'To\'liq funksional saytlar ishlab chiqish: landing sahifalardan korporativ portallargacha',
                'service-10': 'Internet-do\'konlar',
                'desc-10': 'Savat, to\'lov va mahsulotlarni boshqarish bilan to\'liq internet-do\'konlar yaratish',
                'service-11': 'Maxfiy fayllar',
                'desc-11': 'Biznesni avtomatlashtirish va optimallashtirish uchun eksklyuziv materiallar, vositalar va fayllar',
                'service-12': 'Soxta hujjatlar',
                'desc-12': 'Ta\'lim, o\'yin-kulgi va namoyish maqsadlari uchun hujjatlar yaratish',
                'buy-btn': 'WhatsApp orqali buyurtma qilish',
                'vip-only-btn': 'VIP kirish talab qilinadi',
                'vip-only-btn-2': 'VIP kirish talab qilinadi',
                
                // Для студентов
                'students-title': 'Talabalar uchun',
                'students-subtitle': 'O\'zbekiston talabalari uchun maxsus xizmatlar',
                'student-service-1': 'Hisobot yaratish',
                'student-desc-1': 'Talabalar uchun har qanday mavzuda professional hisobotlar, taqdimotlar va ilmiy ishlar yaratish',
                'student-service-2': 'Chiroyli rasmlar yaratish',
                'student-desc-2': 'Loyihalar va taqdimotlar uchun 3D tasvirlar, Pixart, turli formatdagi rasmlar yaratish',
                'student-service-3': '6 sonlik video yaratish',
                'student-desc-3': 'TikTok, Instagram Reels, YouTube Shorts uchun qisqa 6 sonlik video roliklar yaratish',
                
                // Настройка цены
                'custom-price-title': 'Narxni sozlash',
                'custom-price-desc': 'Xizmatning murakkabligi va muddatiga qarab narxni mustaqil ravishda sozlashingiz mumkin',
                'calculator-title': 'Narx kalkulyatori',
                'calculator-desc': 'Xizmatning murakkabligini tanlang:',
                'complexity-label': 'Murakkablik:',
                'opt-1': 'Oddiy (asosiy xizmat)',
                'opt-2': 'O\'rtacha (standart xizmat)',
                'opt-3': 'Murakkab (premium xizmat)',
                'opt-4': 'Juda murakkab (individual ishlab chiqish)',
                'deadline-label': 'Bajarish muddati (kun):',
                'order-custom-btn': 'Ushbu narxda buyurtma qilish',
                
                // Friday Raffle
                'friday-title': 'Omadli Juma',
                'friday-desc': 'Har juma kuni barcha tashrif buyuruvchilar orasida BEPUL xizmat o\'ynaymiz! O\'yinda qatnashing va katalogdagi har qanday xizmatni mutlaqo bepul yutib olish imkoniyatiga ega bo\'ling!',
                'countdown-title': 'Keyingi o\'yingacha qolgan vaqt:',
                'spin-btn-text': 'Omad g\'ildiragini aylantiring!',
                
                // Reviews
                'reviews-title': 'Mijozlarning sharhlari',
                'reviews-subtitle': 'Mijozlar mening xizmatlarim haqida nima deyishadi',
                'review-1': '"Asadbekdan do\'konim uchun Telegram-bot buyurtma qildim. Hammasini tez va sifatli qildi, bot allaqachon 8 oydan beri muammosiz ishlayapti. Mijozlar bot orqali buyurtma berish qulayligidan mamnun!"',
                'review-2': '"Asadbek mening uchun 2 hafta ichida internet-do\'kon yaratdi. Sayt zamonaviy va qulay chiqdi, to\'lov tizimlari bilan integratsiya mukammal ishlaydi. Ishlab chiqarilgandan keyin savdo 40% ga oshdi!"',
                'review-3': '"Asadbekdan Telegram-kanal uchun avatar va YouTube uchun muqova buyurtma qildim. Natija barcha kutganlarimdan oshib ketdi - dizayn zamonaviy, noyob va e\'tiborni tortadi!"',
                'review-4': '"Omadli Jumada kafem uchun bepul QR-kod yutib oldim. Asadbek chiroyli dizayner QR-kodini yaratdi, endi u kirishda osilgan. Mijozlar mamnuniyat bilan skanerlayapti!"',
                
                // Contact
                'contact-title': 'Men bilan bog\'laning',
                'contact-subtitle': 'Barcha buyurtmalar WhatsApp orqali rasmiylashtiriladi. Ish vaqtida 15 daqiqa ichida javob beraman',
                'whatsapp-contact-text': 'WhatsAppga yozish: +998 99 910-00-97',
                'work-hours-title': 'Ish vaqti',
                'work-hours': 'Dush-Paysh: 9:00 - 22:00',
                'delivery-title': 'Bajarish muddati',
                'delivery-time': '1 dan 14 kungacha',
                'support-title': 'Qo\'llab-quvvatlash',
                'support-text': 'Umrbod maslahat',
                
                // Footer
                'footer-logo': 'Asadbek IT Xizmatlari',
                'country-badge-text': 'FAQAT O\'ZBEKISTON UCHUN',
                'footer-text': 'Biznesingiz uchun professional IT xizmatlar',
                'footer-friday-text': 'Har hafta omadli juma! Xizmatni BEPUL olish imkoniyatini qo\'ldan bermang!',
                'copyright-text': '© 2024 Asadbek IT Xizmatlari. Barcha huquqlar himoyalangan. Barcha xizmatlar tanishish maqsadida taqdim etiladi.',
                
                // Modals
                'congrats-title': '🎊 TABRIKLAYMIZ! 🎊',
                'congrats-text': 'Siz BEPUL xizmatni yutib oldingiz:',
                'activate-text': 'Mukofotingizni faollashtirish uchun menga WhatsApp orqali murojaat qiling!',
                'whatsapp-modal-text': 'WhatsAppga yozish',
                'vip-modal-title': '⭐ VIP KIRISH FAOLLASHTIRILDI ⭐',
                'vip-modal-text': 'Endi sizga eksklyuziv imtiyozlar mavjud:',
                'vip-benefit-1': 'Barcha xizmatlarga <strong>35%</strong> chegirma',
                'vip-benefit-2': 'Soxta hujjatlar yaratishga kirish',
                'vip-benefit-3': 'Eksklyuziv maxfiy fayllar',
                'vip-benefit-4': '24/7 ustuvor qo\'llab-quvvatlash',
                'vip-order-text': 'VIP xizmatlarni rasmiylashtirish uchun WhatsApp orqali bog\'laning:',
                'vip-whatsapp-text': 'VIP kirishni sotib olish ($2/oy)'
            }
        };

        let currentLang = 'ru';

        function switchLanguage(lang) {
            currentLang = lang;
            
            // Update language buttons
            document.querySelectorAll('.lang-btn').forEach(btn => {
                btn.classList.remove('active');
                if (btn.id === `lang-${lang}`) {
                    btn.classList.add('active');
                }
            });
            
            // Update all translatable elements
            Object.keys(translations[lang]).forEach(key => {
                const element = document.getElementById(key);
                if (element) {
                    if (key.includes('benefit') && element.parentElement.tagName === 'LI') {
                        element.innerHTML = translations[lang][key];
                    } else {
                        element.textContent = translations[lang][key];
                    }
                }
            });
            
            // Update all buy buttons text
            document.querySelectorAll('.buy-btn-text').forEach(btn => {
                btn.textContent = translations[lang]['buy-btn'];
            });
            
            // Update buy buttons in services section
            document.querySelectorAll('#buy-btn, #buy-btn-2, #buy-btn-3, #buy-btn-4, #buy-btn-5, #buy-btn-6, #buy-btn-7, #buy-btn-8, #buy-btn-9, #buy-btn-10').forEach(btn => {
                btn.textContent = translations[lang]['buy-btn'];
            });
        }

        // Language switcher event listeners
        document.getElementById('lang-ru').addEventListener('click', () => switchLanguage('ru'));
        document.getElementById('lang-uz').addEventListener('click', () => switchLanguage('uz'));

        // Price calculator
        const complexitySelect = document.getElementById('complexity');
        const deadlineSlider = document.getElementById('deadline');
        const deadlineValue = document.getElementById('deadline-value');
        const finalPrice = document.getElementById('final-price');
        
        function calculatePrice() {
            const complexity = parseInt(complexitySelect.value);
            const deadline = parseInt(deadlineSlider.value);
            
            // Base prices based on complexity
            const basePrices = {
                1: 150000, // Простая
                2: 300000, // Средняя
                3: 500000, // Сложная
                4: 800000  // Очень сложная
            };
            
            let price = basePrices[complexity];
            
            // Adjust price based on deadline (shorter deadline = higher price)
            if (deadline < 3) {
                price *= 1.5; // +50% for urgent
            } else if (deadline < 7) {
                price *= 1.2; // +20% for fast
            } else if (deadline > 14) {
                price *= 0.9; // -10% for long term
            }
            
            // Format price
            const formattedPrice = new Intl.NumberFormat('ru-RU').format(Math.round(price));
            finalPrice.textContent = `~ ${formattedPrice} UZS`;
            deadlineValue.textContent = `${deadline} ${currentLang === 'ru' ? 'дней' : 'kun'}`;
        }
        
        complexitySelect.addEventListener('change', calculatePrice);
        deadlineSlider.addEventListener('input', () => {
            deadlineValue.textContent = `${deadlineSlider.value} ${currentLang === 'ru' ? 'дней' : 'kun'}`;
            calculatePrice();
        });
        
        // Custom price order button
        document.getElementById('order-custom-price').addEventListener('click', function() {
            const complexityText = complexitySelect.options[complexitySelect.selectedIndex].text;
            const deadline = deadlineSlider.value;
            const price = finalPrice.textContent;
            
            const whatsappText = currentLang === 'ru' 
                ? `Здравствуйте! Хочу заказать услугу с настройкой цены:\nСложность: ${complexityText}\nСрок: ${deadline} дней\nПримерная цена: ${price}`
                : `Assalomu alaykum! Narx sozlamasi bilan xizmat buyurtma qilmoqchiman:\nMurakkablik: ${complexityText}\nMuddati: ${deadline} kun\nTaxminiy narx: ${price}`;
            window.open(`https://wa.me/998999100097?text=${encodeURIComponent(whatsappText)}`, '_blank');
        });
        
        // Initialize price calculator
        calculatePrice();

        // Проверка дня недели
        function isFriday() {
            const today = new Date();
            return today.getDay() === 5; // 5 = пятница
        }
        
        // Обновление таймера до пятницы
        function updateCountdown() {
            const now = new Date();
            const daysUntilFriday = (5 - now.getDay() + 7) % 7;
            const targetDate = new Date(now);
            targetDate.setDate(now.getDate() + (daysUntilFriday === 0 ? 7 : daysUntilFriday));
            targetDate.setHours(0, 0, 0, 0);
            
            const diff = targetDate - now;
            const days = Math.floor(diff / (1000 * 60 * 60 * 24));
            const hours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((diff % (1000 * 60)) / 1000);
            
            document.getElementById('countdown').textContent = 
                `${days} ${currentLang === 'ru' ? 'д' : 'kun'} ${hours.toString().padStart(2, '0')}:${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
            
            // Показываем/скрываем кнопку в зависимости от дня
            const spinButton = document.getElementById('spin-button');
            const message = document.getElementById('raffle-message');
            
            if (isFriday()) {
                spinButton.disabled = false;
                message.textContent = currentLang === 'ru' 
                    ? 'Сегодня пятница! Крутите рулетку и выигрывайте бесплатную услугу!' 
                    : 'Bugun juma! Omad g\'ildiragini aylantiring va bepul xizmat yuting!';
                message.style.color = 'var(--secondary)';
            } else {
                spinButton.disabled = true;
                message.textContent = currentLang === 'ru'
                    ? `Сегодня не пятница. Приходите в пятницу для участия в розыгрыше! Следующая пятница через ${days} дней`
                    : `Bugun juma emas. O\'yinga qatnashish uchun juma kuni keling! Keyingi juma ${days} kundan keyin`;
                message.style.color = 'rgba(255,255,255,0.7)';
            }
        }
        
        // Обновляем таймер каждую секунду
        setInterval(updateCountdown, 1000);
        updateCountdown();
        
        // Розыгрыш рулетки
        const roulette = document.getElementById('roulette');
        const spinButton = document.getElementById('spin-button');
        const services = [
            'Веб-дизайн',
            'Telegram боты',
            'QR-код обычный',
            'QR-код с дизайном',
            'Обложки для YouTube',
            'Обложки для Instagram',
            'Обложки для Facebook',
            'Аватарки для Telegram',
            'Создание сайтов',
            'Интернет-магазины',
            'Создание доклада',
            'Создание красивых картинок',
            'Создание 6-секундного видео',
            'Секретный файл'
        ];
        
        let isSpinning = false;
        let isPremium = false;
        
        spinButton.addEventListener('click', () => {
            if (!isFriday() || isSpinning) return;
            
            isSpinning = true;
            spinButton.disabled = true;
            
            // Случайный выбор приза
            const spinDuration = 3000;
            const randomPrize = Math.floor(Math.random() * services.length);
            const degrees = 360 * 5 + (randomPrize * (360 / services.length));
            
            // Анимация вращения
            roulette.style.transform = `rotate(${degrees}deg)`;
            
            setTimeout(() => {
                isSpinning = false;
                spinButton.disabled = !isFriday();
                
                // Показ выигрыша
                const prize = services[randomPrize];
                document.getElementById('prize-service').textContent = prize;
                
                // Показ модального окна
                document.getElementById('prize-modal').style.display = 'flex';
                
                // Добавляем монетки за участие
                const coinsElement = document.getElementById('coins');
                let coins = parseInt(coinsElement.textContent.replace(/[^\d]/g, ''));
                coins += 50;
                coinsElement.textContent = coins.toLocaleString();
                
            }, spinDuration + 500);
        });
        
        // Покупка услуг
        document.querySelectorAll('.buy-button:not(.vip-only)').forEach(button => {
            button.addEventListener('click', function() {
                const service = this.getAttribute('data-service');
                const priceContainer = this.closest('.service-card').querySelector('.price-container');
                const price = priceContainer ? priceContainer.querySelector('.current-price').textContent : '';
                const whatsappText = currentLang === 'ru' 
                    ? `Здравствуйте, Асадбек! Хочу заказать услугу: ${service} (${price})`
                    : `Assalomu alaykum, Asadbek! Xizmatni buyurtma qilmoqchiman: ${service} (${price})`;
                window.open(`https://wa.me/998999100097?text=${encodeURIComponent(whatsappText)}`, '_blank');
            });
        });
        
        // Покупка VIP
        function activatePremium() {
            isPremium = true;
            document.getElementById('vip-modal').style.display = 'flex';
            document.getElementById('premium-badge').style.display = 'flex';
            
            // Активируем VIP кнопки
            const fakeDocsBtn = document.getElementById('fake-docs-btn');
            const secretFilesBtn = document.getElementById('secret-files-btn');
            
            if (fakeDocsBtn) {
                fakeDocsBtn.disabled = false;
                fakeDocsBtn.innerHTML = '<i class="fas fa-shopping-cart"></i> ' + translations[currentLang]['buy-btn'];
                fakeDocsBtn.classList.remove('vip-only');
                fakeDocsBtn.onclick = function() {
                    const whatsappText = currentLang === 'ru' 
                        ? 'Хочу заказать фальшивые документы (VIP клиент)'
                        : 'Soxta hujjatlar buyurtma qilmoqchiman (VIP mijoz)';
                    window.open(`https://wa.me/998999100097?text=${encodeURIComponent(whatsappText)}`, '_blank');
                };
            }
            
            if (secretFilesBtn) {
                secretFilesBtn.disabled = false;
                secretFilesBtn.innerHTML = '<i class="fas fa-shopping-cart"></i> ' + translations[currentLang]['buy-btn'];
                secretFilesBtn.classList.remove('vip-only');
                secretFilesBtn.onclick = function() {
                    const whatsappText = currentLang === 'ru' 
                        ? 'Хочу заказать секретные файлы (VIP клиент)'
                        : 'Maxfiy fayllar buyurtma qilmoqchiman (VIP mijoz)';
                    window.open(`https://wa.me/998999100097?text=${encodeURIComponent(whatsappText)}`, '_blank');
                };
            }
        }
        
        // Закрытие модальных окон
        function closeModal() {
            document.getElementById('prize-modal').style.display = 'none';
        }
        
        function closeVipModal() {
            document.getElementById('vip-modal').style.display = 'none';
        }
        
        // Закрытие модальных окон при клике вне их
        window.addEventListener('click', function(event) {
            if (event.target === document.getElementById('prize-modal')) {
                closeModal();
            }
            if (event.target === document.getElementById('vip-modal')) {
                closeVipModal();
            }
        });
        
        // Автоматическое добавление монеток каждые 5 минут для VIP
        setInterval(() => {
            if (isPremium) {
                const coinsElement = document.getElementById('coins');
                let coins = parseInt(coinsElement.textContent.replace(/[^\d]/g, ''));
                coins += 10;
                coinsElement.textContent = coins.toLocaleString();
            }
        }, 300000);
        
        // Инициализация VIP кнопки в WhatsApp
        document.querySelector('.whatsapp-header').addEventListener('click', function(e) {
            if (e.target.closest('.whatsapp-header').getAttribute('href') === '#') {
                activatePremium();
                e.preventDefault();
            }
        });
        
        // Добавление услуги создания контента по желанию
        const servicesContainer = document.querySelector('.services-grid');
        
        // Если нужно добавить еще услуги, можно раскомментировать этот код:
        /*
        const extraServices = [
            {
                title: 'Создание контента',
                desc: 'Разработка уникального контента для соцсетей, блогов и сайтов',
                price: '250,000 UZS',
                icon: 'fas fa-blog'
            },
            {
                title: 'Фальшивый контент',
                desc: 'Создание развлекательного и демонстрационного контента',
                price: '300,000 UZS',
                icon: 'fas fa-film',
                vip: true
            }
        ];
        */
    </script>
</body>
</html>
