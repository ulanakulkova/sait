
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Кулькова Ульяна Андреевна - IT-специалист</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Roboto:wght@300;400;500&display=swap" rel="stylesheet">
    <style>
        /* ===== CSS РЕЗЮМЕ САЙТА ===== */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary-color: #4f46e5;
            --primary-dark: #3730a3;
            --secondary-color: #10b981;
            --text-dark: #1f2937;
            --text-light: #6b7280;
            --bg-light: #f9fafb;
            --bg-white: #ffffff;
            --shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
            --shadow-lg: 0 10px 25px -5px rgba(0, 0, 0, 0.1);
            --transition: all 0.3s ease;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Inter', sans-serif;
            line-height: 1.6;
            color: var(--text-dark);
            background-color: var(--bg-white);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        section {
            padding: 80px 0;
        }

        .section-title {
            font-size: 2.5rem;
            font-weight: 700;
            text-align: center;
            margin-bottom: 20px;
            color: var(--text-dark);
        }

        .section-subtitle {
            text-align: center;
            color: var(--text-light);
            font-size: 1.1rem;
            max-width: 600px;
            margin: 0 auto 50px;
        }

        /* ===== HEADER ===== */
        .header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 100px 0;
            position: relative;
            overflow: hidden;
        }

        .header-content {
            display: flex;
            align-items: center;
            gap: 50px;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .profile-photo-container {
            flex-shrink: 0;
        }

        .profile-photo {
            width: 250px;
            height: 250px;
            border-radius: 50%;
            object-fit: cover;
            border: 8px solid rgba(255, 255, 255, 0.2);
            box-shadow: var(--shadow-lg);
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
        }

        .header-info {
            flex: 1;
        }

        .full-name {
            font-size: 3rem;
            font-weight: 700;
            margin-bottom: 10px;
            animation: fadeInUp 0.8s ease;
        }

        .specialization {
            font-size: 1.5rem;
            font-weight: 500;
            margin-bottom: 20px;
            color: rgba(255, 255, 255, 0.9);
            animation: fadeInUp 0.8s ease 0.2s both;
        }

        .pitch {
            font-size: 1.2rem;
            line-height: 1.8;
            margin-bottom: 30px;
            max-width: 600px;
            animation: fadeInUp 0.8s ease 0.4s both;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* ===== NAVBAR ===== */
        .navbar {
            position: sticky;
            top: 0;
            z-index: 1000;
            background: var(--bg-white);
            box-shadow: var(--shadow);
            transition: var(--transition);
        }

        .navbar.scrolled {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 70px;
        }

        .nav-logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary-color);
            text-decoration: none;
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 30px;
        }

        .nav-link {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 500;
            padding: 8px 16px;
            border-radius: 6px;
            transition: var(--transition);
        }

        .nav-link:hover {
            color: var(--primary-color);
            background: rgba(79, 70, 229, 0.1);
        }

        .nav-link.active {
            color: var(--primary-color);
            background: rgba(79, 70, 229, 0.1);
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            font-size: 1.5rem;
            color: var(--text-dark);
            cursor: pointer;
        }

        /* ===== HERO SECTION ===== */
        .hero {
            background: var(--bg-light);
            padding: 100px 0;
        }

        .hero-content {
            text-align: center;
            max-width: 800px;
            margin: 0 auto;
        }

        .hero-title {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 20px;
            color: var(--text-dark);
        }

        .hero-description {
            font-size: 1.2rem;
            color: var(--text-light);
            margin-bottom: 40px;
            line-height: 1.8;
        }

        .cta-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 14px 32px;
            border-radius: 8px;
            font-weight: 600;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 10px;
            transition: var(--transition);
            cursor: pointer;
            border: none;
            font-size: 1rem;
        }

        .btn-primary {
            background: var(--primary-color);
            color: white;
        }

        .btn-primary:hover {
            background: var(--primary-dark);
            transform: translateY(-2px);
            box-shadow: var(--shadow-lg);
        }

        .btn-secondary {
            background: white;
            color: var(--primary-color);
            border: 2px solid var(--primary-color);
        }

        .btn-secondary:hover {
            background: var(--primary-color);
            color: white;
            transform: translateY(-2px);
        }

        /* ===== COURSES SECTION ===== */
        .courses {
            background: white;
        }

        .filter-buttons {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin-bottom: 40px;
            flex-wrap: wrap;
        }

        .filter-btn {
            padding: 8px 20px;
            background: var(--bg-light);
            border: none;
            border-radius: 20px;
            font-weight: 500;
            cursor: pointer;
            transition: var(--transition);
        }

        .filter-btn.active {
            background: var(--primary-color);
            color: white;
        }

        .certificates-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .certificate-card {
            background: var(--bg-white);
            border-radius: 15px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
            cursor: pointer;
        }

        .certificate-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow-lg);
        }

        .certificate-image-container {
            position: relative;
            height: 200px;
            overflow: hidden;
        }

        .certificate-image {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.3s ease;
        }

        .certificate-card:hover .certificate-image {
            transform: scale(1.05);
        }

        .certificate-overlay {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0, 0, 0, 0.7);
            display: flex;
            align-items: center;
            justify-content: center;
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .certificate-card:hover .certificate-overlay {
            opacity: 1;
        }

        .certificate-info {
            padding: 25px;
        }

        .platform-badge {
            display: inline-block;
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 600;
            margin-bottom: 15px;
        }

        .certificate-title {
            font-size: 1.5rem;
            font-weight: 600;
            margin-bottom: 10px;
            color: var(--text-dark);
        }

        .certificate-meta {
            display: flex;
            gap: 20px;
            margin-bottom: 15px;
            color: var(--text-light);
            font-size: 0.9rem;
        }

        .certificate-meta i {
            margin-right: 5px;
        }

        .certificate-description {
            color: var(--text-dark);
            line-height: 1.6;
            margin-bottom: 20px;
            font-size: 0.95rem;
        }

        .skills-list {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 20px;
        }

        .skill-tag {
            background: var(--bg-light);
            color: var(--text-dark);
            padding: 5px 12px;
            border-radius: 15px;
            font-size: 0.8rem;
            font-weight: 500;
        }

        .view-certificate {
            color: var(--primary-color);
            font-weight: 600;
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        /* ===== МОДАЛЬНОЕ ОКНО ===== */
        .modal {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0, 0, 0, 0.9);
            display: none;
            align-items: center;
            justify-content: center;
            z-index: 2000;
            padding: 20px;
        }

        .modal.active {
            display: flex;
            animation: fadeIn 0.3s ease;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .modal-content {
            background: white;
            border-radius: 15px;
            max-width: 900px;
            max-height: 90vh;
            overflow-y: auto;
            position: relative;
            animation: slideUp 0.3s ease;
        }

        @keyframes slideUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .close-modal {
            position: absolute;
            top: 20px;
            right: 20px;
            background: none;
            border: none;
            font-size: 1.5rem;
            color: var(--text-light);
            cursor: pointer;
            z-index: 2001;
        }

        .modal-header {
            padding: 30px 30px 20px;
            border-bottom: 1px solid #e2e8f0;
        }

        .modal-header h3 {
            font-size: 2rem;
            color: var(--text-dark);
            margin-bottom: 5px;
        }

        .certificate-full-image {
            padding: 30px;
            text-align: center;
        }

        .certificate-full-image img {
            max-width: 100%;
            max-height: 400px;
            border-radius: 10px;
            box-shadow: var(--shadow);
        }

        .modal-info {
            padding: 0 30px 30px;
        }

        .modal-actions {
            padding: 20px 30px;
            border-top: 1px solid #e2e8f0;
            display: flex;
            gap: 15px;
            justify-content: flex-end;
        }

        /* ===== PROJECTS SECTION ===== */
        .projects {
            background: var(--bg-light);
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(400px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .project-card {
            background: white;
            border-radius: 15px;
            padding: 30px;
            box-shadow: var(--shadow);
            transition: var(--transition);
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow-lg);
        }

        .project-title {
            font-size: 1.5rem;
            font-weight: 600;
            margin-bottom: 15px;
            color: var(--text-dark);
        }

        .project-description {
            color: var(--text-light);
            margin-bottom: 20px;
            line-height: 1.6;
        }

        .project-role {
            display: inline-block;
            background: rgba(79, 70, 229, 0.1);
            color: var(--primary-color);
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: 500;
            margin-bottom: 15px;
        }

        .project-technologies {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 20px;
        }

        .tech-tag {
            background: var(--bg-light);
            color: var(--text-dark);
            padding: 5px 12px;
            border-radius: 15px;
            font-size: 0.8rem;
        }

        .project-links {
            display: flex;
            gap: 15px;
        }

        /* ===== PRACTICE SECTION ===== */
        .practice {
            background: white;
        }

        .practice-content {
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
        }

        .practice-description {
            font-size: 1.1rem;
            line-height: 1.8;
            color: var(--text-dark);
            margin-bottom: 40px;
        }

        .practice-image {
            width: 100%;
            max-width: 600px;
            height: auto;
            border-radius: 15px;
            margin-bottom: 30px;
            box-shadow: var(--shadow-lg);
        }

        .twine-link {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            font-size: 1.1rem;
            font-weight: 600;
        }

        /* ===== SELF-DEVELOPMENT SECTION ===== */
        .self-development {
            background: var(--bg-light);
        }

        .roadmap-container {
            max-width: 1000px;
            margin: 0 auto;
            position: relative;
        }

        .roadmap-line {
            position: absolute;
            left: 50%;
            top: 0;
            bottom: 0;
            width: 4px;
            background: var(--primary-color);
            transform: translateX(-50%);
        }

        .roadmap-items {
            display: flex;
            flex-direction: column;
            gap: 60px;
        }

        .roadmap-item {
            display: flex;
            align-items: center;
            gap: 40px;
        }

        .roadmap-item:nth-child(even) {
            flex-direction: row-reverse;
        }

        .roadmap-icon {
            flex-shrink: 0;
            width: 60px;
            height: 60px;
            background: var(--primary-color);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5rem;
            position: relative;
            z-index: 1;
        }

        .roadmap-content {
            flex: 1;
            background: white;
            padding: 25px;
            border-radius: 15px;
            box-shadow: var(--shadow);
        }

        .roadmap-title {
            font-size: 1.3rem;
            font-weight: 600;
            margin-bottom: 15px;
            color: var(--text-dark);
        }

        .skills-categories {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 10px;
        }

        .skill-category {
            background: var(--bg-light);
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 0.9rem;
        }

        /* ===== ABOUT SECTION ===== */
        .about {
            background: white;
        }

        .about-content {
            max-width: 800px;
            margin: 0 auto;
        }

        .biography {
            text-align: center;
            margin-bottom: 50px;
        }

        .biography-text {
            font-size: 1.1rem;
            line-height: 1.8;
            color: var(--text-dark);
            margin-bottom: 30px;
        }

        .skills-section {
            margin-bottom: 50px;
        }

        .skills-category-title {
            font-size: 1.3rem;
            font-weight: 600;
            margin-bottom: 20px;
            color: var(--text-dark);
        }

        .skills-icons {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-bottom: 30px;
        }

        .skill-icon {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 10px;
            width: 80px;
        }

        .skill-icon i {
            font-size: 2rem;
            color: var(--primary-color);
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 40px;
        }

        .social-link {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 12px 24px;
            background: var(--bg-light);
            border-radius: 8px;
            text-decoration: none;
            color: var(--text-dark);
            transition: var(--transition);
        }

        .social-link:hover {
            background: var(--primary-color);
            color: white;
            transform: translateY(-2px);
        }

        /* ===== FOOTER ===== */
        .footer {
            background: var(--text-dark);
            color: white;
            padding: 50px 0 30px;
        }

        .footer-content {
            text-align: center;
        }

        .copyright {
            font-size: 1rem;
            margin-bottom: 20px;
        }

        .footer-links {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-bottom: 30px;
        }

        .footer-link {
            color: rgba(255, 255, 255, 0.8);
            text-decoration: none;
            transition: var(--transition);
        }

        .footer-link:hover {
            color: white;
        }

        .github-info {
            font-size: 0.9rem;
            color: rgba(255, 255, 255, 0.6);
        }

        /* ===== АДАПТИВНОСТЬ ===== */
        @media (max-width: 992px) {
            .header-content {
                flex-direction: column;
                text-align: center;
                gap: 30px;
            }
            
            .full-name {
                font-size: 2.5rem;
            }
            
            .certificates-grid,
            .projects-grid {
                grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            }
            
            .roadmap-line {
                left: 40px;
            }
            
            .roadmap-item {
                flex-direction: row !important;
                gap: 20px;
            }
        }

        @media (max-width: 768px) {
            section {
                padding: 60px 0;
            }
            
            .section-title {
                font-size: 2rem;
            }
            
            .nav-menu {
                display: none;
            }
            
            .mobile-menu-btn {
                display: block;
            }
            
            .nav-menu.active {
                display: flex;
                flex-direction: column;
                position: absolute;
                top: 100%;
                left: 0;
                right: 0;
                background: white;
                padding: 20px;
                box-shadow: var(--shadow);
            }
            
            .cta-buttons {
                flex-direction: column;
                align-items: center;
            }
            
            .btn {
                width: 100%;
                max-width: 300px;
                justify-content: center;
            }
            
            .certificates-grid,
            .projects-grid {
                grid-template-columns: 1fr;
            }
            
            .social-links {
                flex-direction: column;
                align-items: center;
            }
        }

        @media (max-width: 480px) {
            .full-name {
                font-size: 2rem;
            }
            
            .specialization {
                font-size: 1.2rem;
            }
            
            .profile-photo {
                width: 200px;
                height: 200px;
            }
            
            .modal-content {
                margin: 10px;
            }
            
            .modal-header h3 {
                font-size: 1.5rem;
            }
            
            .modal-actions {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <!-- ===== HEADER ===== -->
    <header class="header" id="home">
        <div class="header-content">
            <div class="profile-photo-container">
                <img src="https://images.unsplash.com/photo-1494790108755-2616b612b786?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=500&q=80" 
                     alt="Кулькова Ульяна Андреевна" class="profile-photo">
            </div>
            
            <div class="header-info">
                <h1 class="full-name">Кулькова Ульяна Андреевна</h1>
                <h2 class="specialization">IT-специалист • Менеджер проектов</h2>
                <p class="pitch">
                    Организую эффективную работу команд и контролирую выполнение проектов. 
                    Умею учиться быстро и решать нетривиальные задачи.
                </p>
            </div>
        </div>
    </header>

    <!-- ===== NAVBAR ===== -->
    <nav class="navbar" id="navbar">
        <div class="nav-container">
            <a href="#home" class="nav-logo">Ульяна Кулькова</a>
            
            <button class="mobile-menu-btn" id="mobileMenuBtn">
                <i class="fas fa-bars"></i>
            </button>
            
            <ul class="nav-menu" id="navMenu">
                <li><a href="#home" class="nav-link active">Главная</a></li>
                <li><a href="#courses" class="nav-link">Курсы</a></li>
                <li><a href="#projects" class="nav-link">Проекты</a></li>
                <li><a href="#practice" class="nav-link">Практика</a></li>
                <li><a href="#self-development" class="nav-link">Саморазвитие</a></li>
                <li><a href="#about" class="nav-link">Обо мне</a></li>
            </ul>
        </div>
    </nav>

    <!-- ===== HERO SECTION ===== -->
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <h2 class="hero-title">Управляю проектами и организую работу команд</h2>
                <p class="hero-description">
                    Студентка техникума по специальности "Информационные системы и программирование". 
                    Специализируюсь на организации работы команд, контроле выполнения задач 
                    и управлении проектами в IT-сфере.
                </p>
                <div class="cta-buttons">
                    <a href="#projects" class="btn btn-primary">
                        <i class="fas fa-code"></i> Смотреть проекты
                    </a>
                    <a href="#courses" class="btn btn-secondary">
                        <i class="fas fa-certificate"></i> Мои сертификаты
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== COURSES SECTION ===== -->
    <section class="courses" id="courses">
        <div class="container">
            <h2 class="section-title">📚 Пройденные курсы</h2>
            <p class="section-subtitle">Сертификаты и образовательные программы, подтверждающие мои знания</p>
            
            <div class="filter-buttons">
                <button class="filter-btn active" data-filter="all">Все</button>
                <button class="filter-btn" data-filter="programming">Программирование</button>
                <button class="filter-btn" data-filter="ai">Искусственный интеллект</button>
                <button class="filter-btn" data-filter="marketing">Маркетинг</button>
            </div>
            
            <div class="certificates-grid">
                <!-- СЕРТИФИКАТ 1: ИТ-Диктант -->
                <div class="certificate-card" data-category="programming">
                    <div class="certificate-image-container">
                        <img src="photo_5350481738817277267_y.jpg" 
                             alt="ИТ-Диктант сертификат" class="certificate-image">
                        <div class="certificate-overlay">
                            <i class="fas fa-expand"></i>
                        </div>
                    </div>
                    <div class="certificate-info">
                        <div class="platform-badge">Всероссийская образовательная акция</div>
                        <h3 class="certificate-title">ИТ-Диктант</h3>
                        <div class="certificate-meta">
                            <span><i class="far fa-calendar"></i> 12-13 сентября 2025 г.</span>
                            <span><i class="fas fa-star"></i> 94 из 100 баллов</span>
                        </div>
                        <p class="certificate-description">
                            Всероссийский диктант по информационным технологиям, проверяющий цифровую грамотность
                        </p>
                        <div class="skills-list">
                            <span class="skill-tag">IT-грамотность</span>
                            <span class="skill-tag">Цифровые компетенции</span>
                            <span class="skill-tag">Информационная безопасность</span>
                        </div>
                        <div class="view-certificate" onclick="openCertificateModal('it-dictant')">
                            <span>Нажмите для просмотра сертификата</span>
                            <i class="fas fa-arrow-right"></i>
                        </div>
                    </div>
                </div>
                
                <!-- СЕРТИФИКАТ 2: Генеративное искусство -->
                <div class="certificate-card" data-category="ai">
                    <div class="certificate-image-container">
                        <img src="photo_5350481738817277264_y.jpg" 
                             alt="Генеративное искусство сертификат" class="certificate-image">
                        <div class="certificate-overlay">
                            <i class="fas fa-expand"></i>
                        </div>
                    </div>
                    <div class="certificate-info">
                        <div class="platform-badge">СберУниверситет</div>
                        <h3 class="certificate-title">Генеративное искусство</h3>
                        <div class="certificate-meta">
                            <span><i class="far fa-calendar"></i> 5 ноября 2025 г.</span>
                            <span><i class="fas fa-clock"></i> Электронный курс</span>
                        </div>
                        <p class="certificate-description">
                            Курс по созданию и работе с генеративными нейросетями для создания цифрового искусства
                        </p>
                        <div class="skills-list">
                            <span class="skill-tag">Генеративные нейросети</span>
                            <span class="skill-tag">Цифровое искусство</span>
                            <span class="skill-tag">Промпт-инжиниринг</span>
                        </div>
                        <div class="view-certificate" onclick="openCertificateModal('generative-art')">
                            <span>Нажмите для просмотра сертификата</span>
                            <i class="fas fa-arrow-right"></i>
                        </div>
                    </div>
                </div>
                
                <!-- СЕРТИФИКАТ 3: Работа с LLM GigaChat -->
                <div class="certificate-card" data-category="ai">
                    <div class="certificate-image-container">
                        <img src="photo_5350481738817277265_y.jpg" 
                             alt="Работа с LLM GigaChat сертификат" class="certificate-image">
                        <div class="certificate-overlay">
                            <i class="fas fa-expand"></i>
                        </div>
                    </div>
                    <div class="certificate-info">
                        <div class="platform-badge">СберУниверситет</div>
                        <h3 class="certificate-title">Работа с LLM GigaChat</h3>
                        <div class="certificate-meta">
                            <span><i class="far fa-calendar"></i> 5 ноября 2025 г.</span>
                            <span><i class="fas fa-clock"></i> Электронный курс</span>
                        </div>
                        <p class="certificate-description">
                            Курс по работе с крупными языковыми моделями, их тонкой настройке и интеграции в проекты
                        </p>
                        <div class="skills-list">
                            <span class="skill-tag">LLM</span>
                            <span class="skill-tag">GigaChat</span>
                            <span class="skill-tag">Промпт-инжиниринг</span>
                            <span class="skill-tag">RAG</span>
                        </div>
                        <div class="view-certificate" onclick="openCertificateModal('gigachat')">
                            <span>Нажмите для просмотра сертификата</span>
                            <i class="fas fa-arrow-right"></i>
                        </div>
                    </div>
                </div>
                
                <!-- СЕРТИФИКАТ 4: VK Education -->
                <div class="certificate-card" data-category="marketing">
                    <div class="certificate-image-container">
                        <img src="https://images.unsplash.com/photo-1460925895917-afdab827c52f?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" 
                             alt="VK Education сертификат" class="certificate-image">
                        <div class="certificate-overlay">
                            <i class="fas fa-expand"></i>
                        </div>
                    </div>
                    <div class="certificate-info">
                        <div class="platform-badge">VK Education</div>
                        <h3 class="certificate-title">Новые медиа: SMM и digital-маркетинг</h3>
                        <div class="certificate-meta">
                            <span><i class="far fa-calendar"></i> 2024 г.</span>
                            <span><i class="fas fa-star"></i> 28 из 37 баллов</span>
                        </div>
                        <p class="certificate-description">
                            Программа по эффективному использованию платформ VK в SMM и digital-маркетинге
                        </p>
                        <div class="skills-list">
                            <span class="skill-tag">SMM</span>
                            <span class="skill-tag">Digital-маркетинг</span>
                            <span class="skill-tag">VK Реклама</span>
                            <span class="skill-tag">Контент-стратегия</span>
                        </div>
                        <div class="view-certificate" onclick="openCertificateModal('vk-education')">
                            <span>Нажмите для просмотра сертификата</span>
                            <i class="fas fa-arrow-right"></i>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== PROJECTS SECTION ===== -->
    <section class="projects" id="projects">
        <div class="container">
            <h2 class="section-title">💼 Мои проекты</h2>
            <p class="section-subtitle">Практические работы и реализованные решения</p>
            
            <div class="projects-grid">
                <!-- ПРОЕКТ 1 -->
                <div class="project-card">
                    <h3 class="project-title">Документооборот в команде</h3>
                    <span class="project-role">Менеджер</span>
                    <p class="project-description">
                        Реализация системы документооборота для управления проектной документацией. 
                        Отвечала за выполнение заданий другими участниками команды, 
                        координацию работы и контроль сроков выполнения.
                    </p>
                    <div class="project-technologies">
                        <span class="tech-tag">Управление проектами</span>
                        <span class="tech-tag">Координация команды</span>
                        <span class="tech-tag">Контроль качества</span>
                    </div>
                    <div class="project-links">
                        <a href="#" class="btn btn-secondary">
                            <i class="fab fa-github"></i> Репозиторий
                        </a>
                    </div>
                </div>
                
                <!-- ПРОЕКТ 2 -->
                <div class="project-card">
                    <h3 class="project-title">Проект для конкурса «Система»</h3>
                    <span class="project-role">Менеджер</span>
                    <p class="project-description">
                        Участие в конкурсе с проектом автоматизации образовательного процесса. 
                        Отвечала за организацию работы команды, распределение задач между участниками 
                        и контроль выполнения всех этапов проекта.
                    </p>
                    <div class="project-technologies">
                        <span class="tech-tag">Организация работы</span>
                        <span class="tech-tag">Распределение задач</span>
                        <span class="tech-tag">Контроль выполнения</span>
                    </div>
                    <div class="project-links">
                        <a href="#" class="btn btn-secondary">
                            <i class="fas fa-folder"></i> Документация
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== PRACTICE SECTION ===== -->
    <section class="practice" id="practice">
        <div class="container">
            <h2 class="section-title">🏢 Производственная практика</h2>
            <p class="section-subtitle">Опыт работы в реальных условиях</p>
            
            <div class="practice-content">
                <img src="https://images.unsplash.com/photo-1523240795612-9a054b0db644?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" 
                     alt="Практика в техникуме" class="practice-image">
                
                <p class="practice-description">
                    Прохождение производственной практики в ГБПОУ МО «Люберецкий техникум имени Ю.А. Гагарина». 
                    Получила практический опыт работы с IT-инфраструктурой, участвовала в разработке внутренних систем, 
                    изучала процессы документооборота и управления проектами.
                </p>
                
                <a href="#" class="twine-link">
                    <i class="fas fa-gamepad"></i> Интерактивная новелла о практике
                </a>
            </div>
        </div>
    </section>

    <!-- ===== SELF-DEVELOPMENT SECTION ===== -->
    <section class="self-development" id="self-development">
        <div class="container">
            <h2 class="section-title">🚀 Саморазвитие и обучение</h2>
            <p class="section-subtitle">Дорожная карта моих профессиональных навыков</p>
            
            <div class="roadmap-container">
                <div class="roadmap-line"></div>
                
                <div class="roadmap-items">
                    <!-- Frontend -->
                    <div class="roadmap-item">
                        <div class="roadmap-icon">
                            <i class="fas fa-code"></i>
                        </div>
                        <div class="roadmap-content">
                            <h3 class="roadmap-title">Веб-разработка</h3>
                            <p>Изучение современных технологий веб-разработки</p>
                            <div class="skills-categories">
                                <span class="skill-category">HTML5</span>
                                <span class="skill-category">CSS3</span>
                                <span class="skill-category">JavaScript</span>
                                <span class="skill-category">TypeScript</span>
                            </div>
                        </div>
                    </div>
                    
                    <!-- IT-инфраструктура -->
                    <div class="roadmap-item">
                        <div class="roadmap-icon">
                            <i class="fas fa-server"></i>
                        </div>
                        <div class="roadmap-content">
                            <h3 class="roadmap-title">IT-инфраструктура</h3>
                            <p>Работа с IT-системами и инфраструктурой</p>
                            <div class="skills-categories">
                                <span class="skill-category">Git</span>
                                <span class="skill-category">Linux</span>
                                <span class="skill-category">Базы данных</span>
                                <span class="skill-category">Сети</span>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Безопасность -->
                    <div class="roadmap-item">
                        <div class="roadmap-icon">
                            <i class="fas fa-shield-alt"></i>
                        </div>
                        <div class="roadmap-content">
                            <h3 class="roadmap-title">Информационная безопасность</h3>
                            <p>Защита данных и систем от кибератак</p>
                            <div class="skills-categories">
                                <span class="skill-category">Сетевая безопасность</span>
                                <span class="skill-category">DDoS-защита</span>
                                <span class="skill-category">Шифрование</span>
                                <span class="skill-category">Защита данных</span>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Генеративные модели -->
                    <div class="roadmap-item">
                        <div class="roadmap-icon">
                            <i class="fas fa-brain"></i>
                        </div>
                        <div class="roadmap-content">
                            <h3 class="roadmap-title">Генеративные модели</h3>
                            <p>Работа с искусственным интеллектом</p>
                            <div class="skills-categories">
                                <span class="skill-category">GigaChat</span>
                                <span class="skill-category">Kandinsky</span>
                                <span class="skill-category">Промпт-инжиниринг</span>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Управление проектами -->
                    <div class="roadmap-item">
                        <div class="roadmap-icon">
                            <i class="fas fa-tasks"></i>
                        </div>
                        <div class="roadmap-content">
                            <h3 class="roadmap-title">Управление проектами</h3>
                            <p>Организация работы команд и контроль выполнения задач</p>
                            <div class="skills-categories">
                                <span class="skill-category">Планирование</span>
                                <span class="skill-category">Координация</span>
                                <span class="skill-category">Контроль качества</span>
                                <span class="skill-category">Командная работа</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== ABOUT SECTION ===== -->
    <section class="about" id="about">
        <div class="container">
            <h2 class="section-title">👩‍💻 Обо мне</h2>
            <p class="section-subtitle">Краткая биография и контактная информация</p>
            
            <div class="about-content">
                <div class="biography">
                    <p class="biography-text">
                        Учусь в ГБПОУ МО «Люберецкий техникум имени Ю.А. Гагарина» 
                        по специальности 09.02.07 «Информационные системы и программирование».
                    </p>
                    <p class="biography-text">
                        Специализируюсь на организации работы команд и управлении проектами в IT-сфере. 
                        Имею опыт координации работы разработчиков и контроля выполнения задач. 
                        Стремлюсь к постоянному профессиональному развитию и получению практического опыта.
                    </p>
                </div>
                
                <div class="skills-section">
                    <h3 class="skills-category-title">Языки программирования</h3>
                    <div class="skills-icons">
                        <div class="skill-icon">
                            <i class="fab fa-js-square"></i>
                            <span>JavaScript</span>
                        </div>
                        <div class="skill-icon">
                            <i class="fas fa-database"></i>
                            <span>SQL</span>
                        </div>
                        <div class="skill-icon">
                            <i class="fas fa-code"></i>
                            <span>1C</span>
                        </div>
                        <div class="skill-icon">
                            <i class="fas fa-terminal"></i>
                            <span>Bash</span>
                        </div>
                    </div>
                </div>
                
                <div class="skills-section">
                    <h3 class="skills-category-title">Инструменты и технологии</h3>
                    <div class="skills-icons">
                        <div class="skill-icon">
                            <i class="fab fa-git-alt"></i>
                            <span>Git</span>
                        </div>
                        <div class="skill-icon">
                            <i class="fas fa-cloud"></i>
                            <span>Yandex Cloud</span>
                        </div>
                        <div class="skill-icon">
                            <i class="fab fa-linux"></i>
                            <span>Linux</span>
                        </div>
                        <div class="skill-icon">
                            <i class="fas fa-cogs"></i>
                            <span>LVM</span>
                        </div>
                    </div>
                </div>
                
                <div class="skills-section">
                    <h3 class="skills-category-title">Soft Skills</h3>
                    <div class="skills-icons">
                        <div class="skill-icon">
                            <i class="fas fa-clock"></i>
                            <span>Тайм-менеджмент</span>
                        </div>
                        <div class="skill-icon">
                            <i class="fas fa-tasks"></i>
                            <span>Дисциплина</span>
                        </div>
                        <div class="skill-icon">
                            <i class="fas fa-users"></i>
                            <span>Работа в команде</span>
                        </div>
                        <div class="skill-icon">
                            <i class="fas fa-comments"></i>
                            <span>Коммуникация</span>
                        </div>
                    </div>
                </div>
                
                <div class="social-links">
                    <a href="#" class="social-link">
                        <i class="fab fa-github"></i>
                        <span>GitHub</span>
                    </a>
                    <a href="#" class="social-link">
                        <i class="fab fa-telegram"></i>
                        <span>Telegram</span>
                    </a>
                    <a href="#" class="social-link">
                        <i class="fab fa-vk"></i>
                        <span>ВКонтакте</span>
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== FOOTER ===== -->
    <footer class="footer">
        <div class="container">
            <div class="footer-content">
                <p class="copyright">
                    © 2025 Кулькова Ульяна Андреевна, ГБПОУ МО «Люберецкий техникум имени Героя Советского Союза, лётчика-космонавта Ю.А. Гагарина»
                </p>
                
                <div class="footer-links">
                    <a href="#" class="footer-link">
                        <i class="fab fa-github"></i> GitHub репозиторий
                    </a>
                    <a href="#" class="footer-link">
                        <i class="fas fa-globe"></i> Опубликованная версия
                    </a>
                </div>
                
                <p class="github-info">
                    Сайт доступен по адресу: https://username.github.io/resume/
                </p>
            </div>
        </div>
    </footer>

    <!-- ===== МОДАЛЬНЫЕ ОКНА ДЛЯ СЕРТИФИКАТОВ ===== -->
    <div class="modal" id="certificateModal">
        <div class="modal-content">
            <button class="close-modal" onclick="closeCertificateModal()">
                <i class="fas fa-times"></i>
            </button>
            
            <div class="modal-header">
                <h3 id="modalTitle">ИТ-Диктант</h3>
                <p class="platform" id="modalPlatform">Всероссийская образовательная акция</p>
            </div>
            
            <div class="certificate-full-image">
                <img id="modalImage" src="photo_5350481738817277267_y.jpg" alt="Сертификат">
            </div>
            
            <div class="modal-info">
                <div class="info-item">
                    <strong>Дата:</strong> <span id="modalDate">12-13 сентября 2025 г.</span>
                </div>
                <div class="info-item">
                    <strong>Результат:</strong> <span id="modalScore">94 из 100 баллов</span>
                </div>
                <div class="info-item">
                    <strong>Описание:</strong> 
                    <span id="modalDescription">Всероссийский диктант по информационным технологиям, проверяющий цифровую грамотность</span>
                </div>
            </div>
            
            <div class="modal-actions">
                <button class="btn btn-primary" onclick="openOriginalCertificate()">
                    <i class="fas fa-external-link-alt"></i> Открыть оригинал
                </button>
                <button class="btn btn-secondary" onclick="closeCertificateModal()">
                    Закрыть
                </button>
            </div>
        </div>
    </div>

    <script>
        // ===== ФУНКЦИОНАЛЬНОСТЬ САЙТА =====
        
        // Данные для сертификатов
        const certificates = {
            'it-dictant': {
                title: 'ИТ-Диктант',
                platform: 'Всероссийская образовательная акция',
                image: 'photo_5350481738817277267_y.jpg',
                date: '12-13 сентября 2025 г.',
                score: '94 из 100 баллов',
                description: 'Всероссийский диктант по информационным технологиям, проверяющий цифровую грамотность'
            },
            'generative-art': {
                title: 'Генеративное искусство',
                platform: 'СберУниверситет',
                image: 'photo_5350481738817277264_y.jpg',
                date: '5 ноября 2025 г.',
                score: 'Электронный курс',
                description: 'Курс по созданию и работе с генеративными нейросетями для создания цифрового искусства'
            },
            'gigachat': {
                title: 'Работа с LLM GigaChat',
                platform: 'СберУниверситет',
                image: 'photo_5350481738817277265_y.jpg',
                date: '5 ноября 2025 г.',
                score: 'Электронный курс',
                description: 'Курс по работе с крупными языковыми моделями, их тонкой настройке и интеграции в проекты'
            },
            'vk-education': {
                title: 'Новые медиа: SMM и digital-маркетинг',
                platform: 'VK Education',
                image: 'https://images.unsplash.com/photo-1460925895917-afdab827c52f?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80',
                date: '2024 г.',
                score: '28 из 37 баллов',
                description: 'Программа по эффективному использованию платформ VK в SMM и digital-маркетинге'
            }
        };

        // Открытие модального окна с сертификатом
        function openCertificateModal(certId) {
            const cert = certificates[certId];
            if (!cert) return;
            
            document.getElementById('modalTitle').textContent = cert.title;
            document.getElementById('modalPlatform').textContent = cert.platform;
            document.getElementById('modalImage').src = cert.image;
            document.getElementById('modalDate').textContent = cert.date;
            document.getElementById('modalScore').textContent = cert.score;
            document.getElementById('modalDescription').textContent = cert.description;
            
            document.getElementById('certificateModal').classList.add('active');
            document.body.style.overflow = 'hidden';
        }

        // Закрытие модального окна
        function closeCertificateModal() {
            document.getElementById('certificateModal').classList.remove('active');
            document.body.style.overflow = '';
        }

        // Открытие оригинала сертификата
        function openOriginalCertificate() {
            const currentImage = document.getElementById('modalImage').src;
            window.open(currentImage, '_blank');
        }

        // Фильтрация сертификатов
        document.addEventListener('DOMContentLoaded', function() {
            const filterButtons = document.querySelectorAll('.filter-btn');
            const certificateCards = document.querySelectorAll('.certificate-card');
            
            filterButtons.forEach(button => {
                button.addEventListener('click', function() {
                    // Убираем активный класс у всех кнопок
                    filterButtons.forEach(btn => btn.classList.remove('active'));
                    // Добавляем активный класс нажатой кнопке
                    this.classList.add('active');
                    
                    const filter = this.getAttribute('data-filter');
                    
                    certificateCards.forEach(card => {
                        if (filter === 'all' || card.getAttribute('data-category') === filter) {
                            card.style.display = 'block';
                        } else {
                            card.style.display = 'none';
                        }
                    });
                });
            });
            
            // Навигация
            const navLinks = document.querySelectorAll('.nav-link');
            const sections = document.querySelectorAll('section');
            
            function updateActiveNavLink() {
                let currentSection = '';
                
                sections.forEach(section => {
                    const sectionTop = section.offsetTop - 100;
                    const sectionHeight = section.clientHeight;
                    
                    if (window.scrollY >= sectionTop && window.scrollY < sectionTop + sectionHeight) {
                        currentSection = section.id;
                    }
                });
                
                navLinks.forEach(link => {
                    link.classList.remove('active');
                    if (link.getAttribute('href') === `#${currentSection}`) {
                        link.classList.add('active');
                    }
                });
            }
            
            window.addEventListener('scroll', updateActiveNavLink);
            
            // Sticky navbar при скролле
            const navbar = document.getElementById('navbar');
            
            window.addEventListener('scroll', function() {
                if (window.scrollY > 50) {
                    navbar.classList.add('scrolled');
                } else {
                    navbar.classList.remove('scrolled');
                }
            });
            
            // Мобильное меню
            const mobileMenuBtn = document.getElementById('mobileMenuBtn');
            const navMenu = document.getElementById('navMenu');
            
            mobileMenuBtn.addEventListener('click', function() {
                navMenu.classList.toggle('active');
            });
            
            // Закрытие модального окна при клике вне его
            document.getElementById('certificateModal').addEventListener('click', function(e) {
                if (e.target === this) {
                    closeCertificateModal();
                }
            });
            
            // Закрытие модального окна при нажатии ESC
            document.addEventListener('keydown', function(e) {
                if (e.key === 'Escape') {
                    closeCertificateModal();
                }
            });
        });
    </script>
</body>
</html>
