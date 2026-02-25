<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Sai Ganesh Penchikala — GitHub Profile</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;700&family=Syne:wght@700;800&display=swap" rel="stylesheet"/>
<style>
  :root {
    --bg: #0d0b1e;
    --surface: #13112a;
    --surface2: #1a1735;
    --border: #2e2a5a;
    --accent: #a78bfa;
    --accent2: #60a5fa;
    --accent3: #34d399;
    --accent4: #f472b6;
    --text: #e2e8f0;
    --muted: #94a3b8;
    --glow: rgba(167,139,250,0.15);
  }
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  
  body {
    font-family: 'Space Grotesk', sans-serif;
    background: var(--bg);
    color: var(--text);
    overflow-x: hidden;
  }

  /* Animated background */
  body::before {
    content: '';
    position: fixed;
    top: 0; left: 0; right: 0; bottom: 0;
    background: 
      radial-gradient(ellipse at 20% 20%, rgba(167,139,250,0.08) 0%, transparent 50%),
      radial-gradient(ellipse at 80% 80%, rgba(96,165,250,0.06) 0%, transparent 50%),
      radial-gradient(ellipse at 50% 50%, rgba(52,211,153,0.04) 0%, transparent 60%);
    pointer-events: none;
    z-index: 0;
  }

  .container { max-width: 900px; margin: 0 auto; padding: 0 24px; position: relative; z-index: 1; }

  /* Hero */
  .hero {
    text-align: center;
    padding: 80px 24px 60px;
    position: relative;
  }
  .hero-avatar {
    width: 120px; height: 120px;
    border-radius: 50%;
    background: linear-gradient(135deg, var(--accent), var(--accent2));
    display: flex; align-items: center; justify-content: center;
    font-size: 48px;
    margin: 0 auto 24px;
    box-shadow: 0 0 40px rgba(167,139,250,0.4);
    animation: pulse-avatar 3s ease-in-out infinite;
  }
  @keyframes pulse-avatar {
    0%, 100% { box-shadow: 0 0 40px rgba(167,139,250,0.4); }
    50% { box-shadow: 0 0 70px rgba(167,139,250,0.7); }
  }
  .hero h1 {
    font-family: 'Syne', sans-serif;
    font-size: clamp(2rem, 5vw, 3.5rem);
    font-weight: 800;
    background: linear-gradient(135deg, #fff 0%, var(--accent) 50%, var(--accent2) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    margin-bottom: 8px;
    animation: fadeUp 0.8s ease both;
  }
  .hero .subtitle {
    font-family: 'JetBrains Mono', monospace;
    color: var(--accent);
    font-size: 1rem;
    margin-bottom: 16px;
    animation: fadeUp 0.8s 0.2s ease both;
  }
  .hero .location {
    color: var(--muted);
    font-size: 0.9rem;
    margin-bottom: 32px;
    animation: fadeUp 0.8s 0.3s ease both;
  }
  
  /* Animated typing effect */
  .typing-container {
    font-family: 'JetBrains Mono', monospace;
    font-size: 1.1rem;
    color: var(--accent3);
    height: 28px;
    margin-bottom: 36px;
    animation: fadeUp 0.8s 0.4s ease both;
  }
  .typing-text::after {
    content: '|';
    animation: blink 1s infinite;
    color: var(--accent);
  }
  @keyframes blink { 0%, 100% { opacity: 1; } 50% { opacity: 0; } }

  /* Badges row */
  .badges {
    display: flex; flex-wrap: wrap; gap: 10px; justify-content: center;
    animation: fadeUp 0.8s 0.5s ease both;
    margin-bottom: 48px;
  }
  .badge {
    padding: 6px 16px;
    border-radius: 100px;
    font-size: 0.8rem;
    font-weight: 600;
    border: 1px solid;
    transition: all 0.3s ease;
    cursor: pointer;
    text-decoration: none;
  }
  .badge:hover { transform: translateY(-2px); box-shadow: 0 8px 20px rgba(0,0,0,0.3); }
  .badge-purple { background: rgba(167,139,250,0.1); border-color: rgba(167,139,250,0.4); color: var(--accent); }
  .badge-blue { background: rgba(96,165,250,0.1); border-color: rgba(96,165,250,0.4); color: var(--accent2); }
  .badge-green { background: rgba(52,211,153,0.1); border-color: rgba(52,211,153,0.4); color: var(--accent3); }
  .badge-pink { background: rgba(244,114,182,0.1); border-color: rgba(244,114,182,0.4); color: var(--accent4); }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* Section */
  section {
    margin-bottom: 60px;
    animation: fadeUp 0.8s ease both;
  }
  .section-label {
    display: flex; align-items: center; gap: 12px;
    margin-bottom: 24px;
  }
  .section-label h2 {
    font-family: 'Syne', sans-serif;
    font-size: 1.5rem;
    font-weight: 700;
    color: var(--text);
  }
  .section-icon {
    width: 36px; height: 36px;
    border-radius: 10px;
    background: linear-gradient(135deg, var(--accent), var(--accent2));
    display: flex; align-items: center; justify-content: center;
    font-size: 18px;
    flex-shrink: 0;
  }
  .divider {
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--border), transparent);
    margin-bottom: 60px;
  }

  /* About grid */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
  }
  @media (max-width: 600px) { .about-grid { grid-template-columns: 1fr; } }
  .about-item {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 14px;
    padding: 16px 20px;
    display: flex; align-items: flex-start; gap: 12px;
    transition: all 0.3s ease;
  }
  .about-item:hover {
    border-color: var(--accent);
    transform: translateY(-2px);
    box-shadow: 0 8px 24px rgba(167,139,250,0.1);
  }
  .about-item-icon { font-size: 20px; margin-top: 2px; }
  .about-item-content { font-size: 0.88rem; color: var(--muted); line-height: 1.5; }
  .about-item-content strong { color: var(--text); display: block; margin-bottom: 2px; }

  /* Skills */
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    gap: 20px;
  }
  .skill-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 24px;
    transition: all 0.3s ease;
  }
  .skill-card:hover {
    border-color: var(--accent);
    box-shadow: 0 0 30px var(--glow);
    transform: translateY(-3px);
  }
  .skill-card h3 {
    font-size: 0.8rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    color: var(--accent);
    margin-bottom: 14px;
    font-family: 'JetBrains Mono', monospace;
  }
  .tech-tags { display: flex; flex-wrap: wrap; gap: 8px; }
  .tech-tag {
    padding: 4px 12px;
    border-radius: 6px;
    font-size: 0.78rem;
    font-weight: 600;
    font-family: 'JetBrains Mono', monospace;
  }
  .tag-java { background: rgba(237,139,0,0.15); color: #fbbf24; border: 1px solid rgba(237,139,0,0.3); }
  .tag-python { background: rgba(55,118,171,0.15); color: var(--accent2); border: 1px solid rgba(55,118,171,0.3); }
  .tag-js { background: rgba(247,223,30,0.15); color: #fde68a; border: 1px solid rgba(247,223,30,0.3); }
  .tag-react { background: rgba(97,218,251,0.15); color: #67e8f9; border: 1px solid rgba(97,218,251,0.3); }
  .tag-aws { background: rgba(255,153,0,0.15); color: #fdba74; border: 1px solid rgba(255,153,0,0.3); }
  .tag-spring { background: rgba(109,179,63,0.15); color: var(--accent3); border: 1px solid rgba(109,179,63,0.3); }
  .tag-sql { background: rgba(167,139,250,0.15); color: var(--accent); border: 1px solid rgba(167,139,250,0.3); }
  .tag-html { background: rgba(227,79,38,0.15); color: #fca5a5; border: 1px solid rgba(227,79,38,0.3); }
  .tag-css { background: rgba(21,114,182,0.15); color: #93c5fd; border: 1px solid rgba(21,114,182,0.3); }
  .tag-ai { background: rgba(244,114,182,0.15); color: var(--accent4); border: 1px solid rgba(244,114,182,0.3); }
  .tag-docker { background: rgba(36,150,237,0.15); color: #7dd3fc; border: 1px solid rgba(36,150,237,0.3); }
  .tag-db { background: rgba(49,97,146,0.15); color: #a5b4fc; border: 1px solid rgba(49,97,146,0.3); }

  /* Experience */
  .exp-timeline { position: relative; }
  .exp-timeline::before {
    content: '';
    position: absolute;
    left: 20px;
    top: 0; bottom: 0;
    width: 2px;
    background: linear-gradient(180deg, var(--accent), var(--accent2));
    border-radius: 2px;
  }
  .exp-item {
    position: relative;
    padding-left: 60px;
    margin-bottom: 32px;
  }
  .exp-dot {
    position: absolute;
    left: 12px;
    top: 4px;
    width: 18px; height: 18px;
    border-radius: 50%;
    background: linear-gradient(135deg, var(--accent), var(--accent2));
    box-shadow: 0 0 12px rgba(167,139,250,0.5);
  }
  .exp-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 24px;
    transition: all 0.3s ease;
  }
  .exp-card:hover {
    border-color: var(--accent);
    box-shadow: 0 8px 24px rgba(167,139,250,0.1);
  }
  .exp-header { display: flex; justify-content: space-between; align-items: flex-start; flex-wrap: wrap; gap: 8px; margin-bottom: 8px; }
  .exp-title { font-weight: 700; font-size: 1rem; color: var(--text); }
  .exp-company { color: var(--accent); font-size: 0.9rem; font-weight: 600; }
  .exp-meta { font-size: 0.8rem; color: var(--muted); font-family: 'JetBrains Mono', monospace; text-align: right; }
  .exp-list { list-style: none; margin-top: 12px; }
  .exp-list li {
    font-size: 0.88rem; color: var(--muted); line-height: 1.6;
    padding: 4px 0; padding-left: 16px; position: relative;
  }
  .exp-list li::before {
    content: '▸';
    position: absolute; left: 0;
    color: var(--accent3);
  }

  /* Projects */
  .projects-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(280px, 1fr)); gap: 20px; }
  .project-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 24px;
    position: relative;
    overflow: hidden;
    transition: all 0.3s ease;
    cursor: pointer;
  }
  .project-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 3px;
    border-radius: 16px 16px 0 0;
  }
  .project-card.ai::before { background: linear-gradient(90deg, var(--accent4), var(--accent)); }
  .project-card.ml::before { background: linear-gradient(90deg, var(--accent2), var(--accent3)); }
  .project-card.web::before { background: linear-gradient(90deg, var(--accent), var(--accent2)); }
  .project-card:hover {
    border-color: var(--accent);
    transform: translateY(-4px);
    box-shadow: 0 16px 40px rgba(0,0,0,0.3);
  }
  .project-emoji { font-size: 2rem; margin-bottom: 12px; }
  .project-title { font-weight: 700; font-size: 1rem; color: var(--text); margin-bottom: 8px; }
  .project-desc { font-size: 0.85rem; color: var(--muted); line-height: 1.6; margin-bottom: 16px; }
  .project-stack { display: flex; flex-wrap: wrap; gap: 6px; }
  .stack-tag {
    padding: 3px 10px;
    border-radius: 4px;
    font-size: 0.72rem;
    font-family: 'JetBrains Mono', monospace;
    font-weight: 600;
    background: rgba(167,139,250,0.1);
    color: var(--accent);
    border: 1px solid rgba(167,139,250,0.2);
  }

  /* Achievements */
  .achievement-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(240px, 1fr)); gap: 16px; }
  .achievement-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 14px;
    padding: 20px;
    display: flex; gap: 14px; align-items: flex-start;
    transition: all 0.3s ease;
  }
  .achievement-card:hover { border-color: var(--accent3); transform: translateY(-2px); }
  .achievement-icon { font-size: 24px; }
  .achievement-text { font-size: 0.88rem; color: var(--muted); line-height: 1.5; }
  .achievement-text strong { color: var(--text); display: block; margin-bottom: 2px; }

  /* Stats */
  .stats-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(200px, 1fr)); gap: 16px; margin-bottom: 32px; }
  .stat-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 14px;
    padding: 20px;
    text-align: center;
    transition: all 0.3s ease;
  }
  .stat-card:hover { border-color: var(--accent); box-shadow: 0 0 20px var(--glow); }
  .stat-value {
    font-family: 'Syne', sans-serif;
    font-size: 2rem;
    font-weight: 800;
    background: linear-gradient(135deg, var(--accent), var(--accent2));
    -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;
  }
  .stat-label { font-size: 0.8rem; color: var(--muted); margin-top: 4px; }

  /* GitHub image embed */
  .github-img {
    width: 100%;
    border-radius: 12px;
    border: 1px solid var(--border);
    margin-bottom: 16px;
  }
  .github-imgs { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin-bottom: 16px; }
  @media (max-width: 600px) { .github-imgs { grid-template-columns: 1fr; } }

  /* Footer */
  footer {
    text-align: center;
    padding: 60px 24px 40px;
    border-top: 1px solid var(--border);
    color: var(--muted);
    font-size: 0.85rem;
  }
  footer .quote {
    font-family: 'Syne', sans-serif;
    font-size: 1.3rem;
    color: var(--text);
    margin-bottom: 8px;
  }
  .connect-links { display: flex; justify-content: center; gap: 12px; flex-wrap: wrap; margin-top: 24px; }
  .connect-link {
    padding: 10px 20px;
    border-radius: 10px;
    font-size: 0.85rem;
    font-weight: 600;
    border: 1px solid var(--border);
    color: var(--text);
    text-decoration: none;
    transition: all 0.3s;
    background: var(--surface);
  }
  .connect-link:hover { border-color: var(--accent); color: var(--accent); box-shadow: 0 0 16px var(--glow); }

  /* Scroll reveal */
  .reveal { opacity: 0; transform: translateY(30px); transition: all 0.7s ease; }
  .reveal.visible { opacity: 1; transform: translateY(0); }

  /* Particles */
  .particles {
    position: fixed; top: 0; left: 0; width: 100%; height: 100%;
    pointer-events: none; z-index: 0;
  }
  .particle {
    position: absolute;
    width: 2px; height: 2px;
    border-radius: 50%;
    background: var(--accent);
    animation: float-particle linear infinite;
    opacity: 0;
  }
  @keyframes float-particle {
    0% { opacity: 0; transform: translateY(100vh) scale(0); }
    10% { opacity: 0.6; }
    90% { opacity: 0.2; }
    100% { opacity: 0; transform: translateY(-10vh) scale(1); }
  }
