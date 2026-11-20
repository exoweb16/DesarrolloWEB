# DesarrolloWEB
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Marco Aldair Galicia Montaño | Diseño y Desarrollo Web</title>
    <style>
        /* Estilos Generales */
        :root {
            --primary: #2563eb;
            --primary-dark: #1d4ed8;
            --dark-bg: #0f172a;
            --card-bg: #1e293b;
            --text-light: #f8fafc;
            --text-muted: #94a3b8;
            --whatsapp: #22c55e;
            --whatsapp-dark: #16a34a;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--dark-bg);
            color: var(--text-light);
            line-height: 1.6;
        }

        /* Navegación */
        header {
            background-color: rgba(15, 23, 42, 0.95);
            backdrop-filter: blur(10px);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 1rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.3rem;
            font-weight: 700;
            color: var(--text-light);
            text-decoration: none;
            letter-spacing: 0.5px;
        }

        .logo span {
            color: var(--primary);
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            color: var(--text-muted);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--text-light);
        }

        /* Sección Principal (Hero) */
        .hero {
            padding: 8rem 2rem 5rem;
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
            min-height: 90vh;
        }

        .hero-content h1 {
            font-size: 3rem;
            line-height: 1.2;
            margin-bottom: 1.5rem;
        }

        .hero-content h1 span {
            color: var(--primary);
        }

        .hero-content p {
            color: var(--text-muted);
            font-size: 1.15rem;
            margin-bottom: 2rem;
        }

        .btn-group {
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
        }

        .btn {
            padding: 0.9rem 1.8rem;
            border-radius: 8px;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            cursor: pointer;
            border: none;
            font-size: 1rem;
        }

        .btn-primary {
            background-color: var(--primary);
            color: white;
        }

        .btn-primary:hover {
            background-color: var(--primary-dark);
            transform: translateY(-2px);
        }

        .btn-whatsapp {
            background-color: var(--whatsapp);
            color: white;
        }

        .btn-whatsapp:hover {
            background-color: var(--whatsapp-dark);
            transform: translateY(-2px);
        }

        .hero-image img {
            width: 100%;
            border-radius: 16px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.5);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        /* Secciones Generales */
        section {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            margin-bottom: 3.5rem;
        }

        .section-title h2 {
            font-size: 2.3rem;
            margin-bottom: 0.5rem;
        }

        .section-title p {
            color: var(--text-muted);
        }

        /* Tarjetas de Servicios */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .card {
            background-color: var(--card-bg);
            border-radius: 12px;
            overflow: hidden;
            border: 1px solid rgba(255, 255, 255, 0.08);
            transition: transform 0.3s;
        }

        .card:hover {
            transform: translateY(-8px);
        }

        .card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .card-body {
            padding: 1.5rem;
        }

        .card-body h3 {
            font-size: 1.3rem;
            margin-bottom: 0.8rem;
            color: var(--text-light);
        }

        .card-body p {
            color: var(--text-muted);
            font-size: 0.95rem;
        }

        /* Sobre Mí */
        .about-container {
            background-color: var(--card-bg);
            border-radius: 16px;
            padding: 3rem;
            display: grid;
            grid-template-columns: 1fr 1.2fr;
            gap: 3rem;
            align-items: center;
            border: 1px solid rgba(255, 255, 255, 0.08);
        }

        .about-container img {
            width: 100%;
            border-radius: 12px;
            object-fit: cover;
        }

        .about-text h2 {
            font-size: 2rem;
            margin-bottom: 1rem;
        }

        .about-text p {
            color: var(--text-muted);
            margin-bottom: 1.5rem;
        }

        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 0.6rem;
        }

        .skill-tag {
            background-color: rgba(37, 99, 235, 0.2);
            color: #60a5fa;
            padding: 0.4rem 0.9rem;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: 600;
        }

        /* Contacto */
        .contact-box {
            background: linear-gradient(135deg, #1e293b 0%, #0f172a 100%);
            border: 1px solid rgba(37, 99, 235, 0.4);
            border-radius: 16px;
            padding: 3.5rem 2rem;
            text-align: center;
        }

        .contact-box h2 {
            font-size: 2.2rem;
            margin-bottom: 1rem;
        }

        .contact-box p {
            color: var(--text-muted);
            max-width: 600px;
            margin: 0 auto 2rem;
        }

        .phone-highlight {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 2rem;
            display: block;
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: var(--text-muted);
            font-size: 0.9rem;
        }

        /* Botón Flotante WhatsApp */
        .whatsapp-float {
            position: fixed;
            bottom: 25px;
            right: 25px;
            background-color: var(--whatsapp);
            color: white;
            padding: 14px 20px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 700;
            box-shadow: 0 10px 25px rgba(34, 197, 94, 0.4);
            z-index: 1000;
            transition: transform 0.3s;
        }

        .whatsapp-float:hover {
            transform: scale(1.05);
        }

        /* Responsivo para celulares */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            .hero, .about-container {
                grid-template-columns: 1fr;
                text-align: center;
            }
            .hero-content h1 {
                font-size: 2.2rem;
            }
            .btn-group, .skills {
                justify-content: center;
            }
        }
    </style>
