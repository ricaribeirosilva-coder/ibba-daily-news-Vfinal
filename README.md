# ibba-daily-news-Vfinal
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>IBBA Financial Daily Journal</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,600;9..144,700&family=IBM+Plex+Mono:wght@400;500;600&family=Manrope:wght@400;500;600;700;800&display=swap" rel="stylesheet">

  <style>
    :root {
      --bg: #071019;
      --bg-deep: #03080d;
      --surface: rgba(12, 19, 29, 0.92);
      --surface-strong: rgba(16, 24, 36, 0.98);
      --surface-soft: rgba(20, 29, 42, 0.98);
      --card: rgba(14, 22, 33, 0.98);
      --card-2: rgba(17, 26, 39, 0.98);
      --card-hover: rgba(21, 31, 45, 0.98);
      --border: rgba(255, 255, 255, 0.08);
      --border-strong: rgba(255, 255, 255, 0.12);
      --text: #eef5fb;
      --text-soft: #cad5e0;
      --text-muted: #95a3b2;
      --text-faint: #6d7b8e;
      --brand: #ec7000;
      --brand-strong: #ff9d49;
      --brand-soft: rgba(236, 112, 0, 0.12);
      --success: #4ade80;
      --shadow-xl: 0 28px 80px rgba(0, 0, 0, 0.3);
      --shadow-lg: 0 18px 44px rgba(0, 0, 0, 0.22);
      --shadow-md: 0 10px 26px rgba(0, 0, 0, 0.16);
      --radius-2xl: 28px;
      --radius-xl: 22px;
      --radius-lg: 18px;
      --radius-md: 14px;
      --radius-sm: 10px;
      --max-width: 1380px;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      color-scheme: dark;
      scroll-behavior: smooth;
    }

    body {
      min-height: 100vh;
      font-family: "Manrope", sans-serif;
      color: var(--text);
      line-height: 1.6;
      background:
        radial-gradient(circle at top left, rgba(236, 112, 0, 0.14), transparent 22%),
        radial-gradient(circle at top right, rgba(255, 157, 73, 0.08), transparent 16%),
        linear-gradient(180deg, #08111a 0%, var(--bg) 50%, var(--bg-deep) 100%);
      overflow-x: hidden;
      position: relative;
    }

    body::before {
      content: "";
      position: fixed;
      inset: 0;
      pointer-events: none;
      background:
        linear-gradient(rgba(255,255,255,0.02) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,255,255,0.02) 1px, transparent 1px);
      background-size: 48px 48px;
      mask-image: radial-gradient(circle at center, black 36%, transparent 82%);
      opacity: 0.16;
    }

    body::after {
      content: "";
      position: fixed;
      right: -140px;
      bottom: -160px;
      width: 480px;
      height: 480px;
      border-radius: 999px;
      background: radial-gradient(circle, rgba(236, 112, 0, 0.12), transparent 66%);
      filter: blur(24px);
      pointer-events: none;
    }

    a,
    button,
    input {
      font: inherit;
      -webkit-tap-highlight-color: transparent;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    button {
      background: none;
      border: none;
      cursor: pointer;
    }

    a:focus-visible,
    button:focus-visible,
    input:focus-visible {
      outline: 2px solid rgba(255, 157, 73, 0.85);
      outline-offset: 2px;
    }

    .page-shell {
      max-width: var(--max-width);
      margin: 0 auto;
      padding: 28px 20px 42px;
      position: relative;
      z-index: 1;
    }

    .hero {
      position: relative;
      overflow: hidden;
      padding: 28px;
      border: 1px solid var(--border);
      border-radius: var(--radius-2xl);
      background:
        linear-gradient(135deg, rgba(236, 112, 0, 0.07), transparent 24%),
        linear-gradient(180deg, rgba(17, 26, 40, 0.96), rgba(9, 15, 24, 0.98));
      box-shadow: var(--shadow-xl);
      backdrop-filter: blur(14px);
    }

    .hero::before {
      content: "";
      position: absolute;
      inset: 0;
      background:
        radial-gradient(circle at 12% 16%, rgba(255, 157, 73, 0.14), transparent 18%),
        radial-gradient(circle at 90% 10%, rgba(255, 255, 255, 0.04), transparent 16%);
      pointer-events: none;
    }

    .hero-grid {
      position: relative;
      z-index: 1;
      display: grid;
      grid-template-columns: minmax(0, 1.45fr) minmax(320px, 0.78fr);
      gap: 22px;
      align-items: start;
    }

    .brand-block {
      display: flex;
      gap: 16px;
      align-items: flex-start;
      min-width: 0;
    }

    .brand-mark {
      width: 56px;
      height: 56px;
      border-radius: 18px;
      flex-shrink: 0;
      display: flex;
      align-items: center;
      justify-content: center;
      background: linear-gradient(135deg, var(--brand-strong), #ca5e00);
      box-shadow:
        inset 0 1px 0 rgba(255,255,255,0.24),
        0 14px 30px rgba(236, 112, 0, 0.24);
      color: #fff;
      font-size: 0.8rem;
      font-weight: 800;
      letter-spacing: 0.08em;
    }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      color: var(--text-muted);
      font-size: 0.72rem;
      font-weight: 800;
      text-transform: uppercase;
      letter-spacing: 0.16em;
    }

    .eyebrow::before {
      content: "";
      width: 8px;
      height: 8px;
      border-radius: 999px;
      background: linear-gradient(135deg, var(--brand), var(--brand-strong));
      box-shadow: 0 0 16px rgba(236, 112, 0, 0.4);
    }

    .hero-title {
      margin-top: 8px;
      font-family: "Fraunces", serif;
      font-size: clamp(1.9rem, 4vw, 3.35rem);
      line-height: 0.96;
      font-weight: 700;
      letter-spacing: -0.05em;
      max-width: 760px;
    }

    .hero-subtitle {
      margin-top: 16px;
      max-width: 660px;
      color: var(--text-muted);
      font-size: 1rem;
      line-height: 1.85;
    }

    .hero-inline {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-top: 20px;
    }

    .hero-chip {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      min-height: 36px;
      padding: 0 12px;
      border-radius: 999px;
      border: 1px solid var(--border);
      background: rgba(255, 255, 255, 0.03);
      color: var(--text-soft);
      font-size: 0.76rem;
      font-weight: 800;
      letter-spacing: 0.05em;
      text-transform: uppercase;
    }

    .hero-chip strong {
      color: #fff;
      font-weight: 800;
    }

    .control-card {
      position: relative;
      z-index: 1;
      padding: 18px;
      border: 1px solid var(--border);
      border-radius: var(--radius-xl);
      background: rgba(255, 255, 255, 0.035);
      box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.03);
    }

    .control-label {
      color: var(--text-faint);
      font-size: 0.72rem;
      font-weight: 800;
      letter-spacing: 0.14em;
      text-transform: uppercase;
    }

    .control-date {
      margin-top: 8px;
      font-family: "Fraunces", serif;
      color: var(--text);
      font-size: 1.18rem;
      line-height: 1.25;
      font-weight: 600;
      letter-spacing: -0.03em;
    }

    .control-sub {
      margin-top: 8px;
      color: var(--text-muted);
      font-size: 0.84rem;
      line-height: 1.6;
    }

    .date-nav {
      display: grid;
      grid-template-columns: 44px minmax(0, 1fr) 44px;
      gap: 8px;
      margin-top: 16px;
    }

    .date-btn,
    .date-input {
      height: 44px;
      border: 1px solid var(--border);
      border-radius: 14px;
      background: rgba(255, 255, 255, 0.03);
      color: var(--text-soft);
      transition: border-color 0.18s ease, background 0.18s ease, color 0.18s ease, transform 0.18s ease;
    }

    .date-btn:hover,
    .date-input:hover {
      border-color: rgba(255, 157, 73, 0.22);
      background: rgba(236, 112, 0, 0.08);
      color: #fff;
    }

    .date-btn {
      font-size: 1rem;
      font-weight: 800;
    }

    .date-btn:active {
      transform: translateY(1px);
    }

    .date-input {
      width: 100%;
      padding: 0 12px;
      font-size: 0.86rem;
    }

    .date-input::-webkit-calendar-picker-indicator {
      filter: invert(0.75);
      cursor: pointer;
    }

    .control-foot {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 12px;
      margin-top: 14px;
      padding-top: 14px;
      border-top: 1px solid rgba(255, 255, 255, 0.05);
    }

    .edition-code {
      color: var(--text-faint);
      font-size: 0.75rem;
      font-family: "IBM Plex Mono", monospace;
    }

    .status-dot {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      color: var(--text-soft);
      font-size: 0.75rem;
      font-weight: 700;
    }

    .status-dot::before {
      content: "";
      width: 8px;
      height: 8px;
      border-radius: 999px;
      background: var(--success);
      box-shadow: 0 0 12px rgba(74, 222, 128, 0.45);
    }

    .metrics-grid {
      position: relative;
      z-index: 1;
      display: grid;
      grid-template-columns: repeat(4, minmax(0, 1fr));
      gap: 12px;
      margin-top: 22px;
    }

    .metric-card {
      padding: 15px 16px;
      border: 1px solid var(--border);
      border-radius: 18px;
      background: rgba(255, 255, 255, 0.03);
      box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.025);
      transition: transform 0.18s ease, border-color 0.18s ease, background 0.18s ease;
    }

    .metric-card:hover {
      transform: translateY(-1px);
      border-color: rgba(255, 157, 73, 0.16);
      background: rgba(255, 255, 255, 0.038);
    }

    .metric-label {
      color: var(--text-faint);
      font-size: 0.7rem;
      font-weight: 800;
      letter-spacing: 0.14em;
      text-transform: uppercase;
    }

    .metric-value {
      margin-top: 10px;
      color: var(--text);
      font-size: 1.44rem;
      line-height: 1;
      font-weight: 800;
      letter-spacing: -0.05em;
    }

    .metric-foot {
      margin-top: 8px;
      color: var(--text-muted);
      font-size: 0.8rem;
    }

    .state-panel {
      margin-top: 22px;
      padding: 24px;
      border: 1px solid var(--border);
      border-radius: var(--radius-xl);
      background: linear-gradient(180deg, rgba(14, 22, 34, 0.96), rgba(9, 15, 24, 0.98));
      box-shadow: var(--shadow-lg);
    }

    .state-panel.loading,
    .state-panel.empty {
      min-height: 180px;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 12px;
      text-align: center;
      color: var(--text-muted);
      font-size: 0.96rem;
    }

    .spinner {
      width: 22px;
      height: 22px;
      border-radius: 999px;
      border: 2px solid rgba(255,255,255,0.08);
      border-top-color: var(--brand);
      animation: spin 0.8s linear infinite;
      flex-shrink: 0;
    }

    @keyframes spin {
      to { transform: rotate(360deg); }
    }

    .journal {
      display: none;
      margin-top: 22px;
      gap: 22px;
    }

    .section-head {
      display: flex;
      justify-content: space-between;
      align-items: flex-end;
      gap: 14px;
      margin-bottom: 16px;
    }

    .section-kicker {
      color: var(--text-faint);
      font-size: 0.7rem;
      font-weight: 800;
      letter-spacing: 0.16em;
      text-transform: uppercase;
    }

    .section-title {
      margin-top: 6px;
      font-family: "Fraunces", serif;
      font-size: 1.58rem;
      line-height: 1;
      font-weight: 600;
      letter-spacing: -0.04em;
      color: var(--text);
    }

    .section-note {
      margin-top: 8px;
      color: var(--text-muted);
      font-size: 0.9rem;
    }

    .section-chip {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      min-width: 40px;
      height: 34px;
      padding: 0 12px;
      border-radius: 999px;
      border: 1px solid rgba(236, 112, 0, 0.18);
      background: rgba(236, 112, 0, 0.1);
      color: var(--brand-strong);
      font-size: 0.82rem;
      font-weight: 800;
    }

    .lead-section {
      border: 1px solid var(--border);
      border-radius: var(--radius-xl);
      background: linear-gradient(180deg, rgba(14, 22, 34, 0.96), rgba(9, 15, 24, 0.98));
      box-shadow: var(--shadow-lg);
      overflow: hidden;
      padding: 22px;
    }

    .lead-grid {
      display: grid;
      grid-template-columns: minmax(0, 1.45fr) minmax(0, 0.95fr);
      gap: 16px;
    }

    .lead-main {
      position: relative;
      overflow: hidden;
      min-height: 460px;
      padding: 24px;
      border: 1px solid var(--border);
      border-radius: var(--radius-xl);
      background:
        linear-gradient(180deg, rgba(22, 33, 48, 0.98), rgba(11, 18, 28, 0.98));
      box-shadow: var(--shadow-md);
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }

    .lead-main::before,
    .lead-side-card::before {
      content: "";
      position: absolute;
      inset: 0 auto 0 0;
      width: 4px;
      background: linear-gradient(180deg, var(--brand-strong), rgba(236, 112, 0, 0.12));
    }

    .lead-main::after {
      content: "";
      position: absolute;
      right: -40px;
      bottom: -80px;
      width: 220px;
      height: 220px;
      border-radius: 999px;
      background: radial-gradient(circle, rgba(236, 112, 0, 0.12), transparent 68%);
      pointer-events: none;
    }

    .lead-side {
      display: grid;
      gap: 16px;
    }

    .lead-side-card {
      position: relative;
      overflow: hidden;
      min-height: 222px;
      padding: 20px;
      border: 1px solid var(--border);
      border-radius: 18px;
      background: linear-gradient(180deg, rgba(18, 27, 40, 0.98), rgba(10, 16, 25, 0.98));
      box-shadow: var(--shadow-md);
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }

    .lead-tag {
      position: relative;
      z-index: 1;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      color: var(--text-soft);
      font-size: 0.72rem;
      font-weight: 800;
      letter-spacing: 0.12em;
      text-transform: uppercase;
    }

    .lead-tag::before {
      content: "";
      width: 8px;
      height: 8px;
      border-radius: 999px;
      background: var(--brand-strong);
      box-shadow: 0 0 14px rgba(236, 112, 0, 0.36);
    }

    .lead-main .lead-title {
      margin-top: 16px;
      max-width: 82%;
      font-family: "Fraunces", serif;
      font-size: clamp(1.72rem, 2.4vw, 2.4rem);
      line-height: 1.05;
      font-weight: 700;
      letter-spacing: -0.04em;
    }

    .lead-side-card .lead-title {
      margin-top: 14px;
      max-width: 92%;
      font-family: "Fraunces", serif;
      font-size: 1.18rem;
      line-height: 1.24;
      font-weight: 600;
      letter-spacing: -0.03em;
    }

    .lead-summary {
      margin-top: 14px;
      color: var(--text-muted);
      font-size: 0.95rem;
      line-height: 1.82;
      max-width: 86%;
    }

    .lead-side-card .lead-summary {
      font-size: 0.88rem;
      max-width: 96%;
    }

    .lead-foot {
      margin-top: 22px;
      display: flex;
      justify-content: space-between;
      align-items: flex-end;
      gap: 14px;
    }

    .lead-meta {
      color: var(--text-faint);
      font-size: 0.78rem;
      font-weight: 600;
    }

    .lead-cta {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      min-height: 40px;
      padding: 0 14px;
      border-radius: 12px;
      border: 1px solid rgba(236, 112, 0, 0.18);
      background: rgba(236, 112, 0, 0.08);
      color: #ffba79;
      font-size: 0.8rem;
      font-weight: 800;
      letter-spacing: 0.02em;
      transition: background 0.18s ease, border-color 0.18s ease, color 0.18s ease, transform 0.18s ease;
      white-space: nowrap;
    }

    .lead-cta:hover {
      transform: translateY(-1px);
      background: rgba(236, 112, 0, 0.14);
      border-color: rgba(255, 157, 73, 0.22);
      color: #ffd1a2;
    }

    .desk-grid {
      display: grid;
      grid-template-columns: minmax(0, 1fr) minmax(0, 1fr);
      gap: 22px;
    }

    .panel {
      border: 1px solid var(--border);
      border-radius: var(--radius-xl);
      background: linear-gradient(180deg, rgba(14, 22, 34, 0.96), rgba(9, 15, 24, 0.98));
      box-shadow: var(--shadow-lg);
      overflow: hidden;
    }

    .panel-head {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      gap: 16px;
      padding: 22px 22px 0;
    }

    .panel-title {
      margin-top: 6px;
      font-family: "Fraunces", serif;
      font-size: 1.38rem;
      line-height: 1;
      font-weight: 600;
      letter-spacing: -0.04em;
    }

    .panel-subtitle {
      margin-top: 8px;
      color: var(--text-muted);
      font-size: 0.9rem;
    }

    .stories {
      display: grid;
      gap: 14px;
      padding: 18px 22px 22px;
    }

    .story-card {
      position: relative;
      padding: 18px;
      border: 1px solid var(--border);
      border-radius: 18px;
      background: linear-gradient(180deg, var(--card), rgba(10, 16, 25, 0.98));
      transition: transform 0.18s ease, border-color 0.18s ease, background 0.18s ease, box-shadow 0.18s ease;
    }

    .story-card:hover {
      transform: translateY(-2px);
      border-color: rgba(255, 157, 73, 0.18);
      background: linear-gradient(180deg, var(--card-hover), rgba(10, 16, 25, 0.98));
      box-shadow: var(--shadow-md);
    }

    .story-topline {
      display: flex;
      align-items: center;
      gap: 10px;
      color: var(--text-faint);
      font-size: 0.7rem;
      font-weight: 800;
      letter-spacing: 0.12em;
      text-transform: uppercase;
    }

    .story-topline::before {
      content: "";
      width: 7px;
      height: 7px;
      border-radius: 999px;
      background: rgba(255, 157, 73, 0.9);
      box-shadow: 0 0 10px rgba(236, 112, 0, 0.34);
    }

    .story-head {
      margin-top: 12px;
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      gap: 14px;
    }

    .story-main {
      min-width: 0;
      flex: 1;
    }

    .story-title {
      font-size: 1rem;
      line-height: 1.45;
      font-weight: 700;
      letter-spacing: -0.02em;
      color: var(--text);
    }

    .story-title a:hover {
      color: #fff;
    }

    .story-meta {
      margin-top: 8px;
      color: var(--text-muted);
      font-size: 0.8rem;
      font-weight: 600;
    }

    .tickers {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-top: 12px;
    }

    .ticker {
      display: inline-flex;
      align-items: center;
      min-height: 28px;
      padding: 0 10px;
      border-radius: 999px;
      border: 1px solid rgba(236, 112, 0, 0.16);
      background: rgba(236, 112, 0, 0.08);
      color: #ffb36b;
      font-size: 0.72rem;
      font-weight: 800;
      letter-spacing: 0.02em;
    }

    .story-actions {
      display: flex;
      align-items: center;
      gap: 8px;
      flex-shrink: 0;
      flex-wrap: wrap;
      justify-content: flex-end;
    }

    .story-link,
    .story-toggle {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      min-height: 38px;
      padding: 0 14px;
      border-radius: 12px;
      border: 1px solid var(--border);
      background: rgba(255, 255, 255, 0.03);
      color: var(--text-soft);
      font-size: 0.78rem;
      font-weight: 800;
      letter-spacing: 0.03em;
      transition: border-color 0.18s ease, background 0.18s ease, color 0.18s ease, transform 0.18s ease;
      white-space: nowrap;
    }

    .story-link:hover,
    .story-toggle:hover {
      border-color: rgba(255, 157, 73, 0.22);
      background: rgba(236, 112, 0, 0.08);
      color: #fff;
    }

    .story-link:hover {
      transform: translateY(-1px);
    }

    .story-toggle.is-open {
      background: rgba(236, 112, 0, 0.12);
      border-color: rgba(255, 157, 73, 0.22);
      color: #fff;
    }

    .summary {
      display: none;
      margin-top: 14px;
      padding: 14px 16px;
      border-radius: 14px;
      border: 1px solid rgba(255, 255, 255, 0.05);
      background: rgba(255, 255, 255, 0.03);
      color: var(--text-soft);
      font-size: 0.86rem;
      line-height: 1.82;
    }

    .summary.open {
      display: block;
    }

    .empty-card {
      padding: 20px;
      border: 1px dashed var(--border-strong);
      border-radius: 16px;
      background: rgba(255, 255, 255, 0.02);
      color: var(--text-muted);
      font-size: 0.88rem;
      text-align: center;
    }

    .toast {
      position: fixed;
      left: 50%;
      bottom: 24px;
      transform: translateX(-50%);
      padding: 12px 16px;
      border-radius: 14px;
      border: 1px solid rgba(255, 157, 73, 0.18);
      background: rgba(13, 20, 30, 0.96);
      color: var(--text);
      font-size: 0.82rem;
      font-weight: 700;
      box-shadow: var(--shadow-lg);
      opacity: 0;
      pointer-events: none;
      transition: opacity 0.22s ease, transform 0.22s ease;
      z-index: 100;
      max-width: calc(100vw - 28px);
      text-align: center;
    }

    .toast.show {
      opacity: 1;
      transform: translateX(-50%) translateY(-2px);
    }

    @media (max-width: 1140px) {
      .metrics-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }

      .desk-grid {
        grid-template-columns: 1fr;
      }
    }

    @media (max-width: 980px) {
      .hero-grid {
        grid-template-columns: 1fr;
      }

      .lead-grid {
        grid-template-columns: 1fr;
      }

      .lead-main {
        min-height: 360px;
      }
    }

    @media (max-width: 720px) {
      .page-shell {
        padding: 16px 12px 28px;
      }

      .hero,
      .panel,
      .lead-section,
      .state-panel {
        border-radius: 22px;
      }

      .hero {
        padding: 18px;
      }

      .brand-block {
        flex-direction: column;
      }

      .metrics-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }

      .panel-head,
      .stories,
      .lead-section {
        padding-left: 18px;
        padding-right: 18px;
      }

      .story-head {
        flex-direction: column;
      }

      .story-actions {
        width: 100%;
        justify-content: flex-start;
      }
    }

    @media (max-width: 520px) {
      .metrics-grid {
        grid-template-columns: 1fr;
      }

      .date-nav {
        grid-template-columns: 40px minmax(0, 1fr) 40px;
      }

      .brand-mark {
        width: 48px;
        height: 48px;
        border-radius: 14px;
      }

      .hero-title {
        font-size: 2rem;
      }

      .lead-main .lead-title,
      .lead-side-card .lead-title {
        max-width: 100%;
      }

      .lead-summary {
        max-width: 100%;
      }
    }
  </style>
