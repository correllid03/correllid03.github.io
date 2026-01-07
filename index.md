---
layout: default
---
<style>
/* 1. BREAK THE CONTAINER LIMITS */
.wrapper {
    max-width: 100% !important; /* Force full width */
    width: 100% !important;
    margin: 0 !important;
    padding: 0 !important;
    display: flex; /* Use Flexbox to put sidebar and content side-by-side */
    min-height: 100vh;
}

/* 2. FIX THE SIDEBAR (LEFT) */
header {
    width: 350px !important; /* Fixed width for sidebar */
    min-width: 350px !important;
    background-color: #0d1117; /* Darker background to separate it */
    border-right: 1px solid #30363d; /* Subtle separator line */
    position: fixed; /* Lock it in place */
    height: 100vh; /* Full height */
    overflow-y: auto; /* Scroll if sidebar gets too tall */
    padding: 40px !important;
    z-index: 100;
}

/* 3. EXPAND THE CONTENT (RIGHT) */
section {
    margin-left: 350px !important; /* Push content to right of sidebar */
    width: calc(100% - 350px) !important; /* Take remaining space */
    max-width: 1400px !important; /* Stop lines from getting TOO long to read */
    padding: 60px 80px !important;
}

/* 4. MAKE IT MOBILE FRIENDLY */
@media screen and (max-width: 900px) {
    .wrapper {
        flex-direction: column;
    }
    header {
        position: relative;
        width: 100% !important;
        height: auto;
        border-right: none;
        border-bottom: 1px solid #30363d;
    }
    section {
        margin-left: 0 !important;
        width: 100% !important;
        padding: 30px !important;
    }
}

/* OPTIONAL: MAKE THE HERO SECTION POP */
.hero-section {
    background: linear-gradient(to right, #161b22, #0d1117);
    padding: 40px;
    border-radius: 8px;
    border: 1px solid #30363d;
    margin-bottom: 40px;
}
/* 1. Fix the Sidebar Name Redundancy */
/* We make the sidebar name smaller and less aggressive */
header h1, header h2 {
    font-size: 1.2rem !important; /* Shrink it */
    color: var(--text-muted) !important; /* Dim it */
    margin-bottom: 20px !important;
}

/* 2. Turn the Link into a Proper Button */
/* Targets the link inside the contact-section div */
.contact-section a {
    display: block; /* Make it a block so it fills width */
    background-color: var(--bg-panel);
    border: 1px solid var(--border);
    color: #fff !important;
    text-align: center;
    padding: 10px 0;
    margin-top: 10px;
    border-radius: 6px;
    text-decoration: none;
    font-weight: 600;
    transition: all 0.2s;
}

.contact-section a:hover {
    background-color: var(--accent); /* Turns blue on hover */
    border-color: var(--accent);
    color: #fff !important;
}

/* 3. Clean up the "Floating" text */
header p {
    font-size: 0.85rem;
    color: var(--text-muted);
    line-height: 1.5;
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
  <a href="https://github.com/correllid03" target="_blank" class="contact-link">GitHub</a>
  <a href="https://www.linkedin.com/in/dominic-correlli-756847237/" target="_blank" class="contact-link">LinkedIn</a>
</div>
