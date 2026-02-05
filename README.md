<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio Profesional - Modern Dark Theme</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Sora:wght@300;400;600;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/7.0.1/css/all.min.css" integrity="sha512-2SwdPD6INVrV/lHTZbO2nodKhrnDdJK9/kg2XD1r9uGqPo1cUbujc+IYdlYdEErWNu69gVcYgdxlmVmzTWnetw==" crossorigin="anonymous" referrerpolicy="no-referrer" />
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --bg-primary: #0f1419;
            --bg-secondary: #1a1f2e;
            --bg-card: rgba(26, 31, 46, 0.6);
            --text-primary: #e4e6eb;
            --text-secondary: #a0a5b8;
            --accent-cyan: #00d9ff;
            --accent-teal: #00ffc8;
            --accent-purple: #9d7fff;
            --navy: #0a0e1a;
            --glow-cyan: rgba(0, 217, 255, 0.3);
            --glow-teal: rgba(0, 255, 200, 0.2);
        }

        body {
            font-family: 'Sora', sans-serif;
            background: linear-gradient(135deg, var(--navy) 0%, var(--bg-primary) 50%, #0d1117 100%);
            color: var(--text-primary);
            line-height: 1.6;
            overflow-x: hidden;
            position: relative;
        }

        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                radial-gradient(circle at 20% 20%, rgba(0, 217, 255, 0.08) 0%, transparent 50%),
                radial-gradient(circle at 80% 80%, rgba(157, 127, 255, 0.06) 0%, transparent 50%);
            pointer-events: none;
            z-index: 0;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
            position: relative;
            z-index: 1;
        }

        /* Navigation */
        nav {
            padding: 2rem 0;
            position: sticky;
            top: 0;
            background: rgba(15, 20, 25, 0.8);
            backdrop-filter: blur(20px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
            z-index: 100;
            animation: slideDown 0.8s ease-out;
        }

        @keyframes slideDown {
            from {
                opacity: 0;
                transform: translateY(-20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        nav .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            background: linear-gradient(135deg, var(--accent-cyan), var(--accent-teal));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            letter-spacing: -0.5px;
        }

        .nav-links {
            display: flex;
            gap: 2.5rem;
            list-style: none;
        }

        .nav-links a {
            color: var(--text-secondary);
            text-decoration: none;
            font-size: 0.95rem;
            font-weight: 400;
            transition: all 0.3s ease;
            position: relative;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: linear-gradient(90deg, var(--accent-cyan), var(--accent-teal));
            transition: width 0.3s ease;
        }

        .nav-links a:hover {
            color: var(--text-primary);
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        /* Hero Section */
        .hero {
            padding: 8rem 0 6rem;
            text-align: center;
            animation: fadeInUp 1s ease-out;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }

        .hero-badge {
            display: inline-block;
            padding: 0.5rem 1.5rem;
            background: rgba(0, 217, 255, 0.1);
            border: 1px solid rgba(0, 217, 255, 0.3);
            border-radius: 50px;
            font-size: 0.85rem;
            color: var(--accent-cyan);
            margin-bottom: 2rem;
            animation: pulse 2s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% {
                box-shadow: 0 0 0 0 var(--glow-cyan);
            }
            50% {
                box-shadow: 0 0 20px 5px var(--glow-cyan);
            }
        }

        h1 {
            font-size: 4rem;
            font-weight: 700;
            line-height: 1.1;
            margin-bottom: 1.5rem;
            background: linear-gradient(135deg, var(--text-primary) 0%, var(--accent-cyan) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            letter-spacing: -2px;
        }

        .hero p {
            font-size: 1.25rem;
            color: var(--text-secondary);
            margin-bottom: 3rem;
            line-height: 1.8;
        }

        .cta-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 1rem 2.5rem;
            border-radius: 12px;
            font-size: 1rem;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            position: relative;
            overflow: hidden;
        }

        .btn-primary {
            background: linear-gradient(135deg, var(--accent-cyan), var(--accent-teal));
            color: var(--navy);
            box-shadow: 0 10px 30px rgba(0, 217, 255, 0.3);
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 15px 40px rgba(0, 217, 255, 0.4);
        }

        .btn-secondary {
            background: rgba(255, 255, 255, 0.05);
            color: var(--text-primary);
            border: 1px solid rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
        }

        .btn-secondary:hover {
            background: rgba(255, 255, 255, 0.1);
            border-color: rgba(255, 255, 255, 0.2);
            transform: translateY(-2px);
        }

        /* Section Styling */
        section {
            padding: 6rem 0;
            animation: fadeInUp 1s ease-out;
        }

        .section-header {
            text-align: center;
            margin-bottom: 4rem;
        }

        .section-tag {
            font-size: 0.9rem;
            color: var(--accent-cyan);
            text-transform: uppercase;
            letter-spacing: 2px;
            font-weight: 600;
            margin-bottom: 1rem;
        }

        h2 {
            font-size: 3rem;
            font-weight: 700;
            margin-bottom: 1rem;
            letter-spacing: -1px;
        }

        .section-description {
            font-size: 1.1rem;
            color: var(--text-secondary);
            max-width: 600px;
            margin: 0 auto;
        }

        /* Skills Section */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .skill-card {
            background: var(--bg-card);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.08);
            border-radius: 20px;
            padding: 2.5rem;
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
        }

        .skill-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(0, 217, 255, 0.05), rgba(157, 127, 255, 0.05));
            opacity: 0;
            transition: opacity 0.4s ease;
        }

        .skill-card:hover {
            transform: translateY(-8px);
            border-color: rgba(0, 217, 255, 0.3);
            box-shadow: 0 20px 60px rgba(0, 217, 255, 0.2);
        }

        .skill-card:hover::before {
            opacity: 1;
        }

        .skill-icon {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, rgba(0, 217, 255, 0.2), rgba(0, 255, 200, 0.2));
            border-radius: 16px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
            box-shadow: 0 8px 24px rgba(0, 217, 255, 0.3);
        }

        .skill-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            font-weight: 600;
        }

        .skill-card p {
            color: var(--text-secondary);
            line-height: 1.7;
        }

        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-top: 1.5rem;
        }

        .tag {
            padding: 0.4rem 1rem;
            background: rgba(0, 217, 255, 0.1);
            border: 1px solid rgba(0, 217, 255, 0.2);
            border-radius: 20px;
            font-size: 0.8rem;
            color: var(--accent-cyan);
            font-family: 'JetBrains Mono', monospace;
        }

        /* Projects Section */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background: var(--bg-card);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.08);
            border-radius: 24px;
            overflow: hidden;
            transition: all 0.4s ease;
            position: relative;
        }

        .project-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 25px 70px rgba(0, 217, 255, 0.25);
            border-color: rgba(0, 217, 255, 0.4);
        }

        .project-image {
            width: 100%;
            height: 220px;
            background: linear-gradient(135deg, rgba(0, 217, 255, 0.2), rgba(157, 127, 255, 0.2));
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
            position: relative;
            overflow: hidden;
        }

        .project-image::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at center, transparent 30%, rgba(15, 20, 25, 0.6) 100%);
        }

        .project-content {
            padding: 2rem;
        }

        .project-card h3 {
            font-size: 1.5rem;
            margin-bottom: 0.8rem;
            font-weight: 600;
        }

        .project-card p {
            color: var(--text-secondary);
            margin-bottom: 1.5rem;
            line-height: 1.7;
        }

        .project-links {
            display: flex;
            gap: 1rem;
        }

        .project-link {
            padding: 0.6rem 1.5rem;
            background: rgba(0, 217, 255, 0.1);
            border: 1px solid rgba(0, 217, 255, 0.3);
            border-radius: 10px;
            color: var(--accent-cyan);
            text-decoration: none;
            font-size: 0.9rem;
            font-weight: 500;
            transition: all 0.3s ease;
        }

        .project-link:hover {
            background: rgba(0, 217, 255, 0.2);
            border-color: var(--accent-cyan);
            transform: translateY(-2px);
        }

        /* Contact Section */
        .contact-content {
            max-width: 700px;
            margin: 0 auto;
            background: var(--bg-card);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.08);
            border-radius: 30px;
            padding: 4rem;
            box-shadow: 0 30px 80px rgba(0, 0, 0, 0.3);
        }

        .contact-info {
            text-align: center;
            margin-bottom: 3rem;
        }

        .contact-info h3 {
            font-size: 2rem;
            margin-bottom: 1rem;
        }

        .contact-info p {
            color: var(--text-secondary);
            font-size: 1.1rem;
        }

        .contact-methods {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1.5rem;
            margin-top: 3rem;
        }

        .contact-method {
            background: rgba(0, 217, 255, 0.05);
            border: 1px solid rgba(0, 217, 255, 0.2);
            border-radius: 16px;
            padding: 2rem 1.5rem;
            text-align: center;
            text-decoration: none;
            color: var(--text-primary);
            transition: all 0.3s ease;
        }

        .contact-method:hover {
            background: rgba(0, 217, 255, 0.1);
            border-color: var(--accent-cyan);
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(0, 217, 255, 0.2);
        }

        .contact-icon {
            font-size: 2rem;
            margin-bottom: 1rem;
            display: block;
        }

        .contact-method span {
            display: block;
            font-size: 0.9rem;
            color: var(--text-secondary);
            margin-bottom: 0.5rem;
        }

        .contact-method strong {
            font-size: 1rem;
            color: var(--accent-cyan);
        }

        /* Footer */
        footer {
            padding: 3rem 0;
            text-align: center;
            border-top: 1px solid rgba(255, 255, 255, 0.05);
            margin-top: 4rem;
        }

        footer p {
            color: var(--text-secondary);
            font-size: 0.95rem;
        }

        .social-links {
            display: flex;
            gap: 1.5rem;
            justify-content: center;
            margin-bottom: 2rem;
        }

        .social-link {
            width: 50px;
            height: 50px;
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--text-secondary);
            font-size: 1.3rem;
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .social-link:hover {
            background: rgba(0, 217, 255, 0.1);
            border-color: var(--accent-cyan);
            color: var(--accent-cyan);
            transform: translateY(-3px);
        }

        /* Responsive */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.5rem;
            }

            h2 {
                font-size: 2rem;
            }

            .hero {
                padding: 4rem 0 3rem;
            }

            .nav-links {
                gap: 1.5rem;
            }

            .skills-grid,
            .projects-grid {
                grid-template-columns: 1fr;
            }

            .contact-content {
                padding: 2.5rem 1.5rem;
            }

            .cta-buttons {
                flex-direction: column;
            }

            .btn {
                width: 100%;
            }
        }

        /* Scroll animations */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            animation: fadeInUp 0.8s ease-out forwards;
        }

        .fade-in:nth-child(1) { animation-delay: 0.1s; }
        .fade-in:nth-child(2) { animation-delay: 0.2s; }
        .fade-in:nth-child(3) { animation-delay: 0.3s; }
        .fade-in:nth-child(4) { animation-delay: 0.4s; }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="container">
            <div class="logo">Portfolio</div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container">
            <div class="hero-content">
                <div class="hero-badge">✨ Tersedia untuk Proyek Baru</div>
                <h1>Developer & Designer Digital Kreatif</h1>
                <p>Welcome to My Portfolio
