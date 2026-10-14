

<!DOCTYPE html>
<html lang="en">
<head>

  
  <link rel="icon" href="../Kenyan E-Lost_Found App Emblem.png" type="image/png">   
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>E-Lost and found ID </title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }

    body {
      font-family: 'Segoe UI', system-ui, sans-serif;
      background: #248111;
      color: #d9dcdf;
      line-height: 1.6;
    }

    /* ── Header ── */
    header {
      background: linear-gradient(135deg, #000000, #000000);
      color: #fff;
      padding: 1rem 2rem;
      display: flex;
      align-items: center;
      justify-content: space-between;
      position: sticky;
      top: 0;
      z-index: 100;
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
    }
    header h1 { font-size: 1.4rem; }
    nav a {
      color: #fff;
      text-decoration: none;
      margin-left: 1.5rem;
      font-weight: 500;
      padding: 0.4rem 0.8rem;
      border-radius: 20px;
      transition: all 0.3s ease;
    }
    nav a:hover {
      background: rgba(255,255,255,0.2);
      transform: translateY(-2px);
    }

    /* ── Hero ── */
    .hero {
      text-align: center;
      padding: 5rem 2rem;
      background: linear-gradient(135deg, #BB0000 0%, #BB0000 50%, #fff 100%);
      color: #fff;
      position: relative;
      overflow: hidden;
    }
    .hero::before, .hero::after {
      content: '';
      position: absolute;
      border-radius: 50%;
      opacity: 0.15;
    }
    .hero::before {
      width: 300px; height: 300px;
      background: #fff;
      top: -100px; right: -50px;
      animation: float 6s ease-in-out infinite;
    }
    .hero::after {
      width: 200px; height: 200px;
      background: #ffd700;
      bottom: -50px; left: -30px;
      animation: float 8s ease-in-out infinite reverse;
    }
    @keyframes float {
      0%,100% { transform: translateY(0) rotate(0deg); }
      50% { transform: translateY(-20px) rotate(5deg); }
    }
    .hero h2 {
      font-size: 2.5rem;
      margin-bottom: 0.5rem;
      animation: fadeInUp 0.8s ease;
    }
    .hero p {
      font-size: 1.1rem;
      margin-bottom: 2rem;
      animation: fadeInUp 0.8s ease 0.2s both;
    }
    @keyframes fadeInUp {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    .cta-buttons {
      display: flex;
      gap: 1rem;
      justify-content: center;
      animation: fadeInUp 0.8s ease 0.4s both;
    }

    /* ── Buttons ── */
    .btn {
      display: inline-block;
      padding: 0.8rem 1.8rem;
      border-radius: 50px;
      text-decoration: none;
      font-weight: 600;
      border: none;
      cursor: pointer;
      font-size: 1rem;
      transition: all 0.3s ease;
      position: relative;
      overflow: hidden;
    }
    .btn-primary {
      background: #000000;
      color: #fff;
      box-shadow: 0 4px 15px rgba(255,215,0,0.4);
    }
    .btn-primary:hover {
      transform: translateY(-3px) scale(1.05);
      box-shadow: 0 8px 25px rgba(255,215,0,0.6);
    }
    .btn-secondary {
      background: green;
      color: #fff;
      border: 2px solid #fff;
    }
    .btn-secondary:hover {
      background: rgba(255,255,255,0.15);
      transform: translateY(-3px);
    }
    .btn-small {
      padding: 0.4rem 1rem;
      font-size: 0.85rem;
      background: linear-gradient(135deg, #667eea, #764ba2);
      color: #fff;
    }
    .btn-small:hover {
      transform: scale(1.05);
      box-shadow: 0 4px 12px rgba(102,126,234,0.4);
    }
    @keyframes ripple { to { transform: scale(4); opacity: 0; } }

    /* ── Item Grid ── */
    .recent-items {
      max-width: 1100px;
      margin: 3rem auto;
      padding: 0 1rem;
    }
    .recent-items h3 {
      font-size: 1.6rem;
      margin-bottom: 1rem;
      color: #000000;
    }
    .item-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
      gap: 1.5rem;
      margin-top: 1rem;
    }
    .item-card {
      background: #fff;
      border-radius: 16px;
      padding: 1.2rem;
      box-shadow: 0 4px 15px rgba(0,0,0,0.08);
      text-align: center;
      transition: all 0.3s ease;
      border: 2px solid transparent;
    }
    .item-card:hover {
      transform: translateY(-8px);
      box-shadow: 0 12px 30px rgba(102,126,234,0.2);
      border-color: #667eea;
    }
    .item-card img {
      width: 100%;
      height: 180px;
      object-fit: cover;
      border-radius: 10px;
      margin-bottom: 0.8rem;
      background: #e2e8f0;
    }
    .item-card h4 { margin: 0.5rem 0 0.2rem; color: #4a5568; }
    .item-card p { font-size: 0.9rem; color: #718096; }

    /* ── Footer ── */
    footer {
      text-align: center;
      padding: 2rem;
      color: #a0aec0;
      font-size: 0.9rem;
      background: #f7fafc;
    }
  </style>
</head>
<body>
  <header>
    <h1>E-Lost & Found ID</h1>
    <nav>
      <a href="index.html">Home</a>
      <a href="report-found.html">I Found an ID</a>
      <a href="search.html">Search</a>
    </nav>
  </header>

  <main>
    <section class="hero">
      <h2>Recover Your Lost ID</h2>
      <p>Found an ID card? Upload it here. Lost yours? Search to track it down.</p>
      <div class="cta-buttons">
        <a href="UploadlostIDbuttonsElostandfound codes.html" class="btn btn-primary">📤 I Found an ID</a>
        <a href="search.html" class="btn btn-secondary">🔎 I Lost My ID</a>
      </div>
    </section>

    <section class="recent-items">
      <h3>Recently Found</h3>
      <div class="item-grid" id="item-grid">
        <div class="item-card">
          <img src="../passport 1.png" alt="Found ID">
          <h4>Passport X</h4>
          <p>Found in Archives,Nairobi Oct 1, 2026</p>
          <a href="#" class="btn btn-small">View</a>
        </div>
        <div class="item-card">
          <img src="../Drivers.png" alt="Found ID">
          <h4>Driver's License x</h4>
          <p>Found at Odeon,Nairobi Sep 28, 2026</p>
          <a href="#" class="btn btn-small">View</a>
        </div>
        <div class="item-card">
          <img src="../id 1.png" alt="Found ID">
          <h4>National ID x </h4>
          <p>Found at Metro Station, Sep 25, 2026</p>
          <a href="#" class="btn btn-small">View</a>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <p>Built with the spirit of Harambee.</p>
    <p> © 2026 e-Lost/Found. All rights reserved.</p>
    
  </footer>

  <script>
    // Scroll-reveal animation
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.style.opacity = '1';
          entry.target.style.transform = 'translateY(0)';
        }
      });
    }, { threshold: 0.1 });

    document.querySelectorAll('.item-card').forEach(el => {
      el.style.opacity = '0';
      el.style.transform = 'translateY(20px)';
      el.style.transition = 'all 0.5s ease';
      observer.observe(el);
    });

    // Ripple effect on buttons
    document.querySelectorAll('.btn').forEach(btn => {
      btn.addEventListener('click', function(e) {
        const ripple = document.createElement('span');
        ripple.style.cssText = `
          position:absolute; border-radius:50%;
          background:rgba(255,255,255,0.5);
          width:100px; height:100px;
          transform:scale(0);
          animation:ripple 0.6s ease-out;
          pointer-events:none;
          left:${e.offsetX - 50}px;
          top:${e.offsetY - 50}px;
        `;
        this.appendChild(ripple);
        setTimeout(() => ripple.remove(), 600);
      });
    });
  </script>
</body>
</html>
