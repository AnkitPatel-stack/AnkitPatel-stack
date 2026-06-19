<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="Ankit Patel - Full Stack MERN Developer Portfolio. React, Node.js, Express, MongoDB expert building scalable web applications." />
  <meta name="keywords" content="Ankit Patel, Full Stack Developer, MERN Stack, React Developer, Node.js Developer" />
  <title>Ankit Patel - Full Stack MERN Developer</title>

  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@300;400;600;700&display=swap" rel="stylesheet" />
  
  <!-- Font Awesome -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" />

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Fira Code', monospace;
      background: linear-gradient(135deg, #0a0a1a 0%, #1a1a2e 50%, #16213e 100%);
      color: #e0e0e0;
      padding: 20px;
      min-height: 100vh;
    }

    .container {
      max-width: 1100px;
      margin: 0 auto;
      padding: 20px;
    }

    /* Typing Effect */
    .typing-text {
      font-size: 1.8rem;
      font-weight: 600;
      color: #00f7ff;
      text-align: center;
      min-height: 60px;
      border-right: 3px solid #00f7ff;
      display: inline-block;
      white-space: nowrap;
      overflow: hidden;
      animation: blink-caret 0.75s step-end infinite;
    }

    @keyframes blink-caret {
      0%, 100% { border-color: transparent; }
      50% { border-color: #00f7ff; }
    }

    /* Cards */
    .card {
      background: rgba(255, 255, 255, 0.05);
      backdrop-filter: blur(10px);
      border: 1px solid rgba(255, 255, 255, 0.08);
      border-radius: 20px;
      padding: 30px;
      margin-bottom: 30px;
      transition: all 0.4s ease;
    }

    .card:hover {
      transform: translateY(-5px);
      border-color: #00f7ff;
      box-shadow: 0 0 30px rgba(0, 247, 255, 0.1);
    }

    /* Section Titles */
    .section-title {
      font-size: 2rem;
      font-weight: 700;
      margin-bottom: 20px;
      background: linear-gradient(135deg, #00f7ff, #7b2ffc);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    .section-title i {
      margin-right: 12px;
    }

    /* Profile Image */
    .profile-img {
      width: 180px;
      height: 180px;
      border-radius: 50%;
      border: 4px solid #00f7ff;
      object-fit: cover;
      margin: 0 auto 20px;
      display: block;
      box-shadow: 0 0 40px rgba(0, 247, 255, 0.2);
    }

    /* Badge */
    .badge {
      display: inline-block;
      padding: 8px 20px;
      margin: 5px;
      border-radius: 50px;
      background: rgba(0, 247, 255, 0.1);
      color: #00f7ff;
      border: 1px solid rgba(0, 247, 255, 0.2);
      font-size: 0.85rem;
      transition: all 0.3s ease;
    }

    .badge:hover {
      background: rgba(0, 247, 255, 0.2);
      transform: scale(1.05);
    }

    /* Skill Icons */
    .skill-icon {
      display: inline-block;
      margin: 8px;
      padding: 12px 18px;
      background: rgba(255, 255, 255, 0.05);
      border-radius: 12px;
      border: 1px solid rgba(255, 255, 255, 0.08);
      transition: all 0.3s ease;
      font-size: 0.9rem;
    }

    .skill-icon:hover {
      transform: translateY(-3px);
      border-color: #00f7ff;
      box-shadow: 0 0 20px rgba(0, 247, 255, 0.1);
    }

    .skill-icon i {
      margin-right: 8px;
      color: #00f7ff;
    }

    /* Grid */
    .grid-2 {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 30px;
    }

    .grid-3 {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    /* Project Cards */
    .project-card {
      background: rgba(255, 255, 255, 0.03);
      padding: 25px;
      border-radius: 16px;
      border: 1px solid rgba(255, 255, 255, 0.06);
      transition: all 0.3s ease;
      text-align: center;
    }

    .project-card:hover {
      transform: translateY(-5px);
      border-color: #00f7ff;
      box-shadow: 0 0 30px rgba(0, 247, 255, 0.08);
    }

    .project-card i {
      font-size: 2.5rem;
      color: #00f7ff;
      margin-bottom: 15px;
    }

    .project-card h4 {
      color: #fff;
      margin-bottom: 8px;
    }

    .project-card p {
      color: #aaa;
      font-size: 0.9rem;
      line-height: 1.5;
    }

    /* Social Icons */
    .social-links {
      display: flex;
      justify-content: center;
      gap: 15px;
      flex-wrap: wrap;
      margin: 20px 0;
    }

    .social-links a {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      padding: 12px 25px;
      border-radius: 50px;
      text-decoration: none;
      color: #fff;
      font-weight: 600;
      transition: all 0.3s ease;
      font-size: 0.9rem;
    }

    .social-links a:hover {
      transform: translateY(-3px);
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
    }

    .social-links a i {
      font-size: 1.2rem;
    }

    .social-links .gmail { background: #D14836; }
    .social-links .linkedin { background: #0A66C2; }
    .social-links .github { background: #333; }

    /* Stats */
    .stat-box {
      text-align: center;
      padding: 20px;
      background: rgba(255, 255, 255, 0.03);
      border-radius: 16px;
      border: 1px solid rgba(255, 255, 255, 0.06);
    }

    .stat-box .number {
      font-size: 2.5rem;
      font-weight: 700;
      color: #00f7ff;
    }

    .stat-box .label {
      color: #aaa;
      font-size: 0.85rem;
      margin-top: 5px;
    }

    /* Responsive */
    @media (max-width: 768px) {
      .grid-2, .grid-3 {
        grid-template-columns: 1fr;
      }

      .typing-text {
        font-size: 1.2rem;
        white-space: normal;
      }

      .profile-img {
        width: 140px;
        height: 140px;
      }

      .social-links a {
        padding: 10px 18px;
        font-size: 0.8rem;
      }

      .stat-box .number {
        font-size: 1.8rem;
      }
    }

    /* Scrollbar */
    ::-webkit-scrollbar {
      width: 8px;
    }
    ::-webkit-scrollbar-track {
      background: #0a0a1a;
    }
    ::-webkit-scrollbar-thumb {
      background: #00f7ff;
      border-radius: 10px;
    }
  </style>
</head>
<body>

<div class="container">

  <!-- ===== HEADER ===== -->
  <div class="card" style="text-align: center; border-color: rgba(0,247,255,0.2);">
    <img src="https://github.com/user-attachments/assets/8e881061-d97c-4f0e-8d03-676360dce275" alt="Banner" style="width:100%; border-radius:12px; margin-bottom:25px;" />

    <h1 style="font-size: 2.8rem; font-weight: 700; background: linear-gradient(135deg, #00f7ff, #7b2ffc); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;">
      👋 Hi, I'm Ankit Patel
    </h1>

    <h3 style="color: #00f7ff; font-weight: 400; margin: 10px 0 20px;">
      🚀 Full Stack MERN Developer | React · Node.js · Express · MongoDB
    </h3>

    <!-- Typing Animation -->
    <div style="text-align: center; margin: 15px 0 25px;">
      <div class="typing-text" id="typing-text"></div>
    </div>

    <!-- Social Links -->
    <div class="social-links">
      <a href="mailto:ankitpatellll782@gmail.com" class="gmail">
        <i class="fas fa-envelope"></i> Gmail
      </a>
      <a href="https://www.linkedin.com/in/ankit-patel-460974286" class="linkedin" target="_blank">
        <i class="fab fa-linkedin-in"></i> LinkedIn
      </a>
      <a href="https://github.com/AnkitPatel-stack" class="github" target="_blank">
        <i class="fab fa-github"></i> GitHub
      </a>
    </div>
  </div>

  <!-- ===== ABOUT ===== -->
  <div class="card">
    <h2 class="section-title"><i class="fas fa-user-astronaut"></i> About Me</h2>
    <div class="grid-2">
      <div>
        <p style="font-size: 1.05rem; line-height: 1.8; color: #ccc;">
          💼 <strong>Role:</strong> Full Stack Developer<br />
          🌍 <strong>Location:</strong> India<br />
          ⚡ <strong>Focus:</strong> Scalable Web Apps + SaaS Systems<br />
          🧠 <strong>Learning:</strong> System Design + DevOps + Cloud<br />
          🔥 <strong>Goal:</strong> Product Based Company + Startup Projects
        </p>
      </div>
      <div style="display: flex; flex-wrap: wrap; gap: 10px; align-items: center;">
        <span class="badge"><i class="fas fa-code"></i> MERN Stack</span>
        <span class="badge"><i class="fas fa-database"></i> MongoDB</span>
        <span class="badge"><i class="fas fa-server"></i> Node.js</span>
        <span class="badge"><i class="fab fa-react"></i> React</span>
        <span class="badge"><i class="fas fa-cloud"></i> Cloud Ready</span>
        <span class="badge"><i class="fas fa-rocket"></i> Startup Mindset</span>
      </div>
    </div>
  </div>

  <!-- ===== TECH STACK ===== -->
  <div class="card">
    <h2 class="section-title"><i class="fas fa-cogs"></i> Tech Stack</h2>
    <div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 10px;">
      <span class="skill-icon"><i class="fab fa-html5"></i> HTML5</span>
      <span class="skill-icon"><i class="fab fa-css3-alt"></i> CSS3</span>
      <span class="skill-icon"><i class="fab fa-js"></i> JavaScript</span>
      <span class="skill-icon"><i class="fab fa-react"></i> React</span>
      <span class="skill-icon"><i class="fab fa-node-js"></i> Next.js</span>
      <span class="skill-icon"><i class="fas fa-code"></i> Redux</span>
      <span class="skill-icon"><i class="fab fa-node-js"></i> Node.js</span>
      <span class="skill-icon"><i class="fas fa-server"></i> Express</span>
      <span class="skill-icon"><i class="fas fa-database"></i> MongoDB</span>
      <span class="skill-icon"><i class="fab fa-js"></i> TypeScript</span>
      <span class="skill-icon"><i class="fas fa-fire"></i> Firebase</span>
      <span class="skill-icon"><i class="fab fa-git-alt"></i> Git</span>
      <span class="skill-icon"><i class="fab fa-github"></i> GitHub</span>
      <span class="skill-icon"><i class="fab fa-bootstrap"></i> Bootstrap</span>
      <span class="skill-icon"><i class="fas fa-paint-brush"></i> Material UI</span>
      <span class="skill-icon"><i class="fas fa-code"></i> VS Code</span>
    </div>
  </div>

  <!-- ===== STATS ===== -->
  <div class="card">
    <h2 class="section-title"><i class="fas fa-chart-line"></i> GitHub Analytics</h2>
    <div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 20px;">
      <img src="https://github-readme-stats.vercel.app/api?username=AnkitPatel-stack&show_icons=true&theme=tokyonight&hide_border=true" alt="GitHub Stats" style="max-width:100%;" />
      <img src="https://github-readme-streak-stats.herokuapp.com/?user=AnkitPatel-stack&theme=tokyonight&hide_border=true" alt="GitHub Streak" style="max-width:100%;" />
    </div>
    <div style="text-align: center; margin-top: 20px;">
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=AnkitPatel-stack&layout=compact&theme=tokyonight&hide_border=true" alt="Top Languages" style="max-width:100%;" />
    </div>
  </div>

  <!-- ===== CONTRIBUTION SNAKE ===== -->
  <div class="card">
    <h2 class="section-title"><i class="fas fa-snake"></i> Contribution Snake</h2>
    <div style="text-align: center;">
      <img src="https://raw.githubusercontent.com/AnkitPatel-stack/AnkitPatel-stack/output/github-contribution-grid-snake.svg" alt="Contribution Snake" style="max-width:100%;" />
    </div>
  </div>

  <!-- ===== CONTRIBUTION GRAPH ===== -->
  <div class="card">
    <h2 class="section-title"><i class="fas fa-chart-bar"></i> Contribution Graph</h2>
    <div style="text-align: center;">
      <img src="https://github-readme-activity-graph.vercel.app/graph?username=AnkitPatel-stack&theme=react-dark&hide_border=true" alt="Contribution Graph" style="max-width:100%;" />
    </div>
  </div>

  <!-- ===== TROPHIES ===== -->
  <div class="card">
    <h2 class="section-title"><i class="fas fa-trophy"></i> GitHub Trophies</h2>
    <div style="text-align: center;">
      <img src="https://github-profile-trophy.vercel.app/?username=AnkitPatel-stack&theme=tokyonight&no-frame=true&margin-w=10&margin-h=10" alt="GitHub Trophies" style="max-width:100%;" />
    </div>
  </div>

  <!-- ===== FEATURED PROJECTS ===== -->
  <div class="card">
    <h2 class="section-title"><i class="fas fa-project-diagram"></i> Featured Projects</h2>
    <div class="grid-3">
      <div class="project-card">
        <i class="fas fa-plane"></i>
        <h4>🚀 Tripwale</h4>
        <p>Full Stack Travel Platform (MERN + Deployment)</p>
      </div>
      <div class="project-card">
        <i class="fas fa-users-cog"></i>
        <h4>👥 User Management System</h4>
        <p>Authentication + Admin Panel + CRUD System</p>
      </div>
      <div class="project-card">
        <i class="fas fa-robot"></i>
        <h4>🤖 AI Website</h4>
        <p>AI-powered frontend system with modern UI</p>
      </div>
      <div class="project-card">
        <i class="fas fa-comments"></i>
        <h4>💬 Real-Time Chat App</h4>
        <p>Socket.io based live messaging system</p>
      </div>
    </div>
  </div>

  <!-- ===== SYSTEM SKILLS ===== -->
  <div class="card">
    <h2 class="section-title"><i class="fas fa-microchip"></i> System Skills</h2>
    <div style="display: flex; flex-wrap: wrap; gap: 15px; justify-content: center;">
      <span class="badge"><i class="fab fa-react"></i> React.js</span>
      <span class="badge"><i class="fab fa-node-js"></i> Next.js</span>
      <span class="badge"><i class="fas fa-code"></i> Redux</span>
      <span class="badge"><i class="fab fa-node-js"></i> Node.js</span>
      <span class="badge"><i class="fas fa-server"></i> Express.js</span>
      <span class="badge"><i class="fas fa-database"></i> MongoDB</span>
      <span class="badge"><i class="fas fa-fire"></i> Firebase</span>
      <span class="badge"><i class="fab fa-git-alt"></i> Git</span>
      <span class="badge"><i class="fab fa-github"></i> GitHub</span>
      <span class="badge"><i class="fas fa-bolt"></i> Postman</span>
      <span class="badge"><i class="fas fa-cloud"></i> VPS</span>
      <span class="badge"><i class="fas fa-server"></i> Hostinger</span>
      <span class="badge"><i class="fas fa-rocket"></i> Vercel</span>
    </div>
  </div>

  <!-- ===== DEV MINDSET ===== -->
  <div class="card" style="border-color: rgba(0,247,255,0.2);">
    <h2 class="section-title"><i class="fas fa-brain"></i> Dev Mindset</h2>
    <blockquote style="font-size: 1.2rem; text-align: center; color: #00f7ff; font-style: italic; padding: 15px;">
      “I don’t just write code — I build real-world scalable systems.”
    </blockquote>
    <div style="display: flex; flex-wrap: wrap; gap: 15px; justify-content: center; margin-top: 15px;">
      <span class="badge"><i class="fas fa-check-circle"></i> Clean Architecture</span>
      <span class="badge"><i class="fas fa-tachometer-alt"></i> Performance First</span>
      <span class="badge"><i class="fas fa-cogs"></i> Production Ready</span>
      <span class="badge"><i class="fas fa-server"></i> Scalable Backend</span>
    </div>
  </div>

  <!-- ===== OPEN TO WORK ===== -->
  <div class="card" style="text-align: center; border-color: #00f7ff;">
    <h2 style="font-size: 2.2rem; font-weight: 700; color: #00f7ff;">
      <i class="fas fa-briefcase"></i> Open To Work
    </h2>
    <p style="font-size: 1.1rem; color: #ccc; margin: 10px 0 20px;">
      Full Stack Developer | MERN Stack | Remote · On-site · Freelance
    </p>
    <a href="https://drive.google.com/" target="_blank" style="display: inline-block; padding: 14px 40px; background: #00f7ff; color: #0a0a1a; border-radius: 50px; text-decoration: none; font-weight: 700; margin: 5px; transition: all 0.3s ease;">
      <i class="fas fa-file-pdf"></i> Download Resume
    </a>
    <a href="https://your-portfolio-link.com" target="_blank" style="display: inline-block; padding: 14px 40px; background: rgba(255,255,255,0.1); color: #fff; border-radius: 50px; text-decoration: none; font-weight: 700; margin: 5px; border: 1px solid #00f7ff; transition: all 0.3s ease;">
      <i class="fas fa-globe"></i> Visit Portfolio
    </a>
  </div>

  <!-- ===== FOOTER ===== -->
  <div style="text-align: center; padding: 30px 0 15px; border-top: 1px solid rgba(255,255,255,0.05); margin-top: 20px;">
    <p style="font-size: 0.9rem; color: #666;">
      🚀 Building the future with code &nbsp;·&nbsp; 💙 Passion + Consistency + Projects = Success &nbsp;·&nbsp; ⚡ Always learning, always improving
    </p>
    <p style="font-size: 0.85rem; color: #444; margin-top: 10px;">
      💎 Crafted with Passion by Ankit Patel
    </p>
  </div>

</div>

<!-- ===== TYPING EFFECT SCRIPT ===== -->
<script>
  const phrases = [
    "Full Stack MERN Developer",
    "React | Node | Express | MongoDB",
    "Building Scalable Web Applications",
    "UI + Backend + Deployment",
    "Always Learning New Tech 🚀"
  ];

  let phraseIndex = 0;
  let charIndex = 0;
  let isDeleting = false;
  const typingElement = document.getElementById('typing-text');

  function typeEffect() {
    const currentPhrase = phrases[phraseIndex];
    
    if (isDeleting) {
      typingElement.textContent = currentPhrase.substring(0, charIndex - 1);
      charIndex--;
    } else {
      typingElement.textContent = currentPhrase.substring(0, charIndex + 1);
      charIndex++;
    }

    let delay = isDeleting ? 50 : 100;

    if (!isDeleting && charIndex === currentPhrase.length) {
      delay = 2000;
      isDeleting = true;
    } else if (isDeleting && charIndex === 0) {
      isDeleting = false;
      phraseIndex = (phraseIndex + 1) % phrases.length;
      delay = 500;
    }

    setTimeout(typeEffect, delay);
  }

  typeEffect();
</script>

</body>
</html>
