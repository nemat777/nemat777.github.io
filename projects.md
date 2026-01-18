<!-- projects.html -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Projects | Kian Nematollahi</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">

  <style>
    :root {
      --bg: #0f172a;
      --bg-alt: #020617;
      --card: #020617;
      --accent: #38bdf8;
      --accent-soft: rgba(56, 189, 248, 0.1);
      --text-main: #e5e7eb;
      --text-muted: #9ca3af;
      --border-subtle: #1f2937;
      --radius-lg: 12px;
      --radius-xl: 18px;
      --shadow-soft: 0 18px 40px rgba(15, 23, 42, 0.7);
    }

    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      background: radial-gradient(circle at top, #1e293b, #020617 55%);
      color: var(--text-main);
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }

    a {
      color: var(--accent);
      text-decoration: none;
    }

    a:hover {
      text-decoration: underline;
    }

    header {
      border-bottom: 1px solid var(--border-subtle);
      background: rgba(2, 6, 23, 0.9);
      backdrop-filter: blur(16px);
      position: sticky;
      top: 0;
      z-index: 10;
    }

    .nav {
      max-width: 960px;
      margin: 0 auto;
      padding: 14px 16px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 16px;
    }

    .nav-left {
      display: flex;
      align-items: center;
      gap: 8px;
      font-weight: 600;
      letter-spacing: 0.03em;
      text-transform: uppercase;
      font-size: 13px;
    }

    .nav-dot {
      width: 8px;
      height: 8px;
      border-radius: 999px;
      background: radial-gradient(circle at 30% 20%, #f97316, #ef4444);
      box-shadow: 0 0 16px rgba(248, 113, 113, 0.8);
    }

    .nav-links {
      display: flex;
      gap: 18px;
      align-items: center;
      font-size: 14px;
    }

    .nav-link {
      color: var(--text-muted);
    }

    .nav-link.active {
      color: var(--accent);
      font-weight: 500;
      position: relative;
    }

    .nav-link.active::after {
      content: "";
      position: absolute;
      left: 0;
      right: 0;
      bottom: -4px;
      height: 2px;
      border-radius: 999px;
      background: linear-gradient(to right, #22c55e, #38bdf8);
    }

    .nav-cta {
      padding: 6px 12px;
      border-radius: 999px;
      border: 1px solid rgba(148, 163, 184, 0.4);
      color: var(--text-main);
      font-size: 13px;
      display: flex;
      align-items: center;
      gap: 6px;
      background: radial-gradient(circle at top left, rgba(52, 211, 153, 0.12), transparent 55%);
    }

    .nav-cta span {
      font-size: 11px;
      text-transform: uppercase;
      letter-spacing: 0.12em;
      color: #a5b4fc;
    }

    main {
      flex: 1;
    }

    .page {
      max-width: 960px;
      margin: 24px auto 40px;
      padding: 0 16px 40px;
    }

    .page-header {
      margin-bottom: 28px;
      display: flex;
      flex-direction: column;
      gap: 8px;
    }

    .page-kicker {
      font-size: 12px;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      color: var(--accent);
      font-weight: 600;
    }

    .page-title {
      font-size: clamp(28px, 4vw, 32px);
      letter-spacing: -0.03em;
      font-weight: 650;
    }

    .page-subtitle {
      font-size: 14px;
      color: var(--text-muted);
      max-width: 520px;
    }

    .projects-grid {
      display: grid;
      grid-template-columns: minmax(0, 1fr);
      gap: 18px;
    }

    @media (min-width: 768px) {
      .projects-grid {
        grid-template-columns: minmax(0, 1fr) minmax(0, 1fr);
      }
    }

    .project-card {
      border-radius: var(--radius-xl);
      padding: 18px 18px 16px;
      background: radial-gradient(circle at top