</head>
<body>
  <div class="page-shell">
    <header class="hero">
      <div class="hero-grid">
        <div class="brand-block">
          <div class="brand-mark">IBBA</div>

          <div class="brand-copy">
            <div class="eyebrow">Equity Research · Financials</div>
            <h1 class="hero-title">Financial Daily Journal</h1>
            <p class="hero-subtitle">
              Um front mais silencioso, mais editorial e mais premium para o desk de Financials, priorizando leitura rápida, clareza visual e sensação de produto institucional.
            </p>

            <div class="hero-inline">
              <div class="hero-chip">Desk <strong>Brazil + Global</strong></div>
              <div class="hero-chip">Formato <strong>Morning Journal</strong></div>
              <div class="hero-chip">Visual <strong>Research Desk Premium</strong></div>
            </div>
          </div>
        </div>

        <aside class="control-card">
          <div class="control-label">Edition Date</div>
          <div class="control-date" id="editionDateLabel">Carregando data...</div>
          <div class="control-sub">Selecione a edição para navegar pelo journal diário.</div>

          <div class="date-nav">
            <button type="button" class="date-btn" onclick="changeDate(-1)" title="Dia anterior">&#9664;</button>
            <input type="date" class="date-input" id="datePicker" onchange="loadDate(this.value)">
            <button type="button" class="date-btn" onclick="changeDate(1)" title="Próximo dia">&#9654;</button>
          </div>

          <div class="control-foot">
            <span class="edition-code" id="editionCode">EDITION --</span>
            <div class="status-dot">Database online</div>
          </div>
        </aside>
      </div>

      <div class="metrics-grid">
        <div class="metric-card">
          <div class="metric-label">Total</div>
          <div class="metric-value" id="totalBadge">0</div>
          <div class="metric-foot">Notícias da edição</div>
        </div>

        <div class="metric-card">
          <div class="metric-label">Brasil</div>
          <div class="metric-value" id="brBadge">0</div>
          <div class="metric-foot">Cobertura doméstica</div>
        </div>

        <div class="metric-card">
          <div class="metric-label">Global</div>
          <div class="metric-value" id="glBadge">0</div>
          <div class="metric-foot">Fluxo internacional</div>
        </div>

        <div class="metric-card">
          <div class="metric-label">Edição</div>
          <div class="metric-value" id="editionShortBadge">--</div>
          <div class="metric-foot">Data de referência</div>
        </div>
      </div>
    </header>

    <div id="loadingState" class="state-panel loading">
      <span class="spinner"></span>
      <span>Carregando edição...</span>
    </div>

    <div id="emptyState" class="state-panel empty" style="display:none;">
      Nenhuma notícia disponível para esta data.
    </div>

    <main id="journalContent" class="journal">
      <section class="lead-section">
        <div class="section-head">
          <div>
            <div class="section-kicker">Morning Brief</div>
            <h2 class="section-title">Em destaque</h2>
            <p class="section-note">Os itens que deveriam abrir a leitura do time nesta edição.</p>
          </div>
          <span class="section-chip" id="leadCount">0</span>
        </div>

        <div class="lead-grid" id="leadGrid"></div>
      </section>

      <div class="desk-grid">
        <section class="panel">
          <div class="panel-head">
            <div>
              <div class="section-kicker">Brazil Desk</div>
              <h2 class="panel-title">Brasil</h2>
              <p class="panel-subtitle">O que mais importa no noticiário local da edição.</p>
            </div>
            <span class="section-chip" id="brCount">0</span>
          </div>
          <div class="stories" id="brCards"></div>
        </section>

        <section class="panel">
          <div class="panel-head">
            <div>
              <div class="section-kicker">Global Desk</div>
              <h2 class="panel-title">Global</h2>
              <p class="panel-subtitle">Leituras internacionais com impacto para o setor.</p>
            </div>
            <span class="section-chip" id="glCount">0</span>
          </div>
          <div class="stories" id="glCards"></div>
        </section>
      </div>
    </main>
  </div>

  <div class="toast" id="toast"></div>