</style>
</head>
<body>

<!-- Floating particles -->
<div class="particles" id="particles"></div>

<!-- Hero -->
<div class="hero">
  <div class="hero-avatar">👨‍💻</div>
  <h1>Sai Ganesh Penchikala</h1>
  <div class="subtitle">Full Stack Java Developer & AI Builder</div>
  <div class="location">📍 Pedagarlapadu, Palnadu, Andhra Pradesh, India</div>

  <div class="typing-container">
    <span class="typing-text" id="typing"></span>
  </div>

  <div class="badges">
    <a class="badge badge-blue" href="mailto:saiganeshpenchikala2@gmail.com">✉️ saiganeshpenchikala2@gmail.com</a>
    <a class="badge badge-purple" href="https://linkedin.com/in/SaiGanesh" target="_blank">💼 linkedin.com/in/SaiGanesh</a>
    <a class="badge badge-green" href="https://github.com/SaiGanesh" target="_blank">🐙 github.com/SaiGanesh</a>
    <a class="badge badge-pink" href="tel:+918106967278">📞 +91 8106967278</a>
  </div>
</div>

<div class="container">

  <!-- About -->
  <section class="reveal">
    <div class="section-label">
      <div class="section-icon">🎯</div>
      <h2>About Me</h2>
    </div>
    <div class="about-grid">
      <div class="about-item">
        <div class="about-item-icon">🎓</div>
        <div class="about-item-content">
          <strong>B.Tech CS & IT</strong>
          Siddharth Institute of Engineering & Technology, Puttur, AP (2021–2025)
        </div>
      </div>
      <div class="about-item">
        <div class="about-item-icon">💼</div>
        <div class="about-item-content">
          <strong>Java Full Stack Trainee</strong>
          Codegnan IT Solutions, Hyderabad — June 2025 to Present
        </div>
      </div>
      <div class="about-item">
        <div class="about-item-icon">☁️</div>
        <div class="about-item-content">
          <strong>Cloud Experience</strong>
          AWS services: EC2, RDS, Lambda, CloudFront, S3, Route53
        </div>
      </div>
      <div class="about-item">
        <div class="about-item-icon">🤖</div>
        <div class="about-item-content">
          <strong>AI/ML Enthusiast</strong>
          Built GenAI chatbots, ML evaluation platforms with Hugging Face & OpenAI API
        </div>
      </div>
      <div class="about-item">
        <div class="about-item-icon">📄</div>
        <div class="about-item-content">
          <strong>Published Researcher</strong>
          Paper on Supervised Learning Model Insights in JARIIE journal
        </div>
      </div>
      <div class="about-item">
        <div class="about-item-icon">🏆</div>
        <div class="about-item-content">
          <strong>Award Winner</strong>
          Best Performance in VFX · Best Volunteer of the Year
        </div>
      </div>
    </div>
  </section>
  <div class="divider"></div>

  <!-- Skills -->
  <section class="reveal">
    <div class="section-label">
      <div class="section-icon">🛠️</div>
      <h2>Technology Stack</h2>
    </div>
    <div class="skills-grid">
      <div class="skill-card">
        <h3>💻 Languages</h3>
        <div class="tech-tags">
          <span class="tech-tag tag-java">Java</span>
          <span class="tech-tag tag-python">Python</span>
          <span class="tech-tag tag-js">JavaScript</span>
          <span class="tech-tag tag-sql">SQL</span>
        </div>
      </div>
      <div class="skill-card">
        <h3>🎨 Frontend</h3>
        <div class="tech-tags">
          <span class="tech-tag tag-html">HTML5</span>
          <span class="tech-tag tag-css">CSS3</span>
          <span class="tech-tag tag-react">React</span>
          <span class="tech-tag tag-css">Bootstrap</span>
        </div>
      </div>
      <div class="skill-card">
        <h3>⚙️ Backend & Frameworks</h3>
        <div class="tech-tags">
          <span class="tech-tag tag-spring">Spring</span>
          <span class="tech-tag tag-python">Django</span>
          <span class="tech-tag tag-ai">Hugging Face</span>
          <span class="tech-tag tag-ai">Gradio</span>
        </div>
      </div>
      <div class="skill-card">
        <h3>☁️ Cloud & DevOps</h3>
        <div class="tech-tags">
          <span class="tech-tag tag-aws">AWS EC2</span>
          <span class="tech-tag tag-aws">Lambda</span>
          <span class="tech-tag tag-aws">RDS</span>
          <span class="tech-tag tag-docker">Docker</span>
          <span class="tech-tag tag-aws">S3</span>
          <span class="tech-tag tag-aws">CloudFront</span>
        </div>
      </div>
      <div class="skill-card">
        <h3>🗄️ Databases</h3>
        <div class="tech-tags">
          <span class="tech-tag tag-db">MySQL</span>
          <span class="tech-tag tag-db">PostgreSQL</span>
          <span class="tech-tag tag-db">SQL</span>
        </div>
      </div>
      <div class="skill-card">
        <h3>📊 Data Science</h3>
        <div class="tech-tags">
          <span class="tech-tag tag-python">NumPy</span>
          <span class="tech-tag tag-python">Pandas</span>
          <span class="tech-tag tag-python">Matplotlib</span>
          <span class="tech-tag tag-ai">scikit-learn</span>
          <span class="tech-tag tag-ai">OpenAI API</span>
        </div>
      </div>
    </div>
  </section>
  <div class="divider"></div>

  <!-- Experience -->
  <section class="reveal">
    <div class="section-label">
      <div class="section-icon">💼</div>
      <h2>Experience</h2>
    </div>
    <div class="exp-timeline">
      <div class="exp-item">
        <div class="exp-dot"></div>
        <div class="exp-card">
          <div class="exp-header">
            <div>
              <div class="exp-title">Java Full Stack Trainee</div>
              <div class="exp-company">Codegnan IT Solutions</div>
            </div>
            <div class="exp-meta">June 2025 – Present<br/>Hyderabad, AP</div>
          </div>
          <ul class="exp-list">
            <li>Hands-on experience in HTML, CSS and JavaScript for building responsive web pages</li>
            <li>Learned backend development using Java, Python and database management with SQL</li>
            <li>Built projects integrating front-end and back-end components for full stack understanding</li>
          </ul>
        </div>
      </div>
      <div class="exp-item">
        <div class="exp-dot"></div>
        <div class="exp-card">
          <div class="exp-header">
            <div>
              <div class="exp-title">Full Stack Java Intern</div>
              <div class="exp-company">QSpiders</div>
            </div>
            <div class="exp-meta">Oct 2023 – Dec 2023<br/>Bangalore</div>
          </div>
          <ul class="exp-list">
            <li>Crafted responsive web interfaces using HTML, CSS and JavaScript</li>
            <li>Built dynamic front-ends and robust back-end systems using Java and SQL for data modeling</li>
            <li>Delivered end-to-end solutions with emphasis on performance, clean code architecture and user-centered design</li>
          </ul>
        </div>
      </div>
    </div>
  </section>
  <div class="divider"></div>

  <!-- Projects -->
  <section class="reveal">
    <div class="section-label">
      <div class="section-icon">🚀</div>
      <h2>Featured Projects</h2>
    </div>
    <div class="projects-grid">
      <div class="project-card ai">
        <div class="project-emoji">🤖</div>
        <div class="project-title">Generative AI ChatBot</div>
        <div class="project-desc">Conversational AI chatbot with human-like interactions across domains — includes study tips, career guidance and subject knowledge. Deployed with Hugging Face + OpenAI API for scalability.</div>
        <div class="project-stack">
          <span class="stack-tag">Python</span>
          <span class="stack-tag">Hugging Face</span>
          <span class="stack-tag">Gradio</span>
          <span class="stack-tag">OpenAI API</span>
        </div>
      </div>
      <div class="project-card ml">
        <div class="project-emoji">📊</div>
        <div class="project-title">ML Model Insights & Evaluation</div>
        <div class="project-desc">Web platform for evaluating ML model performance with key metrics and visualizations. Implemented hyperparameter tuning via GridSearchCV. <strong style="color:#34d399">Published in JARIIE Journal.</strong></div>
        <div class="project-stack">
          <span class="stack-tag">Python</span>
          <span class="stack-tag">Hugging Face</span>
          <span class="stack-tag">scikit-learn</span>
          <span class="stack-tag">GridSearchCV</span>
        </div>
      </div>
      <div class="project-card web">
        <div class="project-emoji">🍔</div>
        <div class="project-title">Food Munch Web App</div>
        <div class="project-desc">Responsive restaurant website deployed on AWS. Handles peak traffic with smooth UX across all screen sizes using EC2, RDS, Lambda, CloudFront, S3 and Route53.</div>
        <div class="project-stack">
          <span class="stack-tag">HTML</span>
          <span class="stack-tag">CSS</span>
          <span class="stack-tag">Bootstrap</span>
          <span class="stack-tag">JavaScript</span>
          <span class="stack-tag">AWS</span>
        </div>
      </div>
    </div>
  </section>
  <div class="divider"></div>

  <!-- Achievements -->
  <section class="reveal">
    <div class="section-label">
      <div class="section-icon">🏆</div>
      <h2>Achievements</h2>
    </div>
    <div class="achievement-grid">
      <div class="achievement-card">
        <div class="achievement-icon">🥇</div>
        <div class="achievement-text">
          <strong>Best Performance Award</strong>
          VFX at SFX Academy
        </div>
      </div>
      <div class="achievement-card">
        <div class="achievement-icon">🌟</div>
        <div class="achievement-text">
          <strong>Best Volunteer of the Year</strong>
          Siddharth Institutions
        </div>
      </div>
      <div class="achievement-card">
        <div class="achievement-icon">📄</div>
        <div class="achievement-text">
          <strong>Published Research Paper</strong>
          Supervised Learning Model Insights in JARIIE
        </div>
      </div>
      <div class="achievement-card">
        <div class="achievement-icon">☁️</div>
        <div class="achievement-text">
          <strong>AWS Cloud Deployment</strong>
          Production apps with 6+ AWS services
        </div>
      </div>
    </div>
  </section>
  <div class="divider"></div>

  <!-- GitHub Stats -->
  <section class="reveal">
    <div class="section-label">
      <div class="section-icon">📊</div>
      <h2>GitHub Analytics</h2>
    </div>
    <div class="github-imgs">
      <img class="github-img" src="https://github-readme-stats.vercel.app/api?username=SaiGanesh&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true" alt="GitHub Stats"/>
      <img class="github-img" src="https://github-readme-stats.vercel.app/api/top-langs/?username=SaiGanesh&layout=compact&langs_count=8&theme=tokyonight" alt="Top Languages"/>
    </div>
    <img class="github-img" src="https://github-readme-streak-stats.herokuapp.com/?user=SaiGanesh&theme=tokyonight&hide_border=true" alt="Streak Stats"/>
    <img class="github-img" src="https://github-readme-activity-graph.vercel.app/graph?username=SaiGanesh&theme=tokyo-night&bg_color=1a1b27&color=70a5fd&line=bf91f3&point=38bdae&area=true&hide_border=true" alt="Activity Graph"/>
  </section>

