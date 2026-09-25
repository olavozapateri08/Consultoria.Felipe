<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>THF Agro Consultoria</title>

    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700;800&family=Open+Sans:wght@300;400;600&display=swap" rel="stylesheet">

    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <style>
        :root {
            --primary: #1b4332;
            --primary-dark: #081c15;
            --accent: #52b788;
            --accent-light: #74c69d;
            --accent-gold: #d4af37;
            --text-dark: #2d3142;
            --text-light: #6c757d;
            --bg-light: #f8f9fa;
            --white: #ffffff;
            --shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Open Sans', sans-serif;
            color: var(--text-dark);
            background-color: var(--bg-light);
            line-height: 1.6;
            overflow-x: hidden;
        }

        h1, h2, h3, h4, h5, h6 {
            font-family: 'Montserrat', sans-serif;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }

            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Header & Navigation */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background-color: rgba(27, 67, 50, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            padding: 10px 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 2px 15px rgba(0,0,0,0.2);
            transition: var(--transition);
        }

        .logo-container {
            display: flex;
            align-items: center;
            text-decoration: none;
        }

        .logo-img {
            height: 50px;
            width: auto;
            object-fit: contain;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 25px;
        }

        nav a {
            color: var(--white);
            text-decoration: none;
            font-size: 14px;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            transition: var(--transition);
            position: relative;
            padding: 5px 0;
        }

            nav a::after {
                content: '';
                position: absolute;
                bottom: 0;
                left: 0;
                width: 0;
                height: 2px;
                background-color: var(--accent-light);
                transition: var(--transition);
            }

            nav a:hover::after {
                width: 100%;
            }

        .btn-contact {
            background-color: var(--accent);
            color: var(--primary-dark) !important;
            padding: 8px 20px !important;
            border-radius: 20px;
            font-weight: 700 !important;
        }

            .btn-contact::after {
                display: none !important;
            }

            .btn-contact:hover {
                background-color: var(--accent-light);
                transform: translateY(-2px);
            }

        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(8, 28, 21, 0.75), rgba(8, 28, 21, 0.85)), url('https://images.unsplash.com/photo-1500382017468-9049fed747ef?auto=format&fit=crop&w=1600&q=80') center/cover no-repeat;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: var(--white);
            padding: 0 20px;
        }

        .hero-content {
            max-width: 900px;
            animation: fadeIn 1s ease-in-out;
        }

        .hero h1 {
            font-size: 48px;
            font-weight: 800;
            margin-bottom: 15px;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

            .hero h1 span {
                color: var(--accent-light);
            }

        .hero p.tagline {
            font-size: 22px;
            font-weight: 300;
            margin-bottom: 30px;
            color: #e0e0e0;
        }

        .hero-pills {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 30px;
        }

        .pill {
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            backdrop-filter: blur(5px);
            padding: 10px 20px;
            border-radius: 30px;
            font-size: 14px;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 8px;
        }

            .pill i {
                color: var(--accent-light);
            }

        .hero-cta {
            margin-top: 35px;
        }

        .btn-schedule {
            background-color: #25d366;
            color: var(--white);
            padding: 14px 32px;
            border-radius: 30px;
            font-weight: 700;
            font-size: 16px;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 10px;
            box-shadow: 0 4px 15px rgba(37, 211, 102, 0.3);
            transition: var(--transition);
        }

            .btn-schedule:hover {
                background-color: #128c7e;
                transform: translateY(-3px);
                box-shadow: 0 6px 20px rgba(37, 211, 102, 0.4);
            }

        /* Floating WhatsApp Button */
        .whatsapp-float {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background-color: #25d366;
            color: #ffffff;
            border-radius: 50px;
            padding: 12px 22px;
            font-family: 'Montserrat', sans-serif;
            font-size: 14px;
            font-weight: 700;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.25);
            z-index: 9999;
            display: flex;
            align-items: center;
            gap: 10px;
            text-decoration: none;
            transition: var(--transition);
        }

            .whatsapp-float:hover {
                background-color: #128c7e;
                color: #ffffff;
                transform: scale(1.05);
            }

            .whatsapp-float i {
                font-size: 22px;
            }

        /* Section Commons */
        section {
            padding: 100px 8%;
        }

        .section-header {
            text-align: center;
            margin-bottom: 60px;
        }

            .section-header h2 {
                font-size: 36px;
                color: var(--primary);
                margin-bottom: 15px;
                position: relative;
                display: inline-block;
            }

                .section-header h2::after {
                    content: '';
                    position: absolute;
                    bottom: -10px;
                    left: 50%;
                    transform: translateX(-50%);
                    width: 60px;
                    height: 3px;
                    background-color: var(--accent);
                }

            .section-header p {
                color: var(--text-light);
                font-size: 16px;
                max-width: 600px;
                margin: 0 auto;
            }

        /* Quem Somos */
        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .about-text h3 {
            font-size: 28px;
            color: var(--primary-dark);
            margin-bottom: 20px;
        }

        .about-text p {
            margin-bottom: 20px;
            font-size: 16px;
            color: var(--text-dark);
        }

        .about-highlights {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-top: 30px;
        }

        .highlight-card {
            background-color: var(--white);
            padding: 20px;
            border-radius: 8px;
            box-shadow: var(--shadow);
            border-left: 4px solid var(--accent);
        }

            .highlight-card h4 {
                font-size: 18px;
                color: var(--primary);
                margin-bottom: 8px;
            }

        .about-image {
            position: relative;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: var(--shadow);
        }

            .about-image img {
                width: 100%;
                height: 100%;
                object-fit: cover;
                display: block;
            }

        /* MVV Section */
        .mvv-section {
            background-color: var(--primary);
            color: var(--white);
        }

            .mvv-section .section-header h2 {
                color: var(--white);
            }

            .mvv-section .section-header p {
                color: rgba(255, 255, 255, 0.8);
            }

        .mvv-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
        }

        .mvv-card {
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 12px;
            padding: 40px 30px;
            text-align: center;
            transition: var(--transition);
        }

            .mvv-card:hover {
                transform: translateY(-10px);
                background: rgba(255, 255, 255, 0.1);
            }

        .mvv-icon {
            width: 70px;
            height: 70px;
            background: var(--accent);
            color: var(--primary-dark);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 30px;
            margin: 0 auto 25px;
        }

        .mvv-card h3 {
            font-size: 22px;
            margin-bottom: 15px;
            color: var(--accent-light);
        }

        .mvv-card p {
            font-size: 15px;
            line-height: 1.7;
            color: rgba(255, 255, 255, 0.9);
        }

        .purpose-banner {
            margin-top: 50px;
            background: linear-gradient(135deg, var(--accent) 0%, var(--accent-light) 100%);
            border-radius: 12px;
            padding: 30px;
            text-align: center;
            color: var(--primary-dark);
        }

            .purpose-banner h3 {
                font-size: 18px;
                text-transform: uppercase;
                letter-spacing: 1px;
                margin-bottom: 5px;
            }

            .purpose-banner p {
                font-size: 24px;
                font-weight: 700;
            }

        /* Serviços / Áreas de Atuação */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 30px;
        }

        .service-card {
            background-color: var(--white);
            border-radius: 12px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
            display: flex;
            flex-direction: column;
        }

            .service-card:hover {
                transform: translateY(-5px);
                box-shadow: 0 15px 35px rgba(0, 0, 0, 0.12);
            }

        .service-img {
            height: 200px;
            position: relative;
            overflow: hidden;
        }

            .service-img img {
                width: 100%;
                height: 100%;
                object-fit: cover;
                transition: var(--transition);
            }

        .service-card:hover .service-img img {
            transform: scale(1.05);
        }

        .service-tag {
            position: absolute;
            top: 15px;
            left: 15px;
            background: var(--primary);
            color: var(--white);
            font-size: 12px;
            font-weight: 700;
            padding: 5px 12px;
            border-radius: 20px;
        }

        .service-content {
            padding: 30px;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
        }

            .service-content h3 {
                font-size: 22px;
                color: var(--primary);
                margin-bottom: 10px;
            }

            .service-content .subtitle {
                font-size: 14px;
                font-weight: 600;
                color: var(--accent);
                margin-bottom: 15px;
            }

        .service-list {
            list-style: none;
            margin-top: 15px;
        }

            .service-list li {
                font-size: 14px;
                color: var(--text-dark);
                margin-bottom: 10px;
                display: flex;
                align-items: flex-start;
                gap: 10px;
            }

                .service-list li i {
                    color: var(--accent);
                    margin-top: 4px;
                }

        /* Traceability Flow */
        .traceability-flow {
            background: var(--bg-light);
            border-radius: 8px;
            padding: 15px;
            margin-top: 15px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            text-align: center;
        }

        .flow-step {
            font-size: 12px;
            font-weight: 700;
            color: var(--primary);
        }

        .flow-arrow {
            color: var(--accent);
            font-size: 12px;
        }

        /* Perfis de Clientes */
        .clients-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
        }

        .client-card {
            background-color: var(--white);
            border-radius: 12px;
            padding: 35px 25px;
            box-shadow: var(--shadow);
            border-top: 4px solid var(--accent);
            transition: var(--transition);
        }

            .client-card:hover {
                transform: translateY(-5px);
            }

        .client-icon {
            font-size: 36px;
            color: var(--primary);
            margin-bottom: 20px;
        }

        .client-card h3 {
            font-size: 20px;
            color: var(--primary-dark);
            margin-bottom: 12px;
        }

        .client-card p {
            font-size: 14px;
            color: var(--text-light);
            line-height: 1.6;
        }

        /* Diferenciais */
        .differentials-section {
            background-color: var(--primary-dark);
            color: var(--white);
        }

            .differentials-section .section-header h2 {
                color: var(--white);
            }

            .differentials-section .section-header p {
                color: rgba(255, 255, 255, 0.8);
            }

        .differentials-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 25px;
        }

        .differential-card {
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 12px;
            padding: 30px 20px;
            text-align: center;
            transition: var(--transition);
        }

            .differential-card:hover {
                background: rgba(255, 255, 255, 0.1);
                border-color: var(--accent);
            }

        .differential-icon {
            width: 60px;
            height: 60px;
            background: rgba(82, 183, 136, 0.15);
            color: var(--accent-light);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            margin: 0 auto 20px;
        }

        .differential-card h3 {
            font-size: 18px;
            color: var(--white);
            margin-bottom: 10px;
        }

        .differential-card p {
            font-size: 13px;
            color: rgba(255, 255, 255, 0.7);
            line-height: 1.6;
        }

        /* Processo de Trabalho */
        .process-section {
            background-color: #f0f4f1;
        }

        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }

            .timeline::before {
                content: '';
                position: absolute;
                top: 0;
                left: 20px;
                height: 100%;
                width: 4px;
                background: var(--accent-light);
            }

        .timeline-item {
            position: relative;
            padding-left: 60px;
            margin-bottom: 40px;
        }

        .timeline-number {
            position: absolute;
            left: 0;
            top: 0;
            width: 44px;
            height: 44px;
            border-radius: 50%;
            background: var(--primary);
            color: var(--white);
            font-weight: 700;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 18px;
            box-shadow: 0 0 0 4px #f0f4f1;
        }

        .timeline-content {
            background: var(--white);
            padding: 20px 25px;
            border-radius: 8px;
            box-shadow: var(--shadow);
        }

            .timeline-content h3 {
                font-size: 18px;
                color: var(--primary);
                margin-bottom: 5px;
            }

            .timeline-content p {
                font-size: 14px;
                color: var(--text-light);
            }

        /* Footer / Contato */
        footer {
            background: var(--primary-dark);
            color: var(--white);
            padding: 60px 8% 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        .footer-grid {
            display: grid;
            grid-template-columns: 2fr 1fr 1fr;
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-brand p {
            color: #a0a0a0;
            margin-top: 15px;
            max-width: 400px;
            font-size: 14px;
        }

        .footer-links h4, .footer-contact h4 {
            font-size: 18px;
            margin-bottom: 20px;
            color: var(--accent-light);
        }

        .footer-links ul {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 10px;
        }

        .footer-links a {
            color: #a0a0a0;
            text-decoration: none;
            transition: var(--transition);
            font-size: 14px;
        }

            .footer-links a:hover {
                color: var(--white);
            }

        .footer-contact p {
            color: #a0a0a0;
            font-size: 14px;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .footer-contact i {
            color: var(--accent);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.05);
            font-size: 13px;
            color: #707070;
        }

        /* Responsividade */
        @media (max-width: 992px) {
            .about-grid, .mvv-grid, .services-grid, .clients-grid, .differentials-grid, .footer-grid {
                grid-template-columns: 1fr;
            }

            .hero h1 {
                font-size: 36px;
            }
        }

        @media (max-width: 768px) {
            header {
                flex-direction: column;
                padding: 15px;
            }

            nav ul {
                margin-top: 15px;
                flex-wrap: wrap;
                justify-content: center;
                gap: 15px;
            }

            .hero p.tagline {
                font-size: 18px;
            }

            section {
                padding: 60px 5%;
            }

            .whatsapp-float {
                bottom: 20px;
                right: 20px;
                padding: 10px 16px;
            }
        }
    </style>
</head>

<body>

    <!-- Botão Flutuante de Agendamento via WhatsApp -->
    <a href="https://wa.me/5514999010120?text=Ol%C3%A1!%20Gostaria%20de%20agendar%20uma%20consultoria%20com%20a%20THF%20Agro." target="_blank" class="whatsapp-float">
        <i class="fa-brands fa-whatsapp"></i> Agendar Atendimento
    </a>

    <!-- Header -->
    <header>
        <a href="#" class="logo-container">
            <img src="logo.png" alt="THF Agro Consultoria" class="logo-img">
        </a>
        <nav>
            <ul>
                <li><a href="#sobre">Quem Somos</a></li>
                <li><a href="#proposito">Propósito</a></li>
                <li><a href="#atuacao">Atuação</a></li>
                <li><a href="#clientes">Clientes</a></li>
                <li><a href="#diferenciais">Diferenciais</a></li>
                <li><a href="#metodologia">Como Trabalhamos</a></li>
                <li><a href="#contato" class="btn-contact">Contato</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h1>THF AGRO <span>CONSULTORIA</span></h1>
            <p class="tagline">Gestão, conformidade e sustentabilidade para o Agronegócio</p>

            <div class="hero-pills">
                <div class="pill"><i class="fa-solid fa-leaf"></i> Meio Ambiente</div>
                <div class="pill"><i class="fa-solid fa-users"></i> Trabalho Rural</div>
                <div class="pill"><i class="fa-solid fa-barcode"></i> Rastreabilidade</div>
                <div class="pill"><i class="fa-solid fa-handshake"></i> Relações Comerciais</div>
            </div>

            <div class="hero-cta">
                <a href="https://wa.me/5514999010120?text=Ol%C3%A1!%20Gostaria%20de%20agendar%20uma%20consultoria%20com%20a%20THF%20Agro." target="_blank" class="btn-schedule">
                    <i class="fa-brands fa-whatsapp"></i> Agendar Consultoria no WhatsApp
                </a>
            </div>
        </div>
    </section>

    <!-- Quem Somos -->
    <section id="sobre">
        <div class="about-grid">
            <div class="about-text">
                <div class="section-header" style="text-align: left; margin-bottom: 30px;">
                    <h2>Quem Somos</h2>
                </div>
                <p>A <strong>THF Agro Consultoria</strong> nasce para apoiar produtores, empresas e organizações do agronegócio na gestão de riscos, conformidade socioambiental e rastreabilidade.</p>
                <p>Conectamos produção, legislação, sustentabilidade e segurança para tornar operações rurais mais seguras, transparentes e preparadas para as exigências do mercado global e nacional.</p>

                <div class="about-highlights">
                    <div class="highlight-card">
                        <h4>Gestão de Riscos</h4>
                        <p style="font-size: 13px; color: var(--text-light);">Mitigação proativa de passivos ambientais e trabalhistas.</p>
                    </div>
                    <div class="highlight-card">
                        <h4>Transparência</h4>
                        <p style="font-size: 13px; color: var(--text-light);">Cadeias produtivas rastreáveis da origem ao consumidor final.</p>
                    </div>
                </div>
            </div>
            <div class="about-image">
                <img src="https://images.unsplash.com/photo-1595974482597-4b8da8879bc5?auto=format&fit=crop&w=800&q=80" alt="THF Agro Consultoria em Atuação">
            </div>
        </div>
    </section>

    <!-- Propósito (MVV) -->
    <section id="proposito" class="mvv-section">
        <div class="section-header">
            <h2>Propósito da Empresa</h2>
            <p>Nossa visão estratégica direcionada para o desenvolvimento do setor rural</p>
        </div>
        <div class="mvv-grid">
            <div class="mvv-card">
                <div class="mvv-icon"><i class="fa-solid fa-bullseye"></i></div>
                <h3>Missão</h3>
                <p>Oferecer soluções de consultoria que promovam conformidade, transparência, sustentabilidade e eficiência nas atividades do Agronegócio, gerando valor de mercado.</p>
            </div>
            <div class="mvv-card">
                <div class="mvv-icon"><i class="fa-solid fa-eye"></i></div>
                <h3>Visão</h3>
                <p>Ser referência em consultoria agroambiental e de conformidade, contribuindo para um agronegócio brasileiro mais responsável, rastreável e competitivo.</p>
            </div>
            <div class="mvv-card">
                <div class="mvv-icon"><i class="fa-solid fa-seedling"></i></div>
                <h3>Valores</h3>
                <p>Integridade nas relações, rigor técnico nas análises, respeito ao produtor rural e compromisso com o desenvolvimento sustentável do campo.</p>
            </div>
        </div>

        <div class="purpose-banner">
            <h3>Propósito Central</h3>
            <p>“Transformar conformidade em valor para o Agronegócio.”</p>
        </div>
    </section>

    <!-- Áreas de Atuação -->
    <section id="atuacao">
        <div class="section-header">
            <h2>Áreas de Atuação</h2>
            <p>Soluções integradas cobrindo os pilares fundamentais do agronegócio moderno</p>
        </div>

        <div class="services-grid">
            <!-- 01 Meio Ambiente -->
            <div class="service-card">
                <div class="service-img">
                    <span class="service-tag">Área 01</span>
                    <img src="https://images.unsplash.com/photo-1500382017468-9049fed747ef?auto=format&fit=crop&w=800&q=80" alt="Meio Ambiente">
                </div>
                <div class="service-content">
                    <h3>Meio Ambiente</h3>
                    <div class="subtitle">Gestão ambiental aplicada à realidade do campo</div>
                    <ul class="service-list">
                        <li><i class="fa-solid fa-check-circle"></i> Controle e monitoramento do uso da terra</li>
                        <li><i class="fa-solid fa-check-circle"></i> Avaliação de reservas legais e áreas protegidas</li>
                        <li><i class="fa-solid fa-check-circle"></i> Prevenção e identificação de riscos de desmatamento</li>
                        <li><i class="fa-solid fa-check-circle"></i> Verificação de conformidade ambiental</li>
                        <li><i class="fa-solid fa-check-circle"></i> Adequação às normas e leis de proteção ambiental</li>
                    </ul>
                </div>
            </div>

            <!-- 02 Trabalho Rural -->
            <div class="service-card">
                <div class="service-img">
                    <span class="service-tag">Área 02</span>
                    <img src="Trabalho Rural.jpg" alt="Trabalho Rural">
                </div>
                <div class="service-content">
                    <h3>Trabalho Rural</h3>
                    <div class="subtitle">Pessoas protegidas. Operações mais seguras</div>
                    <ul class="service-list">
                        <li><i class="fa-solid fa-check-circle"></i> Avaliação das condições de trabalho</li>
                        <li><i class="fa-solid fa-check-circle"></i> Verificação de requisitos de saúde e segurança</li>
                        <li><i class="fa-solid fa-check-circle"></i> Identificação de riscos trabalhistas</li>
                        <li><i class="fa-solid fa-check-circle"></i> Prevenção de condições degradantes</li>
                        <li><i class="fa-solid fa-check-circle"></i> Boas práticas de gestão de pessoas no meio rural</li>
                    </ul>
                </div>
            </div>

            <!-- 03 Rastreabilidade -->
            <div class="service-card">
                <div class="service-img">
                    <span class="service-tag">Área 03</span>
                    <img src="https://images.unsplash.com/photo-1586771107445-d3ca888129ff?auto=format&fit=crop&w=800&q=80" alt="Rastreabilidade">
                </div>
                <div class="service-content">
                    <h3>Rastreabilidade</h3>
                    <div class="subtitle">Da origem ao consumidor final</div>
                    <p style="font-size: 14px; color: var(--text-light);">A THF auxilia na construção de processos capazes de demonstrar a origem, trajetória e conformidade dos produtos ao longo de toda a cadeia produtiva.</p>

                    <div class="traceability-flow">
                        <span class="flow-step">Origem</span>
                        <i class="fa-solid fa-chevron-right flow-arrow"></i>
                        <span class="flow-step">Produção</span>
                        <i class="fa-solid fa-chevron-right flow-arrow"></i>
                        <span class="flow-step">Controle</span>
                        <i class="fa-solid fa-chevron-right flow-arrow"></i>
                        <span class="flow-step">Transporte</span>
                        <i class="fa-solid fa-chevron-right flow-arrow"></i>
                        <span class="flow-step">Consumidor</span>
                    </div>
                </div>
            </div>

            <!-- 04 Relações Comerciais -->
            <div class="service-card">
                <div class="service-img">
                    <span class="service-tag">Área 04</span>
                    <img src="https://images.unsplash.com/photo-1521791136064-7986c2920216?auto=format&fit=crop&w=800&q=80" alt="Relações Comerciais">
                </div>
                <div class="service-content">
                    <h3>Relações Comerciais</h3>
                    <div class="subtitle">Integridade que protege o seu negócio</div>
                    <ul class="service-list">
                        <li><i class="fa-solid fa-check-circle"></i> Prevenção de fraudes</li>
                        <li><i class="fa-solid fa-check-circle"></i> Avaliação de conflitos de interesse</li>
                        <li><i class="fa-solid fa-check-circle"></i> Análise de riscos em relações comerciais</li>
                        <li><i class="fa-solid fa-check-circle"></i> Apoio à integridade em contratos</li>
                        <li><i class="fa-solid fa-check-circle"></i> Avaliação de fornecedores e compras de insumos</li>
                    </ul>
                </div>
            </div>

            <!-- 05 Crédito Rural e Financiamento -->
            <div class="service-card">
                <div class="service-img">
                    <span class="service-tag">Área 05</span>
                    <img src="https://images.unsplash.com/photo-1554224155-8d04cb21cd6c?auto=format&fit=crop&w=800&q=80" alt="Crédito Rural e Financiamento">
                </div>
                <div class="service-content">
                    <h3>Crédito Rural e Financiamento</h3>
                    <div class="subtitle">Captação e estruturação financeira para a sua produção</div>
                    <ul class="service-list">
                        <li><i class="fa-solid fa-check-circle"></i> Elaboração de projetos técnicos para custeio e investimento</li>
                        <li><i class="fa-solid fa-check-circle"></i> Enquadramento em linhas oficiais de crédito (Pronaf, Pronamp, Moderfrota, etc.)</li>
                        <li><i class="fa-solid fa-check-circle"></i> Análise de viabilidade financeira de expansão e modernização</li>
                        <li><i class="fa-solid fa-check-circle"></i> Assessoria no relacionamento com bancos e cooperativas de crédito</li>
                        <li><i class="fa-solid fa-check-circle"></i> Otimização de prazos e taxas adequadas ao ciclo produtivo</li>
                    </ul>
                </div>
            </div>

            <!-- 06 Renegociação de Dívidas Rurais -->
            <div class="service-card">
                <div class="service-img">
                    <span class="service-tag">Área 06</span>
                    <img src="https://images.unsplash.com/photo-1450133064473-71024230f91b?auto=format&fit=crop&w=800&q=80" alt="Renegociação de Dívidas Rurais">
                </div>
                <div class="service-content">
                    <h3>Renegociação de Dívidas Rurais</h3>
                    <div class="subtitle">Reestruturação de débitos e segurança do patrimônio</div>
                    <ul class="service-list">
                        <li><i class="fa-solid fa-check-circle"></i> Diagnóstico e revisão de contratos e débitos agropecuários</li>
                        <li><i class="fa-solid fa-check-circle"></i> Pedidos de prorrogação e alongamento de dívidas rurais (Manual de Crédito Rural)</li>
                        <li><i class="fa-solid fa-check-circle"></i> Intermediação técnica e negociação proativa com credores</li>
                        <li><i class="fa-solid fa-check-circle"></i> Readequação do fluxo de caixa e capacidade real de pagamento</li>
                        <li><i class="fa-solid fa-check-circle"></i> Proteção patrimonial e mitigação de riscos judiciais</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Perfis de Clientes -->
    <section id="clientes">
        <div class="section-header">
            <h2>Perfis de Clientes</h2>
            <p>Atendemos diferentes elos da cadeia produtiva com soluções sob medida</p>
        </div>

        <div class="clients-grid">
            <div class="client-card">
                <div class="client-icon"><i class="fa-solid fa-wheat-awn"></i></div>
                <h3>Produtores Rurais</h3>
                <p>Pequenos, médios e grandes produtores que buscam adequação ambiental, conformidade trabalhista e acesso a mercados mais exigentes.</p>
            </div>
            <div class="client-card">
                <div class="client-icon"><i class="fa-solid fa-industry"></i></div>
                <h3>Agroindústrias e Tradings</h3>
                <p>Empresas que necessitam de rigor no controle de fornecedores, rastreabilidade de matéria-prima e mitigação de riscos reputacionais.</p>
            </div>
            <div class="client-card">
                <div class="client-icon"><i class="fa-solid fa-building-columns"></i></div>
                <h3>Investidores e Instituições Financeiras</h3>
                <p>Organizações que demandam auditorias socioambientais e análise de conformidade legal para concessão de crédito ou investimentos no setor.</p>
            </div>
        </div>
    </section>

    <!-- Diferenciais -->
    <section id="diferenciais" class="differentials-section">
        <div class="section-header">
            <h2>Nossos Diferenciais</h2>
            <p>O que nos torna o parceiro ideal para a transformação sustentável do seu negócio</p>
        </div>

        <div class="differentials-grid">
            <div class="differential-card">
                <div class="differential-icon"><i class="fa-solid fa-microscope"></i></div>
                <h3>Rigor Técnico</h3>
                <p>Metodologias analíticas consolidadas e alinhadas às legislações nacionais e internacionais.</p>
            </div>
            <div class="differential-card">
                <div class="differential-icon"><i class="fa-solid fa-compass-drafting"></i></div>
                <h3>Abordagem Prática</h3>
                <p>Soluções viáveis e adaptadas à rotina real do campo, focadas na aplicabilidade direta.</p>
            </div>
            <div class="differential-card">
                <div class="differential-icon"><i class="fa-solid fa-shield-halved"></i></div>
                <h3>Segurança Jurídica</h3>
                <p>Minimização proativa de passivos, autuações e riscos trabalhistas e socioambientais.</p>
            </div>
            <div class="differential-card">
                <div class="differential-icon"><i class="fa-solid fa-chart-line"></i></div>
                <h3>Geração de Valor</h3>
                <p>Transformamos exigências de conformidade em vantagem competitiva e reputacional no mercado.</p>
            </div>
        </div>
    </section>

    <!-- Como Trabalhamos -->
    <section id="metodologia" class="process-section">
        <div class="section-header">
            <h2>Como Trabalhamos</h2>
            <p>Uma abordagem metodológica clara e orientada para resultados sustentáveis</p>
        </div>

        <div class="timeline">
            <div class="timeline-item">
                <div class="timeline-number">01</div>
                <div class="timeline-content">
                    <h3>Diagnóstico</h3>
                    <p>Entender profundamente a operação do cliente e mapear seus pontos críticos.</p>
                </div>
            </div>
            <div class="timeline-item">
                <div class="timeline-number">02</div>
                <div class="timeline-content">
                    <h3>Avaliação de Riscos</h3>
                    <p>Identificar e mensurar riscos ambientais, sociais e comerciais associados ao negócio.</p>
                </div>
            </div>
            <div class="timeline-item">
                <div class="timeline-number">03</div>
                <div class="timeline-content">
                    <h3>Plano de Ação</h3>
                    <p>Priorizar medidas de correção e melhoria, definindo prazos e responsáveis.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contato">
        <div class="footer-grid">
            <div class="footer-brand">
                <div class="logo-container">
                    <img src="logo.png" alt="THF Agro Consultoria" class="logo-img">
                </div>
                <p>Gestão de riscos, conformidade socioambiental e rastreabilidade para o Agronegócio.</p>
            </div>
            <div class="footer-links">
                <h4>Navegação</h4>
                <ul>
                    <li><a href="#sobre">Quem Somos</a></li>
                    <li><a href="#proposito">Propósito</a></li>
                    <li><a href="#atuacao">Atuação</a></li>
                    <li><a href="#clientes">Clientes</a></li>
                    <li><a href="#diferenciais">Diferenciais</a></li>
                    <li><a href="#metodologia">Como Trabalhamos</a></li>
                </ul>
            </div>
            <div class="footer-contact">
                <h4>Contato</h4>
                <p><i class="fa-solid fa-envelope"></i> THF.Consultoria@gmail.com </p>
                <p><i class="fa-solid fa-phone"></i> 14 99901-0120 </p>
            </div>
        </div>
        <div class="footer-bottom">
            <p>&copy; 2026 THF Agro Consultoria. Todos os direitos reservados.</p>
        </div>
    </footer>

</body>
</html>
