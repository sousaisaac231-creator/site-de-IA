# site-de-IA

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Barbearia Elite - Agendamento online de cortes premium com profissionais experientes">
    <meta name="theme-color" content="#D4AF37">
    <title>Barbearia Elite | Agendamento Online</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600;700&family=Playfair+Display:wght@700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <style>
        :root {
            --primary: #D4AF37;
            --dark: #0a0a0a;
            --dark-2: #161616;
            --white: #ffffff;
            --gray: #999;
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Montserrat', sans-serif;
        }

        html { scroll-behavior: smooth; }
        body {
            background: var(--dark);
            color: var(--white);
            line-height: 1.6;
            overflow-x: hidden;
        }

        h1, h2, h3 { font-family: 'Playfair Display', serif; }
        a { text-decoration: none; color: inherit; }
        ul { list-style: none; }
        section { padding: 80px 20px; }
        .container { max-width: 1100px; margin: 0 auto; padding: 0 20px; }

        /* --- HEADER & NAVIGATION --- */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 1000;
            background: rgba(10, 10, 10, 0.98);
            padding: 15px 0;
            border-bottom: 1px solid rgba(212, 175, 55, 0.2);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
        }

        .nav-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .logo {
            font-size: 1.5rem;
            color: var(--primary);
            font-weight: 700;
            letter-spacing: 2px;
        }

        .nav-menu {
            display: flex;
            gap: 30px;
        }

        .nav-menu a {
            transition: var(--transition);
            position: relative;
        }

        .nav-menu a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--primary);
            transition: var(--transition);
        }

        .nav-menu a:hover::after { width: 100%; }

        .menu-toggle {
            display: none;
            font-size: 1.5rem;
            color: var(--primary);
            cursor: pointer;
            background: none;
            border: none;
        }

        /* --- HERO --- */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)),
                        url('https://images.unsplash.com/photo-1585747860715-2ba37e788b70?auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            margin-top: 60px;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 15px;
            color: var(--primary);
            animation: fadeInDown 0.8s ease;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            color: #ccc;
            animation: fadeInUp 0.8s ease 0.2s backwards;
        }

        @keyframes fadeInDown {
            from { opacity: 0; transform: translateY(-30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* --- BOTÕES --- */
        .btn-primary {
            padding: 15px 40px;
            background: var(--primary);
            color: var(--dark);
            font-weight: 700;
            border-radius: 4px;
            cursor: pointer;
            transition: var(--transition);
            border: none;
            font-size: 1rem;
            animation: fadeInUp 0.8s ease 0.4s backwards;
        }

        .btn-primary:hover {
            transform: scale(1.05);
            box-shadow: 0 5px 20px rgba(212, 175, 55, 0.3);
        }

        .btn-primary:active { transform: scale(0.98); }

        .btn-sm {
            padding: 8px 20px;
            background: transparent;
            border: 1px solid var(--primary);
            color: var(--primary);
            cursor: pointer;
            font-weight: 600;
            border-radius: 4px;
            transition: var(--transition);
        }

        .btn-sm:hover {
            background: var(--primary);
            color: var(--dark);
        }

        /* --- SERVIÇOS --- */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
            margin-top: 40px;
        }

        .card {
            background: var(--dark-2);
            padding: 30px;
            border-radius: 8px;
            text-align: center;
            border: 1px solid #333;
            transition: var(--transition);
        }

        .card:hover {
            border-color: var(--primary);
            transform: translateY(-10px);
            box-shadow: 0 10px 30px rgba(212, 175, 55, 0.2);
        }

        .card i {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 20px;
        }

        .card h3 {
            margin-bottom: 10px;
            font-size: 1.3rem;
        }

        .card p {
            color: #ccc;
            margin-bottom: 15px;
        }

        .card .price {
            font-size: 1.5rem;
            color: var(--primary);
            font-weight: 700;
            display: block;
            margin: 15px 0;
        }

        /* --- SOBRE --- */
        .about {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .about-text h3 {
            color: var(--primary);
            margin-bottom: 20px;
            font-size: 1.8rem;
        }

        .about-text p {
            margin-bottom: 15px;
            color: #ccc;
            line-height: 1.8;
        }

        .about-img {
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
        }

        .about-img img {
            width: 100%;
            height: auto;
            display: block;
            transition: var(--transition);
        }

        .about-img:hover img { transform: scale(1.05); }

        /* --- CONTATO --- */
        .contact-form {
            max-width: 600px;
            margin: 0 auto;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: var(--white);
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px;
            background: var(--dark-2);
            border: 1px solid #333;
            color: var(--white);
            border-radius: 4px;
            font-family: 'Montserrat', sans-serif;
            transition: var(--transition);
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 10px rgba(212, 175, 55, 0.2);
        }

        .form-group textarea {
            resize: vertical;
            min-height: 120px;
        }

        .form-message {
            display: none;
            padding: 15px;
            border-radius: 4px;
            margin-bottom: 20px;
            text-align: center;
            font-weight: 600;
        }

        .form-message.success {
            background: rgba(76, 175, 80, 0.2);
            color: #4CAF50;
            display: block;
        }

        .form-message.error {
            background: rgba(244, 67, 54, 0.2);
            color: #f44336;
            display: block;
        }

        /* --- FOOTER --- */
        footer {
            background: var(--dark-2);
            padding: 40px 20px;
            text-align: center;
            border-top: 1px solid rgba(212, 175, 55, 0.2);
        }

        footer p {
            color: var(--gray);
            margin: 10px 0;
        }

        footer .highlight {
            color: var(--primary);
        }

        /* --- SEÇÃO h2 --- */
        section h2 {
            font-size: 2.5rem;
            margin-bottom: 30px;
            text-align: center;
            color: var(--primary);
        }

        /* --- RESPONSIVE --- */
        @media (max-width: 768px) {
            .nav-menu {
                display: none;
                position: absolute;
                top: 60px;
                left: 0;
                right: 0;
                flex-direction: column;
                background: rgba(10, 10, 10, 0.99);
                padding: 20px;
                gap: 15px;
            }

            .nav-menu.active { display: flex; }

            .menu-toggle { display: block; }

            .hero h1 { font-size: 2rem; }
            .hero p { font-size: 1rem; }

            .about { grid-template-columns: 1fr; }

            section { padding: 50px 20px; }

            section h2 { font-size: 2rem; }

            .about-text h3 { font-size: 1.5rem; }
        }
    </style>
</head>
<body>

<!-- HEADER -->
<header>
    <div class="nav-content">
        <div class="logo">✂️ ELITE BARBER</div>
        <nav class="nav-menu">
            <a href="#home">Home</a>
            <a href="#services">Serviços</a>
            <a href="#about">Sobre</a>
            <a href="#contact">Contato</a>
        </nav>
        <button class="menu-toggle" aria-label="Menu"><i class="fas fa-bars"></i></button>
    </div>
</header>

<!-- HERO SECTION -->
<section class="hero" id="home">
    <div class="container">
        <h1>Barbearia Elite</h1>
        <p>Agendamento Online de Cortes Premium</p>
        <button class="btn-primary" onclick="scrollTo('#services')" aria-label="Agende seus serviços">Agende Agora</button>
    </div>
</section>

<!-- SERVIÇOS -->
<section id="services" style="background: var(--dark-2);">
    <div class="container">
        <h2>Nossos Serviços</h2>
        <div class="services-grid">
            <div class="card">
                <i class="fas fa-cut"></i>
                <h3>Corte Clássico</h3>
                <p>Corte tradicional com acabamento impecável</p>
                <span class="price">R$ 45,00</span>
                <button class="btn-sm" onclick="alert('Redirecionando para agendamento...')">Agendar</button>
            </div>
            <div class="card">
                <i class="fas fa-face-smile-wink"></i>
                <h3>Corte + Barba</h3>
                <p>Corte + design de barba completo</p>
                <span class="price">R$ 65,00</span>
                <button class="btn-sm" onclick="alert('Redirecionando para agendamento...')">Agendar</button>
            </div>
            <div class="card">
                <i class="fas fa-spray-can"></i>
                <h3>Design de Sobrancelha</h3>
                <p>Design profissional e alinhamento</p>
                <span class="price">R$ 30,00</span>
                <button class="btn-sm" onclick="alert('Redirecionando para agendamento...')">Agendar</button>
            </div>
            <div class="card">
                <i class="fas fa-water"></i>
                <h3>Pigmentação de Barba</h3>
                <p>Tingimento profissional de barba</p>
                <span class="price">R$ 55,00</span>
                <button class="btn-sm" onclick="alert('Redirecionando para agendamento...')">Agendar</button>
            </div>
        </div>
    </div>
</section>

<!-- SOBRE -->
<section id="about">
    <div class="container">
        <h2>Sobre a Barbearia Elite</h2>
        <div class="about">
            <div class="about-text">
                <h3>Tradição e Excelência</h3>
                <p>
                    Há mais de 15 anos, a Barbearia Elite oferece os melhores serviços de barbearia para homens que valorizam qualidade e estilo.
                </p>
                <p>
                    Nossos profissionais são treinados e experientes, utilizando produtos premium para garantir o melhor resultado.
                </p>
                <p>
                    Venha conhecer nosso espaço aconchegante e deixe-se envolver pelo atendimento personalizado.
                </p>
            </div>
            <div class="about-img">
                <img src="https://images.unsplash.com/photo-1599912676162-22d01489fb33?auto=format&fit=crop&w=500&q=60" alt="Espaço da Barbearia Elite com profissionais trabalhando">
            </div>
        </div>
    </div>
</section>

<!-- CONTATO -->
<section id="contact" style="background: var(--dark-2);">
    <div class="container">
        <h2>Fale Conosco</h2>
        <div class="contact-form">
            <div class="form-message" id="formMessage"></div>
            <form id="contactForm">
                <div class="form-group">
                    <label for="name">Nome</label>
                    <input type="text" id="name" name="name" required minlength="3">
                </div>
                <div class="form-group">
                    <label for="email">E-mail</label>
                    <input type="email" id="email" name="email" required>
                </div>
                <div class="form-group">
                    <label for="phone">Telefone</label>
                    <input type="tel" id="phone" name="phone" required>
                </div>
                <div class="form-group">
                    <label for="message">Mensagem</label>
                    <textarea id="message" name="message" required minlength="10"></textarea>
                </div>
                <button type="submit" class="btn-primary" style="width: 100%;">Enviar Mensagem</button>
            </form>
        </div>
    </div>
</section>

<!-- FOOTER -->
<footer>
    <div class="container">
        <p>&copy; 2026 Barbearia Elite. Todos os direitos reservados.</p>
        <p>
            <span class="highlight">✂️ Agendamento Online</span> |
            <span class="highlight">Qualidade Premium</span> |
            <span class="highlight">Profissionais Experientes</span>
        </p>
    </div>
</footer>

<script>
    // Smooth scroll function
    function scrollTo(selector) {
        const element = document.querySelector(selector);
        element.scrollIntoView({ behavior: 'smooth' });
    }

    // Mobile menu toggle
    const menuToggle = document.querySelector('.menu-toggle');
    const navMenu = document.querySelector('.nav-menu');

    menuToggle.addEventListener('click', function() {
        navMenu.classList.toggle('active');
    });

    // Close menu when link is clicked
    navMenu.querySelectorAll('a').forEach(link => {
        link.addEventListener('click', () => {
            navMenu.classList.remove('active');
        });
    });

    // Form submission with validation
    const contactForm = document.getElementById('contactForm');
    const formMessage = document.getElementById('formMessage');

    contactForm.addEventListener('submit', function(e) {
        e.preventDefault();

        // Validation
        const name = document.getElementById('name').value.trim();
        const email = document.getElementById('email').value.trim();
        const phone = document.getElementById('phone').value.trim();
        const message = document.getElementById('message').value.trim();

        if (!name || !email || !phone || !message) {
            showMessage('Por favor, preencha todos os campos.', 'error');
            return;
        }

        if (message.length < 10) {
            showMessage('A mensagem deve ter pelo menos 10 caracteres.', 'error');
            return;
        }

        // Success (in a real app, this would send data to a server)
        showMessage('✓ Obrigado! Sua mensagem foi enviada com sucesso. Entraremos em contato em breve.', 'success');
        this.reset();

        // Hide message after 5 seconds
        setTimeout(() => {
            formMessage.style.display = 'none';
        }, 5000);
    });

    function showMessage(text, type) {
        formMessage.textContent = text;
        formMessage.className = `form-message ${type}`;
    }
</script>

</body>
</html>
