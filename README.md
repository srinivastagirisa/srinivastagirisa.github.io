[index.html](https://github.com/user-attachments/files/29181013/index.html)
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Srinivas Bhargav Tagirisa | Senior IT Engineer</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&family=Space+Grotesk:wght@400;500;600;700&display=swap" rel="stylesheet" />
  <style>
    :root {
      --bg: #09090b;
      --bg-card: #111113;
      --bg-card2: #18181b;
      --border: #27272a;
      --accent: #0ea5e9;
      --accent2: #8b5cf6;
      --accent3: #10b981;
      --text: #fafafa;
      --text-muted: #71717a;
      --text-secondary: #a1a1aa;
      --aa-red: #cc0000;
      --aa-blue: #00338d;
    }

    * { box-sizing: border-box; margin: 0; padding: 0; }

    html { scroll-behavior: smooth; }

    body {
      font-family: 'Inter', sans-serif;
      background: var(--bg);
      color: var(--text);
      line-height: 1.6;
      overflow-x: hidden;
    }

    /* ─── NAV ─────────────────────────────────────── */
    nav {
      position: fixed; top: 0; left: 0; right: 0; z-index: 100;
      display: flex; align-items: center; justify-content: space-between;
      padding: 1rem 2rem;
      background: rgba(9,9,11,0.85);
      backdrop-filter: blur(12px);
      border-bottom: 1px solid var(--border);
    }

    .nav-logo {
      font-family: 'Space Grotesk', sans-serif;
      font-weight: 700; font-size: 1.1rem;
      background: linear-gradient(135deg, var(--accent), var(--accent2));
      -webkit-background-clip: text; -webkit-text-fill-color: transparent;
    }

    .nav-links { display: flex; gap: 2rem; }
    .nav-links a {
      color: var(--text-secondary); text-decoration: none;
      font-size: 0.9rem; font-weight: 500;
      transition: color .2s;
    }
    .nav-links a:hover { color: var(--text); }

    /* ─── HERO ────────────────────────────────────── */
    .hero {
      min-height: 100vh;
      display: flex; align-items: center; justify-content: center;
      position: relative; overflow: hidden;
      padding: 6rem 2rem 4rem;
    }

    .hero-grid {
      position: absolute; inset: 0;
      background-image:
        linear-gradient(rgba(14,165,233,.06) 1px, transparent 1px),
        linear-gradient(90deg, rgba(14,165,233,.06) 1px, transparent 1px);
      background-size: 60px 60px;
    }

    .hero-glow {
      position: absolute; top: 20%; left: 50%;
      transform: translateX(-50%);
      width: 600px; height: 400px;
      background: radial-gradient(ellipse, rgba(14,165,233,.12) 0%, transparent 70%);
      pointer-events: none;
    }

    .hero-content {
      position: relative; z-index: 1;
      text-align: center; max-width: 900px;
    }

    .hero-badge {
      display: inline-flex; align-items: center; gap: .5rem;
      border: 1px solid var(--border);
      background: var(--bg-card); border-radius: 999px;
      padding: .4rem 1rem; font-size: .8rem;
      color: var(--text-secondary); margin-bottom: 2rem;
    }
    .hero-badge span { color: var(--accent); }

    .hero-title {
      font-family: 'Space Grotesk', sans-serif;
      font-size: clamp(2.5rem, 6vw, 5rem);
      font-weight: 700; line-height: 1.1;
      margin-bottom: 1.5rem;
    }

    .hero-title .name {
      background: linear-gradient(135deg, #fff 30%, var(--accent));
      -webkit-background-clip: text; -webkit-text-fill-color: transparent;
    }
    .hero-title .role {
      display: block; font-size: clamp(1.2rem, 3vw, 2rem);
      font-weight: 500; color: var(--text-secondary); margin-top: .5rem;
    }

    .hero-desc {
      font-size: 1.1rem; color: var(--text-secondary);
      max-width: 640px; margin: 0 auto 2.5rem;
    }

    .hero-stats {
      display: flex; justify-content: center; gap: 3rem; margin-bottom: 2.5rem;
      flex-wrap: wrap;
    }

    .stat { text-align: center; }
    .stat-num {
      font-family: 'Space Grotesk', sans-serif;
      font-size: 2.5rem; font-weight: 700;
      background: linear-gradient(135deg, var(--accent), var(--accent2));
      -webkit-background-clip: text; -webkit-text-fill-color: transparent;
    }
    .stat-label { font-size: .8rem; color: var(--text-muted); text-transform: uppercase; letter-spacing: .08em; }

    .hero-cta { display: flex; justify-content: center; gap: 1rem; flex-wrap: wrap; }

    .btn {
      display: inline-flex; align-items: center; gap: .5rem;
      padding: .75rem 1.75rem; border-radius: 8px;
      font-size: .9rem; font-weight: 600; text-decoration: none;
      transition: all .2s; cursor: pointer; border: none;
    }
    .btn-primary {
      background: linear-gradient(135deg, var(--accent), #0284c7);
      color: #fff;
    }
    .btn-primary:hover { opacity: .9; transform: translateY(-1px); }
    .btn-outline {
      background: transparent; color: var(--text);
      border: 1px solid var(--border);
    }
    .btn-outline:hover { border-color: var(--accent); color: var(--accent); }

    /* ─── SECTIONS ───────────────────────────────── */
    section { padding: 5rem 2rem; max-width: 1100px; margin: 0 auto; }

    .section-label {
      font-size: .75rem; font-weight: 600; letter-spacing: .15em;
      text-transform: uppercase; color: var(--accent);
      margin-bottom: .75rem;
    }
    .section-title {
      font-family: 'Space Grotesk', sans-serif;
      font-size: clamp(1.8rem, 3.5vw, 2.8rem); font-weight: 700;
      margin-bottom: 1rem;
    }
    .section-subtitle { color: var(--text-secondary); max-width: 600px; margin-bottom: 3rem; }

    /* ─── ABOUT ──────────────────────────────────── */
    .about-grid {
      display: grid; grid-template-columns: 1fr 1fr; gap: 3rem;
      align-items: start;
    }

    @media (max-width: 768px) { .about-grid { grid-template-columns: 1fr; } }

    .about-text p { color: var(--text-secondary); margin-bottom: 1rem; line-height: 1.8; }

    .about-highlights { display: flex; flex-direction: column; gap: 1rem; }

    .highlight-card {
      background: var(--bg-card); border: 1px solid var(--border);
      border-radius: 12px; padding: 1.25rem;
      display: flex; align-items: flex-start; gap: 1rem;
      transition: border-color .2s;
    }
    .highlight-card:hover { border-color: var(--accent); }

    .highlight-icon {
      width: 40px; height: 40px; border-radius: 8px;
      display: flex; align-items: center; justify-content: center;
      font-size: 1.2rem; flex-shrink: 0;
    }
    .icon-blue { background: rgba(14,165,233,.15); }
    .icon-purple { background: rgba(139,92,246,.15); }
    .icon-green { background: rgba(16,185,129,.15); }

    .highlight-body h4 { font-size: .95rem; font-weight: 600; margin-bottom: .25rem; }
    .highlight-body p { font-size: .85rem; color: var(--text-secondary); }

    /* ─── AA ACHIEVEMENTS ─────────────────────────── */
    .aa-header {
      display: flex; align-items: center; gap: 1.5rem; margin-bottom: 3rem;
    }
    .aa-logo-wrapper {
      background: #fff; border-radius: 12px; padding: .75rem 1.25rem;
      display: flex; align-items: center;
    }
    .aa-logo-text {
      font-family: 'Space Grotesk', sans-serif;
      font-weight: 800; font-size: 1.5rem;
      color: var(--aa-red);
    }

    .achievement-grid {
      display: grid; grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
      gap: 1.5rem;
    }

    .achievement-card {
      background: var(--bg-card); border: 1px solid var(--border);
      border-radius: 16px; padding: 1.75rem;
      position: relative; overflow: hidden;
      transition: all .25s;
    }
    .achievement-card::before {
      content: ''; position: absolute; top: 0; left: 0; right: 0;
      height: 3px;
      background: linear-gradient(90deg, var(--accent), var(--accent2));
      opacity: 0; transition: opacity .25s;
    }
    .achievement-card:hover { border-color: rgba(14,165,233,.4); transform: translateY(-2px); }
    .achievement-card:hover::before { opacity: 1; }

    .achievement-tag {
      display: inline-block; font-size: .7rem; font-weight: 600;
      letter-spacing: .08em; text-transform: uppercase;
      padding: .2rem .6rem; border-radius: 4px; margin-bottom: 1rem;
    }
    .tag-infra { background: rgba(14,165,233,.15); color: var(--accent); }
    .tag-security { background: rgba(139,92,246,.15); color: var(--accent2); }
    .tag-automation { background: rgba(16,185,129,.15); color: var(--accent3); }
    .tag-migration { background: rgba(245,158,11,.15); color: #f59e0b; }
    .tag-ops { background: rgba(239,68,68,.15); color: #ef4444; }

    .achievement-card h3 { font-size: 1.05rem; font-weight: 600; margin-bottom: .5rem; }
    .achievement-card p { font-size: .875rem; color: var(--text-secondary); line-height: 1.7; }

    .achievement-metric {
      margin-top: 1rem; padding-top: 1rem; border-top: 1px solid var(--border);
      font-size: .8rem; font-weight: 600; color: var(--accent3);
    }

    /* ─── SKILLS ─────────────────────────────────── */
    .skills-container { display: flex; flex-direction: column; gap: 2.5rem; }

    .skill-category h3 {
      font-size: .8rem; font-weight: 600; letter-spacing: .12em;
      text-transform: uppercase; color: var(--text-muted);
      margin-bottom: 1rem;
    }

    .skill-tags { display: flex; flex-wrap: wrap; gap: .6rem; }

    .skill-tag {
      display: inline-flex; align-items: center; gap: .4rem;
      padding: .45rem .9rem; border-radius: 8px;
      font-size: .85rem; font-weight: 500;
      background: var(--bg-card2); border: 1px solid var(--border);
      color: var(--text-secondary); transition: all .2s;
    }
    .skill-tag:hover { border-color: var(--accent); color: var(--text); }

    .skill-tag.primary {
      background: rgba(14,165,233,.1); border-color: rgba(14,165,233,.3);
      color: var(--accent);
    }

    /* ─── LEARNING ───────────────────────────────── */
    .learning-grid {
      display: grid; grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
      gap: 1.5rem;
    }

    .learning-card {
      background: var(--bg-card); border: 1px solid var(--border);
      border-radius: 16px; padding: 1.5rem;
      transition: all .25s; position: relative;
    }
    .learning-card:hover { border-color: rgba(139,92,246,.5); transform: translateY(-2px); }

    .learning-icon {
      width: 48px; height: 48px; border-radius: 12px;
      display: flex; align-items: center; justify-content: center;
      font-size: 1.5rem; margin-bottom: 1rem;
    }

    .learning-card h3 { font-size: 1rem; font-weight: 600; margin-bottom: .4rem; }
    .learning-card p { font-size: .85rem; color: var(--text-secondary); }

    .learning-status {
      display: inline-flex; align-items: center; gap: .35rem;
      font-size: .75rem; font-weight: 600; margin-top: 1rem;
    }
    .status-dot { width: 6px; height: 6px; border-radius: 50%; }
    .status-completed { color: var(--accent3); }
    .status-completed .status-dot { background: var(--accent3); }
    .status-ongoing { color: var(--accent); }
    .status-ongoing .status-dot { background: var(--accent); animation: pulse 2s infinite; }

    @keyframes pulse {
      0%, 100% { opacity: 1; }
      50% { opacity: .3; }
    }

    /* ─── TIMELINE ───────────────────────────────── */
    .timeline { position: relative; padding-left: 2rem; }
    .timeline::before {
      content: ''; position: absolute; left: 0; top: 0; bottom: 0;
      width: 2px; background: linear-gradient(to bottom, var(--accent), var(--accent2), transparent);
    }

    .timeline-item { position: relative; margin-bottom: 2.5rem; }
    .timeline-dot {
      position: absolute; left: -2.5rem; top: .25rem;
      width: 12px; height: 12px; border-radius: 50%;
      background: var(--accent); border: 2px solid var(--bg);
      box-shadow: 0 0 0 3px rgba(14,165,233,.2);
    }

    .timeline-date {
      font-size: .8rem; color: var(--accent); font-weight: 600;
      margin-bottom: .35rem;
    }
    .timeline-role { font-size: 1.05rem; font-weight: 600; margin-bottom: .15rem; }
    .timeline-company { font-size: .9rem; color: var(--text-secondary); margin-bottom: .75rem; }
    .timeline-desc { font-size: .875rem; color: var(--text-secondary); line-height: 1.7; }

    /* ─── CONTACT ────────────────────────────────── */
    .contact-wrapper {
      background: var(--bg-card); border: 1px solid var(--border);
      border-radius: 24px; padding: 3rem;
      display: flex; align-items: center; justify-content: space-between;
      gap: 2rem; flex-wrap: wrap;
      position: relative; overflow: hidden;
    }
    .contact-wrapper::before {
      content: ''; position: absolute;
      top: -50%; right: -10%; width: 400px; height: 400px;
      background: radial-gradient(circle, rgba(14,165,233,.08) 0%, transparent 70%);
      pointer-events: none;
    }

    .contact-text h2 {
      font-family: 'Space Grotesk', sans-serif;
      font-size: 2rem; font-weight: 700; margin-bottom: .5rem;
    }
    .contact-text p { color: var(--text-secondary); }

    .contact-links { display: flex; flex-direction: column; gap: .75rem; }
    .contact-link {
      display: flex; align-items: center; gap: .75rem;
      color: var(--text-secondary); text-decoration: none;
      font-size: .9rem; transition: color .2s;
    }
    .contact-link:hover { color: var(--accent); }
    .contact-link svg { width: 18px; height: 18px; flex-shrink: 0; }

    /* ─── FOOTER ─────────────────────────────────── */
    footer {
      text-align: center; padding: 2rem;
      border-top: 1px solid var(--border);
      color: var(--text-muted); font-size: .8rem;
    }

    /* ─── DIVIDER ────────────────────────────────── */
    .section-divider {
      max-width: 1100px; margin: 0 auto;
      border: none; border-top: 1px solid var(--border);
    }

    /* ─── ANIMATIONS ─────────────────────────────── */
    .fade-in {
      opacity: 0; transform: translateY(24px);
      transition: opacity .6s ease, transform .6s ease;
    }
    .fade-in.visible { opacity: 1; transform: translateY(0); }

    /* ─── CERT BADGE ─────────────────────────────── */
    .cert-badge {
      display: inline-flex; align-items: center; gap: .6rem;
      background: linear-gradient(135deg, rgba(14,165,233,.1), rgba(139,92,246,.1));
      border: 1px solid rgba(14,165,233,.3); border-radius: 12px;
      padding: .75rem 1.25rem; margin-bottom: 1rem;
    }
    .cert-badge-icon { font-size: 1.5rem; }
    .cert-badge-text h4 { font-size: .9rem; font-weight: 600; }
    .cert-badge-text p { font-size: .75rem; color: var(--text-secondary); }
  </style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">SBT</div>
  <div class="nav-links">
    <a href="#about">About</a>
    <a href="#achievements">Achievements</a>
    <a href="#skills">Skills</a>
    <a href="#learning">Learning</a>
    <a href="#contact">Contact</a>
  </div>
</nav>

<!-- HERO -->
<div class="hero">
  <div class="hero-grid"></div>
  <div class="hero-glow"></div>
  <div class="hero-content">
    <div class="hero-badge">
      <span>●</span> Open to new opportunities
    </div>
    <h1 class="hero-title">
      <span class="name">Srinivas Bhargav<br>Tagirisa</span>
      <span class="role">Senior IT Engineer · VDI &amp; Cloud Infrastructure</span>
    </h1>
    <p class="hero-desc">
      Building enterprise-scale infrastructure that keeps 25,000+ global users in the air.
      Specializing in VMware, Azure, and hybrid cloud platforms at American Airlines.
    </p>
    <div class="hero-stats">
      <div class="stat">
        <div class="stat-num">7+</div>
        <div class="stat-label">Years Experience</div>
      </div>
      <div class="stat">
        <div class="stat-num">25K+</div>
        <div class="stat-label">Users Supported</div>
      </div>
      <div class="stat">
        <div class="stat-num">8K+</div>
        <div class="stat-label">VMs Managed</div>
      </div>
      <div class="stat">
        <div class="stat-num">550+</div>
        <div class="stat-label">Systems Migrated</div>
      </div>
    </div>
    <div class="hero-cta">
      <a href="#achievements" class="btn btn-primary">View Achievements</a>
      <a href="https://www.linkedin.com/in/srinivas-bhargav-tagirisa-90028b15b/" target="_blank" class="btn btn-outline">LinkedIn Profile</a>
    </div>
  </div>
</div>

<!-- ABOUT -->
<section id="about" class="fade-in">
  <div class="section-label">About Me</div>
  <h2 class="section-title">Engineer. Problem-Solver. Lifelong Learner.</h2>
  <div class="about-grid">
    <div class="about-text">
      <p>
        I'm a Senior IT Engineer with over 7 years of experience modernizing and governing enterprise-scale
        Virtual Desktop Infrastructure (VDI) and hybrid cloud platforms. Currently at <strong>American Airlines</strong>,
        I support critical airport and operational systems that power one of the world's largest airlines.
      </p>
      <p>
        My expertise spans VMware Horizon Cloud on Azure, Azure VMware Solution (AVS), AWS Cloud, and
        Citrix environments — delivering high-availability deployments that serve global workforces without
        interruption.
      </p>
      <p>
        Beyond operations, I'm passionate about automation, clean infrastructure design, and sharing
        knowledge across teams. I continuously invest in learning — from cloud certifications to Python scripting
        — to stay ahead in a rapidly evolving landscape.
      </p>
    </div>
    <div class="about-highlights">
      <div class="highlight-card">
        <div class="highlight-icon icon-blue">✈️</div>
        <div class="highlight-body">
          <h4>American Airlines · Senior IT Engineer</h4>
          <p>End User Compute team — managing VDI infrastructure for airport kiosk and operational services since August 2023.</p>
        </div>
      </div>
      <div class="highlight-card">
        <div class="highlight-icon icon-purple">🎓</div>
        <div class="highlight-body">
          <h4>Koneru Lakshmaiah University</h4>
          <p>B.Tech — GPA 3.8/4.0 · Vijayawada, India</p>
        </div>
      </div>
      <div class="highlight-card">
        <div class="highlight-icon icon-green">🏅</div>
        <div class="highlight-body">
          <h4>Microsoft Certified: AZ-104</h4>
          <p>Azure Administrator Associate — validating Azure cloud infrastructure expertise.</p>
        </div>
      </div>
      <div class="highlight-card">
        <div class="highlight-icon icon-blue">📍</div>
        <div class="highlight-body">
          <h4>Based in Dallas, TX</h4>
          <p>Working at American Airlines HQ — one of the world's largest airline operations.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<hr class="section-divider" />

<!-- ACHIEVEMENTS AT AA -->
<section id="achievements" class="fade-in">
  <div class="aa-header">
    <div class="aa-logo-wrapper">
      <span class="aa-logo-text">AA</span>
    </div>
    <div>
      <div class="section-label">Current Role</div>
      <h2 class="section-title" style="margin-bottom:0">Key Achievements at American Airlines</h2>
      <p style="color:var(--text-secondary); font-size:.9rem;">End User Compute · Aug 2023 – Present · Dallas, TX</p>
    </div>
  </div>

  <div class="achievement-grid">

    <div class="achievement-card">
      <span class="achievement-tag tag-infra">Infrastructure</span>
      <h3>VDI Fleet Management at Scale</h3>
      <p>Managing 8,000+ Omnissa virtual machines on Azure VMware Solution (AVS) that power airport kiosk and operational services — ensuring SLA adherence and peak performance for mission-critical airline operations.</p>
      <div class="achievement-metric">↑ 25,000+ global users supported</div>
    </div>

    <div class="achievement-card">
      <span class="achievement-tag tag-infra">Platform Upgrade</span>
      <h3>Multi-Region Horizon Upgrade</h3>
      <p>Spearheaded production upgrades from Horizon 2111.1 to a later version across EastUS and NorthCentral Azure regions — coordinating change windows, dependencies, and validation to minimize disruption across production environments.</p>
      <div class="achievement-metric">↑ Zero-downtime production upgrade</div>
    </div>

    <div class="achievement-card">
      <span class="achievement-tag tag-automation">Automation</span>
      <h3>Browser Content Redirection (BCR)</h3>
      <p>Implemented Browser Content Redirection for Amazon Connect, enhancing agent efficiency and reducing VM-side resource consumption by offloading browser rendering — directly improving contact center performance.</p>
      <div class="achievement-metric">↓ ~98% reduction in resource consumption for redirected sessions</div>
    </div>

    <div class="achievement-card">
      <span class="achievement-tag tag-automation">Hygiene</span>
      <h3>Automated DB Cleanup</h3>
      <p>Eliminated non-essential DB records and manual cleanup tasks, improving system hygiene and reducing operational toil. Built repeatable processes that freed engineering hours for higher-value work.</p>
      <div class="achievement-metric">↑ Eliminated recurring manual maintenance</div>
    </div>

    <div class="achievement-card">
      <span class="achievement-tag tag-migration">Migration</span>
      <h3>Consolidated Platform Migration</h3>
      <p>Led the full migration of 550+ consolidated platforms — from legacy systems to unified infrastructure — integrating Unified Access Gateways (v23.12) and ONE SAML authentication to strengthen identity and access security.</p>
      <div class="achievement-metric">↑ 550+ systems successfully migrated</div>
    </div>

    <div class="achievement-card">
      <span class="achievement-tag tag-security">Security</span>
      <h3>UAG &amp; SSO Modernization</h3>
      <p>Deployed and integrated Unified Access Gateways with ONE SAML SSO (including third-party IDP PingFederate) and strengthened AV64 cluster security posture. Renewed PKCS#12 certificates proactively to prevent outages.</p>
      <div class="achievement-metric">↑ Zero auth-related outages</div>
    </div>

    <div class="achievement-card">
      <span class="achievement-tag tag-ops">Operations</span>
      <h3>Incident Resolution &amp; Root Cause Analysis</h3>
      <p>Diagnosed and resolved critical application issues through deep root-cause analysis — including full failover orchestration, App Volumes 4 troubleshooting, and multi-region desktop/file server synchronization incidents.</p>
      <div class="achievement-metric">↑ Reduced MTTR for critical VDI incidents</div>
    </div>

    <div class="achievement-card">
      <span class="achievement-tag tag-infra">Monitoring</span>
      <h3>Lifecycle &amp; Snapshot Management</h3>
      <p>Maintained clean refresh snapshots on a scheduled cadence, validated compatibility across infrastructure versions before production rollouts, and ensured reliable rollback plans for every change window.</p>
      <div class="achievement-metric">↑ 100% rollback readiness on all changes</div>
    </div>

    <div class="achievement-card">
      <span class="achievement-tag tag-security">Observability</span>
      <h3>NXLog &amp; Arctic Wolf Sensor Deployment</h3>
      <p>Deployed NXLog agents and Arctic Wolf sensors across AVD and VDI endpoints for enhanced log aggregation and security monitoring — closing visibility gaps in the enterprise endpoint security posture.</p>
      <div class="achievement-metric">↑ Full endpoint log coverage</div>
    </div>

  </div>
</section>

<hr class="section-divider" />

<!-- CAREER TIMELINE -->
<section id="career" class="fade-in">
  <div class="section-label">Career</div>
  <h2 class="section-title">Experience Timeline</h2>
  <p class="section-subtitle">7+ years building, scaling, and securing infrastructure across enterprise environments.</p>

  <div class="timeline">
    <div class="timeline-item">
      <div class="timeline-dot"></div>
      <div class="timeline-date">Aug 2023 – Present</div>
      <div class="timeline-role">Senior IT Engineer — End User Compute</div>
      <div class="timeline-company">American Airlines · Dallas, TX</div>
      <div class="timeline-desc">
        Managing 8,000+ VMs on Azure VMware Solution for airport and operational services.
        Leading platform upgrades, migrations, automation, and security hardening across
        VMware Horizon and Omnissa environments for 25,000+ users globally.
      </div>
    </div>

    <div class="timeline-item">
      <div class="timeline-dot" style="background:var(--accent2)"></div>
      <div class="timeline-date">2021 – 2023</div>
      <div class="timeline-role">IT Consultant — VDI &amp; Citrix Specialist</div>
      <div class="timeline-company">Osys Limited / Niagara Brands</div>
      <div class="timeline-desc">
        Configured Citrix Virtual Apps and Desktops 8.6.0, deployed Unified Access Gateways (UAGs),
        published applications via StoreFront, and managed thin kiosk environments (v7.1.52).
        Implemented Microsoft LAPS, XenApp, NetScaler, and Endpoint Management solutions.
      </div>
    </div>

    <div class="timeline-item">
      <div class="timeline-dot" style="background:var(--accent3)"></div>
      <div class="timeline-date">2017 – 2021</div>
      <div class="timeline-role">IT Engineer — Infrastructure &amp; Cloud</div>
      <div class="timeline-company">Enterprise IT Environments</div>
      <div class="timeline-desc">
        Built foundational expertise in VMware vSphere/ESXi, Cisco UCS, Dell iDRAC,
        Windows Server (2019), Active Directory, DNS/DHCP, and backup solutions
        including Avamar, Cohesity, and Data Domain. Developed automation skills in
        PowerShell and Python.
      </div>
    </div>
  </div>
</section>

<hr class="section-divider" />

<!-- SKILLS -->
<section id="skills" class="fade-in">
  <div class="section-label">Technical Skills</div>
  <h2 class="section-title">Stack &amp; Expertise</h2>
  <p class="section-subtitle">Technologies I've deployed, maintained, and mastered in production environments.</p>

  <div class="skills-container">
    <div class="skill-category">
      <h3>VDI &amp; Virtual Desktop</h3>
      <div class="skill-tags">
        <span class="skill-tag primary">VMware Horizon (8.x)</span>
        <span class="skill-tag primary">Azure VMware Solution (AVS)</span>
        <span class="skill-tag primary">Omnissa</span>
        <span class="skill-tag">Citrix Virtual Apps &amp; Desktops</span>
        <span class="skill-tag">Azure Virtual Desktop (AVD)</span>
        <span class="skill-tag">AWS WorkSpaces</span>
        <span class="skill-tag">App Volumes 4</span>
        <span class="skill-tag">StoreFront / XenApp</span>
        <span class="skill-tag">Thin Kiosks</span>
      </div>
    </div>

    <div class="skill-category">
      <h3>Cloud &amp; Infrastructure</h3>
      <div class="skill-tags">
        <span class="skill-tag primary">Microsoft Azure</span>
        <span class="skill-tag primary">AWS (EC2, S3, VPC, IAM, Lambda)</span>
        <span class="skill-tag">vSphere / ESXi 7.0.3</span>
        <span class="skill-tag">vCenter</span>
        <span class="skill-tag">Cisco UCS</span>
        <span class="skill-tag">Dell iDRAC</span>
        <span class="skill-tag">IBM SoftLayer</span>
      </div>
    </div>

    <div class="skill-category">
      <h3>Security &amp; Identity</h3>
      <div class="skill-tags">
        <span class="skill-tag primary">Unified Access Gateways (UAG)</span>
        <span class="skill-tag primary">SAML / SSO</span>
        <span class="skill-tag">PingFederate (IDP)</span>
        <span class="skill-tag">Microsoft LAPS</span>
        <span class="skill-tag">Azure AD / Active Directory</span>
        <span class="skill-tag">PKCS#12 Certificate Management</span>
        <span class="skill-tag">Arctic Wolf (SIEM)</span>
        <span class="skill-tag">NXLog</span>
      </div>
    </div>

    <div class="skill-category">
      <h3>Networking &amp; Servers</h3>
      <div class="skill-tags">
        <span class="skill-tag">DNS / DHCP</span>
        <span class="skill-tag">NSGs</span>
        <span class="skill-tag">Load Balancers</span>
        <span class="skill-tag">VPN / NetScaler</span>
        <span class="skill-tag">Windows Server 2019</span>
        <span class="skill-tag">IIS</span>
      </div>
    </div>

    <div class="skill-category">
      <h3>Scripting, Monitoring &amp; DevOps</h3>
      <div class="skill-tags">
        <span class="skill-tag primary">PowerShell</span>
        <span class="skill-tag primary">Python</span>
        <span class="skill-tag">GitHub</span>
        <span class="skill-tag">Azure DevOps (ADO)</span>
        <span class="skill-tag">Grafana</span>
        <span class="skill-tag">Datadog</span>
        <span class="skill-tag">Azure CLI</span>
      </div>
    </div>

    <div class="skill-category">
      <h3>Backup &amp; Recovery</h3>
      <div class="skill-tags">
        <span class="skill-tag">Avamar</span>
        <span class="skill-tag">Cohesity</span>
        <span class="skill-tag">Data Domain</span>
        <span class="skill-tag">DP4400 / IDPA</span>
      </div>
    </div>
  </div>
</section>

<hr class="section-divider" />

<!-- LEARNING JOURNEY -->
<section id="learning" class="fade-in">
  <div class="section-label">Learning Journey</div>
  <h2 class="section-title">Always Growing</h2>
  <p class="section-subtitle">I believe the best engineers never stop learning. Here's what I'm investing in — certifications, skills, and personal projects.</p>

  <div class="learning-grid">

    <div class="learning-card">
      <div class="learning-icon" style="background:rgba(14,165,233,.12)">🏅</div>
      <h3>Microsoft Azure Administrator</h3>
      <p>AZ-104 certified — validating expertise in Azure identity, governance, storage, compute, and networking.</p>
      <div class="learning-status status-completed"><span class="status-dot"></span>Completed</div>
    </div>

    <div class="learning-card">
      <div class="learning-icon" style="background:rgba(139,92,246,.12)">☁️</div>
      <h3>Cloud Architecture Deepdive</h3>
      <p>Expanding hands-on knowledge of multi-cloud patterns — Azure + AWS hybrid architectures, HA design, cost optimization.</p>
      <div class="learning-status status-ongoing"><span class="status-dot"></span>Ongoing</div>
    </div>

    <div class="learning-card">
      <div class="learning-icon" style="background:rgba(16,185,129,.12)">🐍</div>
      <h3>Python Automation for IT Ops</h3>
      <p>Writing scripts to automate routine infrastructure tasks — VM health checks, reporting pipelines, and API integrations with Azure.</p>
      <div class="learning-status status-ongoing"><span class="status-dot"></span>Ongoing</div>
    </div>

    <div class="learning-card">
      <div class="learning-icon" style="background:rgba(245,158,11,.12)">🔐</div>
      <h3>Cybersecurity &amp; Zero Trust</h3>
      <p>Deepening knowledge of Zero Trust architecture, endpoint detection, SIEM tools (Arctic Wolf), and identity-first security models.</p>
      <div class="learning-status status-ongoing"><span class="status-dot"></span>Ongoing</div>
    </div>

    <div class="learning-card">
      <div class="learning-icon" style="background:rgba(239,68,68,.12)">📜</div>
      <h3>SOPs &amp; Knowledge Base Building</h3>
      <p>Developing and maintaining Standard Operating Procedures for VDI operations — improving team efficiency and onboarding quality.</p>
      <div class="learning-status status-completed"><span class="status-dot"></span>Active practice</div>
    </div>

    <div class="learning-card">
      <div class="learning-icon" style="background:rgba(14,165,233,.12)">📊</div>
      <h3>Monitoring &amp; Observability</h3>
      <p>Learning advanced Grafana dashboards and Datadog alerting strategies to build proactive infrastructure monitoring pipelines.</p>
      <div class="learning-status status-ongoing"><span class="status-dot"></span>Ongoing</div>
    </div>

  </div>
</section>

<hr class="section-divider" />

<!-- CONTACT -->
<section id="contact" class="fade-in">
  <div class="contact-wrapper">
    <div class="contact-text">
      <div class="section-label">Get in Touch</div>
      <h2>Let's Connect</h2>
      <p>Open to conversations about infrastructure, cloud, VDI, and new opportunities.</p>
    </div>
    <div class="contact-links">
      <a href="mailto:srinivastagirisa@gmail.com" class="contact-link">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <rect x="2" y="4" width="20" height="16" rx="2"/><path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"/>
        </svg>
        srinivastagirisa@gmail.com
      </a>
      <a href="https://www.linkedin.com/in/srinivas-bhargav-tagirisa-90028b15b/" target="_blank" class="contact-link">
        <svg viewBox="0 0 24 24" fill="currentColor">
          <path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/>
        </svg>
        linkedin.com/in/srinivas-bhargav-tagirisa
      </a>
      <a href="tel:+19086990233" class="contact-link">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07A19.5 19.5 0 0 1 4.69 13.6a19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 3.6 3h3a2 2 0 0 1 2 1.72c.127.96.361 1.903.7 2.81a2 2 0 0 1-.45 2.11L7.91 10.6a16 16 0 0 0 6 6l.94-1.01a2 2 0 0 1 2.11-.45c.907.339 1.85.573 2.81.7A2 2 0 0 1 22 16.92z"/>
        </svg>
        (908) 699-0233
      </a>
      <a class="contact-link" style="cursor:default">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <path d="M20 10c0 6-8 12-8 12s-8-6-8-12a8 8 0 0 1 16 0Z"/><circle cx="12" cy="10" r="3"/>
        </svg>
        Dallas, TX
      </a>
    </div>
  </div>
</section>

<footer>
  <p>Built with ❤️ · Srinivas Bhargav Tagirisa · Senior IT Engineer · Dallas, TX · 2025</p>
</footer>

<script>
  // Fade-in on scroll
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); });
  }, { threshold: 0.1 });
  document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));
</script>

</body>
</html>