Halo, saya M. Syahril Romadhon, pelajar SMK Negeri 1 Bangsri dengan keahlian di bidang desain dan coding.
Portofolio ini berisi karya, proyek, serta hasil pembelajaran yang saya kerjakan selama proses belajar.
Saya terus berusaha mengembangkan kemampuan dan pengalaman di dunia kreatif dan teknologi.</p>
                <div class="cta-buttons">
                    <a href="#projects" class="btn btn-primary">Lihat Karya Saya</a>
                    <a href="#contact" class="btn btn-secondary">Hubungi Saya</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills">
        <div class="container">
            <div class="section-header">
                <div class="section-tag">Keahlian</div>
                <h2>Apa yang Saya Kuasai</h2>
                <p class="section-description">Kombinasi keterampilan teknis dan kreatif untuk menghadirkan solusi digital terbaik</p>
            </div>
            <div class="skills-grid">
                <div class="skill-card fade-in">
                    <div class="skill-icon">💻</div>
                    <h3>Frontend Development</h3>
                    <p>Membangun antarmuka web yang responsif dan interaktif dengan performa optimal menggunakan teknologi terkini.</p>
                    <div class="skill-tags">
                        <span class="tag">HTML</span>
                        <span class="tag">CSS</span>
                        <span class="tag">JavaScript</span>
                    </div>
                </div>

                <div class="skill-card fade-in">
                    <div class="skill-icon">⚙️</div>
                    <h3>Backend Development</h3>
                    <p>Mengembangkan API yang kuat dan skalabel dengan arsitektur yang bersih dan maintainable.</p>
                    <div class="skill-tags">
                        <span class="tag">Node.js</span>
                        <span class="tag">Php</span>
                        <span class="tag">MariaDB</span>
                        <span class="tag">MongoDB</span>
                    </div>
                </div>

                <div class="skill-card fade-in">
                    <div class="skill-icon">🎨</div>
                    <h3>UI/UX Design</h3>
                    <p>Merancang pengalaman pengguna yang intuitif dengan estetika modern dan prinsip desain yang solid.</p>
                    <div class="skill-tags">
                        <span class="tag">Figma</span>
                        <span class="tag">Adobe XD</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects">
        <div class="container">
            <div class="section-header">
                <div class="section-tag">Portfolio</div>
                <h2>Proyek Terbaru</h2>
                <p class="section-description">Koleksi proyek yang telah saya kerjakan dengan teknologi modern</p>
            </div>
            <div class="projects-grid">
                <div class="project-card fade-in">
                    <div class="project-image"><img src="images/Cuplikan layar 2026-02-03 184808.png" alt=""></div>
                    <div class="project-content">
                        <h3>E-Commerce Platform</h3>
                        <p>Platform e-commerce Sepatu full-featured </p>
                        <div class="project-links">
                            <a href="E commerce/index.html" class="project-link">Live Demo</a>
                            <a href="https://github.com/zuiqua827" class="project-link">GitHub</a>
                        </div>
                    </div>
                </div>

                <div class="project-card fade-in">
                    <div class="project-image"><img src="images/application.png" alt=""></div>
                    <div class="project-content">
                        <h3> Media App</h3>
                        <p>Aplikasi social media dengan fitur real-time messaging, stories, dan feed algorithm yang dipersonalisasi.</p>
                        <div class="project-links">
                            <a href="https://www.figma.com/design/LhZNAbGDtaRVAPB9xVubrQ/PORTOFOLIO?node-id=100-408&t=X7GBR5Kv5K0FiXzK-1" class="project-link">Live Demo</a>
                            <a href="https://github.com/zuiqua827" class="project-link">GitHub</a>
                        </div>
                    </div>
                </div>

                <div class="project-card fade-in">
                    <div class="project-image"><img src="images/dashboard.png" alt=""></div>
                    <div class="project-content">
                        <h3>Analytics Dashboard</h3>
                        <p>Dashboard analytics yang powerful dengan visualisasi data interaktif dan reporting otomatis untuk business intelligence.</p>
                        <div class="project-links">
                            <a href="https://www.figma.com/design/LhZNAbGDtaRVAPB9xVubrQ/PORTOFOLIO?node-id=100-2&t=X7GBR5Kv5K0FiXzK-1" class="project-link">Live Demo</a>
                            <a href="https://github.com/zuiqua827" class="project-link">GitHub</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <div class="container">
            <div class="section-header">
                <div class="section-tag">Kontak</div>
                <h2>Mari Bekerja Sama</h2>
                <p class="section-description">Tertarik untuk berkolaborasi? Hubungi saya melalui channel di bawah ini</p>
            </div> 
            <div class="contact-content">
                <div class="contact-info">
                    <h3>Siap untuk Memulai</h3>
                    <p>Saya selalu terbuka untuk diskusi proyek baru, ide kreatif, atau kesempatan untuk menjadi bagian dari visi Anda.</p>
                </div>
                <div class="contact-methods">
                    <a href="mailto:hello@example.com" class="contact-method">
                        <span class="contact-icon"><i class="fa-solid fa-envelope"></i></span>
                        <span>Email</span>
                        <strong>ariljepara08@gmail.com</strong>
                    </a>
                    <a href="tel:+628123456789" class="contact-method">
                        <span class="contact-icon"><i class="fa-solid fa-phone"></i></span>
                        <span>Telepon</span>
                        <strong>+62 821-318-3341</strong>
                    </a>
                    <a href="https://github.com/zuiqua827" class="contact-method">
                        <span class="contact-icon"><i class="fa-brands fa-github"></i></span>
                        <span>GitHub</span>
                        <strong>/zuiqua827</strong>
                    </a>
                    <a href="https://www.instagram.com/ssyahril_r/saved/" class="contact-method">
                        <span class="contact-icon"><i class="fa-brands fa-instagram"></i></span>
                        <span>Instagram</span>
                        <strong>/ssyahril_r</strong>
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="social-links">
                <a href="https://www.instagram.com/ssyahril_r/saved/" class="social-link"><i class="fa-brands fa-instagram"></i></a>
                <a href="#" class="social-link"><i class="fa-solid fa-phone"></i></a>
                <a href="#" class="social-link"><i class="fa-solid fa-envelope"></i></a>
                <a href="https://github.com/zuiqua827" class="social-link"><i class="fa-brands fa-github"></i></a>
            </div>
            <p>&copy; 2026 Portfolio. Dibuat dengan passion dan kopi ☕</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Intersection Observer for scroll animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -100px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        document.querySelectorAll('.fade-in').forEach(el => {
            observer.observe(el);
        });

        // Add active state to navigation
        const sections = document.querySelectorAll('section');
        const navLinks = document.querySelectorAll('.nav-links a');

        window.addEventListener('scroll', () => {
            let current = '';
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                if (scrollY >= sectionTop - 200) {
                    current = section.getAttribute('id');
                }
            });

            navLinks.forEach(link => {
                link.style.color = '';
                if (link.getAttribute('href').slice(1) === current) {
                    link.style.color = 'var(--text-primary)';
                }
            });
        });
    </script>
</body>
</html>
