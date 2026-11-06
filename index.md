              HTML

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Assignment 9.3 — Hybrid Flexbox & Grid Responsive Landing Page</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <!-- ================= STEP 1 & 5: NAVBAR (FLEXBOX) ================= -->
  <header class="site-header">
    <div class="nav-container">
      <a href="#" class="logo">Kinetix<span>Core</span></a>
      <nav class="nav-links">
        <a href="#hero">Overview</a>
        <a href="#features">Features</a>
        <a href="#docs">Docs</a>
      </nav>
      <div class="nav-action">
        <a href="#start" class="btn btn-primary btn-sm">Get Started</a>
      </div>
    </div>
  </header>

  <main>
    <!-- ================= STEP 2, 4 & 5: HERO SECTION (GRID + FLEXBOX) ================= -->
    <section class="hero-section" id="hero">
      <div class="hero-grid">
        
        <!-- Text Column (Flexbox for internal alignment) -->
        <div class="hero-content">
          <span class="badge">Engineered for Latency</span>
          <h1 class="hero-title">Distributed edge caching with atomic consistency</h1>
          <p class="hero-description">
            Accelerate database reads, reduce edge egress costs, and sync data stores worldwide in sub-millisecond roundtrips.
          </p>
          <div class="hero-buttons">
            <a href="#start" class="btn btn-primary">Start Deploying Free</a>
            <a href="#docs" class="btn btn-outline">Read the Spec</a>
          </div>
        </div>

        <!-- Image Column -->
        <div class="hero-visual">
          <img 
            src="https://images.unsplash.com/photo-1558494949-ef010cbdcc31?w=900&auto=format&fit=crop&q=80" 
            alt="High-density network server racks and cabling"
          >
        </div>

      </div>
    </section>

    <!-- ================= STEP 3, 4 & 5: FEATURES SECTION (GRID + FLEXBOX) ================= -->
    <section class="features-section" id="features">
      <div class="section-heading">
        <span class="section-tag">Core Architecture</span>
        <h2>Built from the ground up for scale</h2>
        <p>A unified data plane engineered for cloud-native performance.</p>
      </div>

      <!-- Step 4: Grid Layout Container for Cards -->
      <div class="features-grid">

        <!-- Card 1 (Step 5: Flexbox internal layout) -->
        <article class="feature-card">
          <div class="card-icon">⚡</div>
          <div class="card-body">
            <h3>P99 Sub-10ms Latency</h3>
            <p>Every lookup executes from local L1 memory caches with instant zero-copy replication.</p>
          </div>
          <a href="#" class="card-link">Explore Benchmarks →</a>
        </article>

        <!-- Card 2 -->
        <article class="feature-card">
          <div class="card-icon">🛡️</div>
          <div class="card-body">
            <h3>Zero-Trust Encryption</h3>
            <p>Hardware-level mTLS and end-to-end key rotation out of the box with SOC2 compliance.</p>
          </div>
          <a href="#" class="card-link">Security Whitepaper →</a>
        </article>

        <!-- Card 3 -->
        <article class="feature-card">
          <div class="card-icon">🔄</div>
          <div class="card-body">
            <h3>Multi-Cloud Failover</h3>
            <p>Route traffic transparently across AWS, GCP, and Azure with automatic failover.</p>
          </div>
          <a href="#" class="card-link">Topology Guide →</a>
        </article>

        <!-- Card 4 -->
        <article class="feature-card">
          <div class="card-icon">📦</div>
          <div class="card-body">
            <h3>Instant Replays</h3>
            <p>Debug anomalies using deterministic time-travel event replays across any point in time.</p>
          </div>
          <a href="#" class="card-link">Audit Features →</a>
        </article>

        <!-- Card 5 -->
        <article class="feature-card">
          <div class="card-icon">📈</div>
          <div class="card-body">
            <h3>Auto-Scaling Pools</h3>
            <p>Burst gracefully from zero to millions of transactions without manual cluster reconfiguration.</p>
          </div>
          <a href="#" class="card-link">Capacity Specs →</a>
        </article>

        <!-- Card 6 -->
        <article class="feature-card">
          <div class="card-icon">💻</div>
          <div class="card-body">
            <h3>SDKs in 8 Languages</h3>
            <p>Native type-safe drivers for TypeScript, Go, Rust, Python, Java, C#, Ruby, and PHP.</p>
          </div>
          <a href="#" class="card-link">Quickstart Guides →</a>
        </article>

      </div>
    </section>
  </main>

  <!-- ================= FOOTER ================= -->
  <footer class="site-footer">
    <div class="footer-inner">
      <p>&copy; 2026 KinetixCore Systems, Inc. All rights reserved.</p>
      <div class="footer-links">
        <a href="#">Privacy</a>
        <a href="#">Terms</a>
        <a href="#">Status</a>
      </div>
    </div>
  </footer>

</body>
</html>



                     CSS


/* --- Global Reset & Variables --- */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

:root {
  --primary: #2563eb;
  --primary-hover: #1d4ed8;
  --bg-dark: #0a0f1d;
  --bg-surface: #111827;
  --bg-card: #1f2937;
  --border: #374151;
  --text-main: #f9fafb;
  --text-muted: #9ca3af;
  --accent: #38bdf8;
}

body {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
  background-color: var(--bg-dark);
  color: var(--text-main);
  line-height: 1.6;
  overflow-x: hidden;
}

/* --- Shared Button Components --- */
.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  padding: 0.75rem 1.5rem;
  font-size: 0.95rem;
  font-weight: 600;
  border-radius: 8px;
  text-decoration: none;
  transition: all 0.2s ease;
  cursor: pointer;
}