<script>
var SUPABASE_URL = 'https://nrnxhmkoioalklxqrrpt.supabase.co';
var SUPABASE_KEY = 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6Im5ybnhobWtvaW9hbGtseHFycnB0Iiwicm9sZSI6ImFub24iLCJpYXQiOjE3NzU1NzMwOTQsImV4cCI6MjA5MTE0OTA5NH0.kdPEfa3i0lu2JiyfkYbTcvth47KtnnRMDUpS3rU9eBs';

var brItems = [];
var glItems = [];
var currentDate = '';

async function supaFetch(table, query) {
  var url = SUPABASE_URL + '/rest/v1/' + table + '?' + query;
  var resp = await fetch(url, {
    headers: {
      'apikey': SUPABASE_KEY,
      'Authorization': 'Bearer ' + SUPABASE_KEY,
      'Accept': 'application/json'
    }
  });

  if (!resp.ok) throw new Error('Supabase error: ' + resp.status);
  return resp.json();
}

function esc(value) {
  var div = document.createElement('div');
  div.textContent = value == null ? '' : value;
  return div.innerHTML;
}

function normalizeTickers(value) {
  if (Array.isArray(value)) return value.filter(Boolean);

  if (typeof value === 'string' && value.trim()) {
    var raw = value.trim();

    if (raw[0] === '[') {
      try {
        var parsed = JSON.parse(raw);
        return Array.isArray(parsed) ? parsed.filter(Boolean) : [];
      } catch (err) {}
    }

    return raw.split(/[;,|]/).map(function(item) {
      return item.trim();
    }).filter(Boolean);
  }

  return [];
}

