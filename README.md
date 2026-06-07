<style>
  :root {
    --accent: #6366f1;
    --accent-light: #818cf8;
    --accent-glow: rgba(99, 102, 241, 0.35);
    --gold: #f9c440;
    --bg-card: rgba(22, 27, 34, 0.85);
    --border: rgba(99, 102, 241, 0.25);
    --text-muted: #8b949e;
    --radius: 16px;
    --radius-sm: 10px;
  }

  .profile-wrap {
    max-width: 1100px;
    margin: 0 auto;
    padding: 0 12px;
  }

  .hero-badges {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    justify-content: center;
    align-items: center;
    margin: 16px 0;
  }

  .section-title {
    text-align: center;
    font-size: 1.6rem;
    margin: 2rem 0 1.25rem;
    background: linear-gradient(90deg, var(--accent-light), #a78bfa, var(--accent));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .card {
    background: var(--bg-card);
    border: 1px solid var(--border);
    border-radius: var(--radius);
    padding: 1.5rem;
    margin: 1rem 0;
    box-shadow: 0 8px 32px rgba(0, 0, 0, 0.25);
    backdrop-filter: blur(6px);
  }

  .card-glow {
    border: 1px solid rgba(99, 102, 241, 0.4);
    box-shadow: 0 0 24px var(--accent-glow), inset 0 1px 0 rgba(255,255,255,0.04);
  }

  .about-grid {
    display: grid;
    grid-template-columns: 1fr 280px;
    gap: 1.5rem;
    align-items: center;
  }

  .about-grid ul {
    margin: 0;
    padding-left: 1.2rem;
    line-height: 1.85;
  }

  .about-grid img {
    width: 100%;
    max-width: 280px;
    border-radius: var(--radius);
    border: 2px solid var(--border);
    box-shadow: 0 12px 40px var(--accent-glow);
  }

  .quote-block {
    text-align: center;
    font-size: 1.1rem;
    font-style: italic;
    color: var(--text-muted);
    border-left: 4px solid var(--accent);
    padding: 1rem 1.5rem;
    margin: 1rem auto;
    max-width: 640px;
    background: rgba(99, 102, 241, 0.06);
    border-radius: 0 var(--radius-sm) var(--radius-sm) 0;
  }

  .tech-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1rem;
    text-align: center;
  }

  .tech-cell {
    background: rgba(99, 102, 241, 0.05);
    border: 1px solid var(--border);
    border-radius: var(--radius-sm);
    padding: 1rem 0.5rem;
    transition: transform 0.2s ease, box-shadow 0.2s ease;
  }

  .tech-cell:hover {
    transform: translateY(-3px);
    box-shadow: 0 8px 24px var(--accent-glow);
  }

  .tech-cell strong {
    display: block;
    margin-bottom: 0.75rem;
    font-size: 0.95rem;
  }

  .tech-cell img {
    max-width: 100%;
    height: auto;
  }

  .table-scroll {
    overflow-x: auto;
    -webkit-overflow-scrolling: touch;
    border-radius: var(--radius-sm);
  }

  .styled-table {
    width: 100%;
    border-collapse: collapse;
    min-width: 520px;
  }

  .styled-table th {
    background: linear-gradient(135deg, var(--accent), #7c3aed);
    color: #fff;
    padding: 12px 16px;
    font-weight: 600;
    text-align: center;
  }

  .styled-table th:first-child { border-radius: var(--radius-sm) 0 0 0; }
  .styled-table th:last-child { border-radius: 0 var(--radius-sm) 0 0; }

  .styled-table td {
    padding: 12px 16px;
    border-bottom: 1px solid var(--border);
    text-align: center;
    vertical-align: middle;
  }

  .styled-table tr:last-child td { border-bottom: none; }
  .styled-table tr:hover td { background: rgba(99, 102, 241, 0.06); }

  .project-cards {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 1rem;
  }

  .project-card {
    background: rgba(99, 102, 241, 0.05);
    border: 1px solid var(--border);
    border-radius: var(--radius-sm);
    padding: 1.25rem;
    text-align: left;
    transition: transform 0.2s ease, border-color 0.2s ease;
  }

  .project-card:hover {
    transform: translateY(-4px);
    border-color: var(--accent-light);
  }

  .project-card h4 {
    margin: 0 0 0.5rem;
    color: var(--accent-light);
  }

  .project-card p {
    margin: 0 0 0.75rem;
    color: var(--text-muted);
    font-size: 0.92rem;
    line-height: 1.6;
  }

  .project-tag {
    display: inline-block;
    background: rgba(99, 102, 241, 0.15);
    border: 1px solid var(--border);
    border-radius: 20px;
    padding: 4px 12px;
    font-size: 0.78rem;
    color: var(--accent-light);
  }

  .edu-list {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 0.75rem;
    list-style: none;
    padding: 0;
    margin: 0;
  }

  .edu-list li {
    background: rgba(99, 102, 241, 0.05);
    border: 1px solid var(--border);
    border-radius: var(--radius-sm);
    padding: 0.85rem 1rem;
    line-height: 1.5;
  }

  .leetcode-box {
    border-radius: var(--radius);
    overflow: hidden;
    border: 2px solid var(--gold);
    margin: 1.5rem 0;
  }

  .leetcode-header {
    background: linear-gradient(90deg, var(--gold), #fbbf24);
    color: #1a1a2e;
    text-align: center;
    font-weight: 700;
    padding: 12px 16px;
    font-size: 1rem;
    letter-spacing: 0.5px;
  }

  .leetcode-body {
    background: #161b22;
    padding: 1.5rem 1rem;
    overflow-x: auto;
    -webkit-overflow-scrolling: touch;
  }

  .leetcode-body img {
    display: block;
    margin: 0 auto;
    max-width: 100%;
    height: auto;
    min-width: 600px;
  }

  .stats-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
    justify-content: center;
    align-items: stretch;
  }

  .stats-grid img {
    border-radius: var(--radius-sm);
    max-width: 100%;
    height: auto;
  }

  .stats-row {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
    justify-content: center;
    align-items: center;
  }

  .stats-row .gif-box img {
    width: 100%;
    max-width: 320px;
    border-radius: var(--radius);
    border: 3px solid var(--accent);
    box-shadow: 0 0 28px var(--accent-glow);
  }

  .achievement-img {
    width: 100%;
    max-width: 720px;
    border-radius: var(--radius);
    border: 2px solid var(--border);
    box-shadow: 0 16px 48px rgba(0, 0, 0, 0.35);
  }

  .connect-row {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    justify-content: center;
    align-items: center;
    margin: 1rem 0;
  }

  .divider {
    width: 100%;
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--accent), transparent);
    margin: 2rem 0;
    border: none;
  }

  .philosophy {
    text-align: center;
    max-width: 680px;
    margin: 0 auto;
    line-height: 1.8;
    color: var(--text-muted);
  }

  .philosophy blockquote {
    font-size: 1.05rem;
    font-style: italic;
    border: none;
    margin: 0 0 1rem;
    color: #c9d1d9;
  }

  @media (max-width: 768px) {
    .about-grid {
      grid-template-columns: 1fr;
    }

    .about-grid img {
      margin: 0 auto;
      display: block;
    }

    .tech-grid {
      grid-template-columns: 1fr;
    }

    .section-title {
      font-size: 1.35rem;
    }

    .card {
      padding: 1rem;
    }

    .leetcode-body img {
      min-width: 480px;
    }
  }

  @media (max-width: 480px) {
    .hero-badges img {
      transform: scale(0.95);
    }

    .leetcode-body img {
      min-width: 360px;
    }
  }
