<!-- index.html -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Your Name | Developer</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <style>
    :root {
      --bg: #0a192f;
      --bg-alt: #112240;
      --accent: #64ffda;
      --text: #ccd6f6;
      --muted: #8892b0;
      --border: #233554;
      --mono: "SF Mono", Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;
      --sans: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu, Cantarell,
        "Open Sans", "Helvetica Neue", sans-serif;
      --transition-fast: 0.2s ease;
      --max-width: 1000px;
    }

    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      padding: 0;
      background-color: var(--bg);
      color: var(--text);
      font-family: var(--sans);
      line-height: 1.6;
    }

    a {
      color: var(--accent);
      text-decoration: none;
      transition: color var(--transition-fast), transform var(--transition-fast);
    }

    a:hover {
      color: #bfffea;
      transform: translateY(-1px);
    }

    main {
      max-width: var(--max-width);
      margin: 0 auto;
      padding: 2rem 1.5rem 4rem;
    }

    header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding-top: 1rem;
      padding-bottom: 1rem;
    }

    .logo {
      font-family: var(--mono);
      font-size: 1rem;
      color: var(--accent);
    }

    nav a {
      font-family: var(--mono);
      font-size: 0.8rem;
      margin-left: 1.25rem;
      color: var(--muted);
    }

    nav a span {
      color: var(--accent);
      margin-right: 0.25rem;
    }

    nav a:hover {
      color: var(--accent);
    }

    section {
      padding: 4rem 0;
    }

    .section-title {
      display: flex;
      align-items: center;
      font-size: 1.1rem;
      margin-bottom: 2rem;
      color: var(--text);
      white-space: nowrap;
    }

    .section-title span {
      font-family: var(--mono);
      color: var(--accent);
      font-size: 0.9rem;
      margin-right: 0.5rem;
    }

    .section-title::after {
      content: "";
      display: block;
      height: 1px;
      background-color: var(--border);
      margin-left: 1rem;
      flex: 1;
    }

    /* Hero */

    .hero {
      padding-top: 6rem;
      padding-bottom: 6rem;
    }

    .hero-subtitle {
      font-family: var(--mono);
      color: var(--accent);
      font-size: 0.9rem;
      margin-bottom: 1rem;
    }

    .hero-title {
      font-size: clamp(2.5rem, 6vw, 3.5rem);
      font-weight: 700;
      margin: 0 0 0.5rem;
    }

    .hero-tagline {
      font-size: clamp(1.8rem, 4vw, 2.3rem);
      color: var(--muted);
      margin: 0 0 1.5rem;
    }

    .hero-body {
      max-width: 550px;
      color: var(--muted);
      margin-bottom: 2rem;
    }

    .hero-cta {
      display: inline-block;
      padding: 0.85rem 
