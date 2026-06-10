<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Infotech | Soluciones Digitales Corporativas</title>
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&family=Syncopate:wght@700&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --dark-blue: #090d1a;
            --brand-blue: #0056b3;
            --brand-cyan: #33ccff;
            --brand-gradient: linear-gradient(135deg, #0056b3 0%, #33ccff 100%);
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
            overflow-x: hidden;
        }

        /* NAVEGACIÓN */
        nav {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            border-bottom: 1px solid var(--border-color);
            padding: 1rem 8%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05);
        }

        .brand-container {
            display: flex;
            align-items: center;
            gap: 15px;
            text-decoration: none;
        }

        .brand-logo-svg {
            height: 60px;
            width: 60px;
            filter: drop-shadow(0 4px 6px rgba(51, 204, 255, 0.2));
            transition: transform 0.3s ease;
        }

        .brand-container:hover .brand-logo-svg {
            transform: scale(1.05) rotate(2deg);
        }

        .brand-text-group {
            display: flex;
            flex-direction: column;
            justify-content: center;
            line-height: 1.1;
        }

        .brand-main-text {
            font-family: 'Syncopate', sans-serif;
            font-size: 1.6rem;
            font-weight: 700;
            color: var(--dark-blue);
            letter-spacing: 1px;
        }

        .brand-sub-text {
            font-size: 0.65rem;
            font-weight: 700;
            color: var(--brand-cyan);
            letter-spacing: 2px;
            text-transform: uppercase;
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
            font-weight: 600;
            font-size: 0.95rem;
            transition: color 0.2s ease;
        }

        .nav-links a:hover {
            color: var(--brand-blue);
        }

        .cta-nav {
            background: var(--dark-blue);
            color: var(--white) !important;
            padding: 10px 24px;
            border-radius: 8px;
            font-weight: 700 !important;
            transition: all 0.3s ease !important;
            border: 1px solid transparent;
        }

        .cta-nav:hover {
            background: transparent;
            color: var(--dark-blue) !important;
            border-color: var(--dark-blue);
        }

        /* HERO SECTION */
        .hero-section {
            display: flex;
            align-items: center;
            padding: 7rem 8% 6rem;
            gap: 60px;
            max-width: 1400px;
            margin: 0 auto;
        }

        .hero-text {
            flex: 1.2;
        }

        .tagline {
            display: inline-block;
            background: rgba(51, 204, 255, 0.1);
            color: #0077b6;
            padding: 6px 16px;
            border-radius: 100px;
            font-size: 0.85rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 1.5rem;
        }

        .hero-text h1 {
            font-size: 3.6rem;
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
            font-size: 1.15rem;
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
            height: 500px;
            border-radius: 24px;
            background: #e2e8f0;
            overflow: hidden;
            box-shadow: 0 25px 50px -12px rgba(9, 13, 26, 0.1);
            position: relative;
        }

        .hero-image-container img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .hero-image-container:hover img {
            transform: scale(1.03);
        }

        /* GRID DE SERVICIOS */
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
            position: relative;
            overflow: hidden;
        }

        .solution-card::before {
            content: '';
            position: absolute;
            top: 0; left: 0; width: 100%; height: 4px;
            background: var(--brand-gradient);
            transform: scaleX(0);
            transform-origin: left;
            transition: transform 0.4s ease;
        }

        .solution-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.05);
            border-color: transparent;
        }

        .solution-card:hover::before {
            transform: scaleX(1);
        }

        .icon-box {
            width: 48px;
            height: 48px;
            color: var(--brand-blue);
            margin-bottom: 2rem;
            transition: transform 0.3s ease;
        }

        .solution-card:hover .icon-box {
            transform: scale(1.1);
        }

        .solution-card h3 {
            font-size: 1.35rem;
            font-weight: 700;
            color: var(--dark-blue);
            margin-bottom: 1rem;
        }

        .solution-card p {
            color: var(--text-muted);
            font-size: 0.98rem;
            line-height: 1.6;
        }

        /* METODOLOGÍA DE TRABAJO */
        .process-section {
            padding: 8rem 8%;
            background-color: var(--white);
        }
        
        .process-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 40px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .process-step {
            text-align: center;
            position: relative;
            padding: 2rem;
            background: var(--bg-light);
            border-radius: 16px;
            border: 1px solid var(--border-color);
            transition: transform 0.3s ease;
        }

        .process-step:hover {
            transform: translateY(-5px);
            border-color: var(--brand-cyan);
            box-shadow: 0 10px 20px rgba(0,0,0,0.03);
        }

        .step-number {
            width: 50px;
            height: 50px;
            background: var(--brand-gradient);
            color: var(--white);
            font-size: 1.3rem;
            font-weight: 800;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 1.5rem;
            box-shadow: 0 10px 20px rgba(0, 86, 179, 0.2);
            transform: rotate(-5deg);
        }

        .process-step h4 {
            color: var(--dark-blue);
            font-size: 1.2rem;
            margin-bottom: 1rem;
            font-weight: 700;
        }

        .process-step p {
            color: var(--text-muted);
            font-size: 0.95rem;
            margin: 0;
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
            gap: 25px;
        }

        .value-card {
            border-left: 3px solid var(--brand-cyan);
            padding-left: 20px;
        }

        .value-card h4 {
            font-size: 1.1rem;
            font-weight: 700;
            color: var(--dark-blue);
            margin-bottom: 0.4rem;
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
            box-shadow: 0 15px 35px rgba(0,0,0,0.05);
        }

        .identity-image-container img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .identity-image-container:hover img {
            transform: scale(1.03);
        }

        /* TECNOLOGÍAS */
        .tech-section {
            background-color: var(--white);
            padding: 5rem 8% 8rem;
            text-align: center;
        }

        .tech-section h3 {
            font-size: 1.8rem;
            font-weight: 800;
            color: var(--dark-blue);
            margin-bottom: 3rem;
        }

        .tech-grid {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
            max-width: 900px;
            margin: 0 auto;
        }

        .tech-tag {
            background: var(--bg-light);
            border: 1px solid var(--border-color);
            color: var(--text-dark);
            padding: 10px 24px;
            border-radius: 50px;
            font-weight: 600;
            font-size: 0.9rem;
            transition: all 0.3s ease;
            cursor: default;
        }

        .tech-tag:hover {
            border-color: var(--brand-cyan);
            color: var(--brand-blue);
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(51, 204, 255, 0.15);
            background: var(--white);
        }

        /* FORMULARIO Y CONTACTO */
        .contact-section {
            background-color: var(--dark-blue);
            padding: 8rem 8%;
            display: flex;
            justify-content: center;
        }

        .contact-container {
            background: var(--white);
            border-radius: 24px;
            width: 100%;
            max-width: 1100px;
            display: flex;
            overflow: hidden;
            box-shadow: 0 20px 40px rgba(0,0,0,0.2);
        }

        .contact-details {
            background: #040812;
            color: var(--white);
            padding: 4rem;
            flex: 1;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            position: relative;
            overflow: hidden;
        }
        
        .contact-details::before {
            content: '';
            position: absolute;
            top: -50%; left: -50%; width: 200%; height: 200%;
            background: radial-gradient(circle, rgba(51,204,255,0.05) 0%, rgba(0,0,0,0) 60%);
            z-index: 0;
        }

        .contact-details > * {
            position: relative;
            z-index: 1;
        }

        .contact-details h3 {
            color: var(--white);
            font-size: 2.2rem;
            font-weight: 800;
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
            gap: 30px;
        }

        .info-row {
            display: flex;
            flex-direction: column;
        }

        .info-row label {
            font-size: 0.8rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            color: var(--brand-cyan);
            margin-bottom: 6px;
            font-weight: 700;
        }

        .info-row span {
            font-size: 1.15rem;
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
            font-weight: 700;
            color: var(--dark-blue);
        }

        .input-group input, .input-group textarea {
            border: 1px solid var(--border-color);
            padding: 15px;
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
            box-shadow: 0 0 0 4px rgba(0, 86, 179, 0.1);
        }

        .submit-button {
            background: var(--dark-blue);
            color: var(--white);
            border: none;
            padding: 18px;
            border-radius: 8px;
            font-weight: 700;
            font-size: 1rem;
            cursor: pointer;
            transition: background 0.2s ease;
            margin-top: 10px;
        }

        .submit-button:hover {
            background: var(--brand-blue);
        }

        /* CUSTOM ALERT UI */
        .custom-alert {
            display: none;
            position: fixed;
            bottom: 30px;
            right: 30px;
            background: var(--white);
            color: var(--dark-blue);
            padding: 20px 30px;
            border-radius: 12px;
            box-shadow: 0 15px 30px rgba(0,0,0,0.15);
            z-index: 9999;
            align-items: center;
            gap: 15px;
            border-left: 5px solid var(--brand-cyan);
            font-weight: 600;
        }
        
        .custom-alert.show {
            display: flex;
            animation: slideUp 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275) forwards;
        }

        @keyframes slideUp {
            from { transform: translateY(100px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }

        /* WHATSAPP FLOTANTE */
        .whatsapp-btn {
            position: fixed;
            bottom: 30px;
            left: 30px;
            background-color: #25d366;
            color: white;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            text-decoration: none;
            box-shadow: 0 10px 20px rgba(37, 211, 102, 0.3);
            z-index: 1000;
            transition: all 0.3s ease;
        }

        .whatsapp-btn:hover {
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 15px 25px rgba(37, 211, 102, 0.4);
            background-color: #128C7E;
        }

        .whatsapp-btn svg {
            width: 35px;
            height: 35px;
            fill: currentColor;
        }

        /* CLASES DE ANIMACIÓN AL SCROLLEAR */
        .reveal {
            opacity: 0;
            transform: translateY(40px);
            transition: all 0.8s cubic-bezier(0.5, 0, 0, 1);
        }
        
        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        /* FOOTER */
        footer {
            background: var(--dark-blue);
            padding: 3rem 8%;
            border-top: 1px solid rgba(255,255,255,0.05);
            display: flex;
            justify-content: space-between;
            align-items: center;
            color: #64748b;
            font-size: 0.9rem;
        }

        /* RESPONSIVIDAD */
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
            footer { flex-direction: column; gap: 15px; text-align: center; }
            .contact-details { padding: 3rem 2rem; }
            .contact-form-wrapper { padding: 3rem 2rem; }
            .whatsapp-btn { bottom: 20px; left: 20px; width: 50px; height: 50px; }
            .whatsapp-btn svg { width: 30px; height: 30px; }
        }
    </style>
</head>
<body>

    <nav>
        <a href="#inicio" class="brand-container">
            <svg viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg" class="brand-logo-svg">
                <defs>
                    <linearGradient id="orbBg" x1="0%" y1="0%" x2="100%" y2="100%">
                        <stop offset="0%" stop-color="#060f26"/>
                        <stop offset="100%" stop-color="#0b1e4a"/>
                    </linearGradient>
                    <linearGradient id="orbBorder" x1="0%" y1="0%" x2="100%" y2="100%">
                        <stop offset="0%" stop-color="#33ccff"/>
                        <stop offset="100%" stop-color="#0056b3"/>
                    </linearGradient>
                    <linearGradient id="swooshGrad" x1="0%" y1="0%" x2="100%" y2="100%">
                        <stop offset="0%" stop-color="#ffffff"/>
                        <stop offset="100%" stop-color="#33ccff"/>
                    </linearGradient>
                </defs>
                <circle cx="100" cy="100" r="90" fill="url(#orbBg)" stroke="url(#orbBorder)" stroke-width="5"/>
                <circle cx="100" cy="100" r="78" fill="none" stroke="rgba(51, 204, 255, 0.4)" stroke-width="1.5"/>
                <circle cx="82" cy="65" r="16" fill="url(#swooshGrad)"/>
                <path d="M 77 90 C 50 145, 85 175, 135 150 C 105 135, 95 110, 97 90 Z" fill="url(#swooshGrad)"/>
                <rect x="115" y="52" width="13" height="13" fill="#33ccff" rx="2"/>
                <rect x="135" y="42" width="8" height="8" fill="#ffffff" rx="1"/>
                <rect x="135" y="68" width="11" height="11" fill="#33ccff" rx="2"/>
                <rect x="152" y="60" width="7" height="7" fill="#ffffff" rx="1"/>
                <rect x="120" y="75" width="9" height="9" fill="#0056b3" rx="1"/>
            </svg>
            <div class="brand-text-group">
                <span class="brand-main-text">INFOTECH</span>
                <span class="brand-sub-text">- SOLUCIONES DIGITALES -</span>
            </div>
        </a>
        
        <ul class="nav-links">
            <li><a href="#inicio">Inicio</a></li>
            <li><a href="#soluciones">Servicios</a></li>
            <li><a href="#proceso">Metodología</a></li>
            <li><a href="#identidad">Nosotros</a></li>
            <li><a href="#contacto" class="cta-nav">Contacto Empresarial</a></li>
        </ul>
    </nav>

    <section class="hero-section" id="inicio">
        <div class="hero-text reveal">
            <span class="tagline">Soluciones digitales que impulsan tu negocio</span>
            <h1>TECNOLOGÍA que transforma ideas en <span>soluciones inteligentes.</span></h1>
            <p>Diseñamos e implementamos arquitecturas de software robustas y automatizaciones de alta disponibilidad para elevar los estándares operativos de tu organización.</p>
        </div>
        <div class="hero-visual reveal">
            <div class="hero-image-container">
                <img src="https://images.unsplash.com/photo-1504384308090-c894fdcc538d?q=80&w=1000&auto=format&fit=crop" alt="[attachment_0](attachment)">
            </div>
        </div>
    </section>

    <section class="solutions-section" id="soluciones">
        <div class="section-title-wrapper reveal">
            <h2>NUESTROS SERVICIOS Digitales</h2>
            <p>Ingeniería avanzada alineada de forma precisa con los objetivos estratégicos de tu negocio.</p>
        </div>

        <div class="solutions-grid">
            <div class="solution-card reveal">
                <svg class="icon-box" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19.428 15.428a2 2 0 00-1.022-.547l-2.387-.477a6 6 0 00-3.86.517l-.318.158a6 6 0 01-3.86.517L6.05 15.21a2 2 0 00-1.806.547M8 4h8l-1 1v5.172a2 2 0 00.586 1.414l5 5c1.26 1.26.367 3.414-1.415 3.414H4.828c-1.782 0-2.674-2.154-1.414-3.414l5-5A2 2 0 009 10.172V5L8 4z"/></svg>
                <h3>01. Automatización de Procesos</h3>
                <p>Simplificamos y optimizamos flujos de trabajo complejos, eliminando cuellos de botella para una mayor eficiencia sistémica.</p>
            </div>

            <div class="solution-card reveal">
                <svg class="icon-box" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4"/></svg>
                <h3>02. Desarrollo Web</h3>
                <p>Creamos sitios y aplicaciones web modernas, rápidas, seguras y escalables con los últimos estándares de programación.</p>
            </div>

            <div class="solution-card reveal">
                <svg class="icon-box" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"/></svg>
                <h3>03. Software a Medida</h3>
                <p>Desarrollamos soluciones personalizadas adaptadas 100% a sus necesidades corporativas e integraciones específicas.</p>
            </div>

            <div class="solution-card reveal">
                <svg class="icon-box" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z"/></svg>
                <h3>04. IA y Chatbots</h3>
                <p>Atención 24/7 y automatización analítica inteligente operada mediante modelos avanzados de Inteligencia Artificial.</p>
            </div>
        </div>
    </section>

    <section class="process-section" id="proceso">
        <div class="section-title-wrapper reveal">
            <h2>Nuestra Metodología</h2>
            <p>Un proceso de ingeniería estructurado para garantizar el éxito, la seguridad y la escalabilidad de cada proyecto tecnológico.</p>
        </div>
        
        <div class="process-grid">
            <div class="process-step reveal">
                <div class="step-number">1</div>
                <h4>Consultoría Inicial</h4>
                <p>Auditamos sus necesidades operativas, identificamos cuellos de botella y definimos una hoja de ruta técnica precisa.</p>
            </div>
            <div class="process-step reveal">
                <div class="step-number">2</div>
                <h4>Arquitectura IT</h4>
                <p>Diseñamos la estructura del sistema seleccionando las mejores tecnologías, garantizando escalabilidad a largo plazo.</p>
            </div>
            <div class="process-step reveal">
                <div class="step-number">3</div>
                <h4>Desarrollo Ágil</h4>
                <p>Construimos su solución mediante entregas iterativas, asegurando feedback continuo y control de calidad estricto.</p>
            </div>
            <div class="process-step reveal">
                <div class="step-number">4</div>
                <h4>Despliegue y Soporte</h4>
                <p>Lanzamiento en entornos seguros Cloud con monitoreo 24/7, mantenimiento preventivo y soporte técnico continuo.</p>
            </div>
        </div>
    </section>

    <section class="identity-section" id="identidad">
        <div class="identity-content reveal">
            <h2>Tecnología con Propósito</h2>
            <p>Somos aliados estratégicos para empresas enfocadas en el crecimiento sostenible. Desarrollamos herramientas ágiles y seguras para solventar los desafíos de la era digital.</p>
            
            <div class="values-list">
                <div class="value-card">
                    <h4>Innovación</h4>
                    <p>Evolución continua y herramientas de vanguardia.</p>
                </div>
                <div class="value-card">
                    <h4>Eficiencia</h4>
                    <p>Optimización precisa de recursos y tiempos de ejecución.</p>
                </div>
                <div class="value-card">
                    <h4>Confianza</h4>
                    <p>Relaciones sólidas basadas en la transparencia de datos.</p>
                </div>
                <div class="value-card">
                    <h4>Resultados</h4>
                    <p>Impacto real y medible en su rendimiento comercial.</p>
                </div>
            </div>
        </div>
        <div class="identity-visual reveal">
            <div class="identity-image-container">
                <img src="https://images.unsplash.com/photo-1522071820081-009f0129c71c?q=80&w=1000&auto=format&fit=crop" alt="">
            </div>
        </div>
    </section>

    <section class="tech-section">
        <h3 class="reveal">Stack Tecnológico que Dominamos</h3>
        <div class="tech-grid reveal">
            <div class="tech-tag">HTML5</div>
            <div class="tech-tag">CSS3</div>
            <div class="tech-tag">JavaScript</div>
            <div class="tech-tag">React / Next.js</div>
            <div class="tech-tag">Node.js</div>
            <div class="tech-tag">Python / Django</div>
            <div class="tech-tag">Amazon Web Services (AWS)</div>
            <div class="tech-tag">Docker & Kubernetes</div>
            <div class="tech-tag">TensorFlow (IA)</div>
            <div class="tech-tag">PostgreSQL</div>
            <div class="tech-tag">Ciberseguridad</div>
            <div class="tech-tag">Integración API REST</div>
        </div>
    </section>

    <section class="contact-section" id="contacto">
        <div class="contact-container reveal">
            <div class="contact-details">
                <div>
                    <h3>Hablemos de su proyecto</h3>
                    <p>Consulte con nuestro equipo de ingenieros para recibir un análisis personalizado y potenciar su infraestructura IT.</p>
                </div>
                
                <div class="info-rows">
                    <div class="info-row">
                        <label>Línea Directa</label>
                        <span>+598 099 810 399</span>
                    </div>
                    <div class="info-row">
                        <label>Correo Electrónico</label>
                        <span>infotechsoftware02@gmail.com</span>
                    </div>
                    <div class="info-row">
                        <label>Oficinas</label>
                        <span>Montevideo, Uruguay</span>
                    </div>
                </div>
            </div>
            
            <div class="contact-form-wrapper">
                <form class="form-grid" id="contactForm">
                    <div class="input-group">
                        <label for="name">Nombre / Apellido</label>
                        <input type="text" id="name" required>
                    </div>
                    <div class="input-group">
                        <label for="company">Organización</label>
                        <input type="text" id="company">
                    </div>
                    <div class="input-group full-row">
                        <label for="email">Email Corporativo</label>
                        <input type="email" id="email" required>
                    </div>
                    <div class="input-group full-row">
                        <label for="message">Mensaje / Requerimiento</label>
                        <textarea id="message" rows="4" required></textarea>
                    </div>
                    <button type="submit" class="submit-button full-row">Enviar Solicitud</button>
                </form>
            </div>
        </div>
    </section>

    <footer>
        <p>&copy; 2026 Infotech — Soluciones Digitales. Todos los derechos reservados.</p>
        <p style="font-weight: 600; color: var(--brand-cyan);">www.infotech.digital</p>
    </footer>

    <a href="https://wa.me/598099810399?text=Hola,%20me%20gustaría%20saber%20más%20sobre%20sus%20servicios" class="whatsapp-btn" target="_blank" rel="noopener noreferrer">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
            <path d="M12.031 6.172c-3.181 0-5.767 2.586-5.768 5.766-.001 1.298.38 2.27 1.019 3.287l-.582 2.128 2.182-.573c.978.58 1.911.928 3.145.929 3.178 0 5.767-2.587 5.768-5.766.001-3.187-2.575-5.77-5.764-5.771zm3.392 8.244c-.144.405-.837.774-1.17.824-.299.045-.677.063-1.092-.069-.252-.08-.575-.187-.988-.365-1.739-.751-2.874-2.502-2.961-2.617-.087-.116-.708-.94-.708-1.793s.448-1.273.607-1.446c.159-.173.346-.217.462-.217l.332.006c.106.005.249-.04.39.298.144.347.491 1.2.534 1.287.043.087.072.188.014.304-.058.116-.087.188-.173.289l-.26.304c-.087.086-.177.18-.076.354.101.174.449.741.964 1.201.662.591 1.221.774 1.394.86s.274.072.376-.043c.101-.116.433-.506.549-.68.116-.173.231-.145.39-.087s1.011.477 1.184.564.289.13.332.202c.045.072.045.419-.099.824zm-3.423-14.416c-6.627 0-12 5.373-12 12s5.373 12 12 12 12-5.373 12-12-5.373-12-12-12zm.029 18.88c-1.161 0-2.305-.292-3.318-.844l-3.677.964.984-3.595c-.607-1.052-.927-2.246-.926-3.468.001-3.825 3.113-6.937 6.937-6.937 1.856.001 3.598.723 4.907 2.034 1.31 1.311 2.031 3.054 2.03 4.908-.001 3.825-3.113 6.938-6.937 6.938z"/>
        </svg>
    </a>

    <div class="custom-alert" id="customAlert">
        <svg width="28" height="28" fill="none" stroke="var(--brand-cyan)" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
        <span>Mensaje enviado con éxito. Nos pondremos en contacto a la brevedad.</span>
    </div>

    <script>
        // Lógica de animaciones al hacer scroll
        function revealElements() {
            const reveals = document.querySelectorAll('.reveal');
            
            for (let i = 0; i < reveals.length; i++) {
                const windowHeight = window.innerHeight;
                const elementTop = reveals[i].getBoundingClientRect().top;
                const elementVisible = 100; // Cuántos píxeles antes de aparecer se activa
                
                if (elementTop < windowHeight - elementVisible) {
                    reveals[i].classList.add('active');
                }
            }
        }
        
        window.addEventListener('scroll', revealElements);
        revealElements(); // Para que se ejecute la primera vez al cargar

        // Lógica del formulario de contacto
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const alertBox = document.getElementById('customAlert');
            alertBox.classList.add('show');
            
            setTimeout(() => {
                alertBox.classList.remove('show');
                e.target.reset();
            }, 4000);
        });
    </script>
</body>
</html>