</style>

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=6366f1&height=220&section=header&text=abrshiz&fontSize=72&animation=fadeIn&fontAlignY=38&desc=Java%20Architect%20%7C%20Full-Stack%20Engineer&descAlignY=58&descSize=18&fontColor=ffffff"/>

<div class="profile-wrap">

<div class="hero-badges">
  <a href="https://github.com/abrshiz"><img src="https://img.shields.io/github/followers/abrshiz?label=Followers&style=for-the-badge&color=6366f1" /></a>
  <a href="https://github.com/abrshiz?tab=repositories"><img src="https://img.shields.io/badge/Explore%20Repos-6366f1?style=for-the-badge&logo=github&logoColor=white" /></a>
  <a href="mailto:abrhamwendesen.ta@ddu.edu.et"><img src="https://img.shields.io/badge/Email%20Me-D14836?style=for-the-badge&logo=gmail&logoColor=white" /></a>
  <a href="https://t.me/abrshiz"><img src="https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" /></a>
</div>

<img src="https://komarev.com/ghpvc/?username=abrshiz&label=Profile%20Views&color=6366f1&style=for-the-badge" alt="Profile Views"/>

<br/><br/>

<img src="https://readme-typing-svg.herokuapp.com/?font=Righteous&size=36&center=true&vCenter=true&width=700&height=90&duration=4000&lines=Hi+There!+👋;+☕+I'm+Abrham!+☕;+⚡+Java+%7C+Full-Stack+Dev!+🚀;" alt="Typing SVG" />

</div>

