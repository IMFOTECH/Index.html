<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Infotech | Soluciones Digitales Inteligentes</title>
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --dark-blue: #090d1a;
            --brand-blue: #0066ff;
            --brand-gradient: linear-gradient(135deg, #0066ff 0%, #6852ff 100%);
            --text-dark: #1e293b;
            --text-muted: #64748b;
            --bg-light: #f8fafc;
            --white: #ffffff;
            --border-color: #e2e8f0;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            color: var(--text-dark);
            background-color: var(--white);
            line-height: 1.6;
            -webkit-font-smoothing: antialiased;
        }

        /* NAVEGACIÓN COMPACTA Y PROFESIONAL */
        nav {
            background: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            border-bottom: 1px solid var(--border-color);
            padding: 1.2rem 8%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .logo-wrapper {
            display: flex;
            align-items: center;
            gap: 10px;
            font-weight: 800;
            font-size: 1.4rem;
            letter-spacing: -0.5px;
            color: var(--dark-blue);
        }

        .logo-icon {
            width: 32px;
            height: 32px;
            background: var(--brand-gradient);
            border-radius: 8px;
        }

        .nav-links {
            display: flex;
            align-items: center;
            gap: 35px;
            list-style: none;
        }

        .nav-links a {
            color: var(--text-muted);
            text-decoration: none;
            font-weight: 500;
            font-size: 0.95rem;
            transition: color 0.2s ease;
        }

        .nav-links a:hover {
            color: var(--brand-blue);
        }

        .cta-nav {
            background: var(--dark-blue);
            color: var(--white) !important;
            padding: 10px 20px;
            border-radius: 8px;
            font-weight: 600 !important;
            transition: background 0.2s ease !important;
        }

        .cta-nav:hover {
            background: var(--brand-blue);
        }

        /* HERO SECTION CON MAQUETACIÓN LIMPIA */
        .hero-section {
            display: flex;
            align-items: center;
            padding: 8rem 8% 6rem;
            gap: 60px;
            max-width: 1400px;
            margin: 0 auto;
        }

        .hero-text {
            flex: 1.2;
        }

        .tagline {
            display: inline-block;
            background: rgba(0, 102, 255, 0.06);
            color: var(--brand-blue);
            padding: 6px 16px;
            border-radius: 100px;
            font-size: 0.85rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 1.5rem;
        }

        .hero-text h1 {
            font-size: 3.8rem;
            font-weight: 800;
            line-height: 1.15;
            color: var(--dark-blue);
            letter-spacing: -1.5px;
            margin-bottom: 1.5rem;
        }

        .hero-text h1 span {
            background: var(--brand-gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero-text p {
            font-size: 1.2rem;
            color: var(--text-muted);
            margin-bottom: 2.5rem;
            max-width: 580px;
        }

        .hero-visual {
            flex: 1;
            position: relative;
        }

        .hero-image-container {
            width: 100%;
            height: 480px;
            border-radius: 24px;
            background: #e2e8f0;
            overflow: hidden;
            box-shadow: 0 25px 50px -12px rgba(9, 13, 26, 0.08);
        }

        .hero-image-container img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        /* GRID DE SERVICIOS CORPORATIVOS */
        .solutions-section {
            background-color: var(--bg-light);
            padding: 8rem 8%;
        }

        .section-title-wrapper {
            text-align: center;
            max-width: 700px;
            margin: 0 auto 5rem;
        }

        .section-title-wrapper h2 {
            font-size: 2.6rem;
            font-weight: 800;
            letter-spacing: -1px;
            color: var(--dark-blue);
            margin-bottom: 1rem;
        }

        .section-title-wrapper p {
            color: var(--text-muted);
            font-size: 1.1rem;
        }

        .solutions-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .solution-card {
            background: var(--white);
            padding: 3rem 2.5rem;
            border-radius: 16px;
            border: 1px solid var(--border-color);
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .solution-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.03);
            border-color: var(--brand-blue);
        }

        .icon-box {
            width: 48px;
            height: 48px;
            color: var(--brand-blue);
            margin-bottom: 2rem;
        }

        .solution-card h3 {
            font-size: 1.35rem;
            font-weight: 700;
            color: var(--dark-blue);
            margin-bottom: 1rem;
            letter-spacing: -0.3px;
        }

        .solution-card p {
            color: var(--text-muted);
            font-size: 0.98rem;
            line-height: 1.6;
        }

        /* VALORES E IDENTIDAD */
        .identity-section {
            padding: 8rem 8%;
            max-width: 1400px;
            margin: 0 auto;
            display: flex;
            align-items: center;
            gap: 80px;
        }

        .identity-content {
            flex: 1;
        }

        .identity-content h2 {
            font-size: 2.6rem;
            font-weight: 800;
            letter-spacing: -1px;
            color: var(--dark-blue);
            margin-bottom: 1.5rem;
        }

        .identity-content p {
            color: var(--text-muted);
            font-size: 1.1rem;
            margin-bottom: 2.5rem;
        }

        .values-list {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
        }

        .value-card {
            border-left: 3px solid var(--brand-blue);
            padding-left: 20px;
        }

        .value-card h4 {
            font-size: 1.1rem;
            font-weight: 700;
            color: var(--dark-blue);
            margin-bottom: 0.2rem;
        }

        .value-card p {
            font-size: 0.9rem;
            color: var(--text-muted);
            margin: 0;
        }

        .identity-visual {
            flex: 1;
        }

        .identity-image-container {
            width: 100%;
            height: 400px;
            border-radius: 24px;
            background: #e2e8f0;
            overflow: hidden;
        }

        .identity-image-container img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        /* FORMULARIO Y CONTACTO INTEGRADO */
        .contact-section {
            background-color: var(--bg-light);
            padding: 8rem 8%;
            display: flex;
            justify-content: center;
        }

        .contact-container {
            background: var(--white);
            border-radius: 24px;
            border: 1px solid var(--border-color);
            width: 100%;
            max-width: 1100px;
            display: flex;
            overflow: hidden;
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.01);
        }

        .contact-details {
            background: var(--dark-blue);
            color: var(--white);
            padding: 4rem;
            flex: 1;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .contact-details h3 {
            color: var(--white);
            font-size: 2rem;
            font-weight: 700;
            margin-bottom: 1rem;
        }

        .contact-details p {
            color: #94a3b8;
            font-size: 1rem;
        }

        .info-rows {
            margin-top: 3rem;
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .info-row {
            display: flex;
            flex-direction: column;
        }

        .info-row label {
            font-size: 0.8rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            color: #64748b;
            margin-bottom: 4px;
        }

        .info-row span {
            font-size: 1.1rem;
            font-weight: 500;
        }

        .contact-form-wrapper {
            padding: 4rem;
            flex: 1.3;
        }

        .form-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 24px;
        }

        .full-row {
            grid-column: span 2;
        }

        .input-group {
            display: flex;
            flex-direction: column;
            gap: 8px;
        }

        .input-group label {
            font-size: 0.85rem;
            font-weight: 600;
            color: var(--dark-blue);
        }

        .input-group input, .input-group textarea {
            border: 1px solid var(--border-color);
            padding: 14px;
            border-radius: 8px;
            font-family: inherit;
            font-size: 0.95rem;
            background: var(--bg-light);
            transition: all 0.2s ease;
        }

        .input-group input:focus, .input-group textarea:focus {
            outline: none;
            border-color: var(--brand-blue);
            background: var(--white);
            box-shadow: 0 0 0 4px rgba(0, 102, 255, 0.1);
        }

        .submit-button {
            background: var(--brand-blue);
            color: var(--white);
            border: none;
            padding: 16px;
            border-radius: 8px;
            font-weight: 700;
            font-size: 1rem;
            cursor: pointer;
            transition: background 0.2s ease;
        }

        .submit-button:hover {
            background: var(--dark-blue);
        }

        /* FOOTER */
        footer {
            padding: 3rem 8%;
            border-top: 1px solid var(--border-color);
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1400px;
            margin: 0 auto;
            color: var(--text-muted);
            font-size: 0.9rem;
        }

        /* RESPONSIVIDAD INTEGRADA */
        @media (max-width: 1024px) {
            .hero-section, .identity-section { flex-direction: column; text-align: center; }
            .hero-text p { margin-left: auto; margin-right: auto; }
            .hero-visual, .identity-visual { width: 100%; }
            .contact-container { flex-direction: column; }
            .values-list { grid-template-columns: 1fr; text-align: left; }
        }

        @media (max-width: 768px) {
            .hero-text h1 { font-size: 2.8rem; }
            nav { flex-direction: column; gap: 20px; }
            .form-grid { grid-template-columns: 1fr; }
            .full-row { grid-column: span 1; }
        }
    </style>
</head>
<body>

    <nav>
        <div class="logo-wrapper">
            <div class="logo-icon"></div>
            <span>INFOTECH</span>
        </div>
        <ul class="nav-links">
            <li><a href="#inicio">Inicio</a></li>
            <li><a href="#soluciones">Soluciones</a></li>
            <li><a href="#identidad">Nosotros</a></li>
            <li><a href="#contacto" class="cta-nav">Contacto</a></li>
        </ul>
    </nav>

    <section class="hero-section" id="inicio">
        <div class="hero-text">
            <span class="tagline">Soluciones digitales que impulsan tu negocio</span>
            <h1>TECNOLOGÍA que transforma ideas en <span>soluciones inteligentes.</span></h1>
            <p>Diseñamos e implementamos arquitecturas de software robustas y automatizaciones de alta disponibilidad para elevar los estándares operativos de organizaciones exigentes.</p>
        </div>
        <div class="hero-visual">
            <div class="hero-image-container">
                <img src="https://images.unsplash.com/photo-1451187580459-43490279c0fa?q=80&w=1000&auto=format&fit=crop" alt="Infraestructura Tecnológica Avanzada">
            </div>
        </div>
    </section>

    <section class="solutions-section" id="soluciones">
        <div class="section-title-wrapper">
            <h2>Nuestras Soluciones Digitales</h2>
            <p>Ingeniería avanzada alineada de forma precisa con los objetivos estratégicos y comerciales de su organización.</p>
        </div>

        <div class="solutions-grid">
            <div class="solution-card">
                <svg class="icon-box" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19.428 15.428a2 2 0 00-1.022-.547l-2.387-.477a6 6 0 00-3.86.517l-.318.158a6 6 0 01-3.86.517L6.05 15.21a2 2 0 00-1.806.547M8 4h8l-1 1v5.172a2 2 0 00.586 1.414l5 5c1.26 1.26.367 3.414-1.415 3.414H4.828c-1.782 0-2.674-2.154-1.414-3.414l5-5A2 2 0 009 10.172V5L8 4z"/></svg>
                <h3>01. Automatización de Procesos</h3>
                <p>Simplificamos y optimizamos flujos de trabajo complejos, eliminando fricciones operativas para asegurar una mayor eficiencia sistémica.</p>
            </div>

            <div class="solution-card">
                <svg class="icon-box" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4"/></svg>
                <h3>02. Desarrollo Web</h3>
                <p>Construimos plataformas y aplicaciones web modernas, robustas, con altos estándares de velocidad, escalabilidad y seguridad perimetral.</p>
            </div>

            <div class="solution-card">
                <svg class="icon-box" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"/></svg>
                <h3>03. Software a Medida</h3>
                <p>Desarrollamos soluciones personalizadas adaptadas 100% a sus necesidades corporativas, garantizando integraciones estables.</p>
            </div>

            <div class="solution-card">
                <svg class="icon-box" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z"/></svg>
                <h3>04. IA y Chatbots Inteligentes</h3>
                <p>Implementamos soluciones de atención continua y automatización analítica inteligente operadas mediante modelos de IA 24/7.</p>
            </div>
        </div>
    </section>

    <section class="identity-section" id="identidad">
        <div class="identity-content">
            <h2>Nuestra Identidad Corporativa</h2>
            <p>Somos aliados tecnológicos estratégicos para organizaciones enfocadas en el crecimiento sostenible. Desarrollamos soluciones ágiles y robustas para solventar los desafíos técnicos de la era digital.</p>
            
            <div class="values-list">
                <div class="value-card">
                    <h4>Innovación</h4>
                    <p>Evolución continua y herramientas de vanguardia.</p>
                </div>
                <div class="value-card">
                    <h4>Eficiencia</h4>
                    <p>Optimización precisa de recursos y tiempos.</p>
                </div>
                <div class="value-card">
                    <h4>Confianza</h4>
                    <p>Relaciones sólidas basadas en la transparencia.</p>
                </div>
                <div class="value-card">
                    <h4>Resultados</h4>
                    <p>Impacto real medible en su rendimiento.</p>
                </div>
            </div>
        </div>
        <div class="identity-visual">
            <div class="identity-image-container">
                <img src="https://images.unsplash.com/photo-1522071820081-009f0129c71c?q=80&w=1000&auto=format&fit=crop" alt="Equipo Profesional en Consultoría">
            </div>
        </div>
    </section>

    <section class="contact-section" id="contacto">
        <div class="contact-container">
            <div class="contact-details">
                <div>
                    <h3>Hablemos de su próximo proyecto</h3>
                    <p>Consulte con nuestro equipo de ingenieros para recibir un análisis personalizado de sus necesidades de TI.</p>
                </div>
                
                <div class="info-rows">
                    <div class="info-row">
                        <label>Teléfono Comercial</label>
                        <span>+598 099 810 399</span>
                    </div>
                    <div class="info-row">
                        <label>Canal Digital</label>
                        <span>infotechsoftware02@gmail.com</span>
                    </div>
                    <div class="info-row">
                        <label>Ubicación Central</label>
                        <span>Montevideo, Uruguay</span>
                    </div>
                </div>
            </div>
            
            <div class="contact-form-wrapper">
                <form class="form-grid" onsubmit="event.preventDefault(); alert('Solicitud registrada de forma corporativa.');">
                    <div class="input-group">
                        <label for="name">Nombre</label>
                        <input type="text" id="name" placeholder="Ej. Carlos Dini" required>
                    </div>
                    <div class="input-group">
                        <label for="company">Organización</label>
                        <input type="text" id="company" placeholder="Nombre de la empresa">
                    </div>
                    <div class="input-group full-row">
                        <label for="email">Email Corporativo</label>
                        <input type="email" id="email" placeholder="carlos@empresa.com" required>
                    </div>
                    <div class="input-group full-row">
                        <label for="message">Mensaje / Alcance del Proyecto</label>
                        <textarea id="message" rows="4" placeholder="Describa brevemente el requerimiento..." required></textarea>
                    </div>
                    <button type="submit" class="submit-button full-row">Enviar So
