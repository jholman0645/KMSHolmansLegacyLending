<script>
  let count = $state(0)
</script>

<main>
  <header class="dashboard-header">
    <img src="/firefly.svg" class="logo firefly-logo" alt="Firefly Logo" />
    <h1>FUF Fintech Dashboard</h1>
    <p class="subtitle">KMS Holmans Legacy Lending</p>
  </header>

  <section class="counter-section">
    <h2>Interactive Counter</h2>
    <p class="counter-display">{count}</p>
    <div class="button-group">
      <button class="glow-btn glow-green" onclick={() => count++}>
        + Increment
      </button>
      <button class="glow-btn glow-red" onclick={() => count--}>
        − Decrement
      </button>
      <button class="glow-btn glow-blue" onclick={() => count = 0}>
        ↺ Reset
      </button>
    </div>
  </section>

  <section class="features-section">
    <h2>Platform Features</h2>
    <div class="feature-grid">
      <div class="feature-card">
        <span class="feature-icon">🎯</span>
        <h3>Smart Lending</h3>
        <p>AI-driven loan matching and approval</p>
      </div>
      <div class="feature-card">
        <span class="feature-icon">🔒</span>
        <h3>Secure</h3>
        <p>Blockchain-backed security</p>
      </div>
      <div class="feature-card">
        <span class="feature-icon">⚡</span>
        <h3>Fast Processing</h3>
        <p>Approved in minutes, not days</p>
      </div>
    </div>
  </section>

  <footer>
    <p>© 2025 KMS Holmans Legacy Lending · Founder: Jason Holman</p>
    <p class="tribute"><em>In loving memory of Kiara Jink Holman</em></p>
  </footer>
</main>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&display=swap');

  main {
    font-family: 'Orbitron', sans-serif;
    color: #e0e0e0;
  }

  /* ── Header ── */
  .dashboard-header {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0.5rem;
    padding: 2rem 0 1.5rem;
  }

  .firefly-logo {
    width: 100px;
    height: 100px;
    filter: drop-shadow(0 0 16px #00ff88) drop-shadow(0 0 32px #00ff8844);
    animation: float 3s ease-in-out infinite;
  }

  @keyframes float {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-10px); }
  }

  h1 {
    font-size: 2rem;
    font-weight: 700;
    background: linear-gradient(90deg, #00ff88, #00c8ff, #a78bfa);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    text-shadow: none;
  }

  .subtitle {
    color: #88aacc;
    font-size: 0.9rem;
    letter-spacing: 0.1em;
  }

  /* ── Counter Section ── */
  .counter-section {
    background: rgba(255, 255, 255, 0.04);
    border: 1px solid rgba(255, 255, 255, 0.08);
    border-radius: 16px;
    padding: 2rem;
    margin: 2rem 0;
  }

  .counter-section h2 {
    font-size: 1.2rem;
    color: #88aacc;
    margin-bottom: 1rem;
    letter-spacing: 0.05em;
  }

  .counter-display {
    font-size: 5rem;
    font-weight: 700;
    color: #00ff88;
    text-shadow: 0 0 20px #00ff88, 0 0 40px #00ff8866;
    line-height: 1.1;
    margin-bottom: 1.5rem;
    transition: all 0.15s ease;
  }

  .button-group {
    display: flex;
    gap: 1rem;
    justify-content: center;
    flex-wrap: wrap;
  }

  /* ── Glowing Buttons ── */
  .glow-btn {
    padding: 0.75rem 1.75rem;
    font-family: 'Orbitron', sans-serif;
    font-size: 0.9rem;
    font-weight: 700;
    letter-spacing: 0.05em;
    border: 2px solid;
    border-radius: 8px;
    cursor: pointer;
    background: transparent;
    transition: all 0.25s ease;
    position: relative;
    overflow: hidden;
  }

  .glow-btn::before {
    content: '';
    position: absolute;
    inset: 0;
    background: currentColor;
    opacity: 0;
    transition: opacity 0.25s ease;
  }

  .glow-btn:hover::before { opacity: 0.12; }
  .glow-btn:active { transform: scale(0.97); }

  .glow-green {
    color: #00ff88;
    border-color: #00ff88;
    box-shadow: 0 0 10px #00ff8844, inset 0 0 10px #00ff8811;
  }
  .glow-green:hover {
    box-shadow: 0 0 20px #00ff88, 0 0 40px #00ff8888, inset 0 0 20px #00ff8822;
  }

  .glow-red {
    color: #ff4466;
    border-color: #ff4466;
    box-shadow: 0 0 10px #ff446644, inset 0 0 10px #ff446611;
  }
  .glow-red:hover {
    box-shadow: 0 0 20px #ff4466, 0 0 40px #ff446688, inset 0 0 20px #ff446622;
  }

  .glow-blue {
    color: #00c8ff;
    border-color: #00c8ff;
    box-shadow: 0 0 10px #00c8ff44, inset 0 0 10px #00c8ff11;
  }
  .glow-blue:hover {
    box-shadow: 0 0 20px #00c8ff, 0 0 40px #00c8ff88, inset 0 0 20px #00c8ff22;
  }

  /* ── Features ── */
  .features-section {
    margin: 2rem 0;
  }

  .features-section h2 {
    font-size: 1.2rem;
    color: #88aacc;
    margin-bottom: 1.5rem;
    letter-spacing: 0.05em;
  }

  .feature-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 1rem;
  }

  .feature-card {
    background: rgba(255, 255, 255, 0.04);
    border: 1px solid rgba(0, 200, 255, 0.15);
    border-radius: 12px;
    padding: 1.5rem 1rem;
    transition: border-color 0.3s ease, box-shadow 0.3s ease;
  }

  .feature-card:hover {
    border-color: rgba(0, 200, 255, 0.4);
    box-shadow: 0 0 20px rgba(0, 200, 255, 0.15);
  }

  .feature-icon {
    font-size: 2rem;
    display: block;
    margin-bottom: 0.5rem;
  }

  .feature-card h3 {
    font-size: 0.9rem;
    color: #00c8ff;
    margin-bottom: 0.5rem;
  }

  .feature-card p {
    font-size: 0.8rem;
    color: #88aacc;
    font-family: sans-serif;
  }

  /* ── Footer ── */
  footer {
    margin-top: 3rem;
    padding: 1.5rem 0;
    border-top: 1px solid rgba(255, 255, 255, 0.08);
    color: #556677;
    font-size: 0.75rem;
    font-family: sans-serif;
    line-height: 1.8;
  }

  .tribute {
    color: #445566;
  }
</style>
