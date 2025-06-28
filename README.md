<!DOCTYPE html>
<html lang="en" data-theme>
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Taka Ae | Web Developer</title>

  <!-- Minimal reset -->
  <link rel="stylesheet" href="https://unpkg.com/modern-css-reset/dist/reset.min.css" />

  <!-- ----------  Theme Styles ---------- -->
  <style>
    :root {
      --bg-light: #ffffff;
      --text-light: #1f2937;
      --bg-dark: #0f172a;
      --text-dark: #f1f5f9;
      --accent: #f97316;
      --card: rgba(0,0,0,0.05);
    }

    /* Light & dark palettes */
    html[data-theme="light"] {
      background: var(--bg-light);
      color: var(--text-light);
    }
    html[data-theme="dark"] {
      background: var(--bg-dark);
      color: var(--text-dark);
    }

    /* Page defaults */
    body {
      font-family: "Segoe UI", system-ui, sans-serif;
      max-width: 820px;
      margin: auto;
      padding: 2rem 1rem 4rem;
      line-height: 1.6;
      transition: background 0.3s, color 0.3s;
    }

    h1, h2 {
      margin: 1.2rem 0 0.6rem;
      font-weight: 600;
    }
    h1 { font-size: 2.5rem; color: var(--accent); }
    h2 { font-size: 1.5rem; }

    /* Badges */
    .badge {
      display: inline-block;
      margin: 3px 4px;
      padding: 6px 12px;
      font-size: 0.8rem;
      border-radius: 6px;
      background: var(--accent);
      color: #fff;
    }

    /* Theme toggle button */
    .theme-toggle {
      position: fixed;
      top: 1rem;
      right: 1rem;
      padding: 0.45rem 0.9rem;
      border-radius: 6px;
      border: 1px solid currentColor;
      background: none;
      font-size: 0.9rem;
      cursor: pointer;
      user-select: none;
    }
  </style>
</head>
<body>
  <!-- Manual theme switch -->
  <button class="theme-toggle" onclick="toggleTheme()">🌓 Theme</button>

  <!-- ----------  Header with typing animation ---------- -->
  <h1 align="center">
    <img
      src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=24&pause=1000&color=F97316&center=true&vCenter=true&width=550&lines=Hi%2C+I'm+Taka+Ae;Web+Developer+from+Indonesia;CodeIgniter+%7C+PHP+%7C+Tailwind+%7C+MySQL"
      alt="Typing introduction"
    />
  </h1>

  <p align="center">
    I build modern web apps with clean architecture—mainly CodeIgniter 4, PHP, MySQL, and Tailwind.  
    Passionate about secure REST APIs and elegant UI.
  </p>

  <!-- ---------- Tech Stack ---------- -->
  <h2>🛠 Tech Stack</h2>
  <span class="badge">PHP</span>
  <span class="badge">CodeIgniter 4</span>
  <span class="badge">MySQL</span>
  <span class="badge">Tailwind CSS</span>

  <!-- ---------- Contact ---------- -->
  <h2>📬 Contact</h2>
  <p>Email: <a href="mailto:youremail@example.com">youremail@example.com</a></p>
  <p>LinkedIn: <a href="https://linkedin.com/in/yourprofile">yourprofile</a></p>

  <!-- ---------- GitHub Contribution Graph ---------- -->
  <h2>📊 GitHub Contribution Graph</h2>
  <p align="center">
    <img
      src="https://github-readme-activity-graph.vercel.app/graph?username=taka-ae&theme=github-compact&area=true&hide_border=true"
      alt="Contribution graph"
      loading="lazy"
    />
  </p>

  <!-- ----------  Theme Logic ---------- -->
  <script>
    const root = document.documentElement;
    const storedTheme = localStorage.getItem("taka-theme");
    const mediaPrefersDark = window.matchMedia("(prefers-color-scheme: dark)").matches;
    // Apply stored or system theme on load
    root.setAttribute("data-theme", storedTheme || (mediaPrefersDark ? "dark" : "light"));

    function toggleTheme() {
      const current = root.getAttribute("data-theme");
      const next = current === "dark" ? "light" : "dark";
      root.setAttribute("data-theme", next);
      localStorage.setItem("taka-theme", next); // persist preference
    }
  </script>
</body>
</html>
