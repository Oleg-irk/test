<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Уникальная квартира в Иркутске - со выоими уникальными преимуществами</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        :root {
            --primary: #1a3e2f;
            --secondary: #d4af37;
            --light: #f8f9fa;
            --dark: #212529;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Montserrat', sans-serif;
        }
        
        body {
            overflow-x: hidden;
            color: var(--dark);
            background-color: var(--light);
        }
        
        /* Параллакс секции */
        .parallax-section {
            height: 100vh;
            background-attachment: fixed;
            background-position: center;
            background-repeat: no-repeat;
            background-size: cover;
            position: relative;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            overflow: hidden;
        }
        
        .parallax-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.3);
            z-index: 1;
        }
        
        .parallax-content {
            position: relative;
            z-index: 2;
            text-align: center;
            padding: 0 20px;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        /* Анимация появления */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .fade-in {
            animation: fadeInUp 1s ease-out forwards;
        }
        
        /* Заголовки */
        h1, h2, h3 {
            font-weight: 700;
            margin-bottom: 20px;
            text-transform: uppercase;
        }
        
        h1 {
            font-size: 3.5rem;
            line-height: 1.2;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }
        
        h2 {
            font-size: 2.5rem;
            color: var(--primary);
            position: relative;
            display: inline-block;
            padding-bottom: 10px;
        }
        
        h2:after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background: var(--secondary);
        }
        
        /* Кнопки */
        .btn {
            display: inline-block;
            padding: 15px 30px;
            background: var(--secondary);
            color: var(--primary);
            text-decoration: none;
            font-weight: 700;
            border-radius: 50px;
            margin-top: 20px;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        .btn:hover {
            background: #c9a227;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        .btn-outline {
            background: transparent;
            border: 2px solid white;
            color: white;
            margin-left: 15px;
        }
        
        .btn-outline:hover {
            background: white;
            color: var(--primary);
        }
        
        /* Навигация */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            padding: 20px 0;
            z-index: 1000;
            transition: all 0.3s ease;
        }
        
        header.scrolled {
            background: rgba(26, 62, 47, 0.9);
            padding: 10px 0;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: white;
            text-decoration: none;
        }
        
        .logo span {
            color: var(--secondary);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 30px;
        }
        
        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            position: relative;
        }
        
        .nav-links a:after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--secondary);
            transition: width 0.3s ease;
        }
        
        .nav-links a:hover:after {
            width: 100%;
        }
        
        /* Секции */
        .section {
            padding: 100px 20px;
            text-align: center;
        }
        
        .section-dark {
            background: var(--primary);
            color: white;
        }
        
        .section-dark h2 {
            color: white;
        }
        
        /* Галерея */
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 50px;
        }
        
        .gallery-item {
            position: relative;
            overflow: hidden;
            border-radius: 10px;
            height: 250px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
        }
        
        .gallery-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
        }
        
        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        
        .gallery-item:hover img {
            transform: scale(1.1);
        }
        
        .gallery-caption {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            padding: 20px;
            background: linear-gradient(to top, rgba(0, 0, 0, 0.8), transparent);
            color: white;
            transform: translateY(100%);
            transition: transform 0.3s ease;
        }
        
        .gallery-item:hover .gallery-caption {
            transform: translateY(0);
        }
        
        /* Преимущества */
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }
        
        .feature-item {
            padding: 30px;
            background: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease;
        }
        
        .feature-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
        
        .feature-icon {
            font-size: 3rem;
            color: var(--secondary);
            margin-bottom: 20px;
        }
        
        /* Форма */
        .form-container {
            max-width: 600px;
            margin: 50px auto 0;
            background: white;
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .form-group {
            margin-bottom: 20px;
            text-align: left;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: 600;
            color: var(--primary);
        }
        
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            transition: all 0.3s ease;
        }
        
        .form-group input:focus,
        .form-group textarea:focus {
            border-color: var(--secondary);
            outline: none;
            box-shadow: 0 0 0 3px rgba(212, 175, 55, 0.2);
        }
        
        /* Карта */
        .map-container {
            height: 400px;
            margin-top: 50px;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        /* Футер */
        footer {
            background: var(--dark);
            color: white;
            padding: 50px 20px;
            text-align: center;
        }
        
        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            text-align: left;
        }
        
        .footer-column h3 {
            color: var(--secondary);
            font-size: 1.3rem;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-column h3:after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 2px;
            background: var(--secondary);
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 10px;
        }
        
        .footer-column ul li a {
            color: #aaa;
            text-decoration: none;
            transition: all 0.3s ease;
        }
        
        .footer-column ul li a:hover {
            color: var(--secondary);
            padding-left: 5px;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            color: white;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            background: var(--secondary);
            color: var(--primary);
            transform: translateY(-3px);
        }
        
        .copyright {
            margin-top: 50px;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #aaa;
            font-size: 0.9rem;
        }
        
        /* Адаптивность */
        @media (max-width: 992px) {
            h1 {
                font-size: 2.5rem;
            }
            
            h2 {
                font-size: 2rem;
            }
            
            .nav-links {
                display: none;
            }
            
            .mobile-menu-btn {
                display: block;
                color: white;
                font-size: 1.5rem;
                cursor: pointer;
            }
        }
        
        @media (max-width: 768px) {
            .btn {
                display: block;
                width: 100%;
                margin: 10px 0;
            }
            
            .btn-outline {
                margin-left: 0;
            }
            
            .parallax-content {
                padding: 0 15px;
            }
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700&display=swap" rel="stylesheet">
</head>
<body>
    <!-- Навигация -->
    <header id="header">
        <div class="nav-container">
            <a href="#" class="logo">Катунь<span>Ривер</span></a>
            <ul class="nav-links">
                <li><a href="#about">О проекте</a></li>
                <li><a href="#features">Преимущества</a></li>
                <li><a href="#gallery">Галерея</a></li>
                <li><a href="#location">Расположение</a></li>
                <li><a href="#contact">Контакты</a></li>
            </ul>
            <i class="fas fa-bars mobile-menu-btn"></i>
        </div>
    </header>

    <!-- Герой секция с параллаксом -->
    <section class="parallax-section" style="background-image: url('https://images.unsplash.com/photo-1501785888041-af3ef285b470?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80');">
        <div class="parallax-overlay"></div>
        <div class="parallax-content">
            <h1 class="fade-in">Уникальный участок на первой линии Катуни</h1>
            <p class="fade-in" style="animation-delay: 0.2s;">Эксклюзивный участок земли с потрясающим видом на реку и горы</p>
            <div class="fade-in" style="animation-delay: 0.4s;">
                <a href="#contact" class="btn">Оставить заявку</a>
                <a href="#about" class="btn btn-outline">Подробнее</a>
            </div>
        </div>
    </section>

    <!-- О проекте -->
    <section id="about" class="section">
        <div class="container">
            <h2>О проекте</h2>
            <p>Представляем вашему вниманию уникальный участок земли, расположенный на первой линии реки Катунь в одном из самых живописных мест Алтая. Это место сочетает в себе потрясающие природные виды, удобное расположение и отличные перспективы для инвестиций.</p>
            
            <div class="features" style="margin-top: 50px;">
                <div class="feature-item fade-in">
                    <div class="feature-icon">
                        <i class="fas fa-map-marked-alt"></i>
                    </div>
                    <h3>Идеальное расположение</h3>
                    <p>Участок находится в 200 метрах от реки Катунь с панорамным видом на горы. Близость к инфраструктуре при полной приватности.</p>
                </div>
                
                <div class="feature-item fade-in" style="animation-delay: 0.2s;">
                    <div class="feature-icon">
                        <i class="fas fa-expand"></i>
                    </div>
                    <h3>Большая площадь</h3>
                    <p>Участок площадью 15 соток позволяет реализовать любые архитектурные решения и создать комфортное пространство для жизни.</p>
                </div>
                
                <div class="feature-item fade-in" style="animation-delay: 0.4s;">
                    <div class="feature-icon">
                        <i class="fas fa-tree"></i>
                    </div>
                    <h3>Экология</h3>
                    <p>Чистейший воздух, хвойный лес по границе участка и кристальные воды Катуни создают идеальные условия для жизни и отдыха.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Преимущества -->
    <section id="features" class="section section-dark">
        <div class="container">
            <h2>Преимущества</h2>
            <p>Почему стоит приобрести этот участок прямо сейчас</p>
            
            <div class="features">
                <div class="feature-item fade-in">
                    <h3>Инвестиционная привлекательность</h3>
                    <p>Земля на первой линии Катуни постоянно растет в цене. Это надежная инвестиция с высокой доходностью.</p>
                </div>
                
                <div class="feature-item fade-in" style="animation-delay: 0.1s;">
                    <h3>Готовые коммуникации</h3>
                    <p>К участку подведены электричество, газ и вода. Есть возможность подключения к высокоскоростному интернету.</p>
                </div>
                
                <div class="feature-item fade-in" style="animation-delay: 0.2s;">
                    <h3>Разрешенное использование</h3>
                    <p>Участок предназначен для индивидуального жилищного строительства (ИЖС) с возможностью регистрации.</p>
                </div>
                
                <div class="feature-item fade-in" style="animation-delay: 0.3s;">
                    <h3>Развитая инфраструктура</h3>
                    <p>В пешей доступности магазины, кафе, банкоматы. В 5 км - крупный поселок со всей необходимой инфраструктурой.</p>
                </div>
                
                <div class="feature-item fade-in" style="animation-delay: 0.4s;">
                    <h3>Туристический потенциал</h3>
                    <p>Идеальное место для строительства гостевого дома или базы отдыха с высоким туристическим спросом.</p>
                </div>
                
                <div class="feature-item fade-in" style="animation-delay: 0.5s;">
                    <h3>Круглогодичный доступ</h3>
                    <p>Участок доступен в любое время года. Подъездная дорога обслуживается муниципальными службами.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Галерея -->
    <section id="gallery" class="section">
        <div class="container">
            <h2>Галерея</h2>
            <p>Посмотрите, как выглядит участок и окружающая его природа</p>
            
            <div class="gallery">
                <div class="gallery-item fade-in">
                    <img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80" alt="Вид на участок">
                    <div class="gallery-caption">
                        <h3>Панорамный вид</h3>
                        <p>Вид с участка на реку Катунь</p>
                    </div>
                </div>
                
                <div class="gallery-item fade-in" style="animation-delay: 0.1s;">
                    <img src="https://images.unsplash.com/photo-1470114716159-e389f8712fda?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80" alt="Река Катунь">
                    <div class="gallery-caption">
                        <h3>Река Катунь</h3>
                        <p>Кристально чистая вода и живописные берега</p>
                    </div>
                </div>
                
                <div class="gallery-item fade-in" style="animation-delay: 0.2s;">
                    <img src="https://images.unsplash.com/photo-1501785888041-af3ef285b470?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80" alt="Горный пейзаж">
                    <div class="gallery-caption">
                        <h3>Горный пейзаж</h3>
                        <p>Вид на горы с территории участка</p>
                    </div>
                </div>
                
                <div class="gallery-item fade-in" style="animation-delay: 0.3s;">
                    <img src="https://images.unsplash.com/photo-1476231682828-37e571bc172f?ixlib=rb-1.2.1&auto=format&fit=crop&w=1950&q=80" alt="Хвойный лес">
                    <div class="gallery-caption">
                        <h3>Хвойный лес</h3>
                        <p>Собственный лес по границе участка</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Расположение -->
    <section id="location" class="section section-dark">
        <div class="container">
            <h2>Расположение</h2>
            <p>Удобная транспортная доступность и близость к основным достопримечательностям Алтая</p>
            
            <div class="map-container fade-in">
                <!-- Здесь будет карта -->
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d12345.678901234567!2d84.12345678901234!3d51.123456789012345!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zNTHCsDA3JzI0LjQiTiA4NMKwMDcnMjQuNCJF!5e0!3m2!1sen!2sru!4v1234567890123!5m2!1sen!2sru" width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
            </div>
            
            <div class="features" style="margin-top: 50px;">
                <div class="feature-item fade-in">
                    <h3>Расстояния</h3>
                    <ul style="text-align: left; list-style: none;">
                        <li><i class="fas fa-car" style="margin-right: 10px; color: var(--secondary);"></i> 15 км до аэропорта</li>
                        <li><i class="fas fa-car" style="margin-right: 10px; color: var(--secondary);"></i> 5 км до поселка</li>
                        <li><i class="fas fa-car" style="margin-right: 10px; color: var(--secondary);"></i> 50 км до горнолыжного курорта</li>
                    </ul>
                </div>
                
                <div class="feature-item fade-in" style="animation-delay: 0.2s;">
                    <h3>Достопримечательности рядом</h3>
                    <ul style="text-align: left; list-style: none;">
                        <li><i class="fas fa-mountain" style="margin-right: 10px; color: var(--secondary);"></i> Гора Белуха - 100 км</li>
                        <li><i class="fas fa-water" style="margin-right: 10px; color: var(--secondary);"></i> Озеро Ая - 25 км</li>
                        <li><i class="fas fa-spa" style="margin-right: 10px; color: var(--secondary);"></i> Термальные источники - 40 км</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Контакты -->
    <section id="contact" class="section">
        <div class="container">
            <h2>Оставьте заявку</h2>
            <p>Заполните форму, и мы свяжемся с вами для уточнения деталей</p>
            
            <div class="form-container fade-in">
                <form id="contact-form">
                    <div class="form-group">
                        <label for="name">Ваше имя</label>
                        <input type="text" id="name" name="name" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="phone">Телефон</label>
                        <input type="tel" id="phone" name="phone" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" name="email" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="message">Сообщение</label>
                        <textarea id="message" name="message" rows="4"></textarea>
                    </div>
                    
                    <button type="submit" class="btn">Отправить заявку</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Футер -->
    <footer>
        <div class="footer-content">
            <div class="footer-column">
                <h3>ДоброГрад</h3>
                <p>Продажа элитных участков земли на первой линии реки Катунь в Алтайском крае.</p>
                <div class="social-links">
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-facebook-f"></i></a>
                    <a href="#"><i class="fab fa-whatsapp"></i></a>
                </div>
            </div>
            
            <div class="footer-column">
                <h3>Контакты</h3>
                <ul>
                    <li><i class="fas fa-phone" style="margin-right: 10px;"></i> +7 (950) 126-82-88</li>
                    <li><i class="fas fa-envelope" style="margin-right: 10px;"></i> info@katun-river.ru</li>
                    <li><i class="fas fa-map-marker-alt" style="margin-right: 10px;"></i> Алтайский край, Чемальский район</li>
                </ul>
            </div>
            
            <div class="footer-column">
                <h3>Быстрые ссылки</h3>
                <ul>
                    <li><a href="#about">О проекте</a></li>
                    <li><a href="#features">Преимущества</a></li>
                    <li><a href="#gallery">Галерея</a></li>
                    <li><a href="#location">Расположение</a></li>
                    <li><a href="#contact">Контакты</a></li>
                </ul>
            </div>
        </div>
        
        <div class="copyright">
            <p>&copy; 2023 ДоброГрад. Все права защищены.</p>
        </div>
    </footer>

    <script>
        // Параллакс эффект
        window.addEventListener('scroll', function() {
            const parallaxSections = document.querySelectorAll('.parallax-section');
            const scrollPosition = window.pageYOffset;
            
            parallaxSections.forEach(section => {
                const speed = 0.5;
                const offset = scrollPosition * speed;
                section.style.backgroundPositionY = offset + 'px';
            });
            
            // Фиксированная навигация
            const header = document.getElementById('header');
            if (window.scrollY > 100) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });
        
        // Плавная прокрутка
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // Анимация при скролле
        const fadeElements = document.querySelectorAll('.fade-in');
        
        function checkFade() {
            fadeElements.forEach(element => {
                const elementTop = element.getBoundingClientRect().top;
                const windowHeight = window.innerHeight;
                
                if (elementTop < windowHeight - 100) {
                    element.style.opacity = '1';
                    element.style.transform = 'translateY(0)';
                }
            });
        }
        
        window.addEventListener('scroll', checkFade);
        window.addEventListener('load', checkFade);
        
        // Мобильное меню
        const mobileMenuBtn = document.querySelector('.mobile-menu-btn');
        const navLinks = document.querySelector('.nav-links');
        
        if (mobileMenuBtn && navLinks) {
            mobileMenuBtn.addEventListener('click', function() {
                navLinks.style.display = navLinks.style.display === 'flex' ? 'none' : 'flex';
            });
            
            window.addEventListener('resize', function() {
                if (window.innerWidth > 992) {
                    navLinks.style.display = 'flex';
                } else {
                    navLinks.style.display = 'none';
                }
            });
        }
        
        // Обработка формы
        const contactForm = document.getElementById('contact-form');
        if (contactForm) {
            contactForm.addEventListener('submit', function(e) {
                e.preventDefault();
                
                // Здесь можно добавить AJAX отправку формы
                alert('Спасибо! Ваша заявка отправлена. Мы свяжемся с вами в ближайшее время.');
                this.reset();
            });
        }
    </script>
</body>
</html>
