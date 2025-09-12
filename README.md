<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>lakipop - GitHub Profile</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@300;400;500;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'JetBrains Mono', monospace;
            background: linear-gradient(135deg, #0c1427 0%, #1a1a2e 50%, #16213e 100%);
            color: #e2e8f0;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
            overflow-x: hidden;
        }
        
        .terminal {
            background: rgba(15, 23, 42, 0.95);
            border: 2px solid #334155;
            border-radius: 12px;
            width: 100%;
            max-width: 800px;
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.8);
            backdrop-filter: blur(10px);
            overflow: hidden;
            animation: slideUp 1s ease-out;
        }
        
        @keyframes slideUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .terminal-header {
            background: linear-gradient(90deg, #1e293b, #334155);
            padding: 12px 20px;
            display: flex;
            align-items: center;
            gap: 10px;
            border-bottom: 1px solid #475569;
        }
        
        .terminal-dots {
            display: flex;
            gap: 8px;
        }
        
        .dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            animation: pulse 2s infinite;
        }
        
        .dot.red { background: #ef4444; }
        .dot.yellow { background: #f59e0b; }
        .dot.green { background: #10b981; }
        
        @keyframes pulse {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.6; }
        }
        
        .terminal-title {
            color: #94a3b8;
            font-size: 14px;
            margin-left: 15px;
        }
        
        .terminal-body {
            padding: 30px;
        }
        
        .header-section {
            text-align: center;
            margin-bottom: 40px;
            animation: fadeIn 1.5s ease-out;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        .wave {
            font-size: 3rem;
            display: inline-block;
            animation: wave 2s infinite;
        }
        
        @keyframes wave {
            0%, 100% { transform: rotate(0deg); }
            25% { transform: rotate(-10deg); }
            75% { transform: rotate(10deg); }
        }
        
        .name {
            font-size: 2.5rem;
            font-weight: 700;
            background: linear-gradient(45deg, #60a5fa, #34d399, #f472b6);
            background-clip: text;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin: 10px 0;
            animation: textGlow 3s ease-in-out infinite alternate;
        }
        
        @keyframes textGlow {
            from {
                filter: brightness(1);
            }
            to {
                filter: brightness(1.2);
            }
        }
        
        .role {
            color: #94a3b8;
            font-size: 1.2rem;
            margin-bottom: 10px;
        }
        
        .profile-views {
            background: linear-gradient(45deg, #3b82f6, #8b5cf6);
            color: white;
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 12px;
            display: inline-block;
            animation: bounce 2s infinite;
        }
        
        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-5px); }
        }
        
        .stats-section {
            background: rgba(30, 41, 59, 0.5);
            border: 1px solid #475569;
            border-radius: 8px;
            padding: 25px;
            margin: 30px 0;
            animation: slideIn 1.5s ease-out 0.5s both;
        }
        
        @keyframes slideIn {
            from {
                opacity: 0;
                transform: translateX(-50px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }
        
        .stats-title {
            color: #f1f5f9;
            font-size: 1.3rem;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
        }
        
        .stat-item {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 10px;
            background: rgba(51, 65, 85, 0.3);
            border-radius: 6px;
            transition: all 0.3s ease;
        }
        
        .stat-item:hover {
            background: rgba(51, 65, 85, 0.6);
            transform: translateY(-2px);
        }
        
        .stat-icon {
            width: 16px;
            height: 16px;
            flex-shrink: 0;
        }
        
        .section {
            margin: 30px 0;
            animation: fadeInUp 1s ease-out;
            animation-fill-mode: both;
        }
        
        .section:nth-child(3) { animation-delay: 0.2s; }
        .section:nth-child(4) { animation-delay: 0.4s; }
        .section:nth-child(5) { animation-delay: 0.6s; }
        
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
        
        .section-title {
            color: #f1f5f9;
            font-size: 1.3rem;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .section-content {
            margin-left: 30px;
        }
        
        .tech-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin: 15px 0;
        }
        
        .tech-tag {
            background: linear-gradient(45deg, #1e40af, #7c3aed);
            color: white;
            padding: 6px 12px;
            border-radius: 15px;
            font-size: 12px;
            transition: all 0.3s ease;
            cursor: pointer;
        }
        
        .tech-tag:hover {
            transform: scale(1.05);
            box-shadow: 0 4px 12px rgba(124, 58, 237, 0.4);
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 10px;
            margin: 10px 0;
            padding: 10px;
            background: rgba(30, 41, 59, 0.3);
            border-radius: 6px;
            transition: all 0.3s ease;
        }
        
        .contact-item:hover {
            background: rgba(30, 41, 59, 0.6);
            transform: translateX(10px);
        }
        
        .fun-facts {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
        }
        
        .fun-fact {
            background: linear-gradient(45deg, #ec4899, #f97316);
            color: white;
            padding: 10px 15px;
            border-radius: 20px;
            font-size: 14px;
            display: flex;
            align-items: center;
            gap: 8px;
            animation: float 3s ease-in-out infinite;
        }
        
        .fun-fact:nth-child(2) { animation-delay: 1s; }
        .fun-fact:nth-child(3) { animation-delay: 2s; }
        
        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }
        
        .activity-graph {
            background: rgba(30, 41, 59, 0.3);
            border-radius: 8px;
            padding: 20px;
            margin: 20px 0;
        }
        
        .graph-grid {
            display: grid;
            grid-template-columns: repeat(52, 1fr);
            gap: 2px;
            margin-top: 15px;
        }
        
        .graph-cell {
            width: 12px;
            height: 12px;
            background: #1e293b;
            border-radius: 2px;
            transition: all 0.3s ease;
        }
        
        .graph-cell.level-1 { background: #0f766e; }
        .graph-cell.level-2 { background: #0d9488; }
        .graph-cell.level-3 { background: #14b8a6; }
        .graph-cell.level-4 { background: #5eead4; }
        
        .typing-effect {
            border-right: 2px solid #60a5fa;
            animation: blink 1s infinite;
        }
        
        @keyframes blink {
            0%, 50% { border-color: transparent; }
            51%, 100% { border-color: #60a5fa; }
        }
        
        @media (max-width: 768px) {
            .terminal {
                margin: 10px;
            }
            
            .terminal-body {
                padding: 20px;
            }
            
            .name {
                font-size: 2rem;
            }
            
            .stats-grid {
                grid-template-columns: 1fr;
            }
            
            .tech-grid {
                justify-content: center;
            }
        }
    </style>
</head>
<body>
    <div class="terminal">
        <div class="terminal-header">
            <div class="terminal-dots">
                <div class="dot red"></div>
                <div class="dot yellow"></div>
                <div class="dot green"></div>
            </div>
            <div class="terminal-title">lakipop@github:~$</div>
        </div>
        
        <div class="terminal-body">
            <div class="header-section">
                <div class="wave">👋</div>
                <h1 class="name">Hi there, I'm @lakipop</h1>
                <p class="role">Passionate Developer & Creative Thinker</p>
                <div class="profile-views">Profile views: 247</div>
            </div>
            
            <div class="stats-section">
                <h3 class="stats-title">📊 GitHub Stats Overview</h3>
                <div class="stats-grid">
                    <div class="stat-item">
                        <span class="stat-icon">⭐</span>
                        <span>Total Stars Earned: <strong>12</strong></span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-icon">📝</span>
                        <span>Total Commits (2025): <strong>156</strong></span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-icon">📁</span>
                        <span>Total Projects: <strong>8</strong></span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-icon">🐛</span>
                        <span>Total Issues: <strong>3</strong></span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-icon">🤝</span>
                        <span>Contributions (last year): <strong>89</strong></span>
                    </div>
                </div>
            </div>
            
            <div class="section">
                <h3 class="section-title">👨‍💻 What I Do</h3>
                <div class="section-content">
                    <div class="tech-grid">
                        <span class="tech-tag">Laravel</span>
                        <span class="tech-tag">Vue.js</span>
                        <span class="tech-tag">React</span>
                        <span class="tech-tag">TailwindCSS</span>
                        <span class="tech-tag">SpringBoot</span>
                        <span class="tech-tag">Java</span>
                        <span class="tech-tag">UI/UX Design</span>
                        <span class="tech-tag">Full Stack</span>
                    </div>
                    <p>• Full Stack Web Development</p>
                    <p>• UI/UX Design & Frontend Engineering</p>
                    <p>• Backend API development with Laravel</p>
                    <p>• Currently exploring advanced <span class="typing-effect">Java & SpringBoot</span></p>
                </div>
            </div>
            
            <div class="section">
                <h3 class="section-title">🎯 Interests</h3>
                <div class="section-content">
                    <p>• Science & Research 🔬</p>
                    <p>• Art, Design & Nature 🎨</p>
                    <p>• Frontend frameworks (Vue, React)</p>
                    <p>• Backend development with Laravel</p>
                    <p>• Clean eco-friendly UI/UX principles</p>
                    <p>• Exploring the intersection of tech + creativity</p>
                </div>
            </div>
            
            <div class="section">
                <h3 class="section-title">🤝 Looking to Collaborate On</h3>
                <div class="section-content">
                    <p>• Web development projects (frontend or full stack)</p>
                    <p>• Science-related platforms or education tools</p>
                </div>
            </div>
            
            <div class="section">
                <h3 class="section-title">📫 Connect with Me</h3>
                <div class="section-content">
                    <div class="contact-item">
                        <span>📧</span>
                        <span>lakindu02@gmail.com</span>
                    </div>
                </div>
            </div>
            
            <div class="section">
                <h3 class="section-title">⚡ Fun Facts</h3>
                <div class="section-content">
                    <div class="fun-facts">
                        <div class="fun-fact">
                            <span>🥋</span>
                            <span>Martial Arts Enthusiast</span>
                        </div>
                        <div class="fun-fact">
                            <span>💪</span>
                            <span>Fitness Lover</span>
                        </div>
                        <div class="fun-fact">
                            <span>🎶</span>
                            <span>K-POP Fan</span>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="activity-graph">
                <h4>📈 Contribution Activity</h4>
                <div class="graph-grid" id="activityGraph"></div>
            </div>
        </div>
    </div>
    
    <script>
        // Generate random activity graph
        function generateActivityGraph() {
            const graph = document.getElementById('activityGraph');
            const totalCells = 365; // Roughly a year
            
            for (let i = 0; i < totalCells; i++) {
                const cell = document.createElement('div');
                cell.className = 'graph-cell';
                
                // Random activity level
                const level = Math.floor(Math.random() * 5);
                if (level > 0) {
                    cell.classList.add(`level-${level}`);
                }
                
                // Add hover effect
                cell.addEventListener('mouseenter', () => {
                    cell.style.transform = 'scale(1.2)';
                });
                
                cell.addEventListener('mouseleave', () => {
                    cell.style.transform = 'scale(1)';
                });
                
                graph.appendChild(cell);
            }
        }
        
        // Animate tech tags on load
        function animateTechTags() {
            const techTags = document.querySelectorAll('.tech-tag');
            techTags.forEach((tag, index) => {
                setTimeout(() => {
                    tag.style.animation = 'fadeInUp 0.5s ease-out forwards';
                }, index * 100);
            });
        }
        
        // Fetch real GitHub data
        async function fetchGitHubStats(username) {
            try {
                // Fetch user profile data
                const userResponse = await fetch(`https://api.github.com/users/${username}`);
                const userData = await userResponse.json();
                
                // Fetch repositories data
                const reposResponse = await fetch(`https://api.github.com/users/${username}/repos`);
                const reposData = await reposResponse.json();
                
                // Calculate stats
                const totalStars = reposData.reduce((sum, repo) => sum + repo.stargazers_count, 0);
                const totalForks = reposData.reduce((sum, repo) => sum + repo.forks_count, 0);
                const publicRepos = userData.public_repos;
                const followers = userData.followers;
                const following = userData.following;
                
                // Update DOM with real data
                updateStatsDisplay({
                    stars: totalStars,
                    repos: publicRepos,
                    followers: followers,
                    following: following,
                    forks: totalForks,
                    name: userData.name || userData.login,
                    bio: userData.bio,
                    avatar: userData.avatar_url,
                    location: userData.location,
                    blog: userData.blog,
                    company: userData.company
                });
                
            } catch (error) {
                console.log('Using demo data - GitHub API rate limit or network issue');
                // Falls back to demo data if API fails
            }
        }
        
        function updateStatsDisplay(data) {
            // Update stats grid
            const statsGrid = document.querySelector('.stats-grid');
            statsGrid.innerHTML = `
                <div class="stat-item">
                    <span class="stat-icon">⭐</span>
                    <span>Total Stars Earned: <strong>${data.stars}</strong></span>
                </div>
                <div class="stat-item">
                    <span class="stat-icon">📁</span>
                    <span>Public Repositories: <strong>${data.repos}</strong></span>
                </div>
                <div class="stat-item">
                    <span class="stat-icon">👥</span>
                    <span>Followers: <strong>${data.followers}</strong></span>
                </div>
                <div class="stat-item">
                    <span class="stat-icon">👤</span>
                    <span>Following: <strong>${data.following}</strong></span>
                </div>
                <div class="stat-item">
                    <span class="stat-icon">🍴</span>
                    <span>Total Forks: <strong>${data.forks}</strong></span>
                </div>
            `;
            
            // Update name if available
            if (data.name && data.name !== 'lakipop') {
                document.querySelector('.name').textContent = `Hi there, I'm ${data.name}`;
            }
        }
        
        // Initialize animations and fetch real data
        document.addEventListener('DOMContentLoaded', () => {
            generateActivityGraph();
            animateTechTags();
            fetchGitHubStats('lakipop'); // Replace with your actual GitHub username
        });
        
        // Add interactive hover effects
        document.querySelectorAll('.stat-item').forEach(item => {
            item.addEventListener('mouseenter', () => {
                item.style.boxShadow = '0 4px 12px rgba(59, 130, 246, 0.3)';
            });
            
            item.addEventListener('mouseleave', () => {
                item.style.boxShadow = 'none';
            });
        });
    </script>
</body>
</html>
