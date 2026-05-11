<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mohsin Syed Ali | AIML Professional Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;900&family=DM+Sans:wght@300;400;500&family=Space+Mono:wght@400;700&display=swap" rel="stylesheet">
<style>
  :root {
    --crimson: #8B0000;
    --gold: #C9A84C;
    --cream: #FAF7F2;
    --charcoal: #1A1A1A;
    --slate: #3D3D3D;
    --light-gray: #EFEFEF;
    --white: #FFFFFF;
    --accent: #D4A853;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--cream);
    color: var(--charcoal);
    line-height: 1.7;
  }

  /* NAV */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    background: rgba(139,0,0,0.97);
    backdrop-filter: blur(10px);
    display: flex; justify-content: space-between; align-items: center;
    padding: 1rem 3rem;
    border-bottom: 2px solid var(--gold);
  }
  .nav-brand {
    font-family: 'Space Mono', monospace;
    color: var(--gold);
    font-size: 0.85rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
  }
  .nav-links { display: flex; gap: 2rem; list-style: none; }
  .nav-links a {
    color: var(--cream);
    text-decoration: none;
    font-size: 0.8rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--gold); }

  /* HERO */
  .hero {
    min-height: 100vh;
    background: linear-gradient(135deg, var(--crimson) 0%, #4A0000 60%, #1A0000 100%);
    display: flex; align-items: center;
    padding: 8rem 3rem 4rem;
    position: relative;
    overflow: hidden;
  }
  .hero::before {
    content: '';
    position: absolute; inset: 0;
    background-image: radial-gradient(circle at 80% 20%, rgba(201,168,76,0.15) 0%, transparent 50%),
                      radial-gradient(circle at 20% 80%, rgba(201,168,76,0.08) 0%, transparent 40%);
  }
  .hero::after {
    content: 'AI/ML';
    position: absolute;
    right: -2rem; bottom: -3rem;
    font-family: 'Playfair Display', serif;
    font-size: 18rem;
    font-weight: 900;
    color: rgba(255,255,255,0.03);
    letter-spacing: -0.05em;
    line-height: 1;
    pointer-events: none;
  }
  .hero-content { position: relative; max-width: 900px; }
  .hero-tag {
    display: inline-block;
    font-family: 'Space Mono', monospace;
    font-size: 0.75rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--gold);
    border: 1px solid var(--gold);
    padding: 0.4rem 1rem;
    margin-bottom: 2rem;
  }
  .hero h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(3rem, 7vw, 6rem);
    font-weight: 900;
    color: var(--white);
    line-height: 1.05;
    margin-bottom: 1.5rem;
  }
  .hero h1 span { color: var(--gold); }
  .hero-sub {
    font-size: 1.1rem;
    color: rgba(255,255,255,0.75);
    max-width: 560px;
    margin-bottom: 3rem;
    font-weight: 300;
  }
  .hero-cta {
    display: inline-block;
    background: var(--gold);
    color: var(--charcoal);
    padding: 0.9rem 2.5rem;
    font-family: 'Space Mono', monospace;
    font-size: 0.8rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    text-decoration: none;
    font-weight: 700;
    transition: all 0.2s;
  }
  .hero-cta:hover { background: var(--white); transform: translateY(-2px); }

  /* SECTIONS */
  section { padding: 5rem 3rem; }
  .section-label {
    font-family: 'Space Mono', monospace;
    font-size: 0.7rem;
    letter-spacing: 0.25em;
    text-transform: uppercase;
    color: var(--crimson);
    margin-bottom: 0.75rem;
  }
  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2rem, 4vw, 3rem);
    font-weight: 700;
    color: var(--charcoal);
    margin-bottom: 2rem;
  }
  .section-title span { color: var(--crimson); }
  .divider {
    width: 60px; height: 3px;
    background: var(--gold);
    margin-bottom: 2.5rem;
  }

  /* BIO */
  .bio-section { background: var(--white); }
  .bio-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 4rem; align-items: start; max-width: 1100px; margin: 0 auto; }
  .bio-text p { color: var(--slate); margin-bottom: 1rem; font-size: 1rem; }
  .bio-stats { display: grid; grid-template-columns: 1fr 1fr; gap: 1.5rem; }
  .stat-card {
    background: var(--cream);
    border-left: 4px solid var(--crimson);
    padding: 1.5rem;
  }
  .stat-num {
    font-family: 'Playfair Display', serif;
    font-size: 2.5rem;
    font-weight: 900;
    color: var(--crimson);
    line-height: 1;
  }
  .stat-label { font-size: 0.8rem; color: var(--slate); margin-top: 0.3rem; text-transform: uppercase; letter-spacing: 0.08em; }

  /* VALUE PROPOSITION */
  .vp-section { background: var(--charcoal); }
  .vp-section .section-label { color: var(--gold); }
  .vp-section .section-title { color: var(--white); }
  .vp-card {
    background: rgba(255,255,255,0.05);
    border: 1px solid rgba(201,168,76,0.3);
    border-left: 5px solid var(--gold);
    padding: 2.5rem;
    max-width: 800px;
    font-family: 'Playfair Display', serif;
    font-size: 1.3rem;
    color: var(--cream);
    font-style: italic;
    line-height: 1.8;
    margin-bottom: 2rem;
  }
  .vp-pillars { display: grid; grid-template-columns: repeat(4, 1fr); gap: 1.5rem; max-width: 1000px; }
  .vp-pillar {
    background: rgba(255,255,255,0.04);
    border-top: 3px solid var(--gold);
    padding: 1.5rem;
  }
  .vp-pillar-title { font-family: 'Space Mono', monospace; font-size: 0.75rem; color: var(--gold); letter-spacing: 0.1em; margin-bottom: 0.5rem; }
  .vp-pillar p { font-size: 0.85rem; color: rgba(255,255,255,0.65); }

  /* ARTIFACT */
  .artifact-section { background: var(--cream); }
  .artifact-meta {
    display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.5rem;
    max-width: 1100px; margin-bottom: 3rem;
  }
  .meta-card {
    background: var(--white);
    border-top: 3px solid var(--crimson);
    padding: 1.5rem;
  }
  .meta-card h4 { font-family: 'Space Mono', monospace; font-size: 0.7rem; color: var(--crimson); letter-spacing: 0.15em; text-transform: uppercase; margin-bottom: 0.5rem; }
  .meta-card p { font-size: 0.9rem; color: var(--slate); }

  /* ML FRAMEWORK / INFOGRAPHIC */
  .infographic { max-width: 1100px; margin: 0 auto; }
  .infographic-title {
    font-family: 'Playfair Display', serif;
    font-size: 1.6rem;
    color: var(--charcoal);
    margin-bottom: 0.5rem;
    border-bottom: 2px solid var(--crimson);
    padding-bottom: 0.75rem;
    margin-bottom: 2rem;
  }

  /* Domain header row */
  .domains-row {
    display: grid;
    grid-template-columns: 200px repeat(4, 1fr);
    gap: 2px;
    margin-bottom: 2px;
  }
  .domain-header {
    background: var(--crimson);
    color: var(--white);
    font-family: 'Space Mono', monospace;
    font-size: 0.7rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    padding: 0.75rem 1rem;
    text-align: center;
    font-weight: 700;
  }
  .domain-header:first-child { background: var(--charcoal); }

  /* Algorithm rows */
  .algo-row {
    display: grid;
    grid-template-columns: 200px repeat(4, 1fr);
    gap: 2px;
    margin-bottom: 2px;
  }
  .algo-name {
    background: var(--white);
    border-left: 4px solid var(--crimson);
    padding: 1rem;
    display: flex; flex-direction: column; justify-content: center;
  }
  .algo-name strong {
    font-size: 0.85rem;
    color: var(--charcoal);
    display: block;
    margin-bottom: 0.2rem;
  }
  .algo-name .algo-type {
    font-family: 'Space Mono', monospace;
    font-size: 0.62rem;
    color: var(--crimson);
    letter-spacing: 0.05em;
    text-transform: uppercase;
  }
  .algo-cell {
    background: var(--light-gray);
    padding: 0.75rem 0.5rem;
    text-align: center;
    font-size: 0.78rem;
    color: var(--slate);
    display: flex; align-items: center; justify-content: center;
    min-height: 70px;
    line-height: 1.4;
  }
  .algo-cell.active {
    background: linear-gradient(135deg, #fff8ee, #fef0d5);
    border: 1px solid var(--gold);
    color: var(--charcoal);
    font-weight: 500;
  }
  .algo-cell.primary {
    background: linear-gradient(135deg, #fff0f0, #ffe0e0);
    border: 1px solid var(--crimson);
    color: var(--crimson);
    font-weight: 600;
  }

  /* Legend */
  .legend {
    display: flex; gap: 2rem; margin-top: 1.5rem; flex-wrap: wrap;
  }
  .legend-item { display: flex; align-items: center; gap: 0.5rem; font-size: 0.8rem; color: var(--slate); }
  .legend-box { width: 20px; height: 14px; }
  .legend-box.primary { background: #ffe0e0; border: 1px solid var(--crimson); }
  .legend-box.active { background: #fff8ee; border: 1px solid var(--gold); }
  .legend-box.inactive { background: var(--light-gray); }

  /* Algorithm detail cards */
  .algo-cards { display: grid; grid-template-columns: repeat(2, 1fr); gap: 1.5rem; margin-top: 3rem; max-width: 1100px; }
  .algo-card {
    background: var(--white);
    border-top: 4px solid var(--gold);
    padding: 1.5rem;
  }
  .algo-card-header { display: flex; align-items: flex-start; justify-content: space-between; margin-bottom: 0.75rem; }
  .algo-card h3 { font-family: 'Playfair Display', serif; font-size: 1.1rem; color: var(--charcoal); }
  .tag {
    display: inline-block;
    font-family: 'Space Mono', monospace;
    font-size: 0.6rem;
    padding: 0.2rem 0.6rem;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    border-radius: 2px;
  }
  .tag.supervised { background: #ffe0e0; color: var(--crimson); }
  .tag.unsupervised { background: #e0eaff; color: #1a3a7a; }
  .tag.both { background: #e8ffe0; color: #1a6a1a; }
  .algo-card p { font-size: 0.85rem; color: var(--slate); margin-bottom: 0.75rem; }
  .use-case { font-size: 0.78rem; color: var(--charcoal); background: var(--cream); padding: 0.5rem 0.75rem; border-left: 3px solid var(--gold); }
  .use-case strong { color: var(--crimson); }

  /* PROCESS */
  .process-section { background: var(--white); }
  .process-steps { display: grid; grid-template-columns: repeat(4, 1fr); gap: 1px; background: var(--light-gray); max-width: 1100px; }
  .process-step { background: var(--white); padding: 2rem 1.5rem; position: relative; }
  .step-num {
    font-family: 'Playfair Display', serif;
    font-size: 3rem;
    font-weight: 900;
    color: rgba(139,0,0,0.08);
    line-height: 1;
    margin-bottom: 0.5rem;
  }
  .step-title { font-family: 'Space Mono', monospace; font-size: 0.75rem; color: var(--crimson); letter-spacing: 0.1em; text-transform: uppercase; margin-bottom: 0.5rem; }
  .process-step p { font-size: 0.85rem; color: var(--slate); }

  /* TOOLS */
  .tools-section { background: var(--cream); }
  .tools-grid { display: flex; flex-wrap: wrap; gap: 1rem; max-width: 900px; }
  .tool-chip {
    background: var(--white);
    border: 1px solid rgba(139,0,0,0.2);
    padding: 0.5rem 1.2rem;
    font-family: 'Space Mono', monospace;
    font-size: 0.75rem;
    color: var(--charcoal);
    letter-spacing: 0.05em;
  }
  .tool-chip:hover { background: var(--crimson); color: var(--white); }

  /* FOOTER */
  footer {
    background: var(--charcoal);
    color: rgba(255,255,255,0.5);
    padding: 3rem;
    text-align: center;
    font-size: 0.8rem;
    font-family: 'Space Mono', monospace;
    letter-spacing: 0.05em;
  }
  footer span { color: var(--gold); }

  /* RESPONSIVE */
  @media (max-width: 900px) {
    nav { padding: 1rem 1.5rem; }
    .nav-links { display: none; }
    section { padding: 3.5rem 1.5rem; }
    .bio-grid { grid-template-columns: 1fr; gap: 2rem; }
    .vp-pillars { grid-template-columns: repeat(2, 1fr); }
    .artifact-meta { grid-template-columns: 1fr; }
    .domains-row, .algo-row { grid-template-columns: 140px repeat(4, 1fr); font-size: 0.7rem; }
    .algo-cards { grid-template-columns: 1fr; }
    .process-steps { grid-template-columns: repeat(2, 1fr); }
  }

  /* ANIMATION */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(30px); }
    to   { opacity: 1; transform: translateY(0); }
  }
  .hero-tag  { animation: fadeUp 0.6s ease both; }
  .hero h1   { animation: fadeUp 0.6s 0.15s ease both; }
  .hero-sub  { animation: fadeUp 0.6s 0.3s ease both; }
  .hero-cta  { animation: fadeUp 0.6s 0.45s ease both; }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-brand">Mohsin Syed Ali · AIML Portfolio</div>
  <ul class="nav-links">
    <li><a href="#bio">About</a></li>
    <li><a href="#vp">Value Proposition</a></li>
    <li><a href="#artifact">Artifact</a></li>
    <li><a href="#process">Process</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-content">
    <div class="hero-tag">AIML Professional Portfolio · Indiana Wesleyan University</div>
    <h1>Mohsin<br>Syed <span>Ali</span></h1>
    <p class="hero-sub">Emerging AI & Machine Learning practitioner building expertise in intelligent systems, data-driven decision-making, and generative AI applications.</p>
    <a href="#artifact" class="hero-cta">View Portfolio Artifact →</a>
  </div>
</section>

<!-- BIO -->
<section class="bio-section" id="bio">
  <div class="bio-grid">
    <div class="bio-text">
      <div class="section-label">Professional Bio</div>
      <div class="section-title">About <span>Me</span></div>
      <div class="divider"></div>
      <p>My name is Mohsin Syed Ali, and I am an AIML student at Indiana Wesleyan University with a growing passion for the intersection of data science, machine learning, and real-world problem solving.</p>
      <p>My journey into AI and machine learning is driven by curiosity — a desire to understand not just how algorithms work, but how they can be applied to create meaningful outcomes for organizations and individuals. I bring a structured, analytical approach to problem-solving combined with a commitment to continuous learning in this rapidly evolving field.</p>
      <p>Through my coursework, I am building competencies across supervised and unsupervised learning, computer vision, natural language processing, and generative AI — areas that represent the cutting edge of technological innovation. My goal is to leverage these skills to help organizations make smarter, data-informed decisions.</p>
    </div>
    <div>
      <div class="bio-stats">
        <div class="stat-card">
          <div class="stat-num">10+</div>
          <div class="stat-label">ML Algorithms Studied</div>
        </div>
        <div class="stat-card">
          <div class="stat-num">4</div>
          <div class="stat-label">AI Domains Explored</div>
        </div>
        <div class="stat-card">
          <div class="stat-num">IWU</div>
          <div class="stat-label">Indiana Wesleyan University</div>
        </div>
        <div class="stat-card">
          <div class="stat-num">AI/ML</div>
          <div class="stat-label">Program of Study</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- VALUE PROPOSITION -->
<section class="vp-section" id="vp">
  <div class="section-label">Personal Value Proposition</div>
  <div class="section-title" style="color:var(--white);">What I <span style="color:var(--gold);">Bring</span></div>
  <div class="divider"></div>
  <div class="vp-card">
    "As an AI/ML student with a foundational background in machine learning algorithms, data pattern recognition, and generative AI concepts, I help organizations and peers bridge the gap between theoretical AI knowledge and practical application — translating complex algorithmic frameworks into clear, actionable insights that support smarter decision-making and innovation."
  </div>
  <div class="vp-pillars">
    <div class="vp-pillar">
      <div class="vp-pillar-title">Clarity</div>
      <p>I translate complex ML concepts into accessible frameworks anyone can understand.</p>
    </div>
    <div class="vp-pillar">
      <div class="vp-pillar-title">Focus</div>
      <p>Grounded in practical, real-world application of AI/ML across key industry domains.</p>
    </div>
    <div class="vp-pillar">
      <div class="vp-pillar-title">Growth</div>
      <p>Actively developing skills at the forefront of AI, including generative AI systems.</p>
    </div>
    <div class="vp-pillar">
      <div class="vp-pillar-title">Impact</div>
      <p>Committed to using AI knowledge to drive meaningful outcomes for organizations.</p>
    </div>
  </div>
</section>

<!-- ARTIFACT -->
<section class="artifact-section" id="artifact">
  <div class="section-label">Portfolio Artifact</div>
  <div class="section-title">ML Algorithm <span>Visual Framework</span></div>
  <div class="divider"></div>

  <!-- Meta -->
  <div class="artifact-meta">
    <div class="meta-card">
      <h4>Objective</h4>
      <p>To categorize and visually map 10 key machine learning algorithms across their learning types and primary application domains including Tabular Data, Computer Vision, NLP, and Generative AI.</p>
    </div>
    <div class="meta-card">
      <h4>Tools Used</h4>
      <p>Research synthesis · Visual framework design · Comparative matrix · Real-world use case analysis · Portfolio documentation</p>
    </div>
    <div class="meta-card">
      <h4>Artifact Value Proposition</h4>
      <p>This framework serves as a quick-reference guide for practitioners selecting appropriate ML algorithms — demonstrating my ability to synthesize and communicate complex AI concepts clearly.</p>
    </div>
  </div>

  <!-- INFOGRAPHIC -->
  <div class="infographic">
    <div class="infographic-title">Machine Learning Algorithm Domain Matrix</div>

    <!-- Domain Header Row -->
    <div class="domains-row">
      <div class="domain-header">Algorithm</div>
      <div class="domain-header">📊 Tabular Data</div>
      <div class="domain-header">🖼 Computer Vision</div>
      <div class="domain-header">💬 NLP</div>
      <div class="domain-header">✨ Generative AI</div>
    </div>

    <!-- Algorithm rows -->
    <div class="algo-row">
      <div class="algo-name"><strong>Random Forest</strong><span class="algo-type">Supervised</span></div>
      <div class="algo-cell primary">Classification &amp; Regression<br>on structured data</div>
      <div class="algo-cell active">Basic image classification</div>
      <div class="algo-cell">—</div>
      <div class="algo-cell">—</div>
    </div>
    <div class="algo-row">
      <div class="algo-name"><strong>Gradient Boosting (XGBoost)</strong><span class="algo-type">Supervised</span></div>
      <div class="algo-cell primary">High-accuracy prediction;<br>Kaggle competitions</div>
      <div class="algo-cell">—</div>
      <div class="algo-cell">—</div>
      <div class="algo-cell">—</div>
    </div>
    <div class="algo-row">
      <div class="algo-name"><strong>Decision Tree</strong><span class="algo-type">Supervised</span></div>
      <div class="algo-cell primary">Rule-based classification;<br>Loan approval</div>
      <div class="algo-cell">—</div>
      <div class="algo-cell">—</div>
      <div class="algo-cell">—</div>
    </div>
    <div class="algo-row">
      <div class="algo-name"><strong>Support Vector Machine</strong><span class="algo-type">Supervised</span></div>
      <div class="algo-cell active">High-dimensional classification</div>
      <div class="algo-cell active">Image classification (small data)</div>
      <div class="algo-cell active">Text classification</div>
      <div class="algo-cell">—</div>
    </div>
    <div class="algo-row">
      <div class="algo-name"><strong>Linear Regression</strong><span class="algo-type">Supervised</span></div>
      <div class="algo-cell primary">Price prediction;<br>Trend forecasting</div>
      <div class="algo-cell">—</div>
      <div class="algo-cell">—</div>
      <div class="algo-cell">—</div>
    </div>
    <div class="algo-row">
      <div class="algo-name"><strong>CNN (Convolutional NN)</strong><span class="algo-type">Supervised</span></div>
      <div class="algo-cell">—</div>
      <div class="algo-cell primary">Image classification;<br>Object detection; Face ID</div>
      <div class="algo-cell">—</div>
      <div class="algo-cell active">Image generation base layer</div>
    </div>
    <div class="algo-row">
      <div class="algo-name"><strong>Transformer (GPT/BERT)</strong><span class="algo-type">Supervised</span></div>
      <div class="algo-cell">—</div>
      <div class="algo-cell">—</div>
      <div class="algo-cell primary">Language modeling;<br>Sentiment analysis; QA</div>
      <div class="algo-cell primary">Text generation;<br>ChatGPT, Claude</div>
    </div>
    <div class="algo-row">
      <div class="algo-name"><strong>K-Means Clustering</strong><span class="algo-type">Unsupervised</span></div>
      <div class="algo-cell primary">Customer segmentation;<br>Anomaly detection</div>
      <div class="algo-cell active">Image segmentation</div>
      <div class="algo-cell active">Topic clustering</div>
      <div class="algo-cell">—</div>
    </div>
    <div class="algo-row">
      <div class="algo-name"><strong>GAN (Generative Adversarial)</strong><span class="algo-type">Unsupervised</span></div>
      <div class="algo-cell">—</div>
      <div class="algo-cell active">Synthetic image creation</div>
      <div class="algo-cell">—</div>
      <div class="algo-cell primary">Image generation;<br>Deepfakes; Art synthesis</div>
    </div>
    <div class="algo-row">
      <div class="algo-name"><strong>Diffusion Model (Stable Diffusion)</strong><span class="algo-type">Unsupervised</span></div>
      <div class="algo-cell">—</div>
      <div class="algo-cell active">High-fidelity image synthesis</div>
      <div class="algo-cell">—</div>
      <div class="algo-cell primary">Text-to-image generation;<br>DALL·E, Midjourney</div>
    </div>

    <!-- Legend -->
    <div class="legend">
      <div class="legend-item"><div class="legend-box primary"></div> Primary domain application</div>
      <div class="legend-item"><div class="legend-box active"></div> Secondary / supporting use</div>
      <div class="legend-item"><div class="legend-box inactive"></div> Not applicable</div>
    </div>
  </div>

  <!-- Algorithm Detail Cards -->
  <div class="algo-cards">
    <div class="algo-card">
      <div class="algo-card-header">
        <h3>Random Forest</h3>
        <span class="tag supervised">Supervised</span>
      </div>
      <p>An ensemble method that builds multiple decision trees during training and merges them for more accurate, stable predictions. It reduces overfitting through randomness in feature selection.</p>
      <div class="use-case"><strong>Real-World Use:</strong> Credit risk scoring, medical diagnosis, fraud detection in financial transactions.</div>
    </div>
    <div class="algo-card">
      <div class="algo-card-header">
        <h3>Gradient Boosting (XGBoost)</h3>
        <span class="tag supervised">Supervised</span>
      </div>
      <p>Builds trees sequentially, where each new tree corrects errors of the previous ones. Known for exceptional performance on tabular/structured datasets.</p>
      <div class="use-case"><strong>Real-World Use:</strong> Competitive ML benchmarks, click-through rate prediction, e-commerce recommendation ranking.</div>
    </div>
    <div class="algo-card">
      <div class="algo-card-header">
        <h3>Decision Tree</h3>
        <span class="tag supervised">Supervised</span>
      </div>
      <p>A flowchart-like model that splits data based on feature values. Highly interpretable and ideal for rule-based classification tasks where transparency matters.</p>
      <div class="use-case"><strong>Real-World Use:</strong> Loan approval decisions, medical triage, customer churn classification.</div>
    </div>
    <div class="algo-card">
      <div class="algo-card-header">
        <h3>Support Vector Machine (SVM)</h3>
        <span class="tag supervised">Supervised</span>
      </div>
      <p>Finds the optimal hyperplane that best separates data classes with maximum margin. Effective in high-dimensional spaces and works well for text classification tasks.</p>
      <div class="use-case"><strong>Real-World Use:</strong> Email spam filtering, image categorization, bioinformatics gene classification.</div>
    </div>
    <div class="algo-card">
      <div class="algo-card-header">
        <h3>CNN (Convolutional Neural Network)</h3>
        <span class="tag supervised">Supervised</span>
      </div>
      <p>Uses layers of convolutional filters to automatically learn spatial hierarchies of features from images. The go-to architecture for all visual recognition tasks.</p>
      <div class="use-case"><strong>Real-World Use:</strong> Face recognition (Face ID), tumor detection in medical imaging, autonomous vehicle object detection.</div>
    </div>
    <div class="algo-card">
      <div class="algo-card-header">
        <h3>Transformer (GPT / BERT)</h3>
        <span class="tag supervised">Supervised</span>
      </div>
      <p>Uses self-attention mechanisms to model relationships between all words in a sequence simultaneously, enabling context-aware language understanding at massive scale.</p>
      <div class="use-case"><strong>Real-World Use:</strong> ChatGPT, Google Search, sentiment analysis, legal document summarization.</div>
    </div>
    <div class="algo-card">
      <div class="algo-card-header">
        <h3>K-Means Clustering</h3>
        <span class="tag unsupervised">Unsupervised</span>
      </div>
      <p>Groups data into K clusters by iteratively assigning points to the nearest centroid and updating centroids. No labels required — discovers natural structure in data.</p>
      <div class="use-case"><strong>Real-World Use:</strong> Customer segmentation for marketing, document clustering, anomaly detection in network security.</div>
    </div>
    <div class="algo-card">
      <div class="algo-card-header">
        <h3>GAN (Generative Adversarial Network)</h3>
        <span class="tag unsupervised">Unsupervised</span>
      </div>
      <p>Two networks compete — a generator creates synthetic data and a discriminator judges authenticity. This adversarial process produces highly realistic synthetic outputs.</p>
      <div class="use-case"><strong>Real-World Use:</strong> Synthetic training data generation, deepfake creation, photo enhancement, drug molecule generation.</div>
    </div>
    <div class="algo-card">
      <div class="algo-card-header">
        <h3>Diffusion Model</h3>
        <span class="tag unsupervised">Unsupervised</span>
      </div>
      <p>Learns to reverse a gradual noising process — starting from pure noise and progressively denoising to generate a realistic image guided by text prompts.</p>
      <div class="use-case"><strong>Real-World Use:</strong> DALL·E 3, Stable Diffusion, Midjourney — text-to-image generation, AI art, creative design tools.</div>
    </div>
    <div class="algo-card">
      <div class="algo-card-header">
        <h3>PCA (Principal Component Analysis)</h3>
        <span class="tag unsupervised">Unsupervised</span>
      </div>
      <p>Reduces data dimensionality by finding principal components — directions of maximum variance. Used for visualization and as preprocessing for other algorithms.</p>
      <div class="use-case"><strong>Real-World Use:</strong> Gene expression analysis, image compression, exploratory data analysis, noise reduction.</div>
    </div>
  </div>
</section>

<!-- PROCESS -->
<section class="process-section" id="process">
  <div class="section-label">How This Artifact Was Created</div>
  <div class="section-title">My <span>Process</span></div>
  <div class="divider"></div>
  <div class="process-steps">
    <div class="process-step">
      <div class="step-num">01</div>
      <div class="step-title">Research</div>
      <p>Reviewed course materials, IWU resources, and supplementary reading on AI/ML model categories across supervised, unsupervised, and generative domains.</p>
    </div>
    <div class="process-step">
      <div class="step-num">02</div>
      <div class="step-title">Categorize</div>
      <p>Identified 10 algorithms spanning all required domains. Mapped each to its learning type (supervised vs. unsupervised) and primary application areas.</p>
    </div>
    <div class="process-step">
      <div class="step-num">03</div>
      <div class="step-title">Design</div>
      <p>Built a comparative matrix framework and individual algorithm cards to present information visually and accessibly for both technical and non-technical audiences.</p>
    </div>
    <div class="process-step">
      <div class="step-num">04</div>
      <div class="step-title">Refine</div>
      <p>Added real-world use cases for each algorithm to anchor abstract concepts in practical application, maximizing the portfolio's value to potential employers.</p>
    </div>
  </div>
</section>

<!-- TOOLS -->
<section class="tools-section">
  <div class="section-label">Tools &amp; Technologies</div>
  <div class="section-title">What I <span>Used</span></div>
  <div class="divider"></div>
  <div class="tools-grid">
    <div class="tool-chip">HTML / CSS</div>
    <div class="tool-chip">Research Synthesis</div>
    <div class="tool-chip">Visual Framework Design</div>
    <div class="tool-chip">Generative AI Tools</div>
    <div class="tool-chip">Comparative Matrix</div>
    <div class="tool-chip">Use Case Analysis</div>
    <div class="tool-chip">Academic Coursework (IWU)</div>
    <div class="tool-chip">Portfolio Documentation</div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <p><span>Mohsin Syed Ali</span> · AIML Professional Portfolio · Indiana Wesleyan University · 2025</p>
  <p style="margin-top:0.5rem; font-size:0.7rem;">Artifact: Machine Learning Algorithm Visual Framework · Course Assignment Submission</p>
</footer>

</body>
</html>