<!-- LeetCode Heatmap -->
<div class="profile-wrap leetcode-box">
  <div class="leetcode-header">⚡ LEETCODE CONSISTENCY — FULL ACTIVITY HEATMAP ⚡</div>
  <div class="leetcode-body">
    <img src="https://leetcard.jacoblin.cool/abrshiz?ext=heatmap&theme=dark" alt="LeetCode Heatmap"/>
  </div>
</div>

<div class="profile-wrap">

<h2 class="section-title">⚡ About Me</h2>

<div class="quote-block">
  “Write code that lasts — scalable, maintainable, and meaningful.”
</div>

<div class="card card-glow about-grid">
  <div>
    <h3>👨‍💻 The Developer</h3>
    <ul>
      <li>👋 I'm <strong>Abrham</strong> (<strong>abrshiz</strong>), a developer from <strong>Addis Ababa, Ethiopia 🇪🇹</strong>.</li>
      <li>🎓 <strong>Computer Science Student</strong> — passionate about backend architecture & system design.</li>
      <li>☕ <strong>Java Specialist</strong> — building robust, scalable applications with clean architecture.</li>
      <li>🔭 Currently working on: <strong>Enterprise-level Java applications & full-stack solutions</strong>.</li>
      <li>🌱 Learning: <strong>Microservices Architecture, Spring Boot, Cloud Deployment</strong>.</li>
      <li>⚡ Fun fact: I reduced query response time by <strong>40%</strong> through database optimization and indexing strategies.</li>
    </ul>
  </div>
  <div align="center">
    <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExY3JkbWZodmM4cGFlY2Q2YzZ4NWU4amN6MnQzdHk5a2M0b3R3bGZxcSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/LmNwrBhejkK9EFP504/giphy.gif" alt="Java Developer"/>
  </div>
</div>

<hr class="divider"/>

<h2 class="section-title">🛠️ Tech Arsenal</h2>

<div class="card">
  <div class="tech-grid">
    <div class="tech-cell">
      <strong>☕ Languages</strong>
      <img src="https://skillicons.dev/icons?i=java,javascript,python,cpp,php" alt="Languages"/>
    </div>
    <div class="tech-cell">
      <strong>🎨 Frontend</strong>
      <img src="https://skillicons.dev/icons?i=react,html,css,tailwind,bootstrap" alt="Frontend"/>
    </div>
    <div class="tech-cell">
      <strong>⚙️ Backend</strong>
      <img src="https://skillicons.dev/icons?i=nodejs,spring,express" alt="Backend"/>
    </div>
    <div class="tech-cell">
      <strong>🗄️ Databases</strong>
      <img src="https://skillicons.dev/icons?i=mysql,mongodb,postgres" alt="Databases"/>
    </div>
    <div class="tech-cell">
      <strong>🧰 Dev Tools</strong>
      <img src="https://skillicons.dev/icons?i=git,github,vscode,linux,postman" alt="Dev Tools"/>
    </div>
    <div class="tech-cell">
      <strong>🚀 Deployment</strong>
      <img src="https://skillicons.dev/icons?i=vercel,netlify,heroku" alt="Deployment"/>
    </div>
  </div>
</div>

<hr class="divider"/>

<h2 class="section-title">💼 Experience & Focus Areas</h2>

<div class="card table-scroll">
  <table class="styled-table">
    <thead>
      <tr>
        <th>🏢 Domain</th>
        <th>🎯 Expertise</th>
        <th>🚀 Achievements</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><strong>Java Development</strong></td>
        <td>OOP, Design Patterns, Multithreading</td>
        <td>Built 5+ production-ready Java applications</td>
      </tr>
      <tr>
        <td><strong>Database Systems</strong></td>
        <td>MySQL Optimization, Schema Design</td>
        <td>40% faster queries through indexing strategies</td>
      </tr>
      <tr>
        <td><strong>Full-Stack Apps</strong></td>
        <td>REST APIs, Client-Server Architecture</td>
        <td>Complete solutions from backend to frontend</td>
      </tr>
      <tr>
        <td><strong>System Architecture</strong></td>
        <td>Clean Code, SOLID Principles</td>
        <td>Scalable, maintainable codebases</td>
      </tr>
    </tbody>
  </table>
</div>

<hr class="divider"/>

<h2 class="section-title">🚀 Featured Projects</h2>

<div class="project-cards">
  <div class="project-card">
    <h4>📋 TaskFlow Manager</h4>
    <p>Comprehensive task management with user auth, deadlines, and categories.</p>
    <span class="project-tag">Java • MySQL • OOP • SOLID</span>
  </div>
  <div class="project-card">
    <h4>💬 Real-time ChatVerse</h4>
    <p>Multi-client chat system with real-time messaging & history.</p>
    <span class="project-tag">Java • Sockets • Multithreading • MySQL</span>
  </div>
  <div class="project-card">
    <h4>🏥 MediCare HMS</h4>
    <p>Complete hospital management with patient records, billing & appointments.</p>
    <span class="project-tag">Java • Swing • MySQL • JDBC</span>
  </div>
