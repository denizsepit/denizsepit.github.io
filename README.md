[Mustafa_Deniz_Sepit_Portfolio (2).html](https://github.com/user-attachments/files/33431598/Mustafa_Deniz_Sepit_Portfolio.2.html)
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>M. Deniz Sepit — Electrical &amp; Electronics Engineering Portfolio</title>
  <style>
    :root {
      --navy: #0F2C59;
      --blue: #1E56A0;
      --accent: #00A8E8;
      --emerald: #0D9488;
      --bg: #F8FAFC;
      --card: #FFFFFF;
      --text: #0F172A;
      --muted: #475569;
      --border: #E2E8F0;
    }

    * { box-sizing: border-box; margin: 0; padding: 0; }
    body {
      font-family: -apple-system, BlinkMacSystemFont, 'Inter', 'Segoe UI', Roboto, sans-serif;
      background: var(--bg);
      color: var(--text);
      line-height: 1.6;
    }
    a { color: var(--blue); text-decoration: none; }
    a:hover { text-decoration: underline; }

    /* Top Navigation */
    nav {
      position: sticky;
      top: 0;
      z-index: 100;
      background: rgba(15, 44, 89, 0.96);
      backdrop-filter: blur(8px);
      color: #fff;
      padding: 14px 28px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      gap: 12px;
      border-bottom: 1px solid rgba(255,255,255,0.12);
    }
    .nav-brand {
      font-weight: 800;
      font-size: 1.1rem;
      letter-spacing: -0.3px;
      color: #fff;
    }
    .nav-brand span { color: var(--accent); font-weight: 600; font-size: 0.9rem; margin-left: 8px; }
    .nav-links { display: flex; gap: 20px; font-size: 0.92rem; }
    .nav-links a { color: #E2E8F0; font-weight: 500; text-decoration: none; transition: color 0.2s; }
    .nav-links a:hover { color: var(--accent); }

    /* Hero Section */
    .hero {
      background: linear-gradient(135deg, #0A1E3F 0%, #0F2C59 55%, #1E56A0 100%);
      color: #fff;
      padding: 56px 24px 48px;
    }
    .container {
      max-width: 1120px;
      margin: 0 auto;
    }
    .availability-pill {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: rgba(0, 168, 232, 0.18);
      border: 1px solid rgba(0, 168, 232, 0.45);
      color: #7DD3FC;
      padding: 6px 14px;
      border-radius: 999px;
      font-size: 0.85rem;
      font-weight: 600;
      margin-bottom: 16px;
    }
    .dot {
      width: 8px; height: 8px; border-radius: 50%;
      background: #34D399;
      box-shadow: 0 0 8px #34D399;
    }
    .hero h1 {
      font-size: 2.5rem;
      font-weight: 800;
      letter-spacing: -0.6px;
      margin-bottom: 8px;
    }
    .hero-sub {
      font-size: 1.15rem;
      color: #CBD5E1;
      max-width: 840px;
      margin-bottom: 24px;
    }
    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      margin-bottom: 36px;
    }
    .btn {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 10px 20px;
      border-radius: 8px;
      font-weight: 600;
      font-size: 0.95rem;
      cursor: pointer;
      transition: all 0.2s;
      text-decoration: none;
    }
    .btn-primary {
      background: var(--accent);
      color: #06162E;
    }
    .btn-primary:hover { background: #38BDF8; text-decoration: none; }
    .btn-outline {
      border: 1px solid rgba(255,255,255,0.3);
      color: #fff;
      background: rgba(255,255,255,0.06);
    }
    .btn-outline:hover { background: rgba(255,255,255,0.15); text-decoration: none; }

    /* KPI Strip */
    .kpi-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(210px, 1fr));
      gap: 16px;
    }
    .kpi-card {
      background: rgba(255, 255, 255, 0.08);
      border: 1px solid rgba(255, 255, 255, 0.14);
      border-radius: 10px;
      padding: 16px 18px;
    }
    .kpi-val {
      font-size: 1.55rem;
      font-weight: 800;
      color: #fff;
      line-height: 1.2;
    }
    .kpi-label {
      font-size: 0.84rem;
      color: #94A3B8;
      margin-top: 4px;
    }

    /* Section Styling */
    section {
      padding: 48px 24px;
    }
    .section-header {
      margin-bottom: 28px;
    }
    .section-tag {
      font-size: 0.78rem;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 1px;
      color: var(--blue);
      margin-bottom: 4px;
    }
    .section-title {
      font-size: 1.75rem;
      font-weight: 800;
      color: var(--navy);
      letter-spacing: -0.4px;
    }
    .section-desc {
      color: var(--muted);
      font-size: 0.98rem;
      margin-top: 4px;
    }

    /* Interactive Drive Simulator */
    .sim-wrapper {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 14px;
      padding: 24px;
      box-shadow: 0 4px 20px rgba(15, 44, 89, 0.05);
      display: grid;
      grid-template-columns: 320px 1fr;
      gap: 24px;
    }
    @media (max-width: 860px) {
      .sim-wrapper { grid-template-columns: 1fr; }
    }
    .sim-controls {
      background: #F1F5F9;
      border-radius: 10px;
      padding: 18px;
      display: flex;
      flex-direction: column;
      gap: 14px;
    }
    .control-group label {
      display: flex;
      justify-content: space-between;
      font-size: 0.86rem;
      font-weight: 600;
      color: var(--navy);
      margin-bottom: 4px;
    }
    .control-group input[type="range"] {
      width: 100%;
      accent-color: var(--blue);
    }
    .sim-metrics {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 10px;
      margin-top: 6px;
    }
    .sim-metric-box {
      background: #fff;
      border: 1px solid var(--border);
      border-radius: 8px;
      padding: 10px;
      text-align: center;
    }
    .sim-metric-box .val {
      font-size: 1.1rem;
      font-weight: 800;
      color: var(--navy);
    }
    .sim-metric-box .lbl {
      font-size: 0.74rem;
      color: var(--muted);
    }
    .canvas-box {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }
    canvas#driveCanvas {
      width: 100%;
      height: 310px;
      background: #0B192C;
      border-radius: 10px;
      border: 1px solid #1E293B;
    }
    .legend-bar {
      display: flex;
      flex-wrap: wrap;
      gap: 18px;
      margin-top: 10px;
      font-size: 0.84rem;
      color: var(--muted);
    }
    .legend-item { display: flex; align-items: center; gap: 6px; font-weight: 600; }
    .swatch { width: 12px; height: 12px; border-radius: 3px; }

    /* Filterable Projects Grid */
    .filter-bar {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-bottom: 24px;
    }
    .filter-btn {
      padding: 7px 15px;
      border-radius: 999px;
      border: 1px solid var(--border);
      background: #fff;
      color: var(--muted);
      font-size: 0.86rem;
      font-weight: 600;
      cursor: pointer;
      transition: all 0.15s;
    }
    .filter-btn.active, .filter-btn:hover {
      background: var(--navy);
      color: #fff;
      border-color: var(--navy);
    }
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(330px, 1fr));
      gap: 20px;
    }
    .project-card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 22px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      box-shadow: 0 2px 10px rgba(15, 44, 89, 0.04);
      transition: transform 0.2s, box-shadow 0.2s;
    }
    .project-card:hover {
      transform: translateY(-3px);
      box-shadow: 0 8px 24px rgba(15, 44, 89, 0.09);
    }
    .project-cat {
      font-size: 0.75rem;
      font-weight: 700;
      text-transform: uppercase;
      color: var(--blue);
      letter-spacing: 0.6px;
      margin-bottom: 6px;
    }
    .project-card h3 {
      font-size: 1.18rem;
      color: var(--navy);
      margin-bottom: 10px;
    }
    .project-card ul {
      padding-left: 18px;
      color: var(--muted);
      font-size: 0.92rem;
      margin-bottom: 16px;
    }
    .project-card li { margin-bottom: 6px; }
    .tag-row {
      display: flex;
      flex-wrap: wrap;
      gap: 6px;
      margin-top: auto;
    }
    .tech-tag {
      background: #EFF6FF;
      color: #1D4ED8;
      border: 1px solid #BFDBFE;
      font-size: 0.76rem;
      font-weight: 600;
      padding: 3px 10px;
      border-radius: 6px;
    }

    /* Education & Technical Skills Sections */
    .two-col {
      display: grid;
      grid-template-columns: 1.25fr 1fr;
      gap: 24px;
    }
    @media (max-width: 860px) {
      .two-col { grid-template-columns: 1fr; }
    }
    .panel {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 22px;
    }
    .panel h3 {
      font-size: 1.15rem;
      color: var(--navy);
      margin-bottom: 14px;
    }
    table.course-table {
      width: 100%;
      border-collapse: collapse;
      font-size: 0.86rem;
    }
    table.course-table th, table.course-table td {
      padding: 8px 10px;
      text-align: left;
      border-bottom: 1px solid var(--border);
    }
    table.course-table th {
      color: var(--navy);
      font-weight: 700;
      background: #F8FAFC;
    }
    .grade-badge {
      display: inline-block;
      padding: 2px 8px;
      border-radius: 6px;
      font-weight: 700;
      font-size: 0.76rem;
    }
    .grade-aa { background: #DCFCE7; color: #15803D; }
    .grade-ba { background: #E0F2FE; color: #0369A1; }
    .grade-bb { background: #F1F5F9; color: #334155; }
    .grade-ip { background: #FEF3C7; color: #B45309; }

    .skill-group { margin-bottom: 16px; }
    .skill-group h4 {
      font-size: 0.92rem;
      color: var(--navy);
      margin-bottom: 6px;
    }
    .skill-group p {
      font-size: 0.88rem;
      color: var(--muted);
    }

    footer {
      background: var(--navy);
      color: #CBD5E1;
      text-align: center;
      padding: 32px 24px;
      font-size: 0.9rem;
    }
    footer a { color: #7DD3FC; }
  </style>
</head>
<body>

  <nav>
    <div class="nav-brand">M. Deniz Sepit <span>| Electrical &amp; Electronics Engineering</span></div>
    <div class="nav-links">
      <a href="#simulator">Drive Simulator</a>
      <a href="#projects">Engineering Projects</a>
      <a href="#education">Education</a>
      <a href="#skills">Technical Skills</a>
      <a href="#contact">Contact</a>
    </div>
  </nav>

  <header class="hero">
    <div class="container">
      <div class="availability-pill">
        <span class="dot"></span>
        Mandatory Internship (Pflichtpraktikum): June 15 – September 15, 2027 (3 Months) • Available On-Site in Esslingen am Neckar
      </div>
      <h1>M. Deniz Sepit</h1>
      <p class="hero-sub">
        Third-year Electrical and Electronics Engineering student at Izmir University of Economics with a strong foundation in electric machines, electromagnetic circuit modeling, and power/analog electronics. Experienced in analyzing permanent magnet synchronous motors (PMSM) and induction machines, calculating stator/rotor equivalent circuits and magnetic flux distribution, and simulating closed-loop drive kinematics in MATLAB alongside PSpice and KiCad hardware design.
      </p>
      <div class="hero-actions">
        <a class="btn btn-primary" href="mailto:deniz.sepit@std.izmirekonomi.edu.tr">✉ deniz.sepit@std.izmirekonomi.edu.tr</a>
        <a class="btn btn-outline" href="#simulator">⚡ Try Live S-Curve Drive Simulator</a>
        <a class="btn btn-outline" href="#projects">🔧 View Engineering Projects</a>
      </div>

      <div class="kpi-grid">
        <div class="kpi-card">
          <div class="kpi-val">PMSM &amp; Induction</div>
          <div class="kpi-label">Stator/Rotor Equivalent Circuits &amp; Flux Modeling</div>
        </div>
        <div class="kpi-card">
          <div class="kpi-val">MATLAB • PSpice • KiCad</div>
          <div class="kpi-label">Drive Kinematics, Analog Simulation &amp; PCB Layout</div>
        </div>
        <div class="kpi-card">
          <div class="kpi-val">~75% / -40%</div>
          <div class="kpi-label">Amp Voltage Efficiency / Closed-Loop Water Saved</div>
        </div>
        <div class="kpi-card">
          <div class="kpi-val">EN (C1) • DE (A2+)</div>
          <div class="kpi-label">4 Semesters Univ. German + 1-on-1 Tutoring</div>
        </div>
      </div>
    </div>
  </header>

  <!-- Interactive Elevator Electric Drive Kinematics & Transient Simulator -->
  <section id="simulator">
    <div class="container">
      <div class="section-header">
        <div class="section-tag">Interactive Engineering Demonstration</div>
        <h2 class="section-title">Traction Elevator PMSM Drive S-Curve Kinematics &amp; Torque Simulator</h2>
        <p class="section-desc">
          Interactive browser port of my MATLAB Electromechanical Drive Simulation project. Adjust the S-curve jerk-limited speed profile and closed-loop damping parameters below to inspect transient motor velocity tracking and electromagnetic torque response.
        </p>
      </div>

      <div class="sim-wrapper">
        <div class="sim-controls">
          <div class="control-group">
            <label><span>Target Rated Speed (v<sub>max</sub>)</span> <span id="valSpeed">2.5 m/s</span></label>
            <input type="range" id="sliderSpeed" min="1.0" max="4.0" step="0.1" value="2.5" />
          </div>
          <div class="control-group">
            <label><span>S-Curve Max Accel (a<sub>max</sub>)</span> <span id="valAccel">1.1 m/s²</span></label>
            <input type="range" id="sliderAccel" min="0.5" max="1.8" step="0.1" value="1.1" />
          </div>
          <div class="control-group">
            <label><span>Closed-Loop Damping (ζ)</span> <span id="valZeta">0.75</span></label>
            <input type="range" id="sliderZeta" min="0.30" max="1.20" step="0.05" value="0.75" />
          </div>
          <div class="control-group">
            <label><span>Control Bandwidth (ω<sub>n</sub>)</span> <span id="valWn">6.0 rad/s</span></label>
            <input type="range" id="sliderWn" min="3.0" max="12.0" step="0.5" value="6.0" />
          </div>

          <div class="sim-metrics">
            <div class="sim-metric-box">
              <div class="val" id="metricOvershoot">2.8%</div>
              <div class="lbl">Speed Overshoot</div>
            </div>
            <div class="sim-metric-box">
              <div class="val" id="metricSettling">0.89 s</div>
              <div class="lbl">2% Settling Margin</div>
            </div>
            <div class="sim-metric-box">
              <div class="val" id="metricPeakTorque">1.18 pu</div>
              <div class="lbl">Peak Electromagnetic Torque</div>
            </div>
            <div class="sim-metric-box">
              <div class="val" id="metricRideQuality">ISO Class I</div>
              <div class="lbl">Jerk &amp; Ride Comfort</div>
            </div>
          </div>
        </div>

        <div class="canvas-box">
          <canvas id="driveCanvas" width="720" height="310"></canvas>
          <div class="legend-bar">
            <div class="legend-item"><span class="swatch" style="background:#38BDF8;"></span> S-Curve Reference Velocity v<sub>ref</sub>(t)</div>
            <div class="legend-item"><span class="swatch" style="background:#34D399;"></span> Closed-Loop Motor Velocity v<sub>m</sub>(t) (RK4 ODE Solver)</div>
            <div class="legend-item"><span class="swatch" style="background:#F59E0B;"></span> Electromagnetic Torque / Acceleration Profile</div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Engineering Projects Section -->
  <section id="projects" style="background: #F1F5F9;">
    <div class="container">
      <div class="section-header">
        <div class="section-tag">Academic &amp; Independent Engineering Work</div>
        <h2 class="section-title">Selected Engineering Projects</h2>
        <p class="section-desc">Filter across electric drive &amp; machine simulation, PSpice/KiCad PCB design, ArduKit closed-loop control, and computer vision.</p>
      </div>

      <div class="filter-bar">
        <button class="filter-btn active" onclick="filterProjects('all', this)">All Projects (5)</button>
        <button class="filter-btn" onclick="filterProjects('drives', this)">Electric Drives &amp; Machines</button>
        <button class="filter-btn" onclick="filterProjects('hardware', this)">PSpice &amp; KiCad PCB Design</button>
        <button class="filter-btn" onclick="filterProjects('embedded', this)">ArduKit &amp; Embedded Control</button>
        <button class="filter-btn" onclick="filterProjects('vision', this)">Computer Vision &amp; Numerical Math</button>
      </div>

      <div class="projects-grid" id="projectsGrid">
        <!-- Project 1 -->
        <article class="project-card" data-category="drives">
          <div>
            <div class="project-cat">Electric Machines &amp; Drive Simulation • MATLAB</div>
            <h3>Electromechanical Drive System Simulation</h3>
            <ul>
              <li>Modeled electromagnetic torque generation, stator/rotor equivalent circuit dynamics, and transient speed regulation of electric drive motors (PMSM and DC/induction topologies) in MATLAB using numerical differential equation solvers.</li>
              <li>Implemented S-curve jerk-limited kinematic velocity profiles and closed-loop damping optimization to suppress torque ripple and achieve smooth acceleration/deceleration transitions for traction elevator drives.</li>
            </ul>
          </div>
          <div class="tag-row">
            <span class="tech-tag">MATLAB</span>
            <span class="tech-tag">PMSM &amp; Induction Drives</span>
            <span class="tech-tag">S-Curve Jerk Limitation</span>
            <span class="tech-tag">Torque &amp; Flux Modeling</span>
          </div>
        </article>

        <!-- Project 2 -->
        <article class="project-card" data-category="hardware">
          <div>
            <div class="project-cat">Analog Electronics &amp; EDA • PSpice &amp; KiCad</div>
            <h3>Multi-Stage Audio Amplifier &amp; Low-Noise PCB Layout</h3>
            <ul>
              <li>Simulated and analyzed a multi-stage analog amplifier in <strong>PSpice</strong> combining differential input, voltage amplification, and emitter-follower buffer stages, reducing effective output impedance to reach <strong>~75% voltage transfer efficiency</strong>.</li>
              <li>Designed the board layout in <strong>KiCad</strong> structured by functional blocks with a unified ground plane, isolating high-current output stages from short signal traces to optimize power distribution and suppress electromagnetic interference (EMI).</li>
            </ul>
          </div>
          <div class="tag-row">
            <span class="tech-tag">PSpice Simulation</span>
            <span class="tech-tag">KiCad PCB Layout</span>
            <span class="tech-tag">EMI &amp; Ground Plane Design</span>
            <span class="tech-tag">Multi-Stage Amplifiers</span>
          </div>
        </article>

        <!-- Project 3 -->
        <article class="project-card" data-category="embedded drives">
          <div>
            <div class="project-cat">Independent Embedded Project • Closed-Loop Control</div>
            <h3>Smart Irrigation Control System Prototype (ArduKit)</h3>
            <ul>
              <li>Designed and built an automated, sensor-driven irrigation prototype on an <strong>ArduKit</strong> microcontroller platform integrating soil moisture and temperature sensors for real-time closed-loop feedback control.</li>
              <li>Developed MATLAB data-logging scripts to analyze telemetry logs, predict optimal actuation schedules, and demonstrate a <strong>40% reduction in simulated water consumption</strong> compared to fixed-interval schedules.</li>
            </ul>
          </div>
          <div class="tag-row">
            <span class="tech-tag">ArduKit Microcontroller</span>
            <span class="tech-tag">Closed-Loop Feedback</span>
            <span class="tech-tag">Sensor Telemetry</span>
            <span class="tech-tag">MATLAB Analytics</span>
          </div>
        </article>

        <!-- Project 4 -->
        <article class="project-card" data-category="hardware vision">
          <div>
            <div class="project-cat">Multidisciplinary Team Project • Hardware Lead</div>
            <h3>VisionSense: Smart Library Occupancy Tracker</h3>
            <ul>
              <li>Collaborated in a 4-person Electrical and Software Engineering team to design a real-time computer vision system monitoring <strong>280 library seats</strong> with <strong>&lt;2 s latency</strong> and <strong>&gt;95% human-vs-object detection accuracy</strong>.</li>
              <li>Led hardware optimization and AI server specification, utilizing existing PoE IP camera infrastructure and 24/48-port PoE network switches to eliminate per-desk sensor hardware costs.</li>
            </ul>
          </div>
          <div class="tag-row">
            <span class="tech-tag">PoE Network Architecture</span>
            <span class="tech-tag">AI Server Hardware Spec</span>
            <span class="tech-tag">Computer Vision</span>
            <span class="tech-tag">Team Engineering</span>
          </div>
        </article>

        <!-- Project 5 -->
        <article class="project-card" data-category="vision drives">
          <div>
            <div class="project-cat">Computational Engineering • Numerical Analysis</div>
            <h3>3D Structure from Motion &amp; Spatial Reconstruction</h3>
            <ul>
              <li>Engineered a MATLAB pipeline to reconstruct 3D spatial models from 2D image sequences using Gram-Schmidt orthogonalization and eigenvalue decomposition.</li>
              <li>Implemented Bicubic and Lanczos interpolation algorithms alongside Newton-Raphson, Bisection, and Secant root-finding methods to evaluate resolution and quantify numerical error margins.</li>
            </ul>
          </div>
          <div class="tag-row">
            <span class="tech-tag">MATLAB</span>
            <span class="tech-tag">Eigenvalue &amp; Gram-Schmidt</span>
            <span class="tech-tag">Bicubic / Lanczos Interpolation</span>
            <span class="tech-tag">Numerical Root-Finding</span>
          </div>
        </article>
      </div>
    </div>
  </section>

  <!-- Separate Education & Technical Skills Sections -->
  <section id="education">
    <div class="container">
      <div class="section-header">
        <div class="section-tag">Verified Academic Record (YÖK Transcript • 114 ECTS Completed)</div>
        <h2 class="section-title">Education &amp; Technical Skills</h2>
        <p class="section-desc">
          B.Sc. in Electrical and Electronics Engineering at Izmir University of Economics (100% English Instruction • Aug 2024 – June 2028).
        </p>
      </div>

      <div class="two-col">
        <div class="panel">
          <h3>Education — Izmir University of Economics</h3>
          <p style="font-size:0.88rem; color:var(--muted); margin-bottom:12px;">
            <strong>CGPA:</strong> 3.10 / 4.00 (79 / 100) &nbsp;|&nbsp; <strong>Spring 2026 GPA:</strong> 3.49 / 4.00 (88 / 100, 36 ECTS) &nbsp;|&nbsp; <strong>114 ECTS Completed</strong> (English Prep: Exempt)
          </p>
          <table class="course-table">
            <thead>
              <tr>
                <th>Course Title &amp; Technical Focus</th>
                <th>ECTS</th>
                <th>Status / Grade</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td><strong>Electrical Energy Conversion</strong> (PMSM &amp; Induction Machines, Magnetic Flux Distribution, Stator/Rotor Equivalent Circuits, Core Loss Calculation)</td>
                <td>6</td>
                <td><span class="grade-badge grade-ip">Fall 2026</span></td>
              </tr>
              <tr>
                <td><strong>Signals and Systems</strong></td>
                <td>6</td>
                <td><span class="grade-badge grade-ip">Fall 2026</span></td>
              </tr>
              <tr>
                <td><strong>Fundamentals of Microprocessors</strong></td>
                <td>6</td>
                <td><span class="grade-badge grade-ip">Fall 2026</span></td>
              </tr>
              <tr>
                <td><strong>Digital Design</strong></td>
                <td>5</td>
                <td><span class="grade-badge grade-aa">Grade: AA (4.0)</span></td>
              </tr>
              <tr>
                <td><strong>Electric Circuit Analysis I &amp; II</strong> (Transient, AC Power &amp; Op-Amp Circuits)</td>
                <td>13</td>
                <td><span class="grade-badge grade-ba">Grade: BA (3.5)</span></td>
              </tr>
              <tr>
                <td><strong>Engineering Mathematics I &amp; II</strong> (Differential Equations &amp; Linear Algebra)</td>
                <td>11</td>
                <td><span class="grade-badge grade-ba">Grade: BB / BA</span></td>
              </tr>
              <tr>
                <td><strong>General Physics I &amp; II</strong> (Mechanics &amp; Electromagnetism)</td>
                <td>12</td>
                <td><span class="grade-badge grade-aa">Grade: AA / BA</span></td>
              </tr>
              <tr>
                <td><strong>Calculus II</strong></td>
                <td>6</td>
                <td><span class="grade-badge grade-ba">Grade: BA (3.5)</span></td>
              </tr>
              <tr>
                <td><strong>Microelectronic Devices and Circuits</strong></td>
                <td>6</td>
                <td><span class="grade-badge grade-bb">Grade: BB (3.0)</span></td>
              </tr>
              <tr>
                <td><strong>Introduction to Programming &amp; Computational Methods for Engineers</strong></td>
                <td>13</td>
                <td><span class="grade-badge grade-bb">Grade: BB / CB</span></td>
              </tr>
              <tr>
                <td><strong>German Language I, II, III &amp; IV</strong> (4 University Semesters)</td>
                <td>15</td>
                <td><span class="grade-badge grade-aa">Grade: AA / BB</span></td>
              </tr>
            </tbody>
          </table>
        </div>

        <div class="panel" id="skills">
          <h3>Technical Skills &amp; Competencies</h3>
          <div class="skill-group">
            <h4>Electric Machines, Drive Modeling &amp; EDA Software</h4>
            <p><strong>Electric Machines &amp; Electromagnetic Circuits:</strong> Permanent magnet synchronous motors (PMSM), induction machines, stator/rotor equivalent circuit modeling, magnetic flux distribution, and core loss calculation.<br/>
               <strong>MATLAB:</strong> Electromechanical drive dynamics, S-curve kinematics, numerical ODE solvers, root-finding (Newton-Raphson, Bisection, Secant), IEEE İEÜ <em>Generative AI with MATLAB</em> Workshop (May 2026).<br/>
               <strong>PSpice &amp; KiCad:</strong> Multi-stage analog amplifier transient simulation, schematic capture, functional-block PCB layout, unified ground planes, and high-current vs. signal trace isolation.<br/>
               <strong>SolidWorks &amp; Assembly:</strong> 3D CAD machine element and assembly modeling; 8086 Assembly (EMU8086).</p>
          </div>
          <div class="skill-group">
            <h4>Hardware Debugging &amp; Embedded Prototyping</h4>
            <p><strong>ArduKit Embedded Control:</strong> Closed-loop sensor integration (soil moisture, temperature) and real-time telemetry logging.<br/>
               <strong>Lab Hardware Debugging:</strong> Component-level fault diagnosis, precision through-hole/SMD soldering, cracked trace repair, and capacitor replacement on audio receiver boards.</p>
          </div>
          <div class="skill-group">
            <h4>Languages</h4>
            <p><strong>English:</strong> Fluent / C1 (Exempt from prep class; 100% English B.Sc. instruction; Grade: AA in Technical English for Engineers).<br/>
               <strong>German:</strong> CEFR A2 (15 ECTS across 4 semesters of university German Language I–IV; actively advancing toward B1 via 1-on-1 study with a German teacher).<br/>
               <strong>Turkish:</strong> Native.</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <footer id="contact">
    <div class="container">
      <p style="font-size:1.08rem; font-weight:700; color:#fff; margin-bottom:6px;">M. Deniz Sepit — Electrical &amp; Electronics Engineering Portfolio</p>
      <p>İzmir, Türkiye (Available on-site in Esslingen am Neckar, Germany) &nbsp;|&nbsp; <a href="mailto:deniz.sepit@std.izmirekonomi.edu.tr">deniz.sepit@std.izmirekonomi.edu.tr</a></p>
    </div>
  </footer>

  <script>
    function filterProjects(cat, btn) {
      document.querySelectorAll('.filter-btn').forEach(b => b.classList.remove('active'));
      btn.classList.add('active');
      document.querySelectorAll('.project-card').forEach(card => {
        const cats = card.getAttribute('data-category');
        if (cat === 'all' || cats.includes(cat)) {
          card.style.display = 'flex';
        } else {
          card.style.display = 'none';
        }
      });
    }

    const canvas = document.getElementById('driveCanvas');
    const ctx = canvas.getContext('2d');
    const sSpeed = document.getElementById('sliderSpeed');
    const sAccel = document.getElementById('sliderAccel');
    const sZeta = document.getElementById('sliderZeta');
    const sWn = document.getElementById('sliderWn');

    function runSimulation() {
      const vmax = parseFloat(sSpeed.value);
      const amax = parseFloat(sAccel.value);
      const zeta = parseFloat(sZeta.value);
      const wn = parseFloat(sWn.value);

      document.getElementById('valSpeed').textContent = vmax.toFixed(1) + ' m/s';
      document.getElementById('valAccel').textContent = amax.toFixed(1) + ' m/s²';
      document.getElementById('valZeta').textContent = zeta.toFixed(2);
      document.getElementById('valWn').textContent = wn.toFixed(1) + ' rad/s';

      const T = 8.0;
      const dt = 0.02;
      const steps = Math.floor(T / dt);

      const tArr = [];
      const vRefArr = [];
      const vMotorArr = [];
      const aProfileArr = [];

      const tRamp = vmax / amax;
      const tCruiseEnd = Math.max(tRamp + 1.5, 5.2);

      let y = 0;
      let dy = 0;
      let maxV = 0;

      for (let i = 0; i <= steps; i++) {
        const t = i * dt;
        tArr.push(t);

        let vref = 0;
        let aref = 0;
        if (t < tRamp) {
          const phase = (Math.PI * t) / tRamp;
          vref = vmax * 0.5 * (1 - Math.cos(phase));
          aref = (vmax * 0.5 * Math.PI / tRamp) * Math.sin(phase);
        } else if (t < tCruiseEnd) {
          vref = vmax;
          aref = 0;
        } else if (t < tCruiseEnd + tRamp) {
          const td = t - tCruiseEnd;
          const phase = (Math.PI * td) / tRamp;
          vref = vmax * 0.5 * (1 + Math.cos(phase));
          aref = -(vmax * 0.5 * Math.PI / tRamp) * Math.sin(phase);
        } else {
          vref = 0;
          aref = 0;
        }

        vRefArr.push(vref);
        aProfileArr.push(aref);

        const f = (vel, acc, u) => wn * wn * (u - vel) - 2 * zeta * wn * acc;

        const k1_y = dy;
        const k1_dy = f(y, dy, vref);

        const k2_y = dy + 0.5 * dt * k1_dy;
        const k2_dy = f(y + 0.5 * dt * k1_y, dy + 0.5 * dt * k1_dy, vref);

        const k3_y = dy + 0.5 * dt * k2_dy;
        const k3_dy = f(y + 0.5 * dt * k2_y, dy + 0.5 * dt * k2_dy, vref);

        const k4_y = dy + dt * k3_dy;
        const k4_dy = f(y + dt * k3_y, dy + dt * k3_dy, vref);

        y += (dt / 6) * (k1_y + 2 * k2_y + 2 * k3_y + k4_y);
        dy += (dt / 6) * (k1_dy + 2 * k2_dy + 2 * k3_dy + k4_dy);

        vMotorArr.push(y);
        if (y > maxV) maxV = y;
      }

      const overshoot = Math.max(0, ((maxV - vmax) / vmax) * 100);
      const settling = (4.0 / (zeta * wn)).toFixed(2);
      const peakTorque = (1.0 + (amax / 1.5) * 0.35 + (overshoot / 100)).toFixed(2);

      document.getElementById('metricOvershoot').textContent = overshoot.toFixed(1) + '%';
      document.getElementById('metricSettling').textContent = settling + ' s';
      document.getElementById('metricPeakTorque').textContent = peakTorque + ' pu';

      const comfortEl = document.getElementById('metricRideQuality');
      if (zeta >= 0.65 && zeta <= 0.95 && amax <= 1.3) {
        comfortEl.textContent = 'ISO Class I';
        comfortEl.style.color = '#0D9488';
      } else if (zeta < 0.5) {
        comfortEl.textContent = 'Underdamped';
        comfortEl.style.color = '#D97706';
      } else {
        comfortEl.textContent = 'Standard';
        comfortEl.style.color = '#1E56A0';
      }

      const W = canvas.width;
      const H = canvas.height;
      ctx.clearRect(0, 0, W, H);

      const padL = 48, padR = 20, padT = 24, padB = 34;
      const plotW = W - padL - padR;
      const plotH = H - padT - padB;

      ctx.strokeStyle = 'rgba(148, 163, 184, 0.16)';
      ctx.lineWidth = 1;
      ctx.font = '11px sans-serif';
      ctx.fillStyle = '#94A3B8';

      const yMaxScale = 4.6;
      const yMinScale = -2.2;
      const mapX = (t) => padL + (t / T) * plotW;
      const mapY = (val) => padT + ((yMaxScale - val) / (yMaxScale - yMinScale)) * plotH;

      for (let v = -2; v <= 4; v += 1) {
        const py = mapY(v);
        ctx.beginPath();
        ctx.moveTo(padL, py);
        ctx.lineTo(W - padR, py);
        ctx.stroke();
        ctx.fillText(v.toFixed(0), 18, py + 4);
      }

      for (let t = 0; t <= 8; t += 1) {
        const px = mapX(t);
        ctx.beginPath();
        ctx.moveTo(px, padT);
        ctx.lineTo(px, H - padB);
        ctx.stroke();
        ctx.fillText(t + 's', px - 6, H - 12);
      }

      ctx.strokeStyle = 'rgba(255,255,255,0.28)';
      ctx.beginPath();
      ctx.moveTo(padL, mapY(0));
      ctx.lineTo(W - padR, mapY(0));
      ctx.stroke();

      ctx.strokeStyle = '#F59E0B';
      ctx.lineWidth = 1.8;
      ctx.beginPath();
      for (let i = 0; i < tArr.length; i++) {
        const px = mapX(tArr[i]);
        const py = mapY(aProfileArr[i]);
        if (i === 0) ctx.moveTo(px, py);
        else ctx.lineTo(px, py);
      }
      ctx.stroke();

      ctx.strokeStyle = '#38BDF8';
      ctx.lineWidth = 2;
      ctx.setLineDash([5, 4]);
      ctx.beginPath();
      for (let i = 0; i < tArr.length; i++) {
        const px = mapX(tArr[i]);
        const py = mapY(vRefArr[i]);
        if (i === 0) ctx.moveTo(px, py);
        else ctx.lineTo(px, py);
      }
      ctx.stroke();
      ctx.setLineDash([]);

      ctx.strokeStyle = '#34D399';
      ctx.lineWidth = 2.6;
      ctx.beginPath();
      for (let i = 0; i < tArr.length; i++) {
        const px = mapX(tArr[i]);
        const py = mapY(vMotorArr[i]);
        if (i === 0) ctx.moveTo(px, py);
        else ctx.lineTo(px, py);
      }
      ctx.stroke();
    }

    [sSpeed, sAccel, sZeta, sWn].forEach(el => el.addEventListener('input', runSimulation));
    runSimulation();
  </script>
</body>
</html>