.btn-sm {
  padding: 0.45rem 1rem;
  font-size: 0.85rem;
}

.btn-primary {
  background-color: var(--primary);
  color: #ffffff;
  border: 1px solid var(--primary);
}

.btn-primary:hover {
  background-color: var(--primary-hover);
}

.btn-outline {
  background-color: transparent;
  color: var(--text-main);
  border: 1px solid var(--border);
}

.btn-outline:hover {
  background-color: var(--bg-surface);
  border-color: var(--text-muted);
}

/* ================= STEP 1 & 5: NAVBAR (FLEXBOX) ================= */
.site-header {
  position: sticky;
  top: 0;
  z-index: 100;
  background-color: rgba(10, 15, 29, 0.9);
  backdrop-filter: blur(8px);
  border-bottom: 1px solid var(--border);
}

/* Flexbox container for navbar distribution */
.nav-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1200px;
  margin: 0 auto;
  padding: 1rem 1.5rem;
}

.logo {
  font-size: 1.35rem;
  font-weight: 800;
  color: var(--text-main);
  text-decoration: none;
}

.logo span {
  color: var(--accent);
}

.nav-links {
  display: flex;
  gap: 2rem;
}

.nav-links a {
  text-decoration: none;
  color: var(--text-muted);
  font-size: 0.95rem;
  font-weight: 500;
  transition: color 0.2s;
}

.nav-links a:hover {
  color: var(--accent);
}

/* ================= STEP 2, 4 & 5: HERO SECTION ================= */
.hero-section {
  padding: 5rem 1.5rem;
  border-bottom: 1px solid var(--border);
}

/* Step 4: CSS Grid for Hero 2-column layout */
.hero-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-items: center;
  gap: 3.5rem;
  max-width: 1200px;
  margin: 0 auto;
}

/* Step 5: Flexbox inside Hero text content */
.hero-content {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 1.25rem;
}

.badge {
  background-color: rgba(56, 189, 248, 0.12);
  color: var(--accent);
  padding: 0.35rem 0.85rem;
  border-radius: 9999px;
  font-size: 0.8rem;
  font-weight: 700;
  letter-spacing: 0.05em;
  text-transform: uppercase;
}

.hero-title {
  font-size: 3rem;
  font-weight: 800;
  line-height: 1.15;
  letter-spacing: -0.025em;
}

.hero-description {
  font-size: 1.15rem;
  color: var(--text-muted);
}

/* Step 5: Flexbox for action buttons */
.hero-buttons {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
  margin-top: 0.5rem;
}

.hero-visual {
  width: 100%;
}

.hero-visual img {
  width: 100%;
  height: auto;
  border-radius: 12px;
  border: 1px solid var(--border);
  box-shadow: 0 20px 35px -10px rgba(0, 0, 0, 0.5);
  display: block;
}

/* ================= STEP 3, 4 & 5: FEATURES SECTION ================= */
.features-section {
  padding: 5rem 1.5rem;
  max-width: 1200px;
  margin: 0 auto;
}

.section-heading {
  text-align: center;
  margin-bottom: 3.5rem;
}

.section-tag {
  color: var(--accent);
  font-size: 0.8rem;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.08em;
}

.section-heading h2 {
  font-size: 2.25rem;
  font-weight: 800;
  margin-top: 0.35rem;
}

.section-heading p {
  color: var(--text-muted);
  margin-top: 0.5rem;
}

/* Step 4: CSS Grid for 6 cards layout */
.features-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
}

/* Step 5: Flexbox inside individual feature cards */
.feature-card {
  background-color: var(--bg-surface);
  border: 1px solid var(--border);
  border-radius: 12px;
  padding: 2rem;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  gap: 1.25rem;
  transition: transform 0.2s ease, border-color 0.2s ease;
}

.feature-card:hover {
  transform: translateY(-4px);
  border-color: var(--accent);
}

.card-icon {
  font-size: 2rem;
}

.card-body h3 {
  font-size: 1.2rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.card-body p {
  color: var(--text-muted);
  font-size: 0.925rem;
}

.card-link {
  color: var(--accent);
  text-decoration: none;
  font-size: 0.85rem;
  font-weight: 600;
  margin-top: auto;                  /* Flexbox trick: pins link to card bottom */
}

/* ================= FOOTER ================= */
.site-footer {
  border-top: 1px solid var(--border);
  padding: 2.5rem 1.5rem;
}

.footer-inner {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 0.875rem;
  color: var(--text-muted);
}

.footer-links {
  display: flex;
  gap: 1.5rem;
}

.footer-links a {
  color: var(--text-muted);
  text-decoration: none;
}

.footer-links a:hover {
  color: var(--text-main);
}

/* ================= STEP 6: MOBILE LAYOUT REFLECTION (< 900px) ================= */
@media (max-width: 900px) {
  /* Hero transforms from 2-column grid into 1 single column */
  .hero-grid {
    grid-template-columns: 1fr;
    gap: 2.5rem;
  }

  .hero-title {
    font-size: 2.25rem;
  }

  /* Features transform from 3-column grid into 2 columns on tablets */
  .features-grid {
    grid-template-columns: repeat(2, 1fr);
    gap: 1.5rem;
  }
}

@media (max-width: 640px) {
  .nav-links {
    display: none;                    /* Simplifies header for small screens */
  }

  /* Step 6: Features collapse into a single-column layout */
  .features-grid {
    grid-template-columns: 1fr;
  }

  .hero-buttons {
    flex-direction: column;
    width: 100%;
  }

  .hero-buttons .btn {
    width: 100%;
  }

  .footer-inner {
    flex-direction: column;
    gap: 1.25rem;
    text-align: center;
  }
}