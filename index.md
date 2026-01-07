---
layout: default
---
<style>
/* --- MASTER CSS DASHBOARD THEME --- */
:root {
    --bg-dark: #0d1117;
    --bg-panel: #161b22;
    --border: #30363d;
    --accent: #2f81f7; /* GitHub/Data Blue */
    --text-main: #c9d1d9;
    --text-muted: #8b949e;
}

body {
    background-color: var(--bg-dark);
    color: var(--text-main);
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
}

.wrapper {
    max-width: 100% !important;
    width: 100% !important;
    margin: 0 !important;
    padding: 0 !important;
    display: flex;
    min-height: 100vh;
}

/* --- SIDEBAR --- */
header {
    width: 320px !important;
    min-width: 320px !important;
    background-color: var(--bg-dark);
    border-right: 1px solid var(--border);
    position: fixed;
    height: 100vh;
    padding: 40px !important;
    overflow-y: auto;
    z-index: 100;
}

/* Fix the redundant name in sidebar */
header h1, header h2 {
    font-size: 1.1rem !important; 
    color: var(--text-muted) !important;
    margin-bottom: 20px !important;
    font-weight: 500;
}
header p {
    font-size: 0.85rem;
    color: var(--text-muted);
    line-height: 1.5;
}

/* Sidebar Button Styling */
.contact-section { margin-top: 20px; }
.contact-section a, header a {
    color: var(--accent);
    text-decoration: none;
}
.contact-btn {
    display: block;
    background-color: var(--bg-panel);
    border: 1px solid var(--border);
    color: #fff !important;
    text-align: center;
    padding: 10px 0;
    margin-top: 10px;
    border-radius: 6px;
    font-weight: 600;
    transition: all 0.2s;
}
.contact-btn:hover {
    background-color: var(--accent);
    border-color: var(--accent);
}

/* --- CONTENT AREA --- */
section {
    margin-left: 320px !important;
    width: calc(100% - 320px) !important;
    max-width: 1400px !important;
    padding: 60px 80px !important;
}

/* --- COMPONENTS --- */

/* Hero/KPI Section */
.hero-section {
    background: linear-gradient(180deg, var(--bg-panel) 0%, var(--bg-dark) 100%);
    border: 1px solid var(--border);
    border-radius: 6px;
    padding: 40px;
    margin-bottom: 50px;
}
.hero-label {
    color: var(--accent);
    font-size: 0.8rem;
    font-weight: 600;
    letter-spacing: 1px;
    text-transform: uppercase;
    margin-bottom: 10px;
}
.hero-title {
    font-size: 2.5rem;
    color: #fff;
    margin: 10px 0;
}
.hero-stats {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
    gap: 20px;
    margin-top: 30px;
    border-top: 1px solid var(--border);
    padding-top: 20px;
}
.stat-value { font-size: 1.8rem; font-weight: 700; color: #fff; }
.stat-label { font-size: 0.8rem; color: var(--text-muted); }

/* Projects Grid */
.projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
    gap: 20px;
    margin-bottom: 40px;
}
.project-card {
    background-color: var(--bg-panel);
    border: 1px solid var(--border);
    border-radius: 6px;
    padding: 25px;
    transition: transform 0.2s, border-color 0.2s;
}
.project-card:hover {
    transform: translateY(-2px);
    border-color: var(--accent);
}
.project-label {
    font-size: 0.7rem;
    font-weight: bold;
    color: var(--text-muted);
    border: 1px solid var(--border);
    padding: 2px 8px;
    border-radius: 100px;
}
.project-metrics {
    display: flex;
    gap: 20px;
    margin: 15px 0;
    padding: 10px 0;
    border-top: 1px solid #30363d50;
    border-bottom: 1px solid #30363d50;
}
.metric-value { font-weight: bold; color: #fff; }
.metric-label { font-size: 0.75rem; color: var(--text-muted); }
.project-links { margin-top: 15px; }
.project-link { margin-right: 15px; font-weight: 600; font-size: 0.9rem; }

/* Tech Tags */
.tech-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin: 15px 0;
}
.tech-tag {
    font-size: 0.75rem;
    font-family: monospace;
    background: #21262d;
    color: var(--accent);
    padding: 4px 8px;
    border-radius: 4px;
}