</div>

<!-- Footer -->
<footer>
  <div class="quote">"Code is poetry, and every commit tells a story" ✨</div>
  <p>B.Tech CS&IT · Full Stack Java Developer · AI Enthusiast · AWS Cloud</p>
  <div class="connect-links">
    <a class="connect-link" href="mailto:saiganeshpenchikala2@gmail.com">✉️ Email</a>
    <a class="connect-link" href="https://linkedin.com/in/SaiGanesh" target="_blank">💼 LinkedIn</a>
    <a class="connect-link" href="https://github.com/SaiGanesh" target="_blank">🐙 GitHub</a>
    <a class="connect-link" href="tel:+918106967278">📞 +91 8106967278</a>
  </div>
  <p style="margin-top:24px; font-size:0.78rem; color: #4a4a6a;">
    ⭐ Feel free to star any repositories you find interesting!
  </p>
</footer>

<script>
// Particles
const pc = document.getElementById('particles');
for (let i = 0; i < 30; i++) {
  const p = document.createElement('div');
  p.className = 'particle';
  p.style.left = Math.random() * 100 + 'vw';
  p.style.animationDuration = (8 + Math.random() * 12) + 's';
  p.style.animationDelay = (Math.random() * 10) + 's';
  p.style.width = p.style.height = (1 + Math.random() * 3) + 'px';
  const colors = ['#a78bfa','#60a5fa','#34d399','#f472b6'];
  p.style.background = colors[Math.floor(Math.random() * colors.length)];
  pc.appendChild(p);
}

// Typing effect
const lines = [
  'Java Full Stack Developer 🚀',
  'Building Scalable Web Apps ⚙️',
  'AI & Cloud Enthusiast 🤖',
  'Always Learning, Always Building 💪',
];
let lineIdx = 0, charIdx = 0, deleting = false;
const el = document.getElementById('typing');
function type() {
  const current = lines[lineIdx];
  if (!deleting) {
    el.textContent = current.substring(0, charIdx + 1);
    charIdx++;
    if (charIdx === current.length) {
      deleting = true;
      setTimeout(type, 2000);
      return;
    }
  } else {
    el.textContent = current.substring(0, charIdx - 1);
    charIdx--;
    if (charIdx === 0) {
      deleting = false;
      lineIdx = (lineIdx + 1) % lines.length;
    }
  }
  setTimeout(type, deleting ? 40 : 80);
}
type();

// Scroll reveal
const observer = new IntersectionObserver(entries => {
  entries.forEach(e => {
    if (e.isIntersecting) e.target.classList.add('visible');
  });
}, { threshold: 0.1 });
document.querySelectorAll('.reveal').forEach(el => observer.observe(el));
</script>
</body>
</html>