</div>

<hr class="divider"/>

<h2 class="section-title">🎓 Education & Certifications</h2>

<div class="card">
  <ul class="edu-list">
    <li>🎓 <strong>B.Sc. in Computer Science</strong> — Dire Dawa University (In Progress)</li>
    <li>☕ <strong>Oracle Certified Associate, Java SE</strong> — In Progress</li>
    <li>📊 <strong>Data Structures & Algorithms</strong> — Advanced Problem Solving</li>
    <li>🖥️ <strong>Full-Stack Web Development</strong> — Self-taught & Project-Based</li>
    <li>💡 <strong>Database Design & Optimization</strong> — MySQL Certified</li>
  </ul>
</div>

<hr class="divider"/>

<h2 class="section-title">🏆 Achievements</h2>

<div align="center">
  <img class="achievement-img" src="./assets/Cursor-Virtual-Hackathon-Addis-Ababa-Abreham-Wendesen.png" alt="Hackathon Achievement"/>
</div>

<hr class="divider"/>

<h2 class="section-title">⚡ Live Stats Dashboard</h2>

<div class="card card-glow" align="center">

<img src="https://readme-typing-svg.herokuapp.com/?font=Fira+Code&weight=700&size=26&pause=1000&color=6366F1&center=true&vCenter=true&width=600&lines=───+SYSTEM+STATUS+───;+JAVA+ARCHITECT+ONLINE;+PLAYER:+abrshiz;+CURRENT+RANK:+A-CLASS;+COMPILING..." alt="System Status" />

<br/><br/>

<div class="stats-grid">
  <img height="185" src="https://github-readme-stats-eight-theta.vercel.app/api?username=abrshiz&show_icons=true&theme=radical&include_all_commits=true&count_private=true" alt="GitHub Stats"/>
  <img height="185" src="https://github-readme-stats-eight-theta.vercel.app/api/top-langs/?username=abrshiz&layout=compact&langs_count=7&theme=radical" alt="Top Languages"/>
</div>

<br/>

<div class="stats-row">
  <div class="gif-box">
    <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExenFpbzFqeDk4dmYxaW9nYzFldjE2czY1NGRiN3RmYmN6dWl1dGZwaSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/26tn33aiTi1jkl6H6/giphy.gif" alt="Java Code"/>
  </div>
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=abrshiz&theme=radical&hide_border=false" alt="GitHub Streak"/>
</div>

</div>

<hr class="divider"/>

<h2 class="section-title">📈 Contribution Graph</h2>

<div class="card" align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=abrshiz&theme=react-dark&bg_color=0d1117&color=6366f1&line=8b5cf6&point=ffffff&area=true&hide_border=true" width="100%" alt="Contribution Graph"/>
</div>

<hr class="divider"/>

<h2 class="section-title">🧠 Coding Philosophy</h2>

<div class="philosophy card">
  <blockquote>“Great software is built on solid foundations — clean code, thoughtful architecture, and relentless optimization.”</blockquote>
  <p>I believe in writing code that's not just functional but <strong>elegant</strong> and <strong>maintainable</strong>. Every project is an opportunity to craft something that solves real problems and stands the test of time.</p>
</div>

<hr class="divider"/>

<h2 class="section-title">🤝 Let's Connect</h2>

<p align="center" style="color: var(--text-muted);">Building something awesome? Let's collaborate and create impact together.</p>

<div class="connect-row">
  <a href="mailto:abrhamwendesen.ta@ddu.edu.et"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"/></a>
  <a href="https://linkedin.com/in/abrshiz"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
  <a href="https://github.com/abrshiz"><img src="https://img.shields.io/badge/GitHub-171515?style=for-the-badge&logo=github&logoColor=white"/></a>
  <a href="https://t.me/abrshiz"><img src="https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white"/></a>
  <a href="https://x.com/abrsiz"><img src="https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white"/></a>
</div>

<br/>

<img src="https://readme-typing-svg.herokuapp.com/?font=Fira+Code&size=20&duration=4000&pause=1000&color=6366F1&center=true&vCenter=true&width=600&lines=Thanks+for+stopping+by!;☕+Java+is+life,+but+creativity+is+soul;⭐+Star+my+repos+if+they+inspire+you!;Keep+coding,+keep+building." alt="Thanks Typing SVG"/>

</div>

<br/>

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=100&section=footer"/>

<img src="https://komarev.com/ghpvc/?username=abrshiz&label=Profile%20views&color=6366f1&style=for-the-badge" />

</div>
