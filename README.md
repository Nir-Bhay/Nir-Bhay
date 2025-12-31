<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nirbhay Hiwse - GitHub Profile README</title>
    <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
    <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;600&family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        * {
            font-family: 'Inter', sans-serif;
        }
        code, pre, .mono {
            font-family: 'JetBrains Mono', monospace;
        }
        
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #0d1117;
        }
        ::-webkit-scrollbar-thumb {
            background: #6AD3F7;
            border-radius: 4px;
        }
        
        body {
            background: #0d1117;
            color: #c9d1d9;
        }
        
        .gradient-text {
            background: linear-gradient(135deg, #6AD3F7, #a855f7, #6AD3F7);
            background-size: 200% auto;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: gradient 3s ease infinite;
        }
        
        @keyframes gradient {
            0%, 100% { background-position: 0% center; }
            50% { background-position: 100% center; }
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }
        
        @keyframes pulse-glow {
            0%, 100% { box-shadow: 0 0 20px rgba(106, 211, 247, 0.3); }
            50% { box-shadow: 0 0 40px rgba(106, 211, 247, 0.6); }
        }
        
        @keyframes typing {
            from { width: 0; }
            to { width: 100%; }
        }
        
        @keyframes blink {
            50% { border-color: transparent; }
        }
        
        .typing-effect {
            overflow: hidden;
            white-space: nowrap;
            border-right: 3px solid #6AD3F7;
            animation: typing 3s steps(40) 1s forwards, blink 0.75s step-end infinite;
        }
        
        .card-hover {
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }
        
        .card-hover:hover {
            transform: translateY(-8px) scale(1.02);
            box-shadow: 0 20px 40px rgba(106, 211, 247, 0.2);
        }
        
        .skill-icon {
            transition: all 0.3s ease;
        }
        
        .skill-icon:hover {
            transform: translateY(-5px) rotate(5deg);
            filter: drop-shadow(0 10px 20px rgba(106, 211, 247, 0.4));
        }
        
        .wave-animation {
            animation: float 3s ease-in-out infinite;
        }
        
        .glow-border {
            position: relative;
        }
        
        .glow-border::before {
            content: '';
            position: absolute;
            inset: -2px;
            background: linear-gradient(45deg, #6AD3F7, #a855f7, #6AD3F7, #a855f7);
            background-size: 400% 400%;
            border-radius: inherit;
            z-index: -1;
            animation: gradient 3s ease infinite;
            opacity: 0;
            transition: opacity 0.3s ease;
        }
        
        .glow-border:hover::before {
            opacity: 1;
        }
        
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            animation: fadeInUp 0.8s ease forwards;
        }
        
        @keyframes fadeInUp {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .stagger-1 { animation-delay: 0.1s; }
        .stagger-2 { animation-delay: 0.2s; }
        .stagger-3 { animation-delay: 0.3s; }
        .stagger-4 { animation-delay: 0.4s; }
        .stagger-5 { animation-delay: 0.5s; }
        .stagger-6 { animation-delay: 0.6s; }
        
        .animated-line {
            height: 2px;
            background: linear-gradient(90deg, transparent, #6AD3F7, #a855f7, #6AD3F7, transparent);
            background-size: 200% 100%;
            animation: shimmer 2s linear infinite;
        }
        
        @keyframes shimmer {
            0% { background-position: -200% 0; }
            100% { background-position: 200% 0; }
        }
        
        .code-block {
            background: linear-gradient(135deg, #161b22 0%, #0d1117 100%);
            border: 1px solid #30363d;
            position: relative;
            overflow: hidden;
        }
        
        .code-block::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 30px;
            background: #21262d;
            border-bottom: 1px solid #30363d;
        }
        
        .badge {
            transition: all 0.3s ease;
        }
        
        .badge:hover {
            transform: scale(1.1);
            filter: brightness(1.2);
        }
        
        .project-card {
            background: linear-gradient(135deg, #161b22 0%, #0d1117 100%);
            border: 1px solid #30363d;
            transition: all 0.4s ease;
        }
        
        .project-card:hover {
            border-color: #6AD3F7;
            box-shadow: 0 0 30px rgba(106, 211, 247, 0.15);
        }
        
        .stat-card {
            background: linear-gradient(135deg, rgba(106, 211, 247, 0.1), rgba(168, 85, 247, 0.1));
            backdrop-filter: blur(10px);
        }
        
        .trophy-glow {
            filter: drop-shadow(0 0 10px rgba(255, 215, 0, 0.5));
        }
        
        .section-title {
            position: relative;
            display: inline-block;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 100%;
            height: 3px;
            background: linear-gradient(90deg, #6AD3F7, #a855f7);
            border-radius: 2px;
        }

        .copy-btn {
            transition: all 0.3s ease;
        }
        
        .copy-btn:hover {
            background: #6AD3F7;
            color: #0d1117;
        }
        
        .copy-btn.copied {
            background: #22c55e;
            color: white;
        }

        .readme-container {
            background: #0d1117;
            border: 1px solid #30363d;
            border-radius: 12px;
            overflow: hidden;
        }

        .readme-header {
            background: #161b22;
            border-bottom: 1px solid #30363d;
            padding: 12px 16px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .readme-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
        }

        .social-btn {
            transition: all 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }
        
        .social-btn:hover {
            transform: translateY(-3px) scale(1.05);
        }

        .progress-bar {
            background: linear-gradient(90deg, #6AD3F7, #a855f7);
            height: 100%;
            border-radius: 4px;
            transition: width 1s ease;
        }

        .wavy-line {
            background: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 1440 100'%3E%3Cpath fill='%236AD3F7' fill-opacity='0.3' d='M0,32L48,37.3C96,43,192,53,288,58.7C384,64,480,64,576,58.7C672,53,768,43,864,42.7C960,43,1056,53,1152,53.3C1248,53,1344,43,1392,37.3L1440,32L1440,100L1392,100C1344,100,1248,100,1152,100C1056,100,960,100,864,100C768,100,672,100,576,100C480,100,384,100,288,100C192,100,96,100,48,100L0,100Z'%3E%3C/path%3E%3C/svg%3E") no-repeat center;
            background-size: cover;
            height: 50px;
        }
    </style>
</head>
<body class="min-h-screen">
    <!-- Header Wave -->
    <div class="relative overflow-hidden">
        <div class="absolute inset-0 bg-gradient-to-r from-cyan-500/20 via-purple-500/20 to-cyan-500/20"></div>
        <svg class="w-full" viewBox="0 0 1440 180" fill="none" xmlns="http://www.w3.org/2000/svg">
            <defs>
                <linearGradient id="headerGradient" x1="0%" y1="0%" x2="100%" y2="0%">
                    <stop offset="0%" style="stop-color:#0ea5e9"/>
                    <stop offset="50%" style="stop-color:#8b5cf6"/>
                    <stop offset="100%" style="stop-color:#0ea5e9"/>
                </linearGradient>
            </defs>
            <path fill="url(#headerGradient)" d="M0,0 L1440,0 L1440,120 Q1080,180 720,120 Q360,60 0,120 Z"/>
            <text x="50%" y="70" text-anchor="middle" fill="white" font-size="42" font-weight="bold" font-family="Inter, sans-serif">Nirbhay Hiwse</text>
            <text x="50%" y="105" text-anchor="middle" fill="rgba(255,255,255,0.9)" font-size="16" font-family="Inter, sans-serif">Full-Stack Developer | Mobile Developer | SaaS Builder</text>
        </svg>
    </div>

    <div class="max-w-6xl mx-auto px-4 py-8">
        <!-- Typing Effect -->
        <div class="text-center mb-8 fade-in">
            <div class="inline-block">
                <span class="text-xl md:text-2xl text-[#6AD3F7] mono typing-effect">Building Digital Experiences That Matter 🚀</span>
            </div>
        </div>

        <!-- Profile Badges -->
        <div class="flex flex-wrap justify-center gap-3 mb-8 fade-in stagger-1">
            <a href="https://github.com/Nir-Bhay?tab=followers" class="badge">
                <img src="https://custom-icon-badges.demolab.com/github/followers/Nir-Bhay?color=236ad3&labelColor=1155ba&style=for-the-badge&logo=person-add&label=Follow&logoColor=white" alt="followers"/>
            </a>
            <a href="https://github.com/Nir-Bhay?tab=repositories&sort=stargazers" class="badge">
                <img src="https://custom-icon-badges.demolab.com/github/stars/Nir-Bhay?color=55960c&style=for-the-badge&labelColor=488207&logo=star" alt="stars"/>
            </a>
            <img src="https://visitcount.itsvg.in/api?id=Nir-Bhay&label=Profile%20Views&color=6&icon=5&pretty=true" alt="views" class="badge"/>
        </div>

        <!-- Social Links -->
        <div class="flex flex-wrap justify-center gap-3 mb-12 fade-in stagger-2">
            <a href="https://nirbhayhiwse.dev" target="_blank" class="social-btn">
                <img src="https://img.shields.io/badge/Portfolio-FF5722?style=for-the-badge&logo=todoist&logoColor=white" alt="Portfolio"/>
            </a>
            <a href="https://linkedin.com/in/nirbhay-hiwse-b4036a234" target="_blank" class="social-btn">
                <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/>
            </a>
            <a href="https://twitter.com/nirbhay_987" target="_blank" class="social-btn">
                <img src="https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white" alt="Twitter"/>
            </a>
            <a href="mailto:contact@nirbhayhiwse.com" class="social-btn">
                <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/>
            </a>
        </div>

        <!-- Animated Line -->
        <div class="animated-line mb-12"></div>

        <!-- About Me Section -->
        <section class="mb-16 fade-in stagger-3">
            <h2 class="text-2xl font-bold mb-8 flex items-center gap-3">
                <img src="https://media.giphy.com/media/iY8CRBdQXODJSCERIr/giphy.gif" width="30" class="wave-animation"/>
                <span class="section-title gradient-text">About Me</span>
            </h2>
            
            <div class="grid md:grid-cols-2 gap-8 items-center">
                <div class="code-block rounded-xl p-6 pt-12">
                    <div class="absolute top-2 left-4 flex gap-2">
                        <span class="readme-dot bg-red-500"></span>
                        <span class="readme-dot bg-yellow-500"></span>
                        <span class="readme-dot bg-green-500"></span>
                    </div>
                    <pre class="text-sm md:text-base overflow-x-auto"><code class="text-[#c9d1d9]"><span class="text-purple-400">const</span> <span class="text-[#6AD3F7]">nirbhay</span> = {
    <span class="text-[#7ee787]">pronouns</span>: <span class="text-[#a5d6ff]">"he"</span> | <span class="text-[#a5d6ff]">"him"</span>,
    <span class="text-[#7ee787]">role</span>: <span class="text-[#a5d6ff]">"Full-Stack Developer"</span>,
    <span class="text-[#7ee787]">education</span>: {
        <span class="text-[#7ee787]">degree</span>: <span class="text-[#a5d6ff]">"B.Tech in Computer Science"</span>,
        <span class="text-[#7ee787]">university</span>: <span class="text-[#a5d6ff]">"Sage University"</span>,
        <span class="text-[#7ee787]">batch</span>: <span class="text-[#a5d6ff]">"2022 - 2026"</span>
    },
    <span class="text-[#7ee787]">location</span>: <span class="text-[#a5d6ff]">"India 🇮🇳"</span>,
    
    <span class="text-[#7ee787]">currentlyBuilding</span>: [
        <span class="text-[#a5d6ff]">"🎯 SeatWise SaaS"</span>,
        <span class="text-[#a5d6ff]">"🌾 Agro-Setu"</span>,
        <span class="text-[#a5d6ff]">"♟️ 3D Chess App"</span>
    ],
    
    <span class="text-[#7ee787]">funFact</span>: <span class="text-[#a5d6ff]">"Every code tells a story 📖"</span>
};</code></pre>
                </div>
                
                <div class="flex justify-center">
                    <img src="https://user-images.githubusercontent.com/74038190/229223263-cf2e4b07-2615-4f87-9c38-e37600f8381a.gif" alt="Coding" class="w-full max-w-md rounded-xl"/>
                </div>
            </div>
        </section>

        <!-- Animated Line -->
        <div class="animated-line mb-12"></div>

        <!-- Tech Stack Section -->
        <section class="mb-16 fade-in stagger-4">
            <h2 class="text-2xl font-bold mb-8 flex items-center gap-3">
                <img src="https://media2.giphy.com/media/QssGEmpkyEOhBCb7e1/giphy.gif?cid=ecf05e47a0n3gi1bfqntqmob8g9aid1oyj2wr3ds3mg700bl&rid=giphy.gif" width="30"/>
                <span class="section-title gradient-text">Tech Stack</span>
            </h2>

            <div class="space-y-8">
                <!-- Frontend -->
                <div class="text-center">
                    <h3 class="text-lg font-semibold text-[#6AD3F7] mb-4">🎨 Frontend Development</h3>
                    <div class="flex flex-wrap justify-center gap-2">
                        <img src="https://skillicons.dev/icons?i=html,css,js,ts,react,nextjs,tailwind,sass" class="skill-icon"/>
                    </div>
                </div>

                <!-- Mobile -->
                <div class="text-center">
                    <h3 class="text-lg font-semibold text-[#6AD3F7] mb-4">📱 Mobile Development</h3>
                    <div class="flex flex-wrap justify-center gap-3 items-center">
                        <img src="https://skillicons.dev/icons?i=react,typescript,firebase" class="skill-icon"/>
                        <img src="https://img.shields.io/badge/Expo-000020?style=for-the-badge&logo=expo&logoColor=white" class="skill-icon h-12"/>
                        <img src="https://img.shields.io/badge/React_Native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" class="skill-icon h-12"/>
                    </div>
                </div>

                <!-- Backend -->
                <div class="text-center">
                    <h3 class="text-lg font-semibold text-[#6AD3F7] mb-4">⚙️ Backend Development</h3>
                    <div class="flex flex-wrap justify-center gap-2">
                        <img src="https://skillicons.dev/icons?i=nodejs,express,mongodb,postgres,prisma" class="skill-icon"/>
                    </div>
                </div>

                <!-- 3D & AI -->
                <div class="text-center">
                    <h3 class="text-lg font-semibold text-[#6AD3F7] mb-4">🎮 3D & AI</h3>
                    <div class="flex flex-wrap justify-center gap-3 items-center">
                        <img src="https://skillicons.dev/icons?i=threejs" class="skill-icon"/>
                        <img src="https://img.shields.io/badge/Google%20Gemini-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white" class="skill-icon h-12"/>
                    </div>
                </div>

                <!-- Tools -->
                <div class="text-center">
                    <h3 class="text-lg font-semibold text-[#6AD3F7] mb-4">🛠️ Tools & Platforms</h3>
                    <div class="flex flex-wrap justify-center gap-2">
                        <img src="https://skillicons.dev/icons?i=git,github,vscode,vercel,figma,postman" class="skill-icon"/>
                    </div>
                </div>
            </div>
        </section>

        <!-- Animated Line -->
        <div class="animated-line mb-12"></div>

        <!-- GitHub Analytics -->
        <section class="mb-16 fade-in stagger-5">
            <h2 class="text-2xl font-bold mb-8 flex items-center gap-3">
                <img src="https://media.giphy.com/media/iY8CRBdQXODJSCERIr/giphy.gif" width="30" class="wave-animation"/>
                <span class="section-title gradient-text">GitHub Analytics</span>
            </h2>

            <div class="grid md:grid-cols-2 gap-4 mb-6">
                <div class="card-hover rounded-xl overflow-hidden">
                    <img src="https://github-readme-stats.vercel.app/api?username=Nir-Bhay&show_icons=true&count_private=true&hide_border=true&title_color=6AD3F7&icon_color=6AD3F7&text_color=c9d1d9&bg_color=0d1117" alt="GitHub Stats" class="w-full"/>
                </div>
                <div class="card-hover rounded-xl overflow-hidden">
                    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Nir-Bhay&layout=compact&hide_border=true&title_color=6AD3F7&text_color=c9d1d9&bg_color=0d1117&langs_count=8" alt="Top Languages" class="w-full h-full object-cover"/>
                </div>
            </div>

            <div class="card-hover rounded-xl overflow-hidden mb-6">
                <img src="https://github-readme-streak-stats.herokuapp.com/?user=Nir-Bhay&theme=tokyonight&hide_border=true&stroke=0000&background=0D1117&ring=6AD3F7&fire=6AD3F7&currStreakLabel=6AD3F7" alt="GitHub Streak" class="w-full"/>
            </div>

            <div class="card-hover rounded-xl overflow-hidden mb-6">
                <img src="https://github-readme-activity-graph.vercel.app/graph?username=Nir-Bhay&bg_color=0d1117&color=6AD3F7&line=6AD3F7&point=ffffff&area=true&hide_border=true" alt="Contribution Graph" class="w-full"/>
            </div>

            <!-- Trophies -->
            <div class="text-center card-hover rounded-xl p-4 bg-[#0d1117] border border-[#30363d]">
                <img src="https://github-profile-trophy.vercel.app/?username=Nir-Bhay&theme=tokyonight&no-frame=true&no-bg=true&column=7&margin-w=5&margin-h=5" alt="GitHub Trophies" class="trophy-glow mx-auto"/>
            </div>
        </section>

        <!-- Animated Line -->
        <div class="animated-line mb-12"></div>

        <!-- Featured Projects -->
        <section class="mb-16 fade-in stagger-6">
            <h2 class="text-2xl font-bold mb-8 flex items-center gap-3">
                <img src="https://media.giphy.com/media/WUlplcMpOCEmTGBtBW/giphy.gif" width="35"/>
                <span class="section-title gradient-text">Featured Projects</span>
            </h2>

            <div class="grid md:grid-cols-2 gap-6">
                <!-- Project 1 -->
                <div class="project-card rounded-xl p-6 card-hover">
                    <h3 class="text-xl font-bold text-[#6AD3F7] mb-3">🎯 SeatWise SaaS</h3>
                    <a href="https://github.com/Nir-Bhay/SeatWise-SaaS">
                        <img src="https://github-readme-stats.vercel.app/api/pin/?username=Nir-Bhay&repo=SeatWise-SaaS&theme=tokyonight&hide_border=true&bg_color=0D1117" class="w-full mb-4 rounded-lg"/>
                    </a>
                    <p class="text-gray-400 mb-4"><strong>Smart Exam Seat Allocation System</strong><br/>Automated exam seating with PDF generation & admin dashboard</p>
                    <div class="flex flex-wrap gap-2">
                        <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white"/>
                        <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white"/>
                        <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white"/>
                    </div>
                </div>

                <!-- Project 2 -->
                <div class="project-card rounded-xl p-6 card-hover">
                    <h3 class="text-xl font-bold text-[#6AD3F7] mb-3">🌾 Agro-Setu</h3>
                    <div class="bg-[#1a1a2e] rounded-lg p-8 mb-4 text-center">
                        <img src="https://img.shields.io/badge/🔒_Private_Repository-1a1a2e?style=for-the-badge" class="mx-auto"/>
                    </div>
                    <p class="text-gray-400 mb-4"><strong>Agricultural Connectivity Platform</strong><br/>Mobile app connecting farmers with markets & resources</p>
                    <div class="flex flex-wrap gap-2">
                        <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"/>
                        <img src="https://img.shields.io/badge/Expo-000020?style=flat-square&logo=expo&logoColor=white"/>
                        <img src="https://img.shields.io/badge/React_Native-61DAFB?style=flat-square&logo=react&logoColor=black"/>
                    </div>
                </div>

                <!-- Project 3 -->
                <div class="project-card rounded-xl p-6 card-hover">
                    <h3 class="text-xl font-bold text-[#6AD3F7] mb-3">🌌 3D Solar System</h3>
                    <a href="https://github.com/Nir-Bhay/Interactive-3D-Solar-System-Simulation-0.2">
                        <img src="https://github-readme-stats.vercel.app/api/pin/?username=Nir-Bhay&repo=Interactive-3D-Solar-System-Simulation-0.2&theme=tokyonight&hide_border=true&bg_color=0D1117" class="w-full mb-4 rounded-lg"/>
                    </a>
                    <p class="text-gray-400 mb-4"><strong>Interactive 3D Space Simulation</strong><br/>Realistic orbital mechanics with Three.js</p>
                    <div class="flex flex-wrap gap-2">
                        <img src="https://img.shields.io/badge/Three.js-000000?style=flat-square&logo=three.js&logoColor=white"/>
                        <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black"/>
                    </div>
                </div>

                <!-- Project 4 -->
                <div class="project-card rounded-xl p-6 card-hover">
                    <h3 class="text-xl font-bold text-[#6AD3F7] mb-3">♟️ 3D Chess Game</h3>
                    <a href="https://github.com/Nir-Bhay/chess">
                        <img src="https://github-readme-stats.vercel.app/api/pin/?username=Nir-Bhay&repo=chess&theme=tokyonight&hide_border=true&bg_color=0D1117" class="w-full mb-4 rounded-lg"/>
                    </a>
                    <p class="text-gray-400 mb-4"><strong>Crystal/Azure UI Chess</strong><br/>Premium 3D chess with marble textures & animations</p>
                    <div class="flex flex-wrap gap-2">
                        <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"/>
                        <img src="https://img.shields.io/badge/Expo-000020?style=flat-square&logo=expo&logoColor=white"/>
                    </div>
                </div>
            </div>

            <div class="text-center mt-8">
                <a href="https://github.com/Nir-Bhay?tab=repositories" class="inline-block">
                    <img src="https://img.shields.io/badge/View_All_78+_Repositories-6AD3F7?style=for-the-badge&logo=github&logoColor=black" class="badge"/>
                </a>
            </div>
        </section>

        <!-- Animated Line -->
        <div class="animated-line mb-12"></div>

        <!-- Achievements -->
        <section class="mb-16">
            <h2 class="text-2xl font-bold mb-8 flex items-center gap-3">
                <span class="text-2xl">🏆</span>
                <span class="section-title gradient-text">Achievements & Experience</span>
            </h2>

            <div class="grid md:grid-cols-3 gap-4">
                <div class="stat-card rounded-xl p-6 text-center card-hover border border-[#30363d]">
                    <div class="text-green-400 text-sm font-bold mb-2">💼 Freelance</div>
                    <div class="text-3xl font-bold text-[#6AD3F7] mb-2">₹30,000</div>
                    <p class="text-gray-400"><strong>Sood Infra</strong><br/>Real Estate Website</p>
                </div>
                <div class="stat-card rounded-xl p-6 text-center card-hover border border-[#30363d]">
                    <div class="text-blue-400 text-sm font-bold mb-2">🚀 Hackathon</div>
                    <div class="text-3xl font-bold text-[#6AD3F7] mb-2">MindEasy</div>
                    <p class="text-gray-400"><strong>Mental Health Platform</strong><br/>Sistech, Feb 2024</p>
                </div>
                <div class="stat-card rounded-xl p-6 text-center card-hover border border-[#30363d]">
                    <div class="text-purple-400 text-sm font-bold mb-2">🎤 Conference</div>
                    <div class="text-3xl font-bold text-[#6AD3F7] mb-2">Presenter</div>
                    <p class="text-gray-400"><strong>International Conference</strong><br/>Sage University, 2023</p>
                </div>
                <div class="stat-card rounded-xl p-6 text-center card-hover border border-[#30363d]">
                    <div class="text-orange-400 text-sm font-bold mb-2">🦈 Pitch</div>
                    <div class="text-3xl font-bold text-[#6AD3F7] mb-2">Shark Tank</div>
                    <p class="text-gray-400"><strong>Startup Pitch</strong><br/>Sage University, 2024</p>
                </div>
                <div class="stat-card rounded-xl p-6 text-center card-hover border border-[#30363d]">
                    <div class="text-yellow-400 text-sm font-bold mb-2">📜 Certified</div>
                    <div class="text-3xl font-bold text-[#6AD3F7] mb-2">JavaScript</div>
                    <p class="text-gray-400"><strong>HackerRank</strong><br/>2024</p>
                </div>
                <div class="stat-card rounded-xl p-6 text-center card-hover border border-[#30363d]">
                    <div class="text-red-400 text-sm font-bold mb-2">🎓 Education</div>
                    <div class="text-3xl font-bold text-[#6AD3F7] mb-2">B.Tech CSE</div>
                    <p class="text-gray-400"><strong>Sage University</strong><br/>2022 - 2026</p>
                </div>
            </div>
        </section>

        <!-- Animated Line -->
        <div class="animated-line mb-12"></div>

        <!-- Coding Stats -->
        <section class="mb-16">
            <h2 class="text-2xl font-bold mb-8 flex items-center gap-3">
                <span class="text-2xl">📊</span>
                <span class="section-title gradient-text">Coding Stats</span>
            </h2>

            <div class="code-block rounded-xl p-6 pt-12 mb-6">
                <div class="space-y-4">
                    <div>
                        <div class="flex justify-between mb-1">
                            <span class="text-[#6AD3F7]">JavaScript</span>
                            <span>65.5%</span>
                        </div>
                        <div class="h-3 bg-[#21262d] rounded-full overflow-hidden">
                            <div class="progress-bar" style="width: 65.5%"></div>
                        </div>
                    </div>
                    <div>
                        <div class="flex justify-between mb-1">
                            <span class="text-[#6AD3F7]">TypeScript</span>
                            <span>20.2%</span>
                        </div>
                        <div class="h-3 bg-[#21262d] rounded-full overflow-hidden">
                            <div class="progress-bar" style="width: 20.2%"></div>
                        </div>
                    </div>
                    <div>
                        <div class="flex justify-between mb-1">
                            <span class="text-[#6AD3F7]">CSS</span>
                            <span>8.5%</span>
                        </div>
                        <div class="h-3 bg-[#21262d] rounded-full overflow-hidden">
                            <div class="progress-bar" style="width: 8.5%"></div>
                        </div>
                    </div>
                    <div>
                        <div class="flex justify-between mb-1">
                            <span class="text-[#6AD3F7]">HTML</span>
                            <span>4.3%</span>
                        </div>
                        <div class="h-3 bg-[#21262d] rounded-full overflow-hidden">
                            <div class="progress-bar" style="width: 4.3%"></div>
                        </div>
                    </div>
                    <div>
                        <div class="flex justify-between mb-1">
                            <span class="text-[#6AD3F7]">Java</span>
                            <span>1.5%</span>
                        </div>
                        <div class="h-3 bg-[#21262d] rounded-full overflow-hidden">
                            <div class="progress-bar" style="width: 1.5%"></div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="card-hover rounded-xl overflow-hidden mb-6">
                <img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=Nir-Bhay&theme=tokyonight" alt="Profile Summary" class="w-full"/>
            </div>

            <!-- Snake Animation -->
            <div class="rounded-xl overflow-hidden bg-[#0d1117] p-4 border border-[#30363d]">
                <picture>
                    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/platane/platane/output/github-contribution-grid-snake-dark.svg">
                    <img alt="github contribution grid snake animation" src="https://raw.githubusercontent.com/platane/platane/output/github-contribution-grid-snake-dark.svg" class="w-full">
                </picture>
            </div>
        </section>

        <!-- Animated Line -->
        <div class="animated-line mb-12"></div>

        <!-- Connect Section -->
        <section class="mb-16 text-center">
            <h2 class="text-2xl font-bold mb-8 flex items-center justify-center gap-3">
                <img src="https://media.giphy.com/media/LnQjpWaON8nhr21vNW/giphy.gif" width="30"/>
                <span class="section-title gradient-text">Let's Connect!</span>
            </h2>

            <div class="space-y-4">
                <a href="https://nirbhayhiwse.dev" target="_blank" class="inline-block social-btn">
                    <img src="https://img.shields.io/badge/🌐_Portfolio-nirbhayhiwse.dev-6AD3F7?style=for-the-badge"/>
                </a>
                
                <div class="flex flex-wrap justify-center gap-3">
                    <a href="https://linkedin.com/in/nirbhay-hiwse-b4036a234" target="_blank" class="social-btn">
                        <img src="https://img.shields.io/badge/LinkedIn-Nirbhay_Hiwse-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/>
                    </a>
                    <a href="https://twitter.com/nirbhay_987" target="_blank" class="social-btn">
                        <img src="https://img.shields.io/badge/Twitter-@nirbhay__987-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white"/>
                    </a>
                    <a href="mailto:contact@nirbhayhiwse.com" class="social-btn">
                        <img src="https://img.shields.io/badge/Email-contact@nirbhayhiwse.com-D14836?style=for-the-badge&logo=gmail&logoColor=white"/>
                    </a>
                </div>
            </div>

            <p class="text-xl mt-8 text-gray-400 italic">
                💬 "I believe every piece of code tells a story – I aim to make mine secure and elegant!"
            </p>
        </section>

        <!-- Quote -->
        <div class="text-center mb-12">
            <img src="https://quotes-github-readme.vercel.app/api?type=horizontal&theme=tokyonight" alt="Random Dev Quote" class="mx-auto rounded-xl"/>
        </div>

        <!-- Profile Views -->
        <div class="text-center mb-8">
            <img src="https://komarev.com/ghpvc/?username=Nir-Bhay&label=Profile%20Views&color=6AD3F7&style=for-the-badge" alt="Profile Views" class="mx-auto"/>
        </div>

        <p class="text-center text-gray-500">
            Built with ❤️ by <a href="https://nirbhayhiwse.dev" class="text-[#6AD3F7] hover:underline">Nirbhay Hiwse</a>
        </p>
    </div>

    <!-- Footer Wave -->
    <svg class="w-full mt-8" viewBox="0 0 1440 120" fill="none" xmlns="http://www.w3.org/2000/svg">
        <defs>
            <linearGradient id="footerGradient" x1="0%" y1="0%" x2="100%" y2="0%">
                <stop offset="0%" style="stop-color:#0ea5e9"/>
                <stop offset="50%" style="stop-color:#8b5cf6"/>
                <stop offset="100%" style="stop-color:#0ea5e9"/>
            </linearGradient>
        </defs>
        <path fill="url(#footerGradient)" d="M0,120 L1440,120 L1440,40 Q1080,0 720,40 Q360,80 0,40 Z"/>
    </svg>

    <script>
        // Intersection Observer for fade-in animations
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.animationPlayState = 'running';
                }
            });
        }, { threshold: 0.1 });

        document.querySelectorAll('.fade-in').forEach(el => {
            el.style.animationPlayState = 'paused';
            observer.observe(el);
        });

        // Smooth scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Add hover effects to images
        document.querySelectorAll('img').forEach(img => {
            img.style.transition = 'transform 0.3s ease';
        });
    </script>
</body>
</html>
