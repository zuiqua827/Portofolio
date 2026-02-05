<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>M. Syahril Romadhon - Frontend Developer & UI/UX Designer</title>
    <meta name="description" content="Portfolio M. Syahril Romadhon - Pelajar SMK jurusan RPL yang berfokus pada Frontend Development dan UI/UX Design. Lihat proyek dan karya saya.">
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
            padding: 1rem 2rem;
            border-radius: 12px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1rem;
            transition: all 0.3s ease;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
        }

        .btn-primary {
            background: linear-gradient(135deg, var(--accent-cyan), var(--accent-teal));
            color: var(--navy);
            box-shadow: 0 4px 20px var(--glow-cyan);
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 30px var(--glow-cyan);
        }

        .btn-secondary {
            background: transparent;
            color: var(--text-primary);
            border: 2px solid rgba(255, 255, 255, 0.1);
        }

        .btn-secondary:hover {
            border-color: var(--accent-cyan);
            background: rgba(0, 217, 255, 0.05);
        }

        /* Section Styling */
        section {
            padding: 6rem 0;
        }

        .section-header {
            text-align: center;
            margin-bottom: 4rem;
        }

        .section-tag {
            display: inline-block;
            padding: 0.4rem 1.2rem;
            background: rgba(157, 127, 255, 0.1);
            border: 1px solid rgba(157, 127, 255, 0.3);
            border-radius: 50px;
            font-size: 0.85rem;
            color: var(--accent-purple);
            margin-bottom: 1rem;
            font-weight: 600;
        }

        .section-header h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            background: linear-gradient(135deg, var(--text-primary), var(--accent-teal));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .section-description {
            font-size: 1.1rem;
            color: var(--text-secondary);
            max-width: 600px;
            margin: 0 auto;
        }

        /* Skills Grid */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .skill-card {
            background: var(--bg-card);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            padding: 2.5rem;
            transition: all 0.3s ease;
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
            background: linear-gradient(135deg, rgba(0, 217, 255, 0.05) 0%, transparent 50%);
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .skill-card:hover {
            transform: translateY(-10px);
            border-color: rgba(0, 217, 255, 0.3);
            box-shadow: 0 10px 40px rgba(0, 217, 255, 0.15);
        }

        .skill-card:hover::before {
            opacity: 1;
        }

        .skill-icon {
            font-size: 3rem;
            margin-bottom: 1.5rem;
        }

        .skill-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--text-primary);
        }

        .skill-card p {
            color: var(--text-secondary);
            margin-bottom: 1.5rem;
            line-height: 1.7;
        }

        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
        }

        .tag {
            padding: 0.4rem 1rem;
            background: rgba(0, 217, 255, 0.1);
            border: 1px solid rgba(0, 217, 255, 0.2);
            border-radius: 20px;
            font-size: 0.85rem;
            color: var(--accent-cyan);
            font-family: 'JetBrains Mono', monospace;
        }

        /* Projects Grid */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .project-card {
            background: var(--bg-card);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            overflow: hidden;
            transition: all 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-10px);
            border-color: rgba(0, 255, 200, 0.3);
            box-shadow: 0 10px 40px rgba(0, 255, 200, 0.15);
        }

        .project-image {
            width: 100%;
            height: 250px;
            background: linear-gradient(135deg, rgba(0, 217, 255, 0.1), rgba(157, 127, 255, 0.1));
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
        }

        .project-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.3s ease;
        }

        .project-card:hover .project-image img {
            transform: scale(1.1);
        }

        .project-content {
            padding: 2rem;
        }

        .project-content h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--text-primary);
        }

        .project-content p {
            color: var(--text-secondary);
            margin-bottom: 1.5rem;
            line-height: 1.7;
        }

        .project-links {
            display: flex;
            gap: 1rem;
        }

        .project-link {
            padding: 0.7rem 1.5rem;
            background: rgba(0, 217, 255, 0.1);
            border: 1px solid rgba(0, 217, 255, 0.3);
            border-radius: 10px;
            color: var(--accent-cyan);
            text-decoration: none;
            font-size: 0.9rem;
            transition: all 0.3s ease;
            font-family: 'JetBrains Mono', monospace;
        }

        .project-link:hover {
            background: rgba(0, 217, 255, 0.2);
            transform: translateY(-2px);
        }

        /* Contact Section */
        .contact-content {
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 3rem;
            margin-top: 3rem;
        }

        .contact-info h3 {
            font-size: 2rem;
            margin-bottom: 1rem;
            background: linear-gradient(135deg, var(--accent-cyan), var(--accent-teal));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .contact-info p {
            color: var(--text-secondary);
            line-height: 1.8;
        }

        .contact-methods {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
        }

        .contact-method {
            background: var(--bg-card);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 1.5rem;
            text-decoration: none;
            display: flex;
            flex-direction: column;
            gap: 0.5rem;
            transition: all 0.3s ease;
        }

        .contact-method:hover {
            transform: translateY(-5px);
            border-color: rgba(0, 217, 255, 0.3);
            box-shadow: 0 5px 20px rgba(0, 217, 255, 0.15);
        }

        .contact-icon {
            font-size: 1.5rem;
            color: var(--accent-cyan);
        }

        .contact-method span {
            color: var(--text-secondary);
            font-size: 0.9rem;
        }

        .contact-method strong {
            color: var(--text-primary);
            font-size: 1rem;
        }

        /* Footer */
        footer {
            padding: 3rem 0;
            border-top: 1px solid rgba(255, 255, 255, 0.05);
            text-align: center;
        }

        .social-links {
            display: flex;
            gap: 1rem;
            justify-content: center;
            margin-bottom: 1.5rem;
        }

        .social-link {
            width: 50px;
            height: 50px;
            background: var(--bg-card);
            border: 1px solid rgba(255, 255, 255, 0.05);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--text-secondary);
            text-decoration: none;
            font-size: 1.2rem;
            transition: all 0.3s ease;
        }

        .social-link:hover {
            border-color: var(--accent-cyan);
            color: var(--accent-cyan);
            transform: translateY(-5px);
        }

        footer p {
            color: var(--text-secondary);
            font-size: 0.9rem;
        }

        /* Animations */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s ease-out;
        }

        .fade-in:nth-child(1) { animation-delay: 0.1s; }
        .fade-in:nth-child(2) { animation-delay: 0.2s; }
        .fade-in:nth-child(3) { animation-delay: 0.3s; }
        .fade-in:nth-child(4) { animation-delay: 0.4s; }

        /* Responsive Design */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.5rem;
            }

            .hero p {
                font-size: 1rem;
            }

            .section-header h2 {
                font-size: 2rem;
            }

            .contact-content {
                grid-template-columns: 1fr;
            }

            .nav-links {
                gap: 1.5rem;
            }

            .skills-grid,
            .projects-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="container">
            <div class="logo">M. Syahril R.</div>
            <ul class="nav-links">
                <li><a href="#home">Beranda</a></li>
                <li><a href="#skills">Keahlian</a></li>
                <li><a href="#projects">Proyek</a></li>
                <li><a href="#contact">Kontak</a></li>
            </ul>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container">
            <div class="hero-content">
                <div class="hero-badge">✨ Siap Berkontribusi dalam Proyek Nyata</div>
                <h1>Frontend Developer & UI/UX Designer</h1>
                <p>Halo! Saya M. Syahril Romadhon, pelajar SMK Negeri 1 Bangsri jurusan Rekayasa Perangkat Lunak. Saya membangun pengalaman digital yang menarik dengan menggabungkan kode yang bersih dan desain yang intuitif. Dari konsep hingga implementasi, saya siap mengubah ide menjadi solusi web yang fungsional dan estetis.</p>
                <div class="cta-buttons">
                    <a href="#projects" class="btn btn-primary">
                        <i class="fas fa-folder-open"></i>
                        Lihat Portofolio
                    </a>
                    <a href="#contact" class="btn btn-secondary">
                        <i class="fas fa-envelope"></i>
                        Hubungi Saya
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills">
        <div class="container">
            <div class="section-header">
                <div class="section-tag">Keahlian Teknis</div>
                <h2>Teknologi yang Saya Gunakan</h2>
                <p class="section-description">Stack teknologi yang saya kuasai untuk membangun solusi web modern dan responsif</p>
            </div>
            <div class="skills-grid">
                <div class="skill-card fade-in">
                    <div class="skill-icon">💻</div>
                    <h3>Frontend Development</h3>
                    <p>Mengembangkan antarmuka web yang responsif dan interaktif dengan fokus pada performa dan user experience. Saya menulis kode yang bersih, terstruktur, dan mudah di-maintain dengan menerapkan best practices dalam setiap proyek.</p>
                    <div class="skill-tags">
                        <span class="tag">HTML5</span>
                        <span class="tag">CSS3</span>
                        <span class="tag">JavaScript</span>
                        <span class="tag">Responsive Design</span>
                    </div>
                </div>

                <div class="skill-card fade-in">
                    <div class="skill-icon">⚙️</div>
                    <h3>Backend Development</h3>
                    <p>Membangun logika server-side dan database yang solid untuk mendukung aplikasi web. Saya belajar arsitektur RESTful API dan manajemen database untuk menciptakan sistem yang scalable dan efisien.</p>
                    <div class="skill-tags">
                        <span class="tag">Node.js</span>
                        <span class="tag">PHP</span>
                        <span class="tag">MariaDB</span>
                        <span class="tag">MongoDB</span>
                    </div>
                </div>

                <div class="skill-card fade-in">
                    <div class="skill-icon">🎨</div>
                    <h3>UI/UX Design</h3>
                    <p>Merancang interface yang tidak hanya cantik, tapi juga intuitif dan user-friendly. Saya menerapkan design thinking dan prinsip visual hierarchy untuk menciptakan pengalaman pengguna yang optimal dari wireframe hingga high-fidelity prototype.</p>
                    <div class="skill-tags">
                        <span class="tag">Figma</span>
                        <span class="tag">Adobe XD</span>
                        <span class="tag">Prototyping</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects">
        <div class="container">
            <div class="section-header">
                <div class="section-tag">Karya Terpilih</div>
                <h2>Proyek yang Pernah Saya Kerjakan</h2>
                <p class="section-description">Setiap proyek adalah kesempatan belajar untuk mengasah skill dan memecahkan masalah nyata</p>
            </div>
            <div class="projects-grid">
                <div class="project-card fade-in">
                    <div class="project-image"><img src="images/Cuplikan layar 2026-02-03 184808.png" alt="E-Commerce Sepatu"></div>
                    <div class="project-content">
                        <h3>Platform E-Commerce Sepatu</h3>
                        <p><strong>Tantangan:</strong> Membuat toko online yang mudah dinavigasi dengan katalog produk yang terorganisir.<br>
                        <strong>Solusi:</strong> Membangun website e-commerce dengan sistem filter produk, shopping cart, dan checkout flow yang intuitif.<br>
                        <strong>Hasil:</strong> Interface yang clean dengan user experience yang smooth untuk meningkatkan conversion rate.</p>
                        <div class="project-links">
                            <a href="E commerce/index.html" class="project-link">
                                <i class="fas fa-external-link-alt"></i> Live Demo
                            </a>
                            <a href="https://github.com/zuiqua827" class="project-link">
                                <i class="fab fa-github"></i> GitHub
                            </a>
                        </div>
                    </div>
                </div>

                <div class="project-card fade-in">
                    <div class="project-image"><img src="images/application.png" alt="Social Media App"></div>
                    <div class="project-content">
                        <h3>Desain Social Media App</h3>
                        <p><strong>Tantangan:</strong> Merancang aplikasi social media yang engaging dengan fitur interaktif modern.<br>
                        <strong>Solusi:</strong> Membuat UI/UX design dengan feed algorithm, stories feature, dan real-time messaging menggunakan Figma dengan komponen yang reusable.<br>
                        <strong>Hasil:</strong> Prototype high-fidelity dengan flow yang natural dan visual design yang modern.</p>
                        <div class="project-links">
                            <a href="https://www.figma.com/design/LhZNAbGDtaRVAPB9xVubrQ/PORTOFOLIO?node-id=100-408&t=X7GBR5Kv5K0FiXzK-1" class="project-link">
                                <i class="fas fa-external-link-alt"></i> Lihat Desain
                            </a>
                            <a href="https://github.com/zuiqua827" class="project-link">
                                <i class="fab fa-github"></i> GitHub
                            </a>
                        </div>
                    </div>
                </div>

                <div class="project-card fade-in">
                    <div class="project-image"><img src="images/dashboard.png" alt="Analytics Dashboard"></div>
                    <div class="project-content">
                        <h3>Analytics Dashboard Design</h3>
                        <p><strong>Tantangan:</strong> Menyajikan data kompleks dalam bentuk visual yang mudah dipahami.<br>
                        <strong>Solusi:</strong> Merancang dashboard dengan data visualization yang informatif, layout yang terorganisir, dan navigasi yang efisien untuk business intelligence.<br>
                        <strong>Hasil:</strong> Interface dashboard yang clean dengan hierarchy informasi yang jelas untuk decision making.</p>
                        <div class="project-links">
                            <a href="https://www.figma.com/design/LhZNAbGDtaRVAPB9xVubrQ/PORTOFOLIO?node-id=100-2&t=X7GBR5Kv5K0FiXzK-1" class="project-link">
                                <i class="fas fa-external-link-alt"></i> Lihat Desain
                            </a>
                            <a href="https://github.com/zuiqua827" class="project-link">
                                <i class="fab fa-github"></i> GitHub
                            </a>
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
                <div class="section-tag">Mari Berkolaborasi</div>
                <h2>Hubungi Saya</h2>
                <p class="section-description">Saya terbuka untuk kesempatan magang, proyek freelance, atau sekadar diskusi tentang web development</p>
            </div>
            <div class="contact-content">
                <div class="contact-info">
                    <h3>Siap Bekerja Sama</h3>
                    <p>Sebagai junior developer yang antusias, saya selalu mencari peluang untuk belajar dan berkontribusi dalam proyek nyata. Mari kita wujudkan ide Anda menjadi kenyataan digital yang menarik!</p>
                </div>
                <div class="contact-methods">
                    <a href="mailto:syahril@example.com" class="contact-method">
                        <span class="contact-icon"><i class="fa-solid fa-envelope"></i></span>
                        <span>Email</span>
                        <strong>syahril@example.com</strong>
                    </a>
                    <a href="tel:+6282131831341" class="contact-method">
                        <span class="contact-icon"><i class="fa-solid fa-phone"></i></span>
                        <span>WhatsApp</span>
                        <strong>+62 821-3183-1341</strong>
                    </a>
                    <a href="https://github.com/zuiqua827" class="contact-method" target="_blank">
                        <span class="contact-icon"><i class="fa-brands fa-github"></i></span>
                        <span>GitHub</span>
                        <strong>/zuiqua827</strong>
                    </a>
                    <a href="https://www.instagram.com/ssyahril_r/" class="contact-method" target="_blank">
                        <span class="contact-icon"><i class="fa-brands fa-instagram"></i></span>
                        <span>Instagram</span>
                        <strong>@ssyahril_r</strong>
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="social-links">
                <a href="https://www.instagram.com/ssyahril_r/" class="social-link" target="_blank"><i class="fa-brands fa-instagram"></i></a>
                <a href="tel:+6282131831341" class="social-link"><i class="fa-solid fa-phone"></i></a>
                <a href="mailto:syahril@example.com" class="social-link"><i class="fa-solid fa-envelope"></i></a>
                <a href="https://github.com/zuiqua827" class="social-link" target="_blank"><i class="fa-brands fa-github"></i></a>
            </div>
            <p>&copy; 2026 M. Syahril Romadhon. Dibuat dengan dedikasi dan kopi ☕</p>
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
                link.classList.remove('active');
                if (link.getAttribute('href') === `#${current}`) {
                    link.classList.add('active');
                }
            });
        });
    </script>
</body>
</html>