function formatDateLabel(dateStr) {
  if (!dateStr) return 'Sem data';

  var date = /^\d{4}-\d{2}-\d{2}$/.test(dateStr)
    ? new Date(dateStr + 'T12:00:00')
    : new Date(dateStr);

  if (isNaN(date.getTime())) return dateStr;

  var weekdays = ['domingo', 'segunda-feira', 'terça-feira', 'quarta-feira', 'quinta-feira', 'sexta-feira', 'sábado'];
  var months = ['jan', 'fev', 'mar', 'abr', 'mai', 'jun', 'jul', 'ago', 'set', 'out', 'nov', 'dez'];

  return weekdays[date.getDay()] + ', ' + date.getDate() + ' ' + months[date.getMonth()] + ' ' + date.getFullYear();
}

function formatShortDate(dateStr) {
  if (!dateStr) return '--';

  var date = /^\d{4}-\d{2}-\d{2}$/.test(dateStr)
    ? new Date(dateStr + 'T12:00:00')
    : new Date(dateStr);

  if (isNaN(date.getTime())) return dateStr;

  return String(date.getDate()).padStart(2, '0') + '/' + String(date.getMonth() + 1).padStart(2, '0');
}

function excerpt(text, max) {
  if (!text) return '';
  return text.length > max ? text.slice(0, max).trim() + '...' : text;
}

