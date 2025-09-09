# ZhudyZihe.github.io

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Judy Jiang — Portfolio</title>
  <meta name="description" content="Personal website and portfolio of Judy Jiang." />
  <meta property="og:title" content="Judy Jiang — Portfolio" />
  <meta property="og:description" content="Personal website and portfolio of Judy Jiang." />
  <meta property="og:type" content="website" />
  <meta name="theme-color" content="#059669" />
  <style>
    :root {
      --bg: #06140f;           /* deep green-black */
      --panel: #0b241b;        /* card background */
      --soft: #123928;         /* soft panel */
      --text: #e6fff5;         /* near white with a mint tint */
      --muted: #bfe6d6;        /* muted text */
      --accent: #22c55e;       /* spring green */
      --accent-2: #16a34a;     /* darker accent */
      --ring: #34d399;         /* focus outlines */
      --border: #1a3a2a;       /* borders */
      --shadow: 0 10px 25px rgba(0,0,0,.35);
      --radius: 18px;
    }

    * { box-sizing: border-box; }
    html, body { height: 100%; }
    body {
      margin: 0;
      font: 16px/1.6 system-ui, -apple-system, Segoe UI, Roboto, Ubuntu, Cantarell, "Helvetica Neue", Arial;
      color: var(--text);
      background: radial-gradient(1200px 800px at 80% -10%, #0c2f22 0%, transparent 60%),
                  radial-gradient(1000px 600px at -10% 20%, #0e3b2a 0%, transparent 55%),
                  var(--bg);
      letter-spacing: .2px;
    }

    /* Layout */
    .container { width: min(1100px, 92vw); margin: 0 auto; }
    header { position: sticky; top: 0; z-index: 50; backdrop-filter: blur(10px); background: color-mix(in oklab, var(--bg) 70%, transparent); border-bottom: 1px solid var(--border); }
    .nav { display:flex; align-items:center; justify-content:space-between; padding: 14px 0; }
    .brand { display:flex; align-items:center; gap: .75rem; font-weight: 700; letter-spacing: .6px; }
    .logo { width: 32px; height: 32px; border-radius: 10px; background: linear-gradient(135deg, var(--accent), var(--accent-2)); box-shadow: inset 0 0 0 2px rgba(255,255,255,.08), var(--shadow); }
    .nav a { color: var(--muted); text-decoration: none; margin: 0 .75rem; padding:.35rem .55rem; border-radius: 8px; }
    .nav a:hover { color: var(--text); background: #0f2e22; }

    /* Hero */
    .hero { display:grid; grid-template-columns: 1.1fr .9fr; gap: 2rem; align-items:center; padding: 6rem 0 4rem; }
    .pill { display:inline-flex; align-items:center; gap:.5rem; background: #0e2a1f; border: 1px solid var(--border); color: var(--muted); border-radius: 999px; padding: .45rem .75rem; font-size: .9rem; }
    .spark { width: 8px; height: 8px; border-radius: 999px; background: var(--accent); box-shadow: 0 0 0 6px rgba(34,197,94,.12); }
    h1 { font-size: clamp(2rem, 4.8vw, 3.8rem); line-height: 1.12; margin: .6rem 0 1rem; letter-spacing:.4px; }
    .lead { color: var(--muted); font-size: clamp(1rem, 1.6vw, 1.25rem); }

    .cta { display:flex; gap: .8rem; margin-top: 1.4rem; flex-wrap: wrap; }
    .btn { border: 1px solid var(--border); background: linear-gradient(180deg, #0f2f23, #0b241b); color: var(--text); padding: .8rem 1rem; border-radius: 12px; text-decoration:none; font-weight:600; box-shadow: var(--shadow); }
    .btn:hover { border-color: #255d45; transform: translateY(-1px); }
    .btn.primary { background: linear-gradient(135deg, var(--accent), var(--accent-2)); color:#052011; border-color: transparent; }
    .btn.primary:hover { filter: brightness(1.05); }

    .hero-card { background: linear-gradient(180deg, var(--panel), #0b2018); border:1px solid var(--border); border-radius: var(--radius); padding: 1.25rem; box-shadow: var(--shadow); }
    .statgrid { display:grid; grid-template-columns: repeat(2,1fr); gap: .9rem; margin-top: .6rem; }
    .stat { background: linear-gradient(180deg, #0f2b21, #0b221a); border: 1px solid var(--border); border-radius: 14px; padding: .9rem; }
    .stat h3 { margin: 0 0 .25rem; font-size: .95rem; color: var(--muted); font-weight: 600; }
    .stat p { margin: 0; font-size: 1.25rem; font-weight: 800; }

    /* Sections */
    section { padding: 4rem 0; }
    .section-title { display:flex; align-items:center; gap:.6rem; margin-bottom: 1.6rem; }
    .section-title h2 { margin: 0; font-size: clamp(1.4rem, 2.2vw, 2rem); }
    .bar { flex:1; height: 1px; background: linear-gradient(90deg, var(--accent), transparent); opacity:.5; }

    .cards { display:grid; grid-template-columns: repeat(3, 1fr); gap: 1rem; }
    .card { background: linear-gradient(180deg, var(--panel), #0b2018); border:1px solid var(--border); border-radius: var(--radius); padding: 1.2rem; box-shadow: var(--shadow); display:flex; flex-direction:column; gap:.7rem; }
    .card h3 { margin: 0; font-size: 1.05rem; }
    .tagrow { display:flex; gap:.5rem; flex-wrap:wrap; }
    .tag { font-size:.8rem; padding:.25rem .5rem; border-radius: 999px; background:#0e2a1f; border:1px solid var(--border); color: var(--muted); }

    .about { display:grid; grid-template-columns: 1fr 1fr; gap: 1rem; }
    .about p { margin-top: 0; color: var(--muted); }

    /* Contact */
    form { display:grid; gap:.8rem; }
    input, textarea { width: 100%; background: #0f2b21; color: var(--text); border:1px solid var(--border); border-radius: 12px; padding: .85rem; outline: none; }
    input:focus, textarea:focus { border-color: var(--ring); box-shadow: 0 0 0 4px rgba(52,211,153,.1); }
    textarea { min-height: 140px; resize: vertical; }

    footer { border-top: 1px solid var(--border); padding: 2rem 0; color: var(--muted); }

    /* Responsive */
    @media (max-width: 900px) {
      .hero { grid-template-columns: 1fr; padding-top: 4.5rem; }
      .cards { grid-template-columns: 1fr 1fr; }
      .about { grid-template-columns: 1fr; }
    }
    @media (max-width: 640px) {
      .cards { grid-template-columns: 1fr; }
      .nav .links { display: none; }
    }
  </style>
</head>
<body>
  <header>
    <div class="container nav">
      <div class="brand"><div class="logo" aria-hidden="true"></div> <span>Judy Jiang</span></div>
      <nav class="links" aria-label="Primary Navigation">
        <a href="#about">About</a>
        <a href="#projects">Projects</a>
        <a href="#contact">Contact</a>
        <a class="btn" href="https://github.com/" target="_blank" rel="noopener">GitHub</a>
      </nav>
    </div>
  </header>

  <main class="container">
    <!-- Hero -->
    <section class="hero" id="home">
      <div>
        <span class="pill"><span class="spark"></span> Available for projects & internships</span>
        <h1>Hi, I’m <span style="color:var(--accent)">Judy</span> — I build useful things and tell stories with code.</h1>
        <p class="lead">I’m an environmental engineering student exploring AI, game design, and systems that make life better. Here’s a simple, green-themed site you can deploy to GitHub Pages.</p>
        <div class="cta">
          <a class="btn primary" href="#projects">See my work</a>
          <a class="btn" href="#contact">Get in touch</a>
          <a class="btn" href="resume.pdf" download>Download résumé</a>
        </div>
      </div>
      <aside class="hero-card" aria-label="Quick facts">
        <div class="statgrid">
          <div class="stat"><h3>Focus</h3><p>AI, Games, Env‑Sys</p></div>
          <div class="stat"><h3>Based</h3><p>Los Angeles, CA</p></div>
          <div class="stat"><h3>Tech</h3><p>C++ · Python · HTML</p></div>
          <div class="stat"><h3>Email</h3><p><a href="mailto:you@example.com" style="color:var(--text)">you@example.com</a></p></div>
        </div>
      </aside>
    </section>

    <!-- About -->
    <section id="about">
      <div class="section-title"><h2>About</h2><div class="bar"></div></div>
      <div class="about">
        <div class="card">
          <h3>Who I am</h3>
          <p>Curious builder who loves green tech, thoughtful design, and collaborative teams. I enjoy prototyping ideas fast, learning in public, and keeping systems simple and reliable.</p>
        </div>
        <div class="card">
          <h3>What I do</h3>
          <p>Recent projects include small game prototypes, environmental data visualizations, and workflow tools. I value clear communication, version control, and good documentation.</p>
        </div>
      </div>
    </section>

    <!-- Projects -->
    <section id="projects">
      <div class="section-title"><h2>Projects</h2><div class="bar"></div></div>
      <div class="cards">
        <article class="card">
          <h3>Green Guardian</h3>
          <p>A tiny dashboard that tracks air & water quality data and raises alerts.</p>
          <div class="tagrow">
            <span class="tag">Python</span>
            <span class="tag">Pandas</span>
            <span class="tag">Visualization</span>
          </div>
          <p><a class="btn" href="#" aria-label="Open Green Guardian project">View repo</a></p>
        </article>
        <article class="card">
          <h3>Rogue Roots</h3>
          <p>A roguelike gardening mini‑game about restoring ecosystems.</p>
          <div class="tagrow">
            <span class="tag">C++</span>
            <span class="tag">Game Design</span>
          </div>
          <p><a class="btn" href="#" aria-label="Open Rogue Roots project">View repo</a></p>
        </article>
        <article class="card">
          <h3>Micro Tools</h3>
          <p>A collection of tiny CLI utilities that automate repetitive tasks.</p>
          <div class="tagrow">
            <span class="tag">Shell</span>
            <span class="tag">Python</span>
          </div>
          <p><a class="btn" href="#" aria-label="Open Micro Tools project">View repo</a></p>
        </article>
      </div>
    </section>

    <!-- Contact -->
    <section id="contact">
      <div class="section-title"><h2>Contact</h2><div class="bar"></div></div>
      <div class="card">
        <form onsubmit="event.preventDefault();window.location.href='mailto:you@example.com?subject=' + encodeURIComponent(document.getElementById('subject').value) + '&body=' + encodeURIComponent(document.getElementById('message').value);">
          <label>
            <span>Subject</span>
            <input id="subject" required placeholder="Say hello" />
          </label>
          <label>
            <span>Message</span>
            <textarea id="message" required placeholder="Write your message here..."></textarea>
          </label>
          <div class="cta">
            <button class="btn primary" type="submit">Send email</button>
            <a class="btn" href="mailto:you@example.com">Or email me directly</a>
          </div>
        </form>
      </div>
    </section>
  </main>

  <footer>
    <div class="container">
      <div style="display:flex; justify-content:space-between; gap:1rem; flex-wrap:wrap; align-items:center;">
        <small>© <span id="year"></span> Judy Jiang. Built with ❤️ and lots of green.</small>
        <div style="display:flex; gap:.8rem;">
          <a class="btn" href="https://github.com/" target="_blank" rel="noopener">GitHub</a>
          <a class="btn" href="https://www.linkedin.com/" target="_blank" rel="noopener">LinkedIn</a>
        </div>
      </div>
    </div>
  </footer>

  <script>
    document.getElementById('year').textContent = new Date().getFullYear();
  </script>
</body>
</html>
