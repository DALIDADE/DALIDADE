<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Suwhan Atagulyyew - Backend & Flutter Developer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', 'Fira Code', 'Courier New', monospace;
            background: linear-gradient(135deg, #0a0e1a 0%, #0f1322 100%);
            color: #e4e6f0;
            line-height: 1.6;
            padding: 40px 20px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: rgba(15, 20, 35, 0.6);
            backdrop-filter: blur(10px);
            border-radius: 30px;
            padding: 40px;
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.5), 0 0 0 1px rgba(66, 153, 225, 0.1);
            animation: fadeInUp 0.8s ease-out;
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

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }

        @keyframes glow {
            0%, 100% { text-shadow: 0 0 5px rgba(44, 156, 255, 0.3); }
            50% { text-shadow: 0 0 20px rgba(44, 156, 255, 0.6); }
        }

        @keyframes slideIn {
            from {
                opacity: 0;
                transform: translateX(-30px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        .header {
            text-align: center;
            margin-bottom: 50px;
        }

        .avatar {
            width: 120px;
            height: 120px;
            margin: 0 auto 20px;
            background: linear-gradient(135deg, #2C9CFF, #6c5ce7);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 48px;
            animation: float 3s ease-in-out infinite;
            box-shadow: 0 10px 30px rgba(44, 156, 255, 0.3);
        }

        .typing-text {
            font-size: 2.5rem;
            font-weight: bold;
            background: linear-gradient(135deg, #2C9CFF, #a855f7);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            margin-bottom: 10px;
            animation: glow 2s ease-in-out infinite;
        }

        .subtitle {
            font-size: 1.2rem;
            color: #8b92b0;
            margin-top: 10px;
        }

        .badge-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 12px;
            margin: 30px 0;
        }

        .badge {
            padding: 8px 20px;
            background: rgba(44, 156, 255, 0.1);
            border: 1px solid rgba(44, 156, 255, 0.3);
            border-radius: 50px;
            font-size: 0.9rem;
            font-weight: 500;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .badge:hover {
            transform: translateY(-3px);
            background: rgba(44, 156, 255, 0.2);
            border-color: #2C9CFF;
            box-shadow: 0 5px 15px rgba(44, 156, 255, 0.2);
        }

        .section {
            margin: 40px 0;
            animation: slideIn 0.6s ease-out;
            animation-fill-mode: both;
        }

        .section:nth-child(2) { animation-delay: 0.1s; }
        .section:nth-child(3) { animation-delay: 0.2s; }
        .section:nth-child(4) { animation-delay: 0.3s; }
        .section:nth-child(5) { animation-delay: 0.4s; }
        .section:nth-child(6) { animation-delay: 0.5s; }

        .section-title {
            font-size: 1.8rem;
            margin-bottom: 25px;
            position: relative;
            display: inline-block;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -8px;
            left: 0;
            width: 60%;
            height: 3px;
            background: linear-gradient(90deg, #2C9CFF, #a855f7);
            border-radius: 3px;
        }

        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 30px;
            margin: 30px 0;
        }

        .tech-item {
            text-align: center;
            transition: all 0.3s ease;
            filter: grayscale(0%);
        }

        .tech-item:hover {
            transform: translateY(-8px) scale(1.05);
        }

        .tech-item img {
            width: 60px;
            height: 60px;
            filter: drop-shadow(0 5px 15px rgba(44, 156, 255, 0.3));
        }

        .grid-2 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
            margin: 20px 0;
        }

        .card {
            background: rgba(20, 25, 45, 0.6);
            backdrop-filter: blur(5px);
            border-radius: 20px;
            padding: 25px;
            border: 1px solid rgba(44, 156, 255, 0.2);
            transition: all 0.3s ease;
        }

        .card:hover {
            transform: translateY(-5px);
            border-color: rgba(44, 156, 255, 0.5);
            box-shadow: 0 10px 30px rgba(44, 156, 255, 0.1);
        }

        .card h3 {
            color: #2C9CFF;
            margin-bottom: 15px;
            font-size: 1.3rem;
        }

        .card ul {
            list-style: none;
            padding-left: 0;
        }

        .card li {
            padding: 8px 0;
            padding-left: 20px;
            position: relative;
        }

        .card li::before {
            content: '▹';
            position: absolute;
            left: 0;
            color: #2C9CFF;
        }

        .stats-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            margin: 30px 0;
        }

        .stat-card {
            background: linear-gradient(135deg, rgba(44, 156, 255, 0.1), rgba(168, 85, 247, 0.1));
            border-radius: 20px;
            padding: 20px;
            text-align: center;
            flex: 1;
            min-width: 200px;
            border: 1px solid rgba(44, 156, 255, 0.3);
            transition: all 0.3s ease;
        }

        .stat-card:hover {
            transform: scale(1.05);
            background: linear-gradient(135deg, rgba(44, 156, 255, 0.2), rgba(168, 85, 247, 0.2));
        }

        .stat-number {
            font-size: 2rem;
            font-weight: bold;
            color: #2C9CFF;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 30px 0;
        }

        .social-btn {
            padding: 12px 30px;
            background: rgba(44, 156, 255, 0.1);
            border: 1px solid rgba(44, 156, 255, 0.3);
            border-radius: 50px;
            text-decoration: none;
            color: #e4e6f0;
            font-weight: 500;
            transition: all 0.3s ease;
            display: inline-flex;
            align-items: center;
            gap: 10px;
        }

        .social-btn:hover {
            transform: translateY(-3px);
            background: rgba(44, 156, 255, 0.2);
            border-color: #2C9CFF;
            box-shadow: 0 5px 20px rgba(44, 156, 255, 0.3);
            color: white;
        }

        .footer {
            text-align: center;
            margin-top: 50px;
            padding-top: 30px;
            border-top: 1px solid rgba(44, 156, 255, 0.2);
            color: #8b92b0;
        }

        @media (max-width: 768px) {
            .container {
                padding: 20px;
            }
            .typing-text {
                font-size: 1.5rem;
            }
            .tech-item img {
                width: 45px;
                height: 45px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header Section -->
        <div class="header">
            <div class="avatar">
                💻
            </div>
            <div class="typing-text">
                Suwhan Atagulyyew
            </div>
            <div class="subtitle">
                Backend & API Developer | Flutter Developer
            </div>
        </div>

        <!-- Badges Section -->
        <div class="badge-container">
            <span class="badge">🐍 Python</span>
            <span class="badge">⚡ Django</span>
            <span class="badge">📱 Flutter</span>
            <span class="badge">🎯 Dart</span>
            <span class="badge">🗄️ PostgreSQL</span>
            <span class="badge">🔧 Django REST</span>
            <span class="badge">🐙 Git</span>
            <span class="badge">🚀 API Developer</span>
        </div>

        <!-- About Me Section -->
        <div class="section">
            <h2 class="section-title">🚀 About Me</h2>
            <div class="card">
                <p style="font-size: 1.1rem; margin-bottom: 15px;">
                    👋 Hi, I'm <strong style="color: #2C9CFF;">Suwhan Atagulyyew</strong> - a passionate developer who loves building 
                    scalable backend systems and beautiful cross-platform mobile applications.
                </p>
                <ul>
                    <li>💻 Backend & API Developer specializing in Python/Django</li>
                    <li>📱 Flutter Developer creating cross-platform mobile apps</li>
                    <li>🔧 Building scalable REST APIs and microservices</li>
                    <li>💪 Passionate about coding, fitness, and continuous learning</li>
                    <li>🌍 Based in Turkmenistan, working globally</li>
                </ul>
            </div>
        </div>

        <!-- Tech Stack Section -->
        <div class="section">
            <h2 class="section-title">🛠️ Tech Stack</h2>
            <div class="tech-stack">
                <div class="tech-item">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/c/c3/Python-logo-notext.svg" alt="Python">
                    <div>Python</div>
                </div>
                <div class="tech-item">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/4/45/Django_logo.png" alt="Django">
                    <div>Django</div>
                </div>
                <div class="tech-item">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/7/7e/Dart-logo.png" alt="Dart">
                    <div>Dart</div>
                </div>
                <div class="tech-item">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/1/17/Google-flutter-logo.png" alt="Flutter">
                    <div>Flutter</div>
                </div>
                <div class="tech-item">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/2/29/Postgresql_elephant.svg" alt="PostgreSQL">
                    <div>PostgreSQL</div>
                </div>
                <div class="tech-item">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/3/3f/Git_icon.svg" alt="Git">
                    <div>Git</div>
                </div>
            </div>
        </div>

        <!-- Expertise Section -->
        <div class="section">
            <h2 class="section-title">📊 My Expertise</h2>
            <div class="grid-2">
                <div class="card">
                    <h3>🔙 Backend Development</h3>
                    <ul>
                        <li>Python & Django</li>
                        <li>Django REST Framework</li>
                        <li>PostgreSQL & SQLite</li>
                        <li>RESTful API Design</li>
                        <li>Authentication & Authorization</li>
                        <li>JWT & OAuth2</li>
                    </ul>
                </div>
                <div class="card">
                    <h3>📱 Mobile Development</h3>
                    <ul>
                        <li>Flutter & Dart</li>
                        <li>Cross-platform Apps (iOS/Android)</li>
                        <li>State Management (Provider, Bloc)</li>
                        <li>REST API Integration</li>
                        <li>Firebase & Backend Services</li>
                        <li>Beautiful UI/UX Implementation</li>
                    </ul>
                </div>
            </div>
        </div>

        <!-- GitHub Stats Section -->
        <div class="section">
            <h2 class="section-title">📈 GitHub Stats</h2>
            <div class="stats-container">
                <div class="stat-card">
                    <div class="stat-number">20+</div>
                    <div>Projects Completed</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">100+</div>
                    <div>GitHub Commits</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">3+</div>
                    <div>Years Experience</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">10+</div>
                    <div>API's Developed</div>
                </div>
            </div>
            <div style="text-align: center; margin-top: 20px;">
                <img src="https://github-readme-stats.vercel.app/api?username=DALIDADE&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117" style="border-radius: 15px; margin: 10px; width: 48%;">
                <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=DALIDADE&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117" style="border-radius: 15px; margin: 10px; width: 48%;">
            </div>
        </div>

        <!-- Currently Learning Section -->
        <div class="section">
            <h2 class="section-title">🌱 Currently Learning</h2>
            <div class="card">
                <ul>
                    <li>Advanced Flutter & State Management (Bloc, Riverpod)</li>
                    <li>Microservices Architecture & Docker</li>
                    <li>FastAPI & GraphQL</li>
                    <li>Go Programming Language</li>
                    <li>Cloud Services (AWS, Firebase)</li>
                </ul>
            </div>
        </div>

        <!-- Connect Section -->
        <div class="section">
            <h2 class="section-title">📫 Connect With Me</h2>
            <div class="social-links">
                <a href="https://www.instagram.com/atagulyyew_03" class="social-btn" target="_blank">
                    📷 Instagram
                </a>
                <a href="mailto:suwhanatagulyyew133@gmail.com" class="social-btn">
                    📧 Gmail
                </a>
                <a href="https://github.com/DALIDADE" class="social-btn" target="_blank">
                    🐙 GitHub
                </a>
            </div>
            <div style="text-align: center; margin-top: 20px;">
                <p><strong>📱 Instagram:</strong> @atagulyyew_03</p>
                <p><strong>✉️ Email:</strong> suwhanatagulyyew133@gmail.com</p>
            </div>
        </div>

        <!-- Footer -->
        <div class="footer">
            <p>💡 "Code is like poetry - it should be elegant, readable, and efficient."</p>
            <p style="margin-top: 15px;">
                <img src="https://komarev.com/ghpvc/?username=DALIDADE&label=Profile%20Views&color=2C9CFF&style=flat" alt="Profile Views">
            </p>
            <p style="margin-top: 15px; font-size: 0.9rem;">
                © 2024 Suwhan Atagulyyev | Backend & Flutter Developer
            </p>
        </div>
    </div>
</body>
</html>