function toast(msg) {
  var el = document.getElementById('toast');
  el.textContent = msg;
  el.classList.add('show');
  setTimeout(function() {
    el.classList.remove('show');
  }, 1800);
}

function emptyCard(message) {
  return '<div class="empty-card">' + esc(message) + '</div>';
}

function buildTickers(item) {
  var tickers = normalizeTickers(item.tickers);
  if (!tickers.length) return '';

  return '<div class="tickers">' + tickers.map(function(t) {
    return '<span class="ticker">' + esc(t) + '</span>';
  }).join('') + '</div>';
}

function summaryBlock(id, summary) {
  if (!summary) return '';
  return '<div class="summary" id="' + esc(id) + '">' + esc(summary) + '</div>';
}

function leadCard(entry, index) {
  if (!entry || !entry.item) {
    return index === 0
      ? '<article class="lead-main"><div><div class="lead-tag">Sem destaque</div><h3 class="lead-title">Nenhum item disponível nesta posição</h3><div class="lead-summary">Quando houver mais notícias na edição, o destaque principal aparecerá aqui automaticamente.</div></div><div class="lead-foot"><div class="lead-meta">Aguardando conteúdo</div></div></article>'
      : '<article class="lead-side-card"><div><div class="lead-tag">Sem destaque</div><h3 class="lead-title">Nenhum item disponível</h3><div class="lead-summary">As leituras secundárias da edição aparecem aqui.</div></div><div class="lead-foot"><div class="lead-meta">Aguardando conteúdo</div></div></article>';
  }

  var item = entry.item;
  var cardClass = index === 0 ? 'lead-main' : 'lead-side-card';
  var summaryLimit = index === 0 ? 320 : 180;

  return '<article class="' + cardClass + '">' +
    '<div>' +
      '<div class="lead-tag">' + esc(entry.label) + '</div>' +
      '<h3 class="lead-title"><a href="' + esc(item.url || '#') + '" target="_blank" rel="noopener">' + esc(item.headline || 'Sem headline') + '</a></h3>' +
      '<div class="lead-summary">' + esc(excerpt(item.summary || 'Sem resumo disponível para este item.', summaryLimit)) + '</div>' +
    '</div>' +
    '<div class="lead-foot">' +
      '<div class="lead-meta">' + esc(item.source || 'Fonte não informada') + ' &bull; ' + esc(formatDateLabel(item.pub_date || currentDate)) + '</div>' +
      '<a class="lead-cta" href="' + esc(item.url || '#') + '" target="_blank" rel="noopener">Abrir matéria</a>' +
    '</div>' +
  '</article>';
}

