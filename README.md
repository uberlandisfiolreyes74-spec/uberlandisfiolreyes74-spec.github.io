
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Uberlandis Fiol Reyes | Creador Digital con IA</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Reset y estilos generales */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', system-ui, sans-serif;
        }

        :root {
            --primary: #6C63FF;
            --secondary: #FF6584;
            --accent: #36D1DC;
            --dark: #1A1A2E;
            --darker: #0F0C29;
            --light: #F8F9FA;
            --gray: #6C757D;
            --success: #06D6A0;
            --warning: #FFD166;
            --shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            --transition: all 0.3s ease;
        }

        body {
            background-color: var(--light);
            color: #333;
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        section {
            padding: 80px 0;
        }

        h1, h2, h3, h4 {
            font-weight: 700;
            line-height: 1.2;
            margin-bottom: 20px;
        }

        h1 { font-size: 3rem; }
        h2 { font-size: 2.5rem; }
        h3 { font-size: 1.8rem; }
        h4 { font-size: 1.3rem; }

        p {
            margin-bottom: 15px;
            font-size: 1.1rem;
        }

        a {
            text-decoration: none;
            color: var(--primary);
            transition: var(--transition);
        }

        a:hover {
            color: var(--secondary);
        }

        .btn {
            display: inline-block;
            padding: 14px 32px;
            background: linear-gradient(135deg, var(--primary), var(--accent));
            color: white;
            border-radius: 50px;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            border: none;
            cursor: pointer;
            transition: var(--transition);
            box-shadow: var(--shadow);
        }

        .btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(108, 99, 255, 0.3);
            color: white;
        }

        .btn-outline {
            background: transparent;
            border: 2px solid var(--primary);
            color: var(--primary);
        }

        .btn-outline:hover {
            background: var(--primary);
            color: white;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            width: 80px;
            height: 4px;
            background: linear-gradient(to right, var(--primary), var(--accent));
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            border-radius: 2px;
        }

        .card {
            background: white;
            border-radius: 15px;
            padding: 30px;
            box-shadow: var(--shadow);
            transition: var(--transition);
            height: 100%;
        }

        .card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
        }

        /* Header y navegación */
        header {
            background: linear-gradient(135deg, var(--darker), var(--dark));
            color: white;
            padding: 20px 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.2);
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            display: flex;
            align-items: center;
        }

        .logo i {
            color: var(--accent);
            margin-right: 10px;
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav li {
            margin-left: 30px;
        }

        nav a {
            color: white;
            font-weight: 500;
            font-size: 1.1rem;
        }

        nav a:hover {
            color: var(--accent);
        }

        .mobile-menu-btn {
            display: none;
            font-size: 1.5rem;
            background: none;
            border: none;
            color: white;
            cursor: pointer;
        }

        /* Hero section */
        .hero {
            background: linear-gradient(135deg, var(--darker), var(--dark));
            color: white;
            padding: 180px 0 100px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" preserveAspectRatio="none"><path d="M0,0 L100,0 L100,100 Z" fill="rgba(255,255,255,0.05)"/></svg>');
            background-size: cover;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            background: linear-gradient(to right, var(--accent), var(--primary));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        .hero-subtitle {
            font-size: 1.5rem;
            margin-bottom: 30px;
            opacity: 0.9;
        }

        .hero-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 40px;
        }

        /* Sobre mí */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .about-text h2 {
            text-align: left;
        }

        .about-text h2::after {
            left: 0;
            transform: none;
        }

        .skills-list {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 30px;
        }

        .skill-tag {
            background: rgba(108, 99, 255, 0.1);
            color: var(--primary);
            padding: 8px 20px;
            border-radius: 50px;
            font-weight: 600;
            font-size: 0.9rem;
        }

        .about-image {
            text-align: center;
        }

        .about-image img {
            max-width: 100%;
            border-radius: 20px;
            box-shadow: var(--shadow);
        }

        /* Servicios */
        .services {
            background-color: #f8f9ff;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 30px;
        }

        .service-icon {
            font-size: 3rem;
            margin-bottom: 20px;
            color: var(--primary);
        }

        /* Interpretación de sueños - Sección especial */
        .dream-section {
            background: linear-gradient(135deg, #1a1a2e, #16213e, #0f3460);
            color: white;
            position: relative;
            overflow: hidden;
        }

        .dream-section::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><circle cx="20" cy="20" r="1" fill="rgba(255,255,255,0.1)"/><circle cx="50" cy="80" r="1.5" fill="rgba(255,255,255,0.1)"/><circle cx="80" cy="40" r="1" fill="rgba(255,255,255,0.1)"/><circle cx="10" cy="60" r="2" fill="rgba(255,255,255,0.1)"/><circle cx="90" cy="90" r="1" fill="rgba(255,255,255,0.1)"/></svg>');
            background-size: 300px;
        }

        .dream-section .section-title {
            color: white;
        }

        .dream-section .section-title::after {
            background: linear-gradient(to right, var(--accent), var(--warning));
        }

        .dream-services {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-bottom: 50px;
        }

        .dream-card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            text-align: center;
            padding: 40px 30px;
            border-radius: 15px;
            transition: var(--transition);
        }

        .dream-card:hover {
            background: rgba(255, 255, 255, 0.15);
            transform: translateY(-10px);
            border-color: var(--accent);
        }

        .dream-icon {
            font-size: 3.5rem;
            margin-bottom: 20px;
            display: block;
        }

        .dream-card h3 {
            color: var(--warning);
        }

        .dream-cta {
            text-align: center;
            margin-top: 50px;
        }

        .dream-cta .btn {
            background: linear-gradient(135deg, var(--warning), var(--secondary));
        }

        /* Portafolio */
        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }

        .portfolio-item {
            border-radius: 15px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
            background: white;
        }

        .portfolio-item:hover {
            transform: translateY(-10px);
        }

        .portfolio-img {
            height: 200px;
            background: linear-gradient(135deg, var(--primary), var(--accent));
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
        }

        .portfolio-info {
            padding: 20px;
        }

        /* Contacto */
        .contact {
            background-color: #f8f9ff;
        }

        .contact-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .contact-item {
            display: flex;
            align-items: flex-start;
            gap: 15px;
        }

        .contact-icon {
            font-size: 1.5rem;
            color: var(--primary);
            width: 40px;
            flex-shrink: 0;
        }

        .contact-form input,
        .contact-form textarea,
        .contact-form select {
            width: 100%;
            padding: 15px;
            margin-bottom: 20px;
            border: 1px solid #ddd;
            border-radius: 10px;
            font-size: 1rem;
            transition: var(--transition);
        }

        .contact-form input:focus,
        .contact-form textarea:focus,
        .contact-form select:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 3px rgba(108, 99, 255, 0.2);
        }

        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 60px 0 30px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-logo {
            font-size: 1.8rem;
            font-weight: 700;
            margin-bottom: 20px;
        }

        .footer-links h4 {
            color: var(--accent);
            margin-bottom: 20px;
        }

        .footer-links ul {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 10px;
        }

        .footer-links a {
            color: #ccc;
        }

        .footer-links a:hover {
            color: var(--accent);
            padding-left: 5px;
        }

        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            color: white;
            font-size: 1.2rem;
            transition: var(--transition);
        }

        .social-links a:hover {
            background: var(--primary);
            transform: translateY(-5px);
        }

        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #aaa;
            font-size: 0.9rem;
        }

        /* Responsive */
        @media (max-width: 992px) {
            .about-content {
                grid-template-columns: 1fr;
            }

            .contact-container {
                grid-template-columns: 1fr;
            }

            h1 { font-size: 2.5rem; }
            h2 { font-size: 2rem; }
            .hero h1 { font-size: 2.8rem; }
        }

        @media (max-width: 768px) {
            nav ul {
                display: none;
            }

            .mobile-menu-btn {
                display: block;
            }

            .mobile-menu {
                display: none;
                position: fixed;
                top: 80px;
                left: 0;
                width: 100%;
                background: var(--dark);
                padding: 20px;
                box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
                z-index: 999;
            }

            .mobile-menu.active {
                display: block;
            }

            .mobile-menu ul {
                list-style: none;
            }

            .mobile-menu li {
                margin-bottom: 15px;
            }

            .mobile-menu a {
                color: white;
                font-size: 1.2rem;
                display: block;
                padding: 10px 0;
                border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            }

            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }

            .btn {
                width: 100%;
                max-width: 300px;
                text-align: center;
            }
        }

        @media (max-width: 576px) {
            section {
                padding: 60px 0;
            }

            h1 { font-size: 2rem; }
            h2 { font-size: 1.8rem; }
            .hero h1 { font-size: 2.2rem; }
            .hero-subtitle { font-size: 1.2rem; }

            .services-grid,
            .dream-services,
            .portfolio-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Header y Navegación -->
    <header>
        <div class="container header-container">
            <div class="logo">
                <i class="fas fa-brain"></i> Uberlandis Fiol Reyes
            </div>
            <nav>
                <ul>
                    <li><a href="#inicio">Inicio</a></li>
                    <li><a href="#sobre-mi">Sobre Mí</a></li>
                    <li><a href="#servicios">Servicios</a></li>
                    <li><a href="#suenos">Interpretación de Sueños</a></li>
                    <li><a href="#portafolio">Portafolio</a></li>
                    <li><a href="#contacto">Contacto</a></li>
                </ul>
            </nav>
            <button class="mobile-menu-btn" id="mobileMenuBtn">
                <i class="fas fa-bars"></i>
            </button>
        </div>
        <div class="mobile-menu" id="mobileMenu">
            <ul>
                <li><a href="#inicio">Inicio</a></li>
                <li><a href="#sobre-mi">Sobre Mí</a></li>
                <li><a href="#servicios">Servicios</a></li>
                <li><a href="#suenos">Interpretación de Sueños</a></li>
                <li><a href="#portafolio">Portafolio</a></li>
                <li><a href="#contacto">Contacto</a></li>
            </ul>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="inicio">
        <div class="container">
            <h1>Creador Digital con IA + Intérprete de Sueños</h1>
            <p class="hero-subtitle">Fusión de IA, diseño, estrategia digital y análisis onírico para crear contenido con impacto</p>
            <p>Transformo ideas en experiencias digitales únicas, combinando tecnología de vanguardia con perspectivas espirituales para ofrecer soluciones innovadoras y personalizadas.</p>
            <div class="hero-buttons">
                <a href="#contacto" class="btn">Contáctame para tu proyecto</a>
                <a href="#suenos" class="btn btn-outline">Interpretación de Sueños</a>
            </div>
        </div>
    </section>

    <!-- Sobre Mí -->
    <section id="sobre-mi">
        <div class="container">
            <div class="about-content">
                <div class="about-text">
                    <h2>Sobre Mí</h2>
                    <p>Soy un <strong>investigador independiente y creador digital</strong> especializado en la intersección entre tecnología, estrategia digital y análisis simbólico-espiritual.</p>
                    <p>Con formación en análisis de mercados, resiliencia táctica y estrategia digital, he desarrollado un enfoque único que combina herramientas de IA creativa con perspectivas espirituales para crear contenido transformador.</p>
                    <p>Mi misión es ayudar a individuos y empresas a navegar el panorama digital actual mientras exploran las dimensiones más profundas de la experiencia humana a través del análisis onírico.</p>
                    
                    <div class="skills-list">
                        <span class="skill-tag">IA Creativa (ChatGPT)</span>
                        <span class="skill-tag">Diseño Web</span>
                        <span class="skill-tag">Edición de Video</span>
                        <span class="skill-tag">Estrategia Digital</span>
                        <span class="skill-tag">Análisis de Mercados</span>
                        <span class="skill-tag">Interpretación de Sueños</span>
                        <span class="skill-tag">Contenido Espiritual</span>
                        <span class="skill-tag">Resiliencia Táctica</span>
                    </div>
                </div>
                <div class="about-image">
                    <!-- Imagen de perfil representativa -->
                    <div style="background: linear-gradient(135deg, var(--primary), var(--accent)); height: 400px; border-radius: 20px; display: flex; align-items: center; justify-content: center; color: white; font-size: 1.5rem;">
                        <div style="text-align: center;">
                            <i class="fas fa-user-circle" style="font-size: 5rem; margin-bottom: 20px;"></i>
                            <p>Uberlandis Fiol Reyes</p>
                            <p style="font-size: 1rem; opacity: 0.9;">Creador Digital con IA</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Servicios -->
    <section class="services" 
