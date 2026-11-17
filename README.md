# My-deploy

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Satyabrata Nayak | AWS & DevOps Engineer</title>
  <style>
    :root {
      --bg-dark: #0b0f19;
      --bg-card: #111827;
      --border: #1f2937;
      --primary: #38bdf8;
      --accent: #f59e0b;
      --text-main: #f3f4f6;
      --text-muted: #9ca3af;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
      font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
    }

    body {
      background-color: var(--bg-dark);
      color: var(--text-main);
      line-height: 1.6;
    }

    /* Navigation */
    header {
      position: sticky;
      top: 0;
      z-index: 100;
      background: rgba(11, 15, 25, 0.85);
      backdrop-filter: blur(12px);
      border-bottom: 1px solid var(--border);
    }

    nav {
      max-width: 1100px;
      margin: 0 auto;
      padding: 1rem 1.5rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo {
      font-size: 1.25rem;
      font-weight: 700;
      color: var(--text-main);
      letter-spacing: 0.5px;
    }

    .logo span {
      color: var(--primary);
    }

    .nav-links {
      display: flex;
      gap: 1.75rem;
      list-style: none;
    }

    .nav-links a {
      color: var(--text-muted);
      text-decoration: none;
      font-size: 0.95rem;
      font-weight: 500;
      transition: color 0.2s;
    }

    .nav-links a:hover {
      color: var(--primary);
    }

    /* Hero Section */
    .hero {
      max-width: 1100px;
      margin: 0 auto;
      padding: 5.5rem 1.5rem 4.5rem;
      display: grid;
      grid-template-columns: 1.2fr 0.8fr;
      gap: 3rem;
      align-items: center;
    }

    .badge {
      display: inline-block;
      background: rgba(56, 189, 248, 0.12);
      color: var(--primary);
      border: 1px solid rgba(56, 189, 248, 0.3);
      padding: 0.35rem 0.9rem;
      border-radius: 999px;
      font-size: 0.85rem;
      font-weight: 600;
      margin-bottom: 1.25rem;
    }

    .hero h1 {
      font-size: 3rem;
      line-height: 1.15;
      margin-bottom: 1.25rem;
      background: linear-gradient(to right, #ffffff, #94a3b8);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    .hero p {
      color: var(--text-muted);
      font-size: 1.1rem;
      margin-bottom: 2rem;
      max-width: 560px;
    }

    .btn-group {
      display: flex;
      gap: 1rem;
      flex-wrap: wrap;
    }

    .btn {
      padding: 0.8rem 1.6rem;
      border-radius: 8px;
      font-weight: 600;
      text-decoration: none;
      font-size: 0.95rem;
      transition: transform 0.2s, box-shadow 0.2s;
    }

    .btn:hover {
      transform: translateY(-2px);
    }

    .btn-primary {
      background: var(--primary);
      color: #0b0f19;
      box-shadow: 0 4px 20px rgba(56, 189, 248, 0.3);
    }

    .btn-outline {
      border: 1px solid var(--border);
      color: var(--text-main);
      background: var(--bg-card);
    }

    /* Terminal Card */
    .terminal {
      background: #060911;
      border: 1px solid var(--border);
      border-radius: 12px;
      overflow: hidden;
      box-shadow: 0 20px 40px rgba(0, 0, 0, 0.5);
    }

    .terminal-header {
      background: #161d2f;
      padding: 0.7rem 1rem;
      display: flex;
      align-items: center;
      gap: 0.5rem;
      border-bottom: 1px solid var(--border);
    }

    .dot {
      width: 11px;
      height: 11px;
      border-radius: 50%;
    }

    .dot.red { background: #ef4444; }
    .dot.yellow { background: #f59e0b; }
    .dot.green { background: #10b981; }

    .terminal-title {
      margin-left: 0.5rem;
      font-size: 0.8rem;
      color: var(--text-muted);
      font-family: monospace;
    }

    .terminal-body {
      padding: 1.25rem;
      font-family: 'Courier New', Courier, monospace;
      font-size: 0.88rem;
      color: #e2e8f0;
    }

    .cmd { color: var(--primary); }
    .out { color: #94a3b8; margin-bottom: 0.75rem; display: block; }
    .ok { color: #10b981; }

    /* Sections */
    section {
      max-width: 1100px;
      margin: 0 auto;
      padding: 4rem 1.5rem;
    }

    .section-title {
      font-size: 1.9rem;
      margin-bottom: 0.5rem;
    }

    .section-sub {
      color: var(--text-muted);
      margin-bottom: 2.5rem;
    }

    /* Grid Cards */
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 1.5rem;
    }

    .card {
      background: var(--bg-card);
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 1.6rem;
      transition: border-color 0.25s, transform 0.25s;
    }

    .card:hover {
      border-color: var(--primary);
      transform: translateY(-4px);
    }

    .card h3 {
      font-size: 1.15rem;
      margin-bottom: 0.6rem;
      color: #ffffff;
    }

    .card p {
      color: var(--text-muted);
      font-size: 0.94rem;
    }

    .tags {
      display: flex;
      flex-wrap: wrap;
      gap: 0.5rem;
      margin-top: 1rem;
    }

    .tag {
      background: rgba(255, 255, 255, 0.05);
      color: var(--primary);
      padding: 0.25rem 0.65rem;
      border-radius: 6px;
      font-size: 0.78rem;
      font-weight: 600;
    }

    /* Pipeline Banner */
    .pipeline-box {
      background: linear-gradient(135deg, #111827, #0f172a);
      border: 1px solid var(--border);
      border-radius: 14px;
      padding: 2.2rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      gap: 1.5rem;
    }

    .steps {
      display: flex;
      align-items: center;
      gap: 0.75rem;
      flex-wrap: wrap;
    }

    .step {
      background: #1e293b;
      padding: 0.6rem 1rem;
      border-radius: 8px;
      font-size: 0.9rem;
      font-weight: 600;
      border: 1px solid #334155;
    }

    .arrow {
      color: var(--accent);
      font-weight: bold;
    }

    /* Footer */
    footer {
      border-top: 1px solid var(--border);
      text-align: center;
      padding: 2.5rem 1.5rem;
      color: var(--text-muted);
      font-size: 0.9rem;
      margin-top: 2rem;
    }

    footer a {
      color: var(--primary);
      text-decoration: none;
    }

    @media (max-width: 820px) {
      .hero {
        grid-template-columns: 1fr;
        padding-top: 3.5rem;
      }
      .hero h1 {
        font-size: 2.3rem;
      }
    }
  </style>
</head>
<body>

  <header>
    <nav>
      <div class="logo">Satya<span>.DevOps</span></div>
      <ul class="nav-links">
        <li><a href="#skills">Stack</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#pipeline">CI/CD</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <!-- Hero -->
    <div class="hero">
      <div>
        <span class="badge">● Automated via Jenkins & Apache</span>
        <h1>Satyabrata Nayak</h1>
        <p>
          AWS &amp; DevOps Engineer focused on building resilient cloud infrastructure, automated CI/CD pipelines, and high-availability Linux web deployments.
        </p>
        <div class="btn-group">
          <a href="#projects" class="btn btn-primary">View Deployments</a>
          <a href="https://github.com/satya-pyyc" target="_blank" class="btn btn-outline">GitHub Profile</a>
        </div>
      </div>

      <!-- Live Terminal Aesthetic -->
      <div class="terminal">
        <div class="terminal-header">
          <span class="dot red"></span>
          <span class="dot yellow"></span>
          <span class="dot green"></span>
          <span class="terminal-title">ubuntu@ec2-ap-south-1:~</span>
        </div>
        <div class="terminal-body">
          <div><span class="cmd">$</span> systemctl status apache2</div>
          <span class="out">● apache2.service - The Apache HTTP Server<br>&nbsp;&nbsp;&nbsp;Active: <span class="ok">active (running)</span></span>

          <div><span class="cmd">$</span> jenkins-build --job Website-Deploy</div>
          <span class="out">Fetching origin/main from GitHub...<br>Deploying artifacts to /var/www/html/<br><span class="ok">✔ Build #14 Succeeded (0 errors)</span></span>

          <div><span class="cmd">$</span> echo $REGION</div>
          <span class="out" style="margin-bottom:0;">ap-south-1 (Mumbai)</span>
        </div>
      </div>
    </div>

    <!-- Core Skills -->
    <section id="skills">
      <h2 class="section-title">Cloud &amp; DevOps Stack</h2>
      <p class="section-sub">Core technologies I use to provision, automate, and monitor production workloads.</p>
      <div class="grid">
        <div class="card">
          <h3>AWS Cloud Infrastructure</h3>
          <p>Designing secure virtual networks, scalable compute instances, and highly available storage architectures.</p>
          <div class="tags">
            <span class="tag">EC2</span>
            <span class="tag">VPC &amp; NAT</span>
            <span class="tag">IAM</span>
            <span class="tag">S3</span>
            <span class="tag">ELB</span>
          </div>
        </div>

        <div class="card">
          <h3>CI/CD &amp; Build Automation</h3>
          <p>Automating code integration, artifact builds, and zero-downtime web server deployments from Git commits.</p>
          <div class="tags">
            <span class="tag">Jenkins</span>
            <span class="tag">Git &amp; GitHub</span>
            <span class="tag">Webhooks</span>
            <span class="tag">Maven</span>
          </div>
        </div>

        <div class="card">
          <h3>Linux &amp; Web Servers</h3>
          <p>Hardening servers, managing permissions, writing shell automation scripts, and configuring reverse proxies.</p>
          <div class="tags">
            <span class="tag">Ubuntu</span>
            <span class="tag">Amazon Linux</span>
            <span class="tag">Apache2</span>
            <span class="tag">Bash</span>
          </div>
        </div>
      </div>
    </section>

    <!-- Projects -->
    <section id="projects">
      <h2 class="section-title">Featured Architecture &amp; Projects</h2>
      <p class="section-sub">Hands-on infrastructure labs and production-grade automation setups.</p>
      <div class="grid">
        <div class="card">
          <h3>Automated GitHub-to-Apache Pipeline</h3>
          <p>Configured a Jenkins Freestyle job triggered by GitHub commits to automatically pull static web builds and deploy them to Apache2 on AWS EC2.</p>
          <div class="tags">
            <span class="tag">Jenkins</span>
            <span class="tag">Apache2</span>
            <span class="tag">EC2 Ubuntu</span>
          </div>
        </div>

        <div class="card">
          <h3>Multi-Tier AWS VPC Architecture</h3>
          <p>Built an isolated Virtual Private Cloud in ap-south-1 with public/private subnets, custom Route Tables, NAT Gateways, and Security Groups.</p>
          <div class="tags">
            <span class="tag">AWS VPC</span>
            <span class="tag">Subnets</span>
            <span class="tag">Security Groups</span>
          </div>
        </div>

        <div class="card">
          <h3>DevOps Technical Blog</h3>
          <p>Publishing step-by-step troubleshooting guides on Linux administration, SSH key security, Jenkins recovery, and AWS networking.</p>
          <div class="tags">
            <span class="tag">Documentation</span>
            <span class="tag">Linux</span>
            <span class="tag">Cloud Ops</span>
          </div>
        </div>
      </div>
    </section>

    <!-- Live Deployment Architecture Banner -->
    <section id="pipeline">
      <div class="pipeline-box">
        <div>
          <h3 style="font-size:1.3rem; margin-bottom:0.35rem;">How This Site Is Delivered</h3>
          <p style="color:var(--text-muted); font-size:0.95rem;">End-to-end automated workflow powering this web page.</p>
        </div>
        <div class="steps">
          <div class="step">GitHub Push</div>
          <span class="arrow">→</span>
          <div class="step">Jenkins Build</div>
          <span class="arrow">→</span>
          <div class="step">/var/www/html</div>
          <span class="arrow">→</span>
          <div class="step" style="border-color: var(--primary); color: var(--primary);">Apache Live</div>
        </div>
      </div>
    </section>
  </main>

  <footer id="contact">
    <p>Built &amp; Deployed by <strong>Satyabrata Nayak</strong> • Odisha, India</p>
    <p style="margin-top:0.5rem;">
      <a href="https://github.com/satya-pyyc" target="_blank">GitHub</a> &nbsp;|&nbsp;
      <a href="https://satyabratadevops.blogspot.com" target="_blank">DevOps Blog</a>
    </p>
  </footer>

</body>
</html>