function storyCard(item, prefix, idx) {
  var id = prefix + '-' + idx;
  var hasSummary = !!item.summary;
  var summaryBtn = hasSummary
    ? '<button type="button" class="story-toggle" onclick="toggleSummary(\'' + id + '\', this)" aria-expanded="false"><span class="toggle-text">Resumo</span></button>'
    : '';

  return '<article class="story-card">' +
    '<div class="story-topline">Desk note</div>' +
    '<div class="story-head">' +
      '<div class="story-main">' +
        '<h3 class="story-title"><a href="' + esc(item.url || '#') + '" target="_blank" rel="noopener">' + esc(item.headline || 'Sem headline') + '</a></h3>' +
        '<div class="story-meta">' + esc(item.source || 'Fonte não informada') + ' &bull; ' + esc(formatDateLabel(item.pub_date || currentDate)) + '</div>' +
        buildTickers(item) +
      '</div>' +
      '<div class="story-actions">' +
        '<a class="story-link" href="' + esc(item.url || '#') + '" target="_blank" rel="noopener">Abrir</a>' +
        summaryBtn +
      '</div>' +
    '</div>' +
    summaryBlock(id, item.summary) +
  '</article>';
}

function renderLeadSection() {
  var leads = [];
  if (brItems[0]) leads.push({ label: 'Brasil em foco', item: brItems[0] });
  if (glItems[0]) leads.push({ label: 'Global em foco', item: glItems[0] });

  var pool = brItems.slice(1).concat(glItems.slice(1));
  while (leads.length < 3 && pool.length) {
    leads.push({ label: 'Leitura adicional', item: pool.shift() });
  }
  while (leads.length < 3) {
    leads.push(null);
  }

  document.getElementById('leadCount').textContent = leads.filter(Boolean).length;
  document.getElementById('leadGrid').innerHTML =
    leadCard(leads[0], 0) +
    '<div class="lead-side">' +
      leadCard(leads[1], 1) +
      leadCard(leads[2], 2) +
    '</div>';
}

