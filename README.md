<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Barbearia Elite | Estilo e Tradição</title>
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;700&family=Playfair+Display:ital,wght@0,700;1,700&display=swap" rel="stylesheet">
    
    <!-- Font Awesome (Ícones) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <!-- Animate on Scroll Library -->
    <script src="https://unpkg.com/scrollreveal"></script>

    <style>
        /* --- VARIÁVEIS E RESET --- */
        :root {
            --primary-color: #D4AF37; /* Dourado */
            --secondary-color: #1a1a1a; /* Preto Suave */
            --bg-dark: #0a0a0a; /* Preto Profundo */
            --text-light: #ffffff;
            --text-gray: #b0b0b0;
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            text-decoration: none;
            list-style: none;
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Montserrat', sans-serif;
            background-color: var(--bg-dark);
            color: var(--text-light);
            line-height: 1.6;
            overflow-x: hidden;
        }

        h1, h2, h3 {
            font-family: 'Playfair Display', serif;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .btn {
            display: inline-block;
            padding: 15px 35px;
            background-color: var(--primary-color);
            color: #000;
            font-weight: bold;
            border-radius: 5px;
            transition: var(--transition);
            border: 2px solid var(--primary-color);
            text-transform: uppercase;
            letter-spacing: 1px;
            cursor: pointer;
        }

        .btn:hover {
            background-color: transparent;
            color: var(--primary-color);
        }

        section {
            padding: 100px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-title h2 {
            font-size: 2.5rem;
            color: var(--primary-color);
        }

        .section-title span {
            display: block;
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 3px;
            color: var(--text-gray);
            margin-bottom: 10px;
        }

        /* --- HEADER & NAV --- */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 1000;
            padding: 20px 0;
            transition: var(--transition);
        }

        header.scrolled {
            background: rgba(0, 0, 0, 0.95);
            padding: 15px 0;
            border-bottom: 1px solid var(--primary-color);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-family: 'Playfair Display', serif;
            font-size: 1.8rem;
            font-weight: bold;
            color: var(--primary-color);
        }

        .nav-links {
            display: flex;
            gap: 30px;
        }

        .nav-links a {
            color: var(--text-light);
            font-size: 0.9rem;
            font-weight: 500;
            transition: var(--transition);
        }

        .nav-links a:hover {
            color: var(--primary-color);
        }

        .mobile-menu-icon {
            display: none;
            font-size: 1.8rem;
            color: var(--primary-color);
            cursor: pointer;
        }

        /* --- HERO SECTION --- */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), 
                        url('https://images.unsplash.com/photo-1503951914875-452162b0f3f1?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
        }

        .hero-content h1 {
            font-size: 4rem;
            margin-bottom: 20px;
            letter-spacing: 2px;
        }

        .hero-content p {
            font-size: 1.2rem;
            margin-bottom: 35px;
            color: var(--text-gray);
        }

        /* --- SOBRE NÓS --- */
        .about-flex {
            display: flex;
            align-items: center;
            gap: 50px;
        }

        .about-img img {
            width: 100%;
            border-radius: 10px;
            border-bottom: 10px solid var(--primary-color);
            border-right: 10px solid var(--primary-color);
        }

        .about-text h3 {
            font-size: 2rem;
            margin-bottom: 20px;
            color: var(--primary-color);
        }

        .about-text p {
            margin-bottom: 20px;
            color: var(--text-gray);
        }

        /* --- SERVIÇOS --- */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }

        .service-card {
            background: var(--secondary-color);
            padding: 40px 30px;
            text-align: center;
            border-radius: 10px;
            transition: var(--transition);
            border: 1px solid #333;
        }

        .service-card:hover {
            transform: translateY(-10px);
            border-color: var(--primary-color);
        }

        .service-card i {
            font-size: 3rem;
            color: var(--primary-color);
            margin-bottom: 20px;
        }

        .service-card h3 {
            margin-bottom: 15px;
            font-size: 1.5rem;
        }

        .price {
            font-size: 1.8rem;
            font-weight: bold;
            color: var(--primary-color);
            display: block;
            margin-top: 15px;
        }

        /* --- GALERIA --- */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 15px;
        }

        .gallery-item {
            height: 300px;
            overflow: hidden;
            border-radius: 5px;
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
            filter: grayscale(100%);
        }

        .gallery-item:hover img {
            transform: scale(1.1);
            filter: grayscale(0%);
        }

        /* --- DEPOIMENTOS --- */
        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .testimonial-card {
            background: #111;
            padding: 30px;
            border-left: 4px solid var(--primary-color);
        }

        .testimonial-card p {
            font-style: italic;
            margin-bottom: 20px;
        }

        .client-name {
            font-weight: bold;
            color: var(--primary-color);
        }

        .stars {
            color: var(--primary-color);
            margin-bottom: 10px;
        }

        /* --- LOCALIZAÇÃO E CONTATO --- */
        .contact-flex {
            display: flex;
            flex-wrap: wrap;
            gap: 50px;
        }

        .contact-info {
            flex: 1;
            min-width: 300px;
        }

        .map-container {
            flex: 1;
            min-width: 300px;
            height: 400px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 20px;
            margin-bottom: 30px;
        }

        .contact-item i {
            font-size: 1.5rem;
            color: var(--primary-color);
        }

        .social-links {
            display: flex;
            gap: 20px;
            margin-top: 30px;
        }

        .social-links a {
            font-size: 1.8rem;
            color: var(--text-light);
            transition: var(--transition);
        }

        .social-links a:hover {
            color: var(--primary-color);
        }

        /* --- WHATSAPP FIXO --- */
        .whatsapp-float {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background-color: #25d366;
            color: #FFF;
            width: 60px;
            height: 60px;
            border-radius: 50px;
            text-align: center;
            font-size: 35px;
            box-shadow: 2px 2px 3px #999;
            z-index: 1000;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        /* --- FOOTER --- */
        footer {
            padding: 50px 0;
            text-align: center;
            border-top: 1px solid #333;
            background-color: #000;
        }

        /* --- RESPONSIVIDADE --- */
        @media (max-width: 768px) {
            .nav-links {
                display: none; /* Seria necessário JS para menu mobile completo */
            }

            .mobile-menu-icon {
                display: block;
            }

            .hero-content h1 {
                font-size: 2.5rem;
            }

            .about-flex {
                flex-direction: column;
            }

            .section-title h2 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>

    <!-- WHATSAPP FLOATING BUTTON -->
    <a href="https://wa.me/5500000000000" class="whatsapp-float" target="_blank">
        <i class="fab fa-whatsapp"></i>
    </a>

    <!-- HEADER -->
    <header id="header">
        <div class="container">
            <nav>
                <div class="logo">ELITE BARBER</div>
                <ul class="nav-links">
                    <li><a href="#home">Início</a></li>
                    <li><a href="#sobre">Sobre</a></li>
                    <li><a href="#servicos">Serviços</a></li>
                    <li><a href="#galeria">Galeria</a></li>
                    <li><a href="#contato">Contato</a></li>
                </ul>
                <div class="mobile-menu-icon">
                    <i class="fas fa-bars"></i>
                </div>
            </nav>
        </div>
    </header>

    <!-- HERO SECTION -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <h1 class="reveal-top">Seu estilo começa aqui</h1>
                <p class="reveal-bottom">Cortes modernos, barba e experiência premium em um ambiente exclusivo.</p>
                <a href="https://wa.me/5500000000000" class="btn reveal-bottom">Agendar pelo WhatsApp</a>
            </div>
        </div>
    </section>

    <!-- SOBRE NÓS -->
    <section id="sobre">
        <div class="container">
            <div class="about-flex">
                <div class="about-img reveal-left">
                    <img src="https://images.unsplash.com/photo-1593702295094-ada35bc1307e?ixlib=rb-1.2.1&auto=format&fit=crop&w=600&q=80" alt="Barbeiro trabalhando">
                </div>
                <div class="about-text reveal-right">
                    <div class="section-title" style="text-align: left; margin-bottom: 20px;">
                        <span>Nossa História</span>
                        <h2>Tradição & Qualidade</h2>
                    </div>
                    <p>A Barbearia Elite nasceu da paixão pela cutelaria clássica e pelo design moderno. Aqui, cada cliente é único e cada corte é uma obra de arte.</p>
                    <p>Com mais de 10 anos de experiência, nossos profissionais estão em constante atualização para oferecer o que há de melhor no mundo da estética masculina, desde o degradê perfeito até o tratamento de toalha quente tradicional.</p>
                    <a href="#servicos" class="btn" style="margin-top: 20px;">Veja nossos serviços</a>
                </div>
            </div>
        </div>
    </section>

    <!-- SERVIÇOS -->
    <section id="servicos" style="background-color: #0f0f0f;">
        <div class="container">
            <div class="section-title reveal-top">
                <span>O que fazemos de melhor</span>
                <h2>Nossos Serviços</h2>
            </div>
            <div class="services-grid">
                <!-- Serviço 1 -->
                <div class="service-card reveal-bottom">
                    <i class="fas fa-cut"></i>
                    <h3>Corte Masculino</h3>
                    <p>Cortes modernos, clássicos ou degradê com acabamento impecável.</p>
                    <span class="price">R$ 40</span>
                </div>
                <!-- Serviço 2 -->
                <div class="service-card reveal-bottom">
                    <i class="fas fa-user-tie"></i>
                    <h3>Barba Completa</h3>
                    <p>Modelagem, hidratação e técnica de toalha quente.</p>
                    <span class="price">R$ 35</span>
                </div>
                <!-- Serviço 3 -->
                <div class="service-card reveal-bottom">
                    <i class="fas fa-mustache"></i>
                    <h3>Corte + Barba</h3>
                    <p>O combo completo para renovar seu visual com desconto.</p>
                    <span class="price">R$ 70</span>
                </div>
                <!-- Serviço 4 -->
                <div class="service-card reveal-bottom">
                    <i class="fas fa-paint-brush"></i>
                    <h3>Pigmentação</h3>
                    <p>Destaque seu corte ou cubra falhas com naturalidade.</p>
                    <span class="price">R$ 30</span>
                </div>
            </div>
        </div>
    </section>

    <!-- GALERIA -->
    <section id="galeria">
        <div class="container">
            <div class="section-title reveal-top">
                <span>Portfólio</span>
                <h2>Galeria de Estilos</h2>
            </div>
            <div class="gallery-grid">
                <div class="gallery-item"><img src="https://images.unsplash.com/photo-1621605815841-aa8975485d29?ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80" alt="Corte 1"></div>
                <div class="gallery-item"><img src="https://images.unsplash.com/photo-1599351431247-f10b21ce963f?ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80" alt="Corte 2"></div>
                <div class="gallery-item"><img src="https://images.unsplash.com/photo-1605497788044-5a32c7078486?ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80" alt="Corte 3"></div>
                <div class="gallery-item"><img src="https://images.unsplash.com/photo-1536520002442-39764a41e987?ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80" alt="Corte 4"></div>
            </div>
        </div>
    </section>

    <!-- DEPOIMENTOS -->
    <section id="depoimentos" style="background-color: #0f0f0f;">
        <div class="container">
            <div class="section-title reveal-top">
                <span>Opinião de quem frequenta</span>
                <h2>Depoimentos</h2>
            </div>
            <div class="testimonials-grid">
                <div class="testimonial-card reveal-bottom">
                    <div class="stars">★★★★★</div>
                    <p>"Melhor barbearia da cidade. O ambiente é incrível e o atendimento é diferenciado. O café é ótimo!"</p>
                    <span class="client-name">- Ricardo Santos</span>
                </div>
                <div class="testimonial-card reveal-bottom">
                    <div class="stars">★★★★★</div>
                    <p>"Faço barba e cabelo toda semana. A precisão no degradê é impressionante. Recomendo muito!"</p>
                    <span class="client-name">- Marcos Oliveira</span>
                </div>
                <div class="testimonial-card reveal-bottom">
                    <div class="stars">★★★★★</div>
                    <p>"Ambiente extremamente limpo e profissional. O sistema de agendamento pelo WhatsApp facilita muito."</p>
                    <span class="client-name">- Felipe Mendes</span>
                </div>
            </div>
        </div>
    </section>

    <!-- LOCALIZAÇÃO E CONTATO -->
    <section id="contato">
        <div class="container">
            <div class="section-title reveal-top">
                <span>Onde estamos</span>
                <h2>Contato e Localização</h2>
            </div>
            <div class="contact-flex">
                <div class="contact-info reveal-left">
                    <div class="contact-item">
                        <i class="fas fa-map-marker-alt"></i>
                        <div>
                            <h4>Endereço</h4>
                            <p>Av. Principal, 1234 - Centro, Cidade - UF</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-phone"></i>
                        <div>
                            <h4>Telefone</h4>
                            <p>(11) 98888-7777</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-clock"></i>
                        <div>
                            <h4>Horário de Funcionamento</h4>
                            <p>Seg a Sex: 09h às 20h<br>Sábados: 09h às 18h</p>
                        </div>
                    </div>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-facebook"></i></a>
                        <a href="#"><i class="fab fa-whatsapp"></i></a>
                    </div>
                </div>
                <div class="map-container reveal-right">
                    <!-- Mapa Fictício (Google Maps Embed) -->
                    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3657.1975!2d-46.658!3d-23.561!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zMjPCsDMzJzQwLjAiUyA0NsKwMzknMjguOCJX!5e0!3m2!1spt-BR!2sbr!4v1620000000000!5m2!1spt-BR!2sbr" 
                        width="100%" height="100%" style="border:0; border-radius: 10px;" allowfullscreen="" loading="lazy"></iframe>
                </div>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer>
        <div class="container">
            <p>&copy; 2023 Barbearia Elite. Todos os direitos reservados.</p>
            <p style="font-size: 0.7rem; color: #555; margin-top: 10px;">Desenvolvido com elegância.</p>
        </div>
    </footer>

    <!-- SCRIPTS -->
    <script>
        // Mudar fundo do header ao rolar
        window.addEventListener('scroll', function() {
            const header = document.getElementById('header');
            if (window.scrollY > 50) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });

        // Configuração do ScrollReveal (Animações)
        const sr = ScrollReveal({
            origin: 'bottom',
            distance: '60px',
            duration: 1000,
            delay: 200,
            reset: false // anima apenas uma vez
        });

        sr.reveal('.reveal-top', {origin: 'top'});
        sr.reveal('.reveal-bottom', {origin: 'bottom'});
        sr.reveal('.reveal-left', {origin: 'left'});
        sr.reveal('.reveal-right', {origin: 'right'});
        sr.reveal('.service-card', {interval: 200});
        sr.reveal('.gallery-item', {interval: 150});
        sr.reveal('.testimonial-card', {interval: 200});

        // Clique suave no menu (compatibilidade extra)
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
