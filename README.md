<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Horacio Licona - GitHub Profile</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Helvetica', 'Arial', sans-serif;
            line-height: 1.6;
            color: #24292e;
            max-width: 1000px;
            margin: 0 auto;
            padding: 20px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }
        
        .profile-container {
            background: white;
            border-radius: 15px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
            overflow: hidden;
            margin: 20px 0;
        }
        
        .header {
            background: linear-gradient(135deg, #2196F3 0%, #21CBF3 100%);
            color: white;
            padding: 40px;
            text-align: center;
            position: relative;
        }
        
        .header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grain" width="100" height="100" patternUnits="userSpaceOnUse"><circle cx="20" cy="20" r="1" fill="white" opacity="0.1"/><circle cx="80" cy="80" r="1" fill="white" opacity="0.1"/><circle cx="40" cy="60" r="1" fill="white" opacity="0.05"/></pattern></defs><rect width="100" height="100" fill="url(%23grain)"/></svg>');
        }
        
        .header h1 {
            margin: 0;
            font-size: 3em;
            font-weight: 700;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
            position: relative;
            z-index: 1;
        }
        
        .header p {
            margin: 10px 0 0 0;
            font-size: 1.3em;
            opacity: 0.9;
            position: relative;
            z-index: 1;
        }
        
        .wave {
            font-size: 2em;
            animation: wave 2s infinite;
            display: inline-block;
        }
        
        @keyframes wave {
            0%, 20%, 60%, 100% { transform: rotate(0deg); }
            10% { transform: rotate(14deg); }
            30% { transform: rotate(-8deg); }
            40% { transform: rotate(14deg); }
            50% { transform: rotate(-4deg); }
            70% { transform: rotate(10deg); }
        }
        
        .content {
            padding: 40px;
        }
        
        .section {
            margin-bottom: 40px;
        }
        
        .section h2 {
            color: #2196F3;
            border-bottom: 3px solid #2196F3;
            padding-bottom: 10px;
            margin-bottom: 20px;
            font-size: 1.8em;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            gap: 15px;
            margin: 20px 0;
        }
        
        .tech-item {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            padding: 15px;
            border-radius: 10px;
            text-align: center;
            font-weight: 600;
            transition: all 0.3s ease;
            border: 2px solid transparent;
        }
        
        .tech-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
            border: 2px solid #2196F3;
        }
        
        .experience-item {
            background: #f8f9fa;
            padding: 25px;
            border-radius: 12px;
            margin-bottom: 20px;
            border-left: 5px solid #2196F3;
            transition: all 0.3s ease;
        }
        
        .experience-item:hover {
            transform: translateX(5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .experience-item h3 {
            color: #2196F3;
            margin: 0 0 10px 0;
            font-size: 1.3em;
        }
        
        .experience-item .company {
            font-weight: bold;
            color: #666;
            margin-bottom: 5px;
        }
        
        .experience-item .date {
            color: #888;
            font-size: 0.9em;
            margin-bottom: 10px;
        }
        
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }
        
        .stat-card {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 25px;
            border-radius: 12px;
            text-align: center;
            box-shadow: 0 8px 16px rgba(0,0,0,0.1);
        }
        
        .stat-number {
            font-size: 2.5em;
            font-weight: bold;
            margin-bottom: 5px;
        }
        
        .contact-links {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            justify-content: center;
            margin: 30px 0;
        }
        
        .contact-link {
            background: #2196F3;
            color: white;
            padding: 12px 25px;
            border-radius: 25px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .contact-link:hover {
            background: #1976D2;
            transform: translateY(-2px);
            box-shadow: 0 5px 10px rgba(0,0,0,0.2);
        }
        
        .emoji {
            font-size: 1.2em;
        }
        
        .highlight {
            background: linear-gradient(120deg, #a8edea 0%, #fed6e3 100%);
            padding: 20px;
            border-radius: 10px;
            margin: 20px 0;
            border-left: 4px solid #2196F3;
        }
        
        @media (max-width: 768px) {
            .header h1 { font-size: 2em; }
            .header p { font-size: 1.1em; }
            .content { padding: 20px; }
            .tech-grid { grid-template-columns: repeat(auto-fit, minmax(100px, 1fr)); }
            .contact-links { flex-direction: column; align-items: center; }
        }
    </style>
</head>
<body>
    <div class="profile-container">
        <div class="header">
            <h1>¡Hola! <span class="wave">👋</span> Soy Horacio Licona</h1>
            <p>🚀 Scrum Master | 💻 Full Stack Developer | 🤖 AI Specialist</p>
        </div>
        
        <div class="content">
            <div class="section">
                <div class="highlight">
                    <p><strong>Especialista bilingüe</strong> egresado del <strong>Tecnológico de Monterrey (ITESM)</strong> y próximo a concluir una <strong>Maestría en Administración de Empresas</strong>. Con enfoque en desarrollo Full Stack e Inteligencia Artificial, tengo experiencia coordinando equipos multidisciplinarios bajo marcos ágiles como SCRUM.</p>
                </div>
            </div>

            <div class="section">
                <h2><span class="emoji">🔭</span> Actualmente trabajando en</h2>
                <div class="experience-item">
                    <h3>Consultor y Desarrollador FullStack IA</h3>
                    <div class="company">PRACTIA GLOBAL</div>
                    <div class="date">Enero 2025 - Mayo 2025</div>
                    <p>Desarrollo Full Stack de webapps usando <strong>Flask (Python)</strong> para el Backend y <strong>React</strong> para el Frontend. APIs REST, sistemas escalables, bases de datos SQL y autenticación con JWT y OAuth2.</p>
                </div>
            </div>

            <div class="section">
                <h2><span class="emoji">🌱</span> Mi Stack Tecnológico</h2>
                <div class="tech-grid">
                    <div class="tech-item">Python</div>
                    <div class="tech-item">JavaScript</div>
                    <div class="tech-item">TypeScript</div>
                    <div class="tech-item">Java</div>
                    <div class="tech-item">React</div>
                    <div class="tech-item">Angular</div>
                    <div class="tech-item">Flask</div>
                    <div class="tech-item">Django</div>
                    <div class="tech-item">TensorFlow</div>
                    <div class="tech-item">PyTorch</div>
                    <div class="tech-item">Docker</div>
                    <div class="tech-item">Kafka</div>
                    <div class="tech-item">PostgreSQL</div>
                    <div class="tech-item">MySQL</div>
                    <div class="tech-item">Golang</div>
                    <div class="tech-item">Spring Boot</div>
                </div>
            </div>

            <div class="section">
                <h2><span class="emoji">💼</span> Experiencia Destacada</h2>
                
                <div class="experience-item">
                    <h3>Consultor y Desarrollador FullStack</h3>
                    <div class="company">FORD MOTOR COMPANY - ALTEN</div>
                    <div class="date">Agosto 2024 - Enero 2025</div>
                    <p>Desarrollo de software para pantallas TFT LCD en nuevos modelos de Ford, usando <strong>TypeScript, JavaScript, React</strong> y metodología Scrum.</p>
                </div>
                
                <div class="experience-item">
                    <h3>Consultor y Desarrollador de IA / FullStack</h3>
                    <div class="company">PRAXIS GLOBE</div>
                    <div class="date">Agosto 2022 - Agosto 2024</div>
                    <p>Lideré equipos técnicos bajo SCRUM, desarrollé microservicios para SPEI usando <strong>Golang y Java</strong>, y creé chatbots con <strong>NLP, TensorFlow, Rasa</strong>.</p>
                </div>
            </div>

            <div class="section">
                <h2><span class="emoji">🚀</span> Proyectos Destacados</h2>
                <div class="stats-grid">
                    <div class="stat-card">
                        <div class="stat-number">🏦</div>
                        <div>Sistema SPEI</div>
                        <small>Microservicios bancarios con Golang, Java y Kafka</small>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">🤖</div>
                        <div>Chatbot IA</div>
                        <small>NLP con Python, TensorFlow y Rasa</small>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">🚗</div>
                        <div>Sistema Ford</div>
                        <small>React + TypeScript para pantallas automotrices</small>
                    </div>
                </div>
            </div>

            <div class="section">
                <h2><span class="emoji">🎓</span> Certificaciones</h2>
                <div class="tech-grid">
                    <div class="tech-item">🏅 SCRUM Master</div>
                    <div class="tech-item">📋 Product Owner</div>
                    <div class="tech-item">🧠 Redes Neuronales</div>
                    <div class="tech-item">🐍 Python Certified</div>
                    <div class="tech-item">☕ Java Certified</div>
                    <div class="tech-item">🌐 Django Certified</div>
                    <div class="tech-item">🗣️ TOEFL C1</div>
                    <div class="tech-item">🤖 ChatGPT Certified</div>
                </div>
            </div>

            <div class="section">
                <h2><span class="emoji">👯</span> Colaboraciones</h2>
                <p>🔍 Busco colaborar en proyectos de <strong>Inteligencia Artificial</strong>, <strong>Microservicios</strong> y <strong>desarrollo Full Stack</strong></p>
                <p>🤝 Especializado en liderar equipos ágiles y facilitar ceremonias SCRUM</p>
                <p>💡 Interesado en proyectos que combinen <strong>IA, Backend robusto y Frontend moderno</strong></p>
            </div>

            <div class="section">
                <h2><span class="emoji">💬</span> Pregúntame sobre</h2>
                <div class="highlight">
                    <p>🔹 <strong>Desarrollo Full Stack</strong> con Python, JavaScript, React<br>
                    🔹 <strong>Inteligencia Artificial</strong> y Machine Learning<br>
                    🔹 <strong>Metodologías Ágiles</strong> y Scrum Master<br>
                    🔹 <strong>Microservicios</strong> y arquitecturas escalables<br>
                    🔹 <strong>Chatbots</strong> y procesamiento de lenguaje natural</p>
                </div>
            </div>

            <div class="section">
                <h2><span class="emoji">📫</span> Contacto</h2>
                <div class="contact-links">
                    <a href="mailto:horaciolicona0711@gmail.com" class="contact-link">
                        📧 Email
                    </a>
                    <a href="https://www.linkedin.com/in/horacio-licona-gonz%C3%A1lez-591655212/" class="contact-link">
                        💼 LinkedIn
                    </a>
                    <a href="https://horaciolicona.my.canva.site/portafolio" class="contact-link">
                        🎨 Portafolio
                    </a>
                    <a href="https://horacio-licona-portfolio.onrender.com/" class="contact-link">
                        🌐 Website
                    </a>
                    <a href="https://github.com/HoracioLicona07?tab=repositories" class="contact-link">
                        💻 GitHub
                    </a>
                </div>
            </div>

            <div class="section">
                <h2><span class="emoji">⚡</span> Datos Curiosos</h2>
                <p>🌎 Ubicado en <strong>CDMX, México</strong><br>
                🎓 <strong>Ingeniero Mecatrónico</strong> del Tec de Monterrey<br>
                🏢 <strong>MBA en proceso</strong> - Tecnológico de Monterrey<br>
                🗣️ <strong>Bilingüe</strong> - Español/Inglés (C1)<br>
                🚀 Apasionado por la <strong>innovación tecnológica</strong> y el <strong>liderazgo ágil</strong></p>
            </div>
        </div>
    </div>

    <script>
        // Animación sutil para las tarjetas
        document.addEventListener('DOMContentLoaded', function() {
            const cards = document.querySelectorAll('.tech-item, .experience-item');
            
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.opacity = '1';
                        entry.target.style.transform = 'translateY(0)';
                    }
                });
            });

            cards.forEach(card => {
                card.style.opacity = '0';
                card.style.transform = 'translateY(20px)';
                card.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
                observer.observe(card);
            });
        });
    </script>
</body>
</html>