function render() {
  var total = brItems.length + glItems.length;

  document.getElementById('editionDateLabel').textContent = formatDateLabel(currentDate);
  document.getElementById('editionCode').textContent = 'EDITION ' + currentDate;
  document.getElementById('editionShortBadge').textContent = formatShortDate(currentDate);

  document.getElementById('totalBadge').textContent = total;
  document.getElementById('brBadge').textContent = brItems.length;
  document.getElementById('glBadge').textContent = glItems.length;
  document.getElementById('brCount').textContent = brItems.length;
  document.getElementById('glCount').textContent = glItems.length;

  renderLeadSection();

  document.getElementById('brCards').innerHTML = brItems.length
    ? brItems.map(function(item, i) { return storyCard(item, 'br', i); }).join('')
    : emptyCard('Nenhuma notícia Brasil nesta edição.');

  document.getElementById('glCards').innerHTML = glItems.length
    ? glItems.map(function(item, i) { return storyCard(item, 'gl', i); }).join('')
    : emptyCard('Nenhuma notícia Global nesta edição.');
}

async function loadDate(dateStr) {
  if (!dateStr) return;

  currentDate = dateStr;
  document.getElementById('datePicker').value = dateStr;
  document.getElementById('loadingState').style.display = 'flex';
  document.getElementById('journalContent').style.display = 'none';
  document.getElementById('emptyState').style.display = 'none';

  try {
    var rows = await supaFetch('news_items', 'edition_date=eq.' + dateStr + '&order=id.asc');

    brItems = rows.filter(function(r) { return r.region === 'brazil'; });
    glItems = rows.filter(function(r) { return r.region === 'global'; });

    render();
    document.getElementById('loadingState').style.display = 'none';

    if (!rows.length) {
      document.getElementById('emptyState').textContent = 'Nenhuma notícia disponível para esta data.';
      document.getElementById('emptyState').style.display = 'flex';
    } else {
      document.getElementById('journalContent').style.display = 'grid';
    }
  } catch (err) {
    brItems = [];
    glItems = [];
    render();

    document.getElementById('loadingState').style.display = 'none';
    document.getElementById('emptyState').textContent = 'Erro ao carregar: ' + err.message;
    document.getElementById('emptyState').style.display = 'flex';
    console.error(err);
  }
}