/* Skills Grid */
.skills-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
}
.skill-category {
    background: var(--bg-panel);
    padding: 20px;
    border-radius: 6px;
    border: 1px solid var(--border);
}
.skill-category h3 {
    margin-top: 0;
    font-size: 1rem;
    color: #fff;
    border-bottom: 1px solid var(--border);
    padding-bottom: 10px;
}

/* Experience Timeline */
.experience-timeline {
    display: flex;
    flex-direction: column;
    gap: 20px;
    margin-top: 20px;
    position: relative;
    border-left: 2px solid var(--border);
    padding-left: 20px;
}
.experience-card {
    background-color: var(--bg-panel);
    border: 1px solid var(--border);
    border-radius: 6px;
    padding: 25px;
    position: relative;
}
.experience-card::before {
    content: '';
    position: absolute;
    left: -27px;
    top: 30px;
    width: 12px;
    height: 12px;
    background: var(--accent);
    border-radius: 50%;
    border: 2px solid var(--bg-dark);
}
.experience-header {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    margin-bottom: 15px;
    flex-wrap: wrap;
    gap: 10px;
}
.experience-title { font-size: 1.1rem; font-weight: 700; color: #fff; }
.experience-company { font-size: 0.9rem; color: var(--accent); margin-top: 4px; }
.experience-period {
    font-size: 0.85rem;
    color: var(--text-muted);
    font-family: monospace;
    background: #21262d;
    padding: 4px 8px;
    border-radius: 4px;
}

/* Mobile Fix */
@media screen and (max-width: 900px) {
    .wrapper { flex-direction: column; }
    header { width: 100% !important; position: relative; height: auto; border-right: none; }
    section { margin-left: 0 !important; width: 100% !important; padding: 20px !important; }
    .skills-grid { grid-template-columns: 1fr; }
    .experience-timeline { padding-left: 0; border-left: none; }
    .experience-card::before { display: none; }
}
</style>

<div class="hero-section">
  <div class="hero-label">DATA ANALYST • SUPPLY CHAIN & OPERATIONS RESEARCH</div>
  <h1 class="hero-title">Dominic Correlli</h1>
  <p class="hero-description">
    Building data-driven solutions for supply chain optimization and operational analytics. 
    Combining SQL, Python, and statistical modeling to solve complex business problems.
  </p>
  
  <div class="hero-stats">
    <div class="stat-item">
      <div class="stat-value">100K+</div>
      <div class="stat-label">Records Analyzed</div>
    </div>
    <div class="stat-item">
      <div class="stat-value">3.5</div>
      <div class="stat-label">GPA, MS Analytics</div>
    </div>
    <div class="stat-item">
      <div class="stat-value">2026</div>
      <div class="stat-label">Graduation</div>
    </div>
  </div>
</div>

## Featured Projects

<div class="projects-grid">
  <div class="project-card">
    <span class="project-label">HACKATHON SUBMISSION</span>
    <h3><a href="https://aistudio.google.com/app/prompts?state=%7B%22ids%22:%5B%2210Ilr0ZjTGTSeEU5f54OON0zdIhpIH1WO%22%5D,%22action%22:%22open%22,%22userId%22:%22102934307143670763064%22,%22resourceKeys%22:%7B%7D%7D&usp=sharing" target="_blank">E.S.T.E.R. Invoice Intelligence</a></h3>
    <p>AI-powered invoice processing platform built for Google DeepMind Gemini API Developer Competition. Handles 11 languages with automated price discrepancy detection and prescriptive procurement analytics.</p>
    <div class="tech-tags">
      <span class="tech-tag">Python</span>
      <span class="tech-tag">Gemini API</span>
      <span class="tech-tag">OCR</span>
      <span class="tech-tag">Streamlit</span>
    </div>
    <div class="project-metrics">
      <div class="metric">
        <div class="metric-value">11</div>
        <div class="metric-label">Languages</div>
      </div>
      <div class="metric">
        <div class="metric-value">~2000</div>
        <div class="metric-label">Competitors</div>
      </div>
    </div>
    <div class="project-links">
      <a href="https://aistudio.google.com/app/prompts?state=%7B%22ids%22:%5B%2210Ilr0ZjTGTSeEU5f54OON0zdIhpIH1WO%22%5D,%22action%22:%22open%22,%22userId%22:%22102934307143670763064%22,%22resourceKeys%22:%7B%7D%7D&usp=sharing" target="_blank" class="project-link">Live Demo →</a>
    </div>
  </div>

  <div class="project-card">
    <span class="project-label">SUPPLY CHAIN ANALYTICS</span>
    <h3><a href="https://github.com/correllid03/OM621Assignments" target="_blank">Global Transportation Cost Optimization</a></h3>
    <p>Analyzed 100K+ shipment records across three continents to identify $180M+ in potential savings. Built Power BI dashboards and predictive models for strategic routing decisions.</p>
    <div class="tech-tags">
      <span class="tech-tag">Python</span>
      <span class="tech-tag">SQL</span>
      <span class="tech-tag">Power BI</span>
      <span class="tech-tag">Pandas</span>
    </div>
    <div class="project-metrics">
      <div class="metric">
        <div class="metric-value">$1.1B</div>
        <div class="metric-label">Annual Spend</div>
      </div>
      <div class="metric">
        <div class="metric-value">40-50%</div>
        <div class="metric-label">Cost Variance</div>
      </div>
    </div>
    <div class="project-links">
      <a href="https://github.com/correllid03/OM621Assignments" target="_blank" class="project-link">View Repository →</a>
      <a href="/om621/" class="project-link">Full Analysis →</a>
    </div>
  </div>
</div>

## Technical Skills

<div class="skills-grid">
  <div class="skill-category">
    <h3>Programming & Data</h3>
    <ul class="skill-list">
      <li>Python (Pandas, NumPy, SciPy)</li>
      <li>SQL (Query Optimization, Database Design)</li>
      <li>R (Statistical Modeling)</li>
      <li>Git & Version Control</li>
    </ul>
  </div>

  <div class="skill-category">
    <h3>Analytics & Visualization</h3>
    <ul class="skill-list">
      <li>Power BI (DAX, Data Modeling)</li>
      <li>Tableau</li>
      <li>Statistical Analysis</li>
      <li>Monte Carlo Simulation</li>
    </ul>
  </div>

  <div class="skill-category">
    <h3>Supply Chain Domain</h3>
    <ul class="skill-list">
      <li>Logistics Operations Management</li>
      <li>Inventory Optimization</li>
      <li>Transportation Cost Analysis</li>
      <li>Demand Forecasting</li>
    </ul>
  </div>

  <div class="skill-category">
    <h3>AI & Development</h3>
    <ul class="skill-list">
      <li>LLM Integration (Gemini, Claude)</li>
      <li>Streamlit Applications</li>
      <li>AI-Assisted Development</li>
      <li>OCR & Document Processing</li>
    </ul>
  </div>
</div>

## Experience & Education

<div class="experience-timeline">
  <div class="experience-card">
    <div class="experience-header">
      <div>
        <div class="experience-title">MS in Supply Chain Analytics</div>
        <div class="experience-company">California State University San Marcos</div>
      </div>
      <div class="experience-period">Expected Aug 2026 • 3.5 GPA</div>
    </div>
    <p class="experience-description">
      Advanced coursework in operations research, statistical modeling, inventory management, 
      and transportation optimization. Developed production-grade analytical applications and 
      completed projects analyzing 100K+ records for cost optimization and forecasting.
    </p>
  </div>

  <div class="experience-card">
    <div class="experience-header">
      <div>
        <div class="experience-title">Shipping Operations</div>
        <div class="experience-company">Gear Hugger</div>
      </div>
      <div class="experience-period">Jun 2023 - Present</div>
    </div>
    <p class="experience-description">
      Manage multi-channel distribution operations and FBA inventory for eco-friendly product line. 
      Developed transportation cost analysis frameworks and data collection systems supporting 
      academic research in supply chain optimization.
    </p>
  </div>

  <div class="experience-card">
    <div class="experience-header">
      <div>
        <div class="experience-title">BA in History</div>
        <div class="experience-company">California State University San Marcos</div>
      </div>
      <div class="experience-period">Completed</div>
    </div>
    <p class="experience-description">
      Dean's List recognition for six out of eight semesters. Developed strong research, 
      analytical thinking, and written communication skills through capstone projects.
    </p>
  </div>
</div>

---

<div class="contact-section">
  <a href="https://github.com/correllid03" target="_blank" class="contact-btn">View GitHub Profile</a>
  <a href="https://www.linkedin.com/in/dominic-correlli-756847237/" target="_blank" class="contact-btn">View LinkedIn Profile</a>
</div>