</head>
<body>

    <!-- Barra de Navegación -->
    <header>
        <div class="nav-container">
            <a href="#" class="logo">Marco<span>Dev</span></a>
            <ul class="nav-links">
                <li><a href="#inicio">Inicio</a></li>
                <li><a href="#servicios">Servicios</a></li>
                <li><a href="#sobre-mi">Sobre Mí</a></li>
                <li><a href="#contacto">Contacto</a></li>
            </ul>
        </div>
    </header>

    <!-- Sección Principal -->
    <section id="inicio" class="hero">
        <div class="hero-content">
            <h1>Diseño y Desarrollo Web de <span>Alto Impacto</span></h1>
            <p>Hola, soy <strong>Marco Aldair Galicia Montaño</strong>. Creo sitios web modernos, rápidos y adaptados a cualquier dispositivo para impulsar tu negocio o marca personal en internet.</p>
            <div class="btn-group">
                <a href="https://wa.me/528445870614?text=Hola%20Marco,%20me%20interesa%20cotizar%20una%20p%C3%A1gina%20web" target="_blank" class="btn btn-whatsapp">
                    Contactar por WhatsApp
                </a>
                <a href="#servicios" class="btn btn-primary">Ver Servicios</a>
            </div>
        </div>
        <div class="hero-image">
            <img src="https://images.unsplash.com/photo-1498050108023-c5249f4df085?auto=format&fit=crop&w=900&q=80" alt="Espacio de trabajo de desarrollo web">
        </div>
    </section>

    <!-- Sección de Servicios -->
    <section id="servicios">
        <div class="section-title">
            <h2>Servicios de Desarrollo Web</h2>
            <p>Soluciones digitales a la medida de tus objetivos</p>
        </div>

        <div class="services-grid">
            <!-- Servicio 1 -->
            <div class="card">
                <img src="https://images.unsplash.com/photo-1547658719-da2b51169166?auto=format&fit=crop&w=800&q=80" alt="Diseño Web Responsivo">
                <div class="card-body">
                    <h3>Diseño Web Moderno</h3>
                    <p>Interfaces atractivas, limpias y 100% responsivas que se ven perfectas en celulares, tabletas y computadoras.</p>
                </div>
            </div>

            <!-- Servicio 2 -->
            <div class="card">
                <img src="https://images.unsplash.com/photo-1555066931-4365d14bab8c?auto=format&fit=crop&w=800&q=80" alt="Programación Frontend y Backend">
                <div class="card-body">
                    <h3>Desarrollo a la Medida</h3>
                    <p>Programación estructurada con código limpio, rápido y optimizado para ofrecer la mejor experiencia a tus usuarios.</p>
                </div>
            </div>

            <!-- Servicio 3 -->
            <div class="card">
                <img src="https://images.unsplash.com/photo-1460925895917-afdab827c52f?auto=format&fit=crop&w=800&q=80" alt="Landing Pages y Tiendas Online">
                <div class="card-body">
                    <h3>Landing Pages y Negocios</h3>
                    <p>Páginas enfocadas en convertir visitantes en clientes reales, con integración directa a tus redes y WhatsApp.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección Sobre Mí -->
    <section id="sobre-mi">
        <div class="about-container">
            <img src="https://images.unsplash.com/photo-1517694712202-14dd9538aa97?auto=format&fit=crop&w=800&q=80" alt="Código de programación en pantalla">
            <div class="about-text">
                <h2>Sobre el Desarrollador</h2>
                <p>Soy <strong>Marco Aldair Galicia Montaño</strong>, desarrollador web enfocado en transformar ideas en plataformas funcionales y profesionales. Me encargo de cada detalle técnico y visual para que tu presencia digital destaque frente a la competencia.</p>
                <div class="skills">
                    <span class="skill-tag">HTML5</span>
                    <span class="skill-tag">CSS3</span>
                    <span class="skill-tag">JavaScript</span>
                    <span class="skill-tag">Diseño Responsivo</span>
                    <span class="skill-tag">Optimización Web</span>
                    <span class="skill-tag">UI / UX</span>
                </div>
            </div>
        </div>
    </section>

    <!-- Sección de Contacto -->
    <section id="contacto">
        <div class="contact-box">
            <h2>¿Listo para iniciar tu proyecto web?</h2>
            <p>Contáctame directamente para platicar sobre tu idea y enviarte una cotización sin compromiso.</p>
            <span class="phone-highlight">Tel / WhatsApp: 844 587 0614</span>
            <div class="btn-group" style="justify-content: center;">
                <a href="https://wa.me/528445870614?text=Hola%20Marco,%20quisiera%20informaci%C3%B3n%20sobre%20el%20dise%C3%B1o%20de%20una%20p%C3%A1gina%20web" target="_blank" class="btn btn-whatsapp">
                    Enviar Mensaje por WhatsApp
                </a>
                <a href="tel:8445870614" class="btn btn-primary">
                    Llamar Ahora
                </a>
            </div>
        </div>
    </section>

    <!-- Pie de Página -->
    <footer>
        <p>&copy; <span id="year"></span> Marco Aldair Galicia Montaño - Todos los derechos reservados.</p>
    </footer>

    <!-- Botón Flotante -->
    <a href="https://wa.me/528445870614?text=Hola%20Marco,%20me%20interesa%20una%20p%C3%A1gina%20web" target="_blank" class="whatsapp-float">
        WhatsApp: 844 587 0614
    </a>

    <script>
        // Actualiza el año automáticamente en el pie de página
        document.getElementById('year').textContent = new Date().getFullYear();
    </script>
</body>
</html>