function changeDate(delta) {
  if (!currentDate) return;
  var d = new Date(currentDate + 'T12:00:00');
  d.setDate(d.getDate() + delta);
  loadDate(d.toISOString().split('T')[0]);
}

function toggleSummary(id, btn) {
  var el = document.getElementById(id);
  if (!el) return;

  var isOpen = el.classList.toggle('open');
  btn.classList.toggle('is-open', isOpen);
  btn.setAttribute('aria-expanded', isOpen ? 'true' : 'false');

  var text = btn.querySelector('.toggle-text');
  if (text) text.textContent = isOpen ? 'Fechar' : 'Resumo';
}

async function init() {
  try {
    var latest = await supaFetch('news_items', 'select=edition_date&order=edition_date.desc&limit=1');

    if (latest.length > 0) {
      loadDate(latest[0].edition_date);
    } else {
      currentDate = new Date().toISOString().split('T')[0];
      render();
      document.getElementById('datePicker').value = currentDate;
      document.getElementById('loadingState').style.display = 'none';
      document.getElementById('emptyState').style.display = 'flex';
    }
  } catch (err) {
    currentDate = new Date().toISOString().split('T')[0];
    render();
    document.getElementById('datePicker').value = currentDate;
    document.getElementById('loadingState').style.display = 'none';
    document.getElementById('emptyState').textContent = 'Erro de conexão com o banco de dados.';
    document.getElementById('emptyState').style.display = 'flex';
    console.error(err);
  }
}

init();
</script>
</body>
</html>
