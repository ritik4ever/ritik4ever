<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ritik Patel - GitHub Profile</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;600;700&family=Inter:wght@300;400;500;600;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: linear-gradient(135deg, #0f0f23 0%, #1a1a2e 50%, #16213e 100%);
            color: #e4e4e7;
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }

        /* Animated Header */
        .header {
            text-align: center;
            padding: 4rem 0;
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(79, 70, 229, 0.1), transparent);
            animation: shimmer 3s infinite;
        }

        @keyframes shimmer {
            0% { left: -100%; }
            100% { left: 100%; }
        }

        .hero-title {
            font-size: clamp(3rem, 8vw, 6rem);
            font-weight: 700;
            background: linear-gradient(135deg, #60a5fa, #a78bfa, #f472b6);
            background-clip: text;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 1rem;
            animation: glow 2s ease-in-out infinite alternate;
        }

        @keyframes glow {
            from { filter: drop-shadow(0 0 20px rgba(96, 165, 250, 0.3)); }
            to { filter: drop-shadow(0 0 30px rgba(167, 139, 250, 0.5)); }
        }

        .subtitle {
            font-size: 1.5rem;
            color: #a1a1aa;
            margin-bottom: 2rem;
            font-weight: 300;
        }

        .highlight {
            color: #60a5fa;
            font-weight: 600;
        }

        /* Stats Cards */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            margin: 4rem 0;
        }

        .stat-card {
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            padding: 2rem;
            text-align: center;
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .stat-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: linear-gradient(90deg, #60a5fa, #a78bfa, #f472b6);
        }

        .stat-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(96, 165, 250, 0.2);
            border-color: rgba(96, 165, 250, 0.3);
        }

        .stat-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
            display: block;
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: 700;
            color: #60a5fa;
            font-family: 'JetBrains Mono', monospace;
        }

        .stat-label {
            color: #a1a1aa;
            font-size: 1.1rem;
            margin-top: 0.5rem;
        }

        /* Tech Stack */
        .section {
            margin: 5rem 0;
        }

        .section-title {
            font-size: 2.5rem;
            font-weight: 700;
            text-align: center;
            margin-bottom: 3rem;
            background: linear-gradient(135deg, #60a5fa, #a78bfa);
            background-clip: text;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 1.5rem;
            margin: 3rem 0;
        }

        .tech-item {
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            padding: 1.5rem;
            text-align: center;
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
        }

        .tech-item:hover {
            transform: scale(1.05);
            background: rgba(96, 165, 250, 0.1);
            border-color: rgba(96, 165, 250, 0.3);
        }

        .tech-icon {
            width: 60px;
            height: 60px;
            margin: 0 auto 1rem;
            background: linear-gradient(135deg, #60a5fa, #a78bfa);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            color: white;
            font-weight: 600;
        }

        /* Projects */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
            gap: 2rem;
            margin: 3rem 0;
        }

        .project-card {
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            padding: 2rem;
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: linear-gradient(90deg, #10b981, #06b6d4, #8b5cf6);
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.3);
        }

        .project-title {
            font-size: 1.5rem;
            font-weight: 600;
            margin-bottom: 1rem;
            color: #60a5fa;
        }

        .project-description {
            color: #a1a1aa;
            margin-bottom: 1.5rem;
        }

        .project-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-bottom: 1.5rem;
        }

        .tag {
            background: rgba(96, 165, 250, 0.2);
            color: #60a5fa;
            padding: 0.3rem 0.8rem;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 500;
        }

        .project-links {
            display: flex;
            gap: 1rem;
        }

        .project-link {
            background: linear-gradient(135deg, #60a5fa, #a78bfa);
            color: white;
            padding: 0.8rem 1.5rem;
            border-radius: 10px;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
        }

        .project-link:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 20px rgba(96, 165, 250, 0.3);
        }

        /* Experience */
        .experience-item {
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            padding: 2rem;
            margin: 2rem 0;
            backdrop-filter: blur(10px);
            position: relative;
        }

        .experience-item::before {
            content: '';
            position: absolute;
            left: 0;
            top: 0;
            bottom: 0;
            width: 4px;
            background: linear-gradient(180deg, #60a5fa, #a78bfa);
            border-radius: 0 4px 4px 0;
        }

        .experience-title {
            font-size: 1.5rem;
            font-weight: 600;
            color: #60a5fa;
            margin-bottom: 0.5rem;
        }

        .experience-company {
            font-size: 1.2rem;
            color: #f472b6;
            margin-bottom: 0.5rem;
        }

        .experience-date {
            color: #a1a1aa;
            font-size: 0.9rem;
            margin-bottom: 1rem;
        }

        /* Contact */
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1.5rem;
            margin: 3rem 0;
        }

        .contact-item {
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            padding: 1.5rem;
            text-align: center;
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
        }

        .contact-item:hover {
            transform: translateY(-5px);
            background: rgba(96, 165, 250, 0.1);
            border-color: rgba(96, 165, 250, 0.3);
        }

        .contact-icon {
            font-size: 2rem;
            margin-bottom: 1rem;
            color: #60a5fa;
        }

        .contact-link {
            color: #e4e4e7;
            text-decoration: none;
            font-weight: 500;
        }

        .contact-link:hover {
            color: #60a5fa;
        }

        /* GitHub Stats */
        .github-stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin: 3rem 0;
        }

        .github-stat {
            text-align: center;
        }

        .github-stat img {
            width: 100%;
            height: auto;
            border-radius: 15px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        /* Responsive */
        @media (max-width: 768px) {
            .projects-grid {
                grid-template-columns: 1fr;
            }
            
            .hero-title {
                font-size: 3rem;
            }
            
            .container {
                padding: 1rem;
            }
        }

        /* Animations */
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

        .animate-fadeInUp {
            animation: fadeInUp 0.6s ease-out;
        }

        /* Floating elements */
        .floating {
            animation: float 3s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <div class="header">
            <h1 class="hero-title">RITIK PATEL</h1>
            <p class="subtitle">
                🚀 <span class="highlight">Full-Stack Developer</span> | 
                ⛓️ <span class="highlight">Web3 Engineer</span> | 
                🏆 <span class="highlight">Hackathon Winner</span>
            </p>
            <p style="font-size: 1.2rem; color: #a1a1aa; max-width: 600px; margin: 0 auto;">
                Building the decentralized future with cutting-edge blockchain solutions and scalable web applications
            </p>
        </div>

        <!-- Stats -->
        <div class="stats-grid">
            <div class="stat-card floating">
                <span class="stat-icon">🏆</span>
                <div class="stat-number">TOP 25</div>
                <div class="stat-label">HackHazard 2025<br>(15,000+ participants)</div>
            </div>
            <div class="stat-card floating" style="animation-delay: 0.2s;">
                <span class="stat-icon">💼</span>
                <div class="stat-number">SDE</div>
                <div class="stat-label">Intern at Razorpay<br>Fintech Experience</div>
            </div>
            <div class="stat-card floating" style="animation-delay: 0.4s;">
                <span class="stat-icon">📊</span>
                <div class="stat-number">8.4</div>
                <div class="stat-label">GPA at PEC<br>Computer Science</div>
            </div>
            <div class="stat-card floating" style="animation-delay: 0.6s;">
                <span class="stat-icon">🌟</span>
                <div class="stat-number">15+</div>
                <div class="stat-label">Full-Stack Projects<br>Client Deliveries</div>
            </div>
        </div>

        <!-- Tech Stack -->
        <div class="section">
            <h2 class="section-title">🛠️ Tech Arsenal</h2>
            <div class="tech-grid">
                <div class="tech-item">
                    <div class="tech-icon">TS</div>
                    <div>TypeScript</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">⚛️</div>
                    <div>React/Next.js</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🟢</div>
                    <div>Node.js</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">⛓️</div>
                    <div>Solidity</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🦀</div>
                    <div>Rust</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🐘</div>
                    <div>PostgreSQL</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">🍃</div>
                    <div>MongoDB</div>
                </div>
                <div class="tech-item">
                    <div class="tech-icon">☁️</div>
                    <div>AWS</div>
                </div>
            </div>
        </div>

        <!-- Featured Projects -->
        <div class="section">
            <h2 class="section-title">🚀 Featured Projects</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <h3 class="project-title">🔒 Smart Contract Vulnerability Detector</h3>
                    <p class="project-description">
                        Advanced security tool that scans smart contract source code for known vulnerabilities, 
                        detects exploitable patterns, and provides early warnings before deployment.
                    </p>
                    <div class="project-tags">
                        <span class="tag">Python</span>
                        <span class="tag">Next.js</span>
                        <span class="tag">Solidity</span>
                        <span class="tag">Security</span>
                    </div>
                    <div class="project-links">
                        <a href="#" class="project-link">🌐 Live Demo</a>
                        <a href="#" class="project-link">📂 GitHub</a>
                    </div>
                </div>

                <div class="project-card">
                    <h3 class="project-title">✈️ Crypto-Travel Platform</h3>
                    <p class="project-description">
                        Decentralized travel booking platform enabling crypto payments, NFT-based rewards, 
                        blockchain identity verification, and tokenized travel experiences.
                    </p>
                    <div class="project-tags">
                        <span class="tag">Next.js</span>
                        <span class="tag">Solidity</span>
                        <span class="tag">Web3</span>
                        <span class="tag">NFTs</span>
                    </div>
                    <div class="project-links">
                        <a href="#" class="project-link">🌐 Live Demo</a>
                        <a href="#" class="project-link">📂 GitHub</a>
                    </div>
                </div>

                <div class="project-card">
                    <h3 class="project-title">⛏️ Crypto Mining Game (HackHazard Winner)</h3>
                    <p class="project-description">
                        Award-winning blockchain game built on Monad network that secured Top 25 position 
                        among 15,000+ participants at HackHazard 2025.
                    </p>
                    <div class="project-tags">
                        <span class="tag">Monad</span>
                        <span class="tag">GameFi</span>
                        <span class="tag">Blockchain</span>
                        <span class="tag">Award Winner</span>
                    </div>
                    <div class="project-links">
                        <a href="#" class="project-link">🎮 Play Game</a>
                        <a href="#" class="project-link">📂 GitHub</a>
                    </div>
                </div>
            </div>
        </div>

        <!-- Experience -->
        <div class="section">
            <h2 class="section-title">💼 Experience</h2>
            
            <div class="experience-item">
                <h3 class="experience-title">Software Development Engineer Intern</h3>
                <div class="experience-company">🏦 Razorpay</div>
                <div class="experience-date">Oct 2024 - Dec 2024</div>
                <p>Developed and maintained backend services using TypeScript and PostgreSQL, contributing to robust fintech solutions. Collaborated with cross-functional teams to deliver impactful features and enhanced system performance in a fast-paced environment.</p>
            </div>

            <div class="experience-item">
                <h3 class="experience-title">Full-Stack Developer (Freelance)</h3>
                <div class="experience-company">🌐 Various Clients</div>
                <div class="experience-date">Ongoing</div>
                <p>Delivered 15+ end-to-end projects using MERN stack, Next.js, and crypto integrations. Built scalable web applications with focus on performance, security, and modern UI/UX principles.</p>
            </div>

            <div class="experience-item">
                <h3 class="experience-title">Open Source Contributor</h3>
                <div class="experience-company">🔗 Web3 Ecosystem</div>
                <div class="experience-date">Ongoing</div>
                <p>Active contributor to OnlyDust, StarkNet, StarkCairo, and Nethermind projects. Focused on smart contract development, zero-knowledge proofs, and developer tooling.</p>
            </div>
        </div>

        <!-- GitHub Stats -->
        <div class="section">
            <h2 class="section-title">📊 GitHub Analytics</h2>
            <div class="github-stats">
                <div class="github-stat">
                    <img src="https://github-readme-stats.vercel.app/api?username=ritik4ever&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0d1117" alt="GitHub Stats">
                </div>
                <div class="github-stat">
                    <img src="https://github-readme-streak-stats.herokuapp.com/?user=ritik4ever&theme=tokyonight&hide_border=true&background=0d1117" alt="GitHub Streak">
                </div>
                <div class="github-stat">
                    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=ritik4ever&layout=compact&theme=tokyonight&hide_border=true&bg_color=0d1117" alt="Top Languages">
                </div>
            </div>
        </div>

        <!-- Contact -->
        <div class="section">
            <h2 class="section-title">📬 Let's Connect</h2>
            <div class="contact-grid">
                <div class="contact-item">
                    <div class="contact-icon">📧</div>
                    <a href="mailto:ritikverma0050@gmail.com" class="contact-link">
                        ritikverma0050@gmail.com
                    </a>
                </div>
                <div class="contact-item">
                    <div class="contact-icon">📱</div>
                    <a href="tel:+918887555059" class="contact-link">
                        +91-8887555059
                    </a>
                </div>
                <div class="contact-item">
                    <div class="contact-icon">💼</div>
                    <a href="https://www.linkedin.com/in/ritik-patel-3b15b2327/" class="contact-link">
                        LinkedIn Profile
                    </a>
                </div>
                <div class="contact-item">
                    <div class="contact-icon">🐙</div>
                    <a href="https://github.com/ritik4ever" class="contact-link">
                        GitHub Profile
                    </a>
                </div>
            </div>
        </div>

        <!-- Footer -->
        <div style="text-align: center; margin: 4rem 0 2rem; padding: 2rem 0; border-top: 1px solid rgba(255, 255, 255, 0.1);">
            <p style="color: #a1a1aa; font-size: 1.1rem;">
                🌟 <strong>Always building, always learning, always innovating</strong> 🌟
            </p>
            <p style="color: #71717a; font-size: 0.9rem; margin-top: 1rem;">
                "Code is poetry written in logic" - Let's create something amazing together!
            </p>
        </div>
    </div>

    <script>
        // Add scroll animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -100px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('animate-fadeInUp');
                }
            });
        }, observerOptions);

        // Observe all sections
        document.querySelectorAll('.section, .stat-card, .project-card, .experience-item').forEach(el => {
            observer.observe(el);
        });

        // Add typing effect to subtitle
        const subtitle = document.querySelector('.subtitle');
        const text = subtitle.innerHTML;
        subtitle.innerHTML = '';
        let i = 0;

        function typeWriter() {
            if (i < text.length) {
                subtitle.innerHTML += text.charAt(i);
                i++;
                setTimeout(typeWriter, 50);
            }
        }

        setTimeout(typeWriter, 1000);
    </script>
</body>
</html>
