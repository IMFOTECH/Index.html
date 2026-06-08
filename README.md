
    <!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Infotech | Soluciones Digitales Corporativas</title>
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Outfit:wght@400;600;700&display=swap" rel="stylesheet">
    
    <style>
        /* Paleta de colores Corporativa */
        :root {
            --primary: #0a2540;       /* Azul marino profundo */
            --secondary: #635bff;     /* Azul acento / Tecnológico */
            --text-dark: #1c2a38;     /* Texto principal */
            --text-light: #64748b;    /* Texto secundario */
            --bg-light: #f8fafc;      /* Fondo gris muy claro */
            --white: #ffffff;
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
            font-family: 'Inter', sans-serif;
            color: var(--text-dark);
            background-color: var(--white);
            line-height: 1.7;
        }

        h1, h2, h3, h4 {
            font-family: 'Outfit', sans-serif;
            color: var(--primary);
            font-weight: 700;
        }

        /* BARRA DE NAVEGACIÓN CORPORATIVA */
        nav {
            background: var(--white);
            border-bottom: 1px solid #e2e8f0;
            padding: 1.2rem 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 4px rgba(0,0,0,0.02);
        }

        .logo-area {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .logo-img {
            height: 40px; /* Ajusta según el tamaño de tu logo */
            width: auto;
        }

        .logo-title {
            font-size: 1.6rem;
            letter-spacing: -0.5px;
            color: var(--primary);
        }

        .nav-menu {
            display: flex;
            align-items: center;
            gap: 30px;
            list-style: none;
        }

        .nav-menu a {
            color: var(--text-light);
            text-decoration: none;
            font-weight: 500;
            font-size: 0.95rem;
            transition: color 0.2s ease;
        }

        .nav-menu a:hover {
            color: var(--secondary);
        }

        .btn-nav {
            background: var(--primary);
            color: var(--white) !important;
            padding: 8px 18px;
            border-radius: 6px;
            font-size: 0.9rem !important;
        }

        .btn-nav:hover {
            background: var(--secondary);
        }

        /* SECCIÓN HERO (BIENVENIDA EMPRESARIAL) */
        .hero {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 5rem 5%;
            background: linear-gradient(135deg, #f8fafc 0%, #e2e8f0 100%);
            min-height: 70vh;
            gap: 40px;
        }

        .hero-content {
            flex: 1;
            max-width: 600px;
        }

        .hero-tagline {
            color: var(--secondary);
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1.5px;
            font-size: 0.9rem;
            margin-bottom: 1rem;
        }

        .hero h1 {
            font-size: 3.2rem;
            line-height: 1.2;
            margin-bottom: 1.5rem;
            color: var(--primary);
        }

        .hero p {
            font-size: 1.15rem;
            color: var(--text-light);
            margin-bottom: 2rem;
        }

        .hero-buttons {
            display: flex;
            gap: 15px;
        }

        .btn-primary {
            background: var(--secondary);
            color: var(--white);
            padding: 12px 28px;
            text-decoration: none;
            border-radius: 6px;
            font-weight: 600;
            box-shadow: 0 4px 12px rgba(99, 91, 255, 0.2);
            transition: all 0.2s ease;
        }

        .btn-primary:hover {
            background: var(--primary);
            transform: translateY(-2px);
        }

        .hero-image {
            flex: 1;
            text-align: right;
        }

        .hero-image img {
            max-width: 100%;
            height: auto;
            border-radius: 12px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.06);
        }

        /* SECCIÓN SOBRE NOSOTROS (NUEVA INFO) */
        .about {
            padding: 6rem 5%;
            display: flex;
            align-items: center;
            gap: 60px;
        }

        .about-image {
            flex: 1;
        }

        .about-image img {
            width: 100%;
            border-radius: 12px;
            box-shadow: 0 15px 30px rgba(0,0,0,0.05);
        }

        .about-content {
            flex: 1;
        }

        .about-content h2 {
            font-size: 2.3rem;
            margin-bottom: 1.5rem;
        }

        .about-content p {
            color: var(--text-light);
            margin-bottom: 1.5rem;
        }

        /* SECCIÓN ESTADÍSTICAS (NUEVA INFO) */
        .stats {
            background: var(--primary);
            color: var(--white);
            padding: 4rem 5%;
            display: flex;
            justify-content: space-around;
            text-align: center;
            flex-wrap: wrap;
            gap: 30px;
        }

        .stat-item h3 {
            color: var(--white);
            font-size: 3rem;
            margin-bottom: 0.5rem;
        }

        .stat-item p {
            color: #94a3b8;
            font-size: 1rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* SECCIÓN DE SERVICIOS CORPORATIVOS */
        .services {
            padding: 6rem 5%;
            background-color: var(--bg-light);
            text-align: center;
        }

        .services-intro {
            max-width: 700px;
            margin: 0 auto 4rem;
        }

        .services-intro h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .services-intro p {
            color: var(--text-light);
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 30px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .service-card {
            background: var(--white);
            padding: 2.5rem 2rem;
            border-radius: 8px;
            text-align: left;
            border: 1px solid #e2e8f0;
            transition: all 0.3s ease;
        }

        .service-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 24px rgba(0,0,0,0.04);
            border-color: var(--secondary);
        }

        .service-icon {
            width: 50px;
            height: 50px;
            background: rgba(99, 91, 255, 0.1);
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 1.5rem;
            color: var(--secondary);
            font-weight: bold;
            font-size: 1.2rem;
        }

        .service-card h3 {
            font-size: 1.3rem;
            margin-bottom: 1rem;
        }

        .service-card p {
            color: var(--text-light);
            font-size: 0.95rem;
        }

        /* FORMULARIO DE CONTACTO (NUEVA INFO) */
        .contact-section {
            padding: 6rem 5%;
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
        }

        .contact-section h2 {
            font-size: 2.3rem;
            margin-bottom: 1rem;
        }

        .contact-section p {
            color: var(--text-light);
            margin-bottom: 3rem;
        }

        .contact-form {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            text-align: left;
        }

        .form-group {
            display: flex;
            flex-direction: column;
            gap: 8px;
        }

        .form-group.full-width {
            grid-column: span 2;
        }

        .form-group label {
            font-size: 0.9rem;
            font-weight: 500;
            color: var(--primary);
        }

        .form-group input, .form-group textarea {
            padding: 12px;
            border: 1px solid #cbd5e1;
            border-radius: 6px;
            font-family: inherit;
            font-size: 1rem;
        }

        .form-group input:focus, .form-group textarea:focus {
            outline: none;
            border-color: var(--secondary);
            box-shadow: 0 0 0 3px rgba(99, 91, 255, 0.15);
        }

        .btn-submit {
            grid-column: span 2;
            background: var(--primary);
            color: var(--white);
            padding: 14px;
            border: none;
            border-radius: 6px;
            font-weight: 600;
            font-size: 1rem;
            cursor: pointer;
            transition: background 0.2s;
            margin-top: 10px;
        }

        .btn-submit:hover {
            background: var(--secondary);
        }

        /* PIE DE PÁGINA CORPORATIVO */
        footer {
            background: var(--primary);
            color: #94a3b8;
            padding: 4rem 5% 2rem;
            font-size: 0.95rem;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            max-width: 1200px;
            margin: 0 auto 3rem;
        }

        .footer-col h4 {
            color: var(--white);
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
        }

        .footer-col p {
            margin-bottom: 10px;
        }

        .footer-bottom {
            border-top: 1px solid #1e293b;
            padding-top: 2rem;
            text-align: center;
            max-width: 1200px;
            margin: 0 auto;
        }

        /* RESPONSIVIDAD */
        @media (max-width: 768px) {
            .hero { flex-direction: column; text-align: center; padding-top: 3rem; }
            .hero-image { text-align: center; }
            .about { flex-direction: column-reverse; }
            .contact-form { grid-template-columns: 1fr; }
            .form-group.full-width { grid-column: span 1; }
            .btn-submit { grid-column: span 1; }
        }
    </style>
</head>
<body>

    <nav>
        <div class="logo-area">
            <img src="img/logo-infotech.png" alt="Infotech" class="logo-img" onerror="this.style.display='none'">
            <div class="logo-title"><strong>INFO</strong>TECH</div>
        </div>
        <ul class="nav-menu">
            <li><a href="#inicio">Inicio</a></li>
            <li><a href="#nosotros">Nosotros</a></li>
            <li><a href="#servicios">Servicios</a></li>
            <li><a href="#contacto" class="btn-nav">Contacto</a></li>
        </ul>
    </nav>

    <section class="hero" id="inicio">
        <div class="hero-content">
            <p class="hero-tagline">Soluciones digitales que impulsan tu negocio</p>
            <h1>Tecnología corporativa para transformar tus ideas</h1>
            <p>Ayudamos a empresas e instituciones a optimizar sus operaciones, desarrollar plataformas robustas y adoptar inteligencia artificial con estándares profesionales de nivel internacional.</p>
            <div class="hero-buttons">
                <a href="#contacto" class="btn-primary">Agendar Consultoría</a>
            </div>
        </div>
        <div class="hero-image">
            <img src="img/hero-business.jpg" alt="Transformación Digital Corporativa" placeholder="Imagen de equipo tecnológico de trabajo">
        </div>
    </section>

    <section class="about" id="nosotros">
        <div class="about-image">
            <img src="img/about-team.jpg" alt="Equipo Infotech" placeholder="Imagen del equipo o infraestructura">
        </div>
        <div class="about-content">
            <h2>Quiénes Somos</h2>
            <p>En <strong>Infotech</strong>, nos dedicamos a diseñar e implementar arquitecturas digitales de alto rendimiento. Nuestro compromiso es dotar a las corporaciones con herramientas tecnológicas avanzadas que garanticen la escalabilidad, la seguridad de la información y la automatización inteligente.</p>
            <p>Con sede en Montevideo, Uruguay, brindamos soporte y consultoría especializada a nivel regional, asegurando que cada solución impacte directamente en la rentabilidad y eficiencia de nuestros clientes.</p>
        </div>
    </section>

    <section class="stats">
        <div class="stat-item">
            <h3>99%</h3>
            <p>Disponibilidad de Sistemas</p>
        </div>
        <div class="stat-item">
            <h3>+50</h3>
            <p>Procesos Automatizados</p>
        </div>
        <div class="stat-item">
            <h3>100%</h3>
            <p>A Medida del Cliente</p>
        </div>
        <div class="stat-item">
            <h3>24/7</h3>
            <p>Soporte e Infraestructura</p>
        </div>
    </section>

    <section class="services" id="servicios">
        <div class="services-intro">
            <h2>Nuestras Soluciones Corporativas</h2>
            <p>Desarrollamos ingeniería de software y automatizaciones alineadas a los objetivos estratégicos de su organización.</p>
        </div>

        <div class="services-grid">
            <div class="service-card">
                <div class="service-icon">01</div>
                <h3>Automatización de Procesos</h3>
                <p>Simplificamos y optimizamos flujos de trabajo internos para reducir costes y eliminar fallos operativos mediante integraciones inteligentes.</p>
            </div>

            <div class="service-card">
                <div class="service-icon">02</div>
                <h3>Desarrollo Web Profesional</h3>
                <p>Arquitectura y despliegue de sitios corporativos y aplicaciones web dinámicas: seguras, ultrarrápidas y optimizadas para alta demanda.</p>
            </div>

            <div class="service-card">
                <div class="service-icon">03</div>
                <h3>Software a Medida</h3>
                <p>Diseño de sistemas a la medida exacta de las necesidades de su empresa, garantizando una infraestructura limpia, robusta y con proyección a futuro.</p>
            </div>

            <div class="service-card">
                <div class="service-icon">04</div>
                <h3>IA y Chatbots Inteligentes</h3>
                <p>Implementación de Inteligencia Artificial avanzada para atención al cliente automatizada y análisis de datos en tiempo real las 24 horas del día.</p>
            </div>
        </div>
    </section>

    <section class="contact-section" id="contacto">
        <h2>Hablemos de su Próximo Proyecto</h2>
        <p>Póngase en contacto con nuestro equipo de consultores IT para recibir una propuesta adaptada a su empresa.</p>
        
        <form class="contact-form" action="#" method="POST" onsubmit="event.preventDefault(); alert('Formulario de prueba corporativo');">
            <div class="form-group">
                <label for="nombre">Nombre Completo</label>
                <input type="text" id="nombre" required placeholder="Ej. Juan Pérez">
            </div>
            <div class="form-group">
                <label for="empresa">Empresa</label>
                <input type="text" id="empresa" placeholder="Nombre de su compañía">
            </div>
            <div class="form-group">
                <label for="email">Correo Corporativo</label>
                <input type="email" id="email" required placeholder="juan@empresa.com">
            </div>
            <div class="form-group">
                <label for="telefono">Teléfono de Contacto</label>
                <input type="tel" id="telefono" required placeholder="+598 099...">
            </div>
            <div class="form-group full-width">
                <label for="mensaje">Requerimientos o Mensaje</label>
                <textarea id="mensaje" rows="5" required placeholder="Describa brevemente las necesidades tecnológicas de su organización..."></textarea>
            </div>
            <button type="submit" class="btn-submit">Enviar Solicitud de Información</button>
        </form>
    </section>

    <footer>
        <div class="footer-grid">
            <div class="footer-col">
                <h4>Infotech</h4>
                <p>Soluciones digitales corporativas de alto impacto y rendimiento tecnológico.</p>
            </div>
            <div class="footer-col">
                <h4>Contacto Directo</h4>
                <p><strong>Teléfono:</strong> +598 099 810 399</p>
                <p><strong>Email:</strong> infotechsoftware02@gmail.com</p>
            </div>
            <div class="footer-col">
                <h4>Ubicación</h4>
                <p>Montevideo, Uruguay</p>
                <p><strong>Sitio oficial:</strong> www.infotech.digital</p>
            </div>
        </div>
        <div class="footer-bottom">
            <p>&copy; 2026 Infotech. Todos los derechos reservados. Soluciones Digitales.</p>
        </div>
    </footer>

</body>
</html>
        color: var(--white);
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
        }

        .footer-col p {
            margin-bottom: 10px;
        }

        .footer-bottom {
            border-top: 1px solid #1e293b;
            padding-top: 2rem;
            text-align: center;
            max-width: 1200px;
            margin: 0 auto;
        }

        /* RESPONSIVIDAD */
        @media (max-width: 768px) {
            .hero { flex-direction: column; text-align: center; padding-top: 3rem; }
            .hero-image { text-align: center; }
            .about { flex-direction: column-reverse; }
            .contact-form { grid-template-columns: 1fr; }
            .form-group.full-width { grid-column: span 1; }
            .btn-submit { grid-column: span 1; }
        }
    </style>
</head>
<body>

    <nav>
        <div class="logo-area">
            <img src="img/logo-infotech.png" alt="Infotech" class="logo-img" onerror="this.style.display='none'">
            <div class="logo-title"><strong>INFO</strong>TECH</div>
        </div>
        <ul class="nav-menu">
            <li><a href="#inicio">Inicio</a></li>
            <li><a href="#nosotros">Nosotros</a></li>
            <li><a href="#servicios">Servicios</a></li>
            <li><a href="#contacto" class="btn-nav">Contacto</a></li>
        </ul>
    </nav>

    <section class="hero" id="inicio">
        <div class="hero-content">
            <p class="hero-tagline">Soluciones digitales que impulsan tu negocio</p>
            <h1>Tecnología corporativa para transformar tus ideas</h1>
            <p>Ayudamos a empresas e instituciones a optimizar sus operaciones, desarrollar plataformas robustas y adoptar inteligencia artificial con estándares profesionales de nivel internacional.</p>
            <div class="hero-buttons">
                <a href="#contacto" class="btn-primary">Agendar Consultoría</a>
            </div>
        </div>
        <div class="hero-image">
            <img src="img/hero-business.jpg" alt="Transformación Digital Corporativa" placeholder="Imagen de equipo tecnológico de trabajo">
        </div>
    </section>

    <section class="about" id="nosotros">
        <div class="about-image">
            <img src="img/about-team.jpg" alt="Equipo Infotech" placeholder="Imagen del equipo o infraestructura">
        </div>
        <div class="about-content">
            <h2>Quiénes Somos</h2>
            <p>En <strong>Infotech</strong>, nos dedicamos a diseñar e implementar arquitecturas digitales de alto rendimiento. Nuestro compromiso es dotar a las corporaciones con herramientas tecnológicas avanzadas que garanticen la escalabilidad, la seguridad de la información y la automatización inteligente.</p>
            <p>Con sede en Montevideo, Uruguay, brindamos soporte y consultoría especializada a nivel regional, asegurando que cada solución impacte directamente en la rentabilidad y eficiencia de nuestros clientes.</p>
        </div>
    </section>

    <section class="stats">
        <div class="stat-item">
            <h3>99%</h3>
            <p>Disponibilidad de Sistemas</p>
        </div>
        <div class="stat-item">
            <h3>+50</h3>
            <p>Procesos Automatizados</p>
        </div>
        <div class="stat-item">
            <h3>100%</h3>
            <p>A Medida del Cliente</p>
        </div>
        <div class="stat-item">
            <h3>24/7</h3>
            <p>Soporte e Infraestructura</p>
        </div>
    </section>

    <section class="services" id="servicios">
        <div class="services-intro">
            <h2>Nuestras Soluciones Corporativas</h2>
            <p>Desarrollamos ingeniería de software y automatizaciones alineadas a los objetivos estratégicos de su organización.</p>
        </div>

        <div class="services-grid">
            <div class="service-card">
                <div class="service-icon">01</div>
                <h3>Automatización de Procesos</h3>
                <p>Simplificamos y optimizamos flujos de trabajo internos para reducir costes y eliminar fallos operativos mediante integraciones inteligentes.</p>
            </div>

            <div class="service-card">
                <div class="service-icon">02</div>
                <h3>Desarrollo Web Profesional</h3>
                <p>Arquitectura y despliegue de sitios corporativos y aplicaciones web dinámicas: seguras, ultrarrápidas y optimizadas para alta demanda.</p>
            </div>

            <div class="service-card">
                <div class="service-icon">03</div>
                <h3>Software a Medida</h3>
                <p>Diseño de sistemas a la medida exacta de las necesidades de su empresa, garantizando una infraestructura limpia, robusta y con proyección a futuro.</p>
            </div>

            <div class="service-card">
                <div class="service-icon">04</div>
                <h3>IA y Chatbots Inteligentes</h3>
                <p>Implementación de Inteligencia Artificial avanzada para atención al cliente automatizada y análisis de datos en tiempo real las 24 horas del día.</p>
            </div>
        </div>
    </section>

    <section class="contact-section" id="contacto">
        <h2>Hablemos de su Próximo Proyecto</h2>
        <p>Póngase en contacto con nuestro equipo de consultores IT para recibir una propuesta adaptada a su empresa.</p>
        
        <form class="contact-form" action="#" method="POST" onsubmit="event.preventDefault(); alert('Formulario de prueba corporativo');">
            <div class="form-group">
                <label for="nombre">Nombre Completo</label>
                <input type="text" id="nombre" required placeholder="Ej. Juan Pérez">
            </div>
            <div class="form-group">
                <label for="empresa">Empresa</label>
                <input type="text" id="empresa" placeholder="Nombre de su compañía">
            </div>
            <div class="form-group">
                <label for="email">Correo Corporativo</label>
                <input type="email" id="email" required placeholder="juan@empresa.com">
            </div>
            <div class="form-group">
                <label for="telefono">Teléfono de Contacto</label>
                <input type="tel" id="telefono" required placeholder="+598 099...">
            </div>
            <div class="form-group full-width">
                <label for="mensaje">Requerimientos o Mensaje</label>
                <textarea id="mensaje" rows="5" required placeholder="Describa brevemente las necesidades tecnológicas de su organización..."></textarea>
            </div>
            <button type="submit" class="btn-submit">Enviar Solicitud de Información</button>
        </form>
    </section>

    <footer>
        <div class="footer-grid">
            <div class="footer-col">
                <h4>Infotech</h4>
                <p>Soluciones digitales corporativas de alto impacto y rendimiento tecnológico.</p>
            </div>
            <div class="footer-col">
                <h4>Contacto Directo</h4>
                <p><strong>Teléfono:</strong> +598 099 810 399</p>
                <p><strong>Email:</strong> infotechsoftware02@gmail.com</p>
            </div>
            <div class="footer-col">
                <h4>Ubicación</h4>
                <p>Montevideo, Uruguay</p>
                <p><strong>Sitio oficial:</strong> www.infotech.digital</p>
            </div>
        </div>
        <div class="footer-bottom">
            <p>&copy; 2026 Infotech. Todos los derechos reservados. Soluciones Digitales.</p>
        </div>
    </footer>

</body>
</html>

        .copyright {
            text-align: center;
            color: #475569;
            font-size: 0.85rem;
        }

        /* RESPONSIVIDAD */
        @media (max-width: 768px) {
            .hero h2 { font-size: 2.3rem; }
            nav { flex-direction: column; gap: 15px; }
            .nav-links { gap: 15px; }
        }
    </style>
</head>
<body>

    <nav>
        <div class="logo-container">
            <div class="logo-text">INFOTECH</div>
        </div>
        <div class="nav-links">
            <a href="#inicio">Inicio</a>
            <a href="#servicios">Servicios</a>
            <a href="#contacto">Contacto</a>
        </div>
    </nav>

    <section class="hero" id="inicio">
        <p class="hero-slogan-top">Soluciones digitales que impulsan tu negocio</p>
        <h2>TECNOLOGÍA que transforma ideas en <span>soluciones inteligentes.</span></h2>
        <p class="hero-description">Llevamos tu infraestructura corporativa al siguiente nivel implementando las herramientas digitales más potentes y modernas del mercado.</p>
        <a href="#contacto" class="btn-cyber">INICIAR PROYECTO</a>
    </section>

    <section class="values-section">
        <div class="values-container">
            <div class="value-badge">Innovación</div>
            <div class="value-badge">Eficiencia</div>
            <div class="value-badge">Confianza</div>
            <div class="value-badge">Resultados</div>
        </div>
    </section>

    <section class="services-section" id="servicios">
        <div class="section-header">
            <h2>NUESTROS SERVICIOS DIGITALES</h2>
            <p>Estrategias avanzadas a la medida de tu empresa</p>
        </div>

        <div class="services-grid">
            <div class="service-card card-purple">
                <div class="service-number">01</div>
                <h3>AUTOMATIZACIÓN DE PROCESOS</h3>
                <p>Simplificamos y optimizamos flujos de trabajo complejos para alcanzar la máxima eficiencia operativa en tu negocio.</p>
            </div>

            <div class="service-card card-blue">
                <div class="service-number">02</div>
                <h3>DESARROLLO WEB</h3>
                <p>Diseño y arquitectura de sitios y aplicaciones web robustas: modernas, ultrarrápidas, blindadas y totalmente escalables.</p>
            </div>

            <div class="service-card card-purple">
                <div class="service-number">03</div>
                <h3>SOFTWARE A MEDIDA</h3>
                <p>Ingeniería de software adaptada al 100% a tus necesidades específicas. Soluciones digitales únicas para problemas reales.</p>
            </div>

            <div class="service-card card-gold">
                <div class="service-number">04</div>
                <h3>IA Y CHATBOTS INTELIGENTES</h3>
                <p>Automatización avanzada con Inteligencia Artificial. Sistemas de soporte y atención al cliente disponibles 24/7 de forma autónoma.</p>
            </div>
        </div>
    </section>

    <footer id="contacto">
        <div class="footer-grid">
            <div class="footer-info">
                <h4>Teléfono móvil</h4>
                <p>+598 099 810 399</p>
            </div>
            <div class="footer-info">
                <h4>Correo electrónico</h4>
                <p>infotechsoftware02@gmail.com</p>
            </div>
            <div class="footer-info">
                <h4>Sitio Web</h4>
                <p style="color: var(--neon-blue);">www.infotech.digital</p>
            </div>
            <div class="footer-info">
                <h4>Casa Central</h4>
                <p>Montevideo, Uruguay</p>
            </div>
        </div>
        <p class="copyright">&copy; 2026 Infotech - Soluciones Digitales. Todos los derechos reservados.</p>
    </footer>

</body>
</html>
