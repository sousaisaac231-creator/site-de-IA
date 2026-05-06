# site-de-IA

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Barbearia Elite | Agendamento Online</title>
    
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600;700&family=Playfair+Display:wght@700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <style>
        :root {
            --primary: #D4AF37;
            --dark: #0a0a0a;
            --dark-2: #161616;
            --white: #ffffff;
            --transition: all 0.3s ease;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Montserrat', sans-serif; }
        body { background: var(--dark); color: var(--white); line-height: 1.6; overflow-x: hidden; }
        h1, h2, h3 { font-family: 'Playfair Display', serif; }
        a { text-decoration: none; color: inherit; }
        ul { list-style: none; }
        section { padding: 80px 20px; }
        .container { max-width: 1100px; margin: 0 auto; }

        /* --- HEADER & NAVIGATION --- */
        header {
            position: fixed; top: 0; width: 100%; z-index: 1000;
            background: rgba(10, 10, 10, 0.95); padding: 15px 0;
            border-bottom: 1px solid rgba(212, 175, 55, 0.2);
        }

        .nav-content {
            display: flex; justify-content: space-between; align-items: center;
            max-width: 1100px; margin: 0 auto; padding: 0 20px;
        }

        .logo { font-size: 1.5rem; color: var(--primary); font-weight: 700; letter-spacing: 2px; }

        .nav-menu { display: flex; gap: 30px; }
        .nav-menu a:hover { color: var(--primary); }

        .menu-toggle { display: none; font-size: 1.5rem; color: var(--primary); cursor: pointer; }

        /* --- HERO --- */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('https://images.unsplash.com/photo-1585747860715-2ba37e788b70?auto=format&fit=crop&w=1350&q=80');
            background-size: cover; background-position: center;
            display: flex; align-items: center; justify-content: center; text-align: center;
            margin-top: 60px;
        }

        .hero h1 { font-size: 3.5rem; margin-bottom: 15px; color: var(--primary); }
        .hero p { font-size: 1.2rem; margin-bottom: 30px; color: #ccc; }

        .btn-primary {
            padding: 15px 40px; background: var(--primary); color: var(--dark);
            font-weight: 700; border-radius: 4px; cursor: pointer; transition: var(--transition);
            border: none;
        }

        .btn-primary:hover { transform: scale(1.05); }

        /* --- SERVIÇOS --- */
        .services-grid {
            display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 25px; margin-top: 40px;
        }

        .card {
            background: var(--dark-2); padding: 30px; border-radius: 8px; text-align: center;
            border: 1px solid #333; transition: var(--transition);
        }

        .card:hover { border-color: var(--primary); transform: translateY(-5px); }
        .card i { font-size: 2.5rem; color: var(--primary); margin-bottom: 20px; }
        .card h3 { margin-bottom: 10px; }
        .card .price { font-size: 1.5rem; color: var(--primary); font-weight: 700; display: block; margin: 15px 0; }

        .btn-sm {
            padding: 8px 20px; background: transparent; border: 1px solid var(--primary);
            color: var(--primary); cursor: pointer; font-weight: 600; border-radius: 4px;
            transition: var(--transition);
        }

        .btn-sm:hover { background: var(--primary); color: var(--dark); }

        /* --- SOBRE --- */
        .about {
            display: grid; grid-template-columns: 1fr 1fr; gap: 50px; align-items: center;
        }

        .about-text h2 { font-size: 2.5rem; margin-bottom: 20px; color: var(--primary); }
        .about-text p { margin-bottom: 15px; color: #ccc; }

        .about-img { border-radius: 8px; overflow: hidden; }
        .about-img img { width: 100%; height: auto; }

        /* --- CONTATO --- */
        .contact-form {
            max-width: 600px; margin: 0 auto;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block; margin-bottom: 8px; font-weight: 600;
        }

        .form-group input,
        .form-group textarea {
            width: 100%; padding: 12px; background: var(--dark-2);
            border: 1px solid #333; color: var(--white); border-radius: 4px;
            font-family: 'Montserrat', sans-serif;
        }

        .form-group textarea { resize: vertical; min-height: 120px; }

        /* --- FOOTER --- */
        footer {
            background: var(--dark-2); padding: 40px 20px; text-align: center;
            border-top: 1px solid rgba(212, 175, 55, 0.2);
        }

        footer p { color: #999; }

        /* --- RESPONSIVE --- */
        @media (max-width: 768px) {
            .nav-menu { display: none; }
            .menu-toggle { display: block; }

            .hero h1 { font-size: 2rem; }
            .hero p { font-size: 1rem; }

            .about { grid-template-columns: 1fr; }

            section { padding: 50px 20px; }
        }

        section h2 { font-size: 2.5rem; margin-bottom: 30px; text-align: center; color: var(--primary); }
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
        <div class="menu-toggle"><i class="fas fa-bars"></i></div>
    </div>
</header>

<!-- HERO SECTION -->
<section class="hero" id="home">
    <div class="container" style="text-align: center;">
        <h1>Barbearia Elite</h1>
        <p>Agendamento Online de Cortes Premium</p>
        <button class="btn-primary" onclick="scrollTo('#services')">Agende Agora</button>
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
                <button class="btn-sm">Agendar</button>
            </div>
            <div class="card">
                <i class="fas fa-face-smile-wink"></i>
                <h3>Corte + Barba</h3>
                <p>Corte + design de barba completo</p>
                <span class="price">R$ 65,00</span>
                <button class="btn-sm">Agendar</button>
            </div>
            <div class="card">
                <i class="fas fa-spray-can"></i>
                <h3>Design de Sobrancelha</h3>
                <p>Design profissional e alinhamento</p>
                <span class="price">R$ 30,00</span>
                <button class="btn-sm">Agendar</button>
            </div>
            <div class="card">
                <i class="fas fa-water"></i>
                <h3>Pigmentação de Barba</h3>
                <p>Tingimento profissional de barba</p>
                <span class="price">R$ 55,00</span>
                <button class="btn-sm">Agendar</button>
            </div>
        </div>
    </div>
</section>

<!-- SOBRE -->
<section id="about">
    <div class="container">
        <h2 style="text-align: left; margin-bottom: 40px;">Sobre a Barbearia Elite</h2>
        <div class="about">
            <div class="about-text">
                <h3 style="color: var(--primary); margin-bottom: 20px;">Tradição e Excelência</h3>
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
                <img src="https://images.unsplash.com/photo-1599912676162-22d01489fb33?auto=format&fit=crop&w=500&q=60" alt="Barbearia Elite">
            </div>
        </div>
    </div>
</section>

<!-- CONTATO -->
<section id="contact" style="background: var(--dark-2);">
    <div class="container">
        <h2>Fale Conosco</h2>
        <div class="contact-form">
            <form>
                <div class="form-group">
                    <label for="name">Nome</label>
                    <input type="text" id="name" name="name" required>
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
                    <textarea id="message" name="message" required></textarea>
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
        <p style="margin-top: 15px; color: var(--primary);">✂️ Agendamento Online | Qualidade Premium | Profissionais Experientes</p>
    </div>
</footer>

<script>
    function scrollTo(selector) {
        document.querySelector(selector).scrollIntoView({ behavior: 'smooth' });
    }

    // Mobile menu toggle
    document.querySelector('.menu-toggle').addEventListener('click', function() {
        const menu = document.querySelector('.nav-menu');
        menu.style.display = menu.style.display === 'flex' ? 'none' : 'flex';
    });

    // Form submission
    document.querySelector('form').addEventListener('submit', function(e) {
        e.preventDefault();
        alert('Obrigado! Sua mensagem foi enviada com sucesso.');
        this.reset();
    });
</script>

</body>
</html>
