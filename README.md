# AIDoc-website<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AiDoc Salud | Inteligencia Artificial para Historias Clínicas Laborales</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&family=Open+Sans:wght@400;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #004D40; /* Verde oscuro, profesional y asociado a salud/crecimiento */
            --secondary-color: #4CAF50; /* Verde más claro para acentos */
            --accent-color: #FFC107; /* Amarillo para destacar CTA o iconos */
            --text-dark: #212121;
            --text-light: #f4f4f4;
            --bg-light: #f8f8f8;
            --bg-dark: #333333;
            --border-color: #e0e0e0;
        }

        body {
            font-family: 'Open Sans', sans-serif;
            margin: 0;
            padding: 0;
            line-height: 1.6;
            color: var(--text-dark);
            background-color: var(--bg-light);
        }

        h1, h2, h3 {
            font-family: 'Montserrat', sans-serif;
            color: var(--text-dark);
            line-height: 1.2;
        }

        h1 { font-size: 3.2em; font-weight: 700; }
        h2 { font-size: 2.5em; font-weight: 600; }
        h3 { font-size: 1.8em; font-weight: 600; }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Header */
        header {
            background-color: var(--primary-color);
            color: var(--text-light);
            padding: 15px 0;
            text-align: center;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        header .logo {
            font-family: 'Montserrat', sans-serif;
            font-size: 1.8em;
            font-weight: 700;
            color: var(--text-light);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, var(--primary-color) 0%, #00796B 100%);
            color: var(--text-light);
            padding: 100px 20px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        .hero::before { /* Para un efecto visual sutil */
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" opacity="0.1"><circle cx="25" cy="25" r="15" fill="white"/><circle cx="75" cy="75" r="15" fill="white"/><circle cx="50" cy="10" r="10" fill="white"/></svg>') no-repeat center center / cover;
            opacity: 0.1;
            animation: moveBackground 30s linear infinite;
        }
        @keyframes moveBackground {
            from { background-position: 0% 0%; }
            to { background-position: 100% 100%; }
        }
        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 900px;
            margin: 0 auto;
        }
        .hero h1 {
            color: var(--text-light);
            margin-bottom: 20px;
        }
        .hero p {
            font-size: 1.3em;
            margin-bottom: 40px;
            font-weight: 500;
        }
        .cta-button {
            display: inline-block;
            background-color: var(--accent-color);
            color: var(--text-dark);
            padding: 15px 30px;
            font-size: 1.1em;
            font-weight: 700;
            border-radius: 50px;
            text-decoration: none;
            transition: background-color 0.3s ease, transform 0.3s ease;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
        }
        .cta-button:hover {
            background-color: #FFD54F;
            transform: translateY(-3px);
        }

        /* Features/How it works section */
        .section-title {
            text-align: center;
            margin-bottom: 60px;
            position: relative;
        }
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background-color: var(--secondary-color);
            border-radius: 2px;
        }
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
            margin-top: 50px;
        }
        .feature-item {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.08);
            text-align: center;
            transition: transform 0.3s ease;
        }
        .feature-item:hover {
            transform: translateY(-10px);
        }
        .feature-item h3 {
            color: var(--primary-color);
            margin-bottom: 15px;
        }
        .feature-item p {
            font-size: 1em;
            color: var(--text-dark);
        }
        .feature-item .icon {
            font-size: 3em;
            color: var(--secondary-color);
            margin-bottom: 20px;
        }

        /* Benefits section */
        .benefits-section {
            padding: 80px 0;
            background-color: var(--bg-light);
        }
        .benefits-list {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 30px;
        }
        .benefit-card {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            width: calc(33% - 20px); /* Para 3 columnas */
            min-width: 280px;
            display: flex;
            align-items: flex-start;
        }
        .benefit-card .icon {
            font-size: 2em;
            color: var(--secondary-color);
            margin-right: 20px;
            flex-shrink: 0;
        }
        .benefit-card h3 {
            color: var(--primary-color);
            margin-top: 0;
            margin-bottom: 10px;
        }

        /* Target Audience section */
        .target-section {
            background-color: var(--primary-color);
            color: var(--text-light);
            padding: 80px 0;
            text-align: center;
        }
        .target-section h2 {
            color: var(--text-light);
        }
        .target-section ul {
            list-style: none;
            padding: 0;
            margin-top: 40px;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
        }
        .target-section ul li {
            background-color: rgba(255,255,255,0.1);
            padding: 15px 25px;
            border-radius: 5px;
            font-size: 1.1em;
            font-weight: 500;
            border: 1px solid rgba(255,255,255,0.2);
        }

        /* Testimonials (Placeholder) */
        .testimonials-section {
            padding: 80px 0;
            background-color: var(--bg-light);
            text-align: center;
        }
        .testimonial-card {
            background-color: white;
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.08);
            max-width: 700px;
            margin: 0 auto;
            font-style: italic;
            font-size: 1.1em;
            position: relative;
        }
        .testimonial-card::before {
            content: "“";
            font-size: 5em;
            color: var(--border-color);
            position: absolute;
            top: 10px;
            left: 20px;
            line-height: 1;
        }
        .testimonial-card p {
            margin-bottom: 20px;
        }
        .testimonial-card .author {
            font-style: normal;
            font-weight: 600;
            color: var(--primary-color);
        }

        /* Contact Section */
        .contact-section {
            background-color: var(--bg-dark);
            color: var(--text-light);
            padding: 80px 0;
            text-align: center;
        }
        .contact-section h2 {
            color: var(--text-light);
        }
        .contact-form-container {
            max-width: 600px;
            margin: 0 auto;
            background-color: white;
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.1);
            text-align: left;
        }
        .contact-form-container label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: var(--text-dark);
        }
        .contact-form-container input[type="text"],
        .contact-form-container input[type="email"],
        .contact-form-container input[type="tel"] {
            width: 100%;
            padding: 12px;
            margin-bottom: 20px;
            border: 1px solid var(--border-color);
            border-radius: 5px;
            font-size: 1em;
            font-family: 'Open Sans', sans-serif;
            box-sizing: border-box;
        }
        .contact-form-container .submit-button {
            display: block;
            width: 100%;
            background-color: var(--accent-color);
            color: var(--text-dark);
            padding: 15px;
            font-size: 1.1em;
            font-weight: 700;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        .contact-form-container .submit-button:hover {
            background-color: #FFD54F;
        }
        
        /* Footer */
        footer {
            background-color: var(--text-dark);
            color: var(--text-light);
            padding: 30px 0;
            text-align: center;
            font-size: 0.9em;
        }
        footer a {
            color: var(--secondary-color);
            text-decoration: none;
        }
        footer a:hover {
            text-decoration: underline;
        }

        /* Responsive adjustments */
        @media (max-width: 768px) {
            h1 { font-size: 2.5em; }
            h2 { font-size: 2em; }
            .hero { padding: 80px 20px; }
            .features-grid, .benefits-list, .tech-security-content {
                grid-template-columns: 1fr;
                flex-direction: column;
                align-items: center;
            }
            .benefit-card, .tech-item {
                width: 90%;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>

    <header>
        <div class="container">
            <span class="logo">AiDoc Salud</span>
        </div>
    </header>

    <section class="hero">
        <div class="hero-content">
            <h1>Gestiona tus dictámenes de calificación de invalidez con ayuda de Inteligencia Artificial, de forma ágil, rápida y segura.</h1>
            <p>Los profesionales de salud gastan menos de la mitad del tiempo haciendo sus dictámenes de calificación con AiDoc Salud. Obtén rapidez en el análisis de documentos de múltiples páginas.</p>
            <a href="#contact" class="cta-button">Solicitar Demo Gratuita</a>
        </div>
    </section>

    <section class="container benefits-section">
        <h2 class="section-title">¿Cómo funciona AiDoc Salud?</h2>
        <div class="features-grid">
            <div class="feature-item">
                <div class="icon"><i class="fas fa-file-upload"></i></div>
                <h3>1. Sube tus Documentos</h3>
                <p>Carga fácilmente cualquier tipo de documento de Historia Clínica: notas SOAP, informes de laboratorio, imágenes con texto, PDFs y documentos escaneados. Nuestra plataforma acepta todos los formatos.</p>
            </div>
            <div class="feature-item">
                <div class="icon"><i class="fas fa-robot"></i></div>
                <h3>2. IA Analiza</h3>
                <p>Nuestra avanzada Inteligencia Artificial procesa y analiza el contenido de tus documentos en cuestión de segundos, sin importar la cantidad de páginas. Es la única solución en el mercado que ofrece esta capacidad.</p>
            </div>
            <div class="feature-item">
                <div class="icon"><i class="fas fa-notes-medical"></i></div>
                <h3>3. Historia Clínica Estructurada</h3>
                <p>Recibe tu Historia Clínica generada de forma estructurada, organizada y lista para su uso. Toda la información relevante presentada de manera clara para tus dictámenes de calificación.</p>
            </div>
        </div>
    </section>

    <section class="container tech-security-section">
        <h2 class="section-title">Beneficios que Transforman tu Práctica</h2>
        <div class="benefits-list">
            <div class="benefit-card">
                <div class="icon"><i class="fas fa-hourglass-half"></i></div>
                <div>
                    <h3>Optimización de Tiempo</h3>
                    <p>Realiza tu trabajo de análisis y dictamen de calificación mucho más rápido, reduciendo drásticamente el tiempo dedicado a la documentación manual.</p>
                </div>
            </div>
            <div class="benefit-card">
                <div class="icon"><i class="fas fa-shield-alt"></i></div>
                <div>
                    <h3>Reducción de Errores</h3>
                    <p>Minimiza los errores de transcripción y omisiones, mejorando la precisión y la calidad de los documentos que elaboras.</p>
                </div>
            </div>
            <div class="benefit-card">
                <div class="icon"><i class="fas fa-file-medical-alt"></i></div>
                <div>
                    <h3>Calidad Documental Superior</h3>
                    <p>Obtén historias clínicas estructuradas y organizadas, lo que facilita la revisión, el seguimiento y el cumplimiento normativo.</p>
                </div>
            </div>
            <div class="benefit-card">
                <div class="icon"><i class="fas fa-chart-line"></i></div>
                <div>
                    <h3>Agilidad en el Proceso</h3>
                    <p>Acelera todo el flujo de trabajo de calificación de pérdida de capacidad laboral, desde el análisis hasta el dictamen final.</p>
                </div>
            </div>
            <div class="benefit-card">
                <div class="icon"><i class="fas fa-stethoscope"></i></div>
                <div>
                    <h3>Enfoque en el Paciente</h3>
                    <p>Libera tiempo valioso para que los profesionales de la salud puedan dedicarse más a la atención y menos a la burocracia.</p>
                </div>
            </div>
            <div class="benefit-card">
                <div class="icon"><i class="fas fa-lock"></i></div>
                <div>
                    <h3>Seguridad y Confidencialidad</h3>
                    <p>Gestiona documentos sensibles con la máxima seguridad y cumplimiento de normativas de privacidad de datos.</p>
                </div>
            </div>
        </div>
    </section>

    <section class="target-section">
        <div class="container">
            <h2 class="section-title">Ideal para Profesionales de la Medicina Laboral</h2>
            <p>AiDoc Salud está diseñado específicamente para:</p>
            <ul>
                <li>Médicos Generales</li>
                <li>Especialistas en Salud Ocupacional</li>
                <li>Enfermeros</li>
                <li>Fisioterapeutas</li>
                <li>Profesionales Independientes dedicados a la calificación de Pérdida de la Capacidad Laboral</li>
            </ul>
        </div>
    </section>

    <section class="testimonials-section">
        <div class="container">
            <h2 class="section-title">Lo que dicen nuestros usuarios (Próximamente)</h2>
            <div class="testimonial-card">
                <p>"¡AiDoc Salud ha revolucionado mi forma de trabajar! El tiempo que ahorraremos en la elaboración de dictámenes es invaluable. La IA es increíblemente precisa y la historia clínica estructurada me permite enfocarme en lo realmente importante: el paciente."</p>
                <p class="author">- Dr. [Nombre del Profesional], Médico Ocupacional</p>
            </div>
        </div>
    </section>

    <section class="tech-security-section">
        <div class="container">
            <h2 class="section-title">Tecnología y Seguridad de Vanguardia</h2>
            <div class="tech-security-content">
                <div class="tech-item">
                    <div class="icon"><i class="fas fa-cloud"></i></div>
                    <h3>Solución en la Nube</h3>
                    <p>Accede a AiDoc Salud desde cualquier lugar y en cualquier momento. Nuestra plataforma está 100% basada en la nube para tu comodidad.</p>
                </div>
                <div class="tech-item">
                    <div class="icon"><i class="fas fa-lock"></i></div>
                    <h3>Seguridad Garantizada</h3>
                    <p>Disponemos de servidores en la nube en estricto cumplimiento de todas las condiciones de seguridad y privacidad para la protección de datos sensibles.</p>
                </div>
                <div class="tech-item">
                    <div class="icon"><i class="fas fa-desktop"></i></div>
                    <h3>Compatibilidad Universal</h3>
                    <p>Solo necesitas un navegador web moderno para empezar a usar AiDoc Salud. Sin instalaciones complejas ni requisitos técnicos adicionales.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- SECCIÓN DE CONTACTO CON FORMULARIO -->
    <section id="contact" class="contact-section">
        <div class="container">
            <h2 class="section-title">¿Listo para transformar tu práctica?</h2>
            <p>Contáctanos hoy mismo para solicitar una demo gratuita.</p>
            
            <div class="contact-form-container">
                <form action="https://formsubmit.co/comercial@bol.net.co" method="POST">
                    <label for="name">Nombre completo</label>
                    <input type="text" id="name" name="Nombre" required>
    
                    <label for="email">Correo electrónico</label>
                    <input type="email" id="email" name="Email" required>
    
                    <label for="phone">Teléfono</label>
                    <input type="tel" id="phone" name="Teléfono">

                    <!-- Campo oculto para redirigir a la página de agradecimiento -->
                    <!-- Asume que 'gracias.html' está en la misma carpeta que este archivo -->
                    <input type="hidden" name="_next" value="gracias.html">
                    <button type="submit" class="submit-button">Solicitar Demostración</button>
                </form>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <p>&copy; 2025 AiDoc Salud. Todos los derechos reservados.</p>
            <p>Hecho con <i class="fas fa-heart" style="color: #E31937;"></i> para profesionales de la salud.</p>
        </div>
    </footer>

</body>
</html>
