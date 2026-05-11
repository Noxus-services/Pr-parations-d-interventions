<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Fiches de Préparation · Noxus Services</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Syne:wght@400;600;700;800&family=JetBrains+Mono:wght@500;700&display=swap" rel="stylesheet">
<style>
  :root {
    --green: #004d00;
    --green-mid: #0a6b0a;
    --green-bright: #15C55A;
    --gold: #eda10c;
    --gold-soft: #f5c869;
    --cream: #F3F0E8;
    --dark: #0C0C0A;
    --red: #c8321e;
    --blue: #2d7dd2;
    --purple: #7c3aed;
    --orange: #f97316;
    --teal: #0d9488;
    --pink: #db2777;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'Syne', sans-serif;
    background: var(--dark);
    color: var(--cream);
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* ── BACKGROUND ── */
  .bg-grid {
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(0,77,0,0.06) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,77,0,0.06) 1px, transparent 1px);
    background-size: 48px 48px;
    pointer-events: none;
    z-index: 0;
  }

  .bg-glow {
    position: fixed;
    top: -200px; left: -200px;
    width: 600px; height: 600px;
    background: radial-gradient(circle, rgba(0,77,0,0.25) 0%, transparent 70%);
    border-radius: 50%;
    pointer-events: none;
    z-index: 0;
    animation: driftA 18s ease-in-out infinite;
  }

  .bg-glow2 {
    position: fixed;
    bottom: -150px; right: -150px;
    width: 500px; height: 500px;
    background: radial-gradient(circle, rgba(237,161,12,0.12) 0%, transparent 70%);
    border-radius: 50%;
    pointer-events: none;
    z-index: 0;
    animation: driftB 22s ease-in-out infinite;
  }

  @keyframes driftA {
    0%, 100% { transform: translate(0,0); }
    50% { transform: translate(80px, 60px); }
  }

  @keyframes driftB {
    0%, 100% { transform: translate(0,0); }
    50% { transform: translate(-60px, -80px); }
  }

  /* ── HEADER ── */
  header {
    position: relative;
    z-index: 10;
    padding: 40px 40px 0;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .logo-wrap {
    display: flex;
    align-items: center;
    gap: 16px;
  }

  .logo-svg {
    height: 52px;
    width: auto;
    filter: drop-shadow(0 4px 16px rgba(237,161,12,0.3));
  }

  .certif {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 6px 14px;
    border: 1px solid rgba(21,197,90,0.4);
    border-radius: 100px;
    font-size: 11px;
    color: var(--green-bright);
    font-weight: 700;
    letter-spacing: 2px;
    text-transform: uppercase;
    background: rgba(21,197,90,0.06);
  }

  .certif::before {
    content: "✓";
    font-size: 12px;
  }

  /* ── HERO ── */
  .hero {
    position: relative;
    z-index: 10;
    padding: 60px 40px 40px;
    max-width: 1100px;
    margin: 0 auto;
  }

  .hero-tag {
    font-family: 'JetBrains Mono', monospace;
    font-size: 12px;
    color: var(--gold);
    letter-spacing: 3px;
    text-transform: uppercase;
    margin-bottom: 16px;
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .hero-tag::before {
    content: "";
    display: block;
    width: 32px;
    height: 2px;
    background: var(--gold);
  }

  h1 {
    font-family: 'Bebas Neue', sans-serif;
    font-size: clamp(52px, 8vw, 96px);
    line-height: 0.95;
    letter-spacing: 1px;
    margin-bottom: 16px;
    color: var(--cream);
  }

  h1 .accent {
    color: var(--green-bright);
    display: block;
  }

  .hero-sub {
    font-size: 16px;
    color: rgba(243,240,232,0.55);
    max-width: 480px;
    line-height: 1.6;
    margin-bottom: 40px;
  }

  /* ── STATS ROW ── */
  .stats {
    display: flex;
    gap: 32px;
    margin-bottom: 60px;
    flex-wrap: wrap;
  }

  .stat {
    display: flex;
    flex-direction: column;
    gap: 2px;
  }

  .stat-num {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 36px;
    color: var(--gold);
    line-height: 1;
  }

  .stat-label {
    font-size: 11px;
    color: rgba(243,240,232,0.45);
    text-transform: uppercase;
    letter-spacing: 1.5px;
    font-weight: 700;
  }

  .stat-divider {
    width: 1px;
    background: rgba(243,240,232,0.1);
    align-self: stretch;
  }

  /* ── SECTION TITLE ── */
  .section-label {
    position: relative;
    z-index: 10;
    padding: 0 40px;
    max-width: 1100px;
    margin: 0 auto 24px;
    display: flex;
    align-items: center;
    gap: 14px;
  }

  .section-label-text {
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px;
    color: rgba(243,240,232,0.4);
    text-transform: uppercase;
    letter-spacing: 3px;
    font-weight: 700;
    white-space: nowrap;
  }

  .section-label::after {
    content: "";
    flex: 1;
    height: 1px;
    background: rgba(243,240,232,0.08);
  }

  /* ── GRID ── */
  .grid {
    position: relative;
    z-index: 10;
    padding: 0 40px 80px;
    max-width: 1100px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 16px;
  }

  /* ── CARD ── */
  .card {
    position: relative;
    border-radius: 20px;
    padding: 28px;
    cursor: pointer;
    text-decoration: none;
    color: inherit;
    overflow: hidden;
    border: 1px solid rgba(255,255,255,0.06);
    background: rgba(255,255,255,0.03);
    backdrop-filter: blur(20px);
    transition: all 0.4s cubic-bezier(0.16, 1, 0.3, 1);
    display: flex;
    flex-direction: column;
    gap: 20px;
  }

  .card::before {
    content: "";
    position: absolute;
    inset: 0;
    border-radius: 20px;
    padding: 1px;
    background: linear-gradient(135deg, var(--card-color, #fff) 0%, transparent 60%);
    -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
    -webkit-mask-composite: xor;
    mask-composite: exclude;
    opacity: 0.15;
    transition: opacity 0.4s;
  }

  .card::after {
    content: "";
    position: absolute;
    inset: 0;
    border-radius: 20px;
    background: radial-gradient(ellipse at 30% 20%, rgba(255,255,255,0.04) 0%, transparent 60%);
    pointer-events: none;
  }

  .card:hover {
    transform: translateY(-6px) scale(1.01);
    border-color: rgba(255,255,255,0.12);
    background: rgba(255,255,255,0.06);
    box-shadow:
      0 24px 48px rgba(0,0,0,0.4),
      0 0 0 1px var(--card-color, #fff),
      0 0 60px -10px var(--card-color, #fff);
  }

  .card:hover::before { opacity: 0.4; }

  .card.disponible { cursor: pointer; }
  .card.bientot { cursor: default; opacity: 0.5; }
  .card.bientot:hover {
    transform: none;
    box-shadow: none;
    border-color: rgba(255,255,255,0.06);
    background: rgba(255,255,255,0.03);
  }

  /* Card top */
  .card-top {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    gap: 12px;
  }

  .card-icon {
    width: 64px;
    height: 64px;
    border-radius: 16px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 32px;
    flex-shrink: 0;
    position: relative;
    background: var(--card-bg, rgba(255,255,255,0.06));
    box-shadow: 0 8px 24px -4px var(--card-color, #fff);
    transition: transform 0.4s cubic-bezier(0.16, 1, 0.3, 1);
  }

  .card:hover .card-icon { transform: scale(1.1) rotate(-4deg); }

  .card-status {
    display: inline-flex;
    align-items: center;
    gap: 5px;
    padding: 4px 10px;
    border-radius: 100px;
    font-size: 10px;
    font-weight: 700;
    letter-spacing: 1px;
    text-transform: uppercase;
    flex-shrink: 0;
  }

  .card-status.dispo {
    background: rgba(21,197,90,0.12);
    color: var(--green-bright);
    border: 1px solid rgba(21,197,90,0.3);
  }

  .card-status.dispo::before {
    content: "";
    width: 6px;
    height: 6px;
    border-radius: 50%;
    background: var(--green-bright);
    animation: blink 2s infinite;
  }

  @keyframes blink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.3; }
  }

  .card-status.soon {
    background: rgba(243,240,232,0.06);
    color: rgba(243,240,232,0.4);
    border: 1px solid rgba(243,240,232,0.1);
  }

  /* Card content */
  .card-body { flex: 1; }

  .card-nuisible {
    font-family: 'JetBrains Mono', monospace;
    font-size: 10px;
    text-transform: uppercase;
    letter-spacing: 2px;
    font-weight: 700;
    margin-bottom: 6px;
    color: var(--card-color, rgba(243,240,232,0.5));
  }

  .card-title {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 28px;
    letter-spacing: 0.5px;
    line-height: 1;
    margin-bottom: 10px;
    color: var(--cream);
    transition: color 0.3s;
  }

  .card:hover .card-title { color: var(--card-color, var(--cream)); }

  .card-desc {
    font-size: 13px;
    color: rgba(243,240,232,0.45);
    line-height: 1.5;
  }

  /* Card footer */
  .card-footer {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding-top: 16px;
    border-top: 1px solid rgba(255,255,255,0.06);
  }

  .card-steps {
    display: flex;
    gap: 4px;
  }

  .step-dot {
    width: 8px;
    height: 8px;
    border-radius: 50%;
    background: var(--card-color, rgba(243,240,232,0.2));
    opacity: 0.3;
  }

  .step-dot.active { opacity: 1; }

  .card-arrow {
    width: 32px;
    height: 32px;
    border-radius: 50%;
    background: var(--card-color, rgba(243,240,232,0.1));
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--dark);
    transition: transform 0.3s;
    opacity: 0;
  }

  .card:hover .card-arrow {
    opacity: 1;
    transform: translateX(4px);
  }

  .card-arrow svg { width: 16px; height: 16px; }

  .card-pages {
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px;
    color: rgba(243,240,232,0.3);
  }

  /* ── CARD LARGE (featured) ── */
  .card.featured {
    grid-column: span 2;
    flex-direction: row;
    align-items: center;
    gap: 32px;
    padding: 36px;
  }

  .card.featured .card-icon {
    width: 96px;
    height: 96px;
    font-size: 48px;
    border-radius: 22px;
    flex-shrink: 0;
  }

  .card.featured .card-title { font-size: 40px; }

  .card.featured .card-body { flex: 1; }

  /* ── FOOTER ── */
  footer {
    position: relative;
    z-index: 10;
    padding: 32px 40px;
    border-top: 1px solid rgba(255,255,255,0.06);
    display: flex;
    align-items: center;
    justify-content: space-between;
    max-width: 1100px;
    margin: 0 auto;
    flex-wrap: wrap;
    gap: 16px;
  }

  .footer-brand {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 20px;
    letter-spacing: 2px;
    color: var(--gold);
  }

  .footer-info {
    font-size: 12px;
    color: rgba(243,240,232,0.3);
    text-align: center;
  }

  .footer-zones {
    display: flex;
    gap: 8px;
    flex-wrap: wrap;
    justify-content: flex-end;
  }

  .zone {
    font-size: 10px;
    color: rgba(243,240,232,0.3);
    padding: 3px 8px;
    border: 1px solid rgba(255,255,255,0.06);
    border-radius: 100px;
  }

  /* ── MOBILE ── */
  @media (max-width: 700px) {
    header { padding: 24px 20px 0; }
    .hero { padding: 40px 20px 30px; }
    .section-label { padding: 0 20px; }
    .grid { padding: 0 20px 60px; grid-template-columns: 1fr; }
    .card.featured { grid-column: span 1; flex-direction: column; }
    .card.featured .card-title { font-size: 28px; }
    footer { padding: 24px 20px; }
    .stats { gap: 20px; }
  }
</style>
</head>
<body>

<div class="bg-grid"></div>
<div class="bg-glow"></div>
<div class="bg-glow2"></div>

<!-- ── HEADER ── -->
<header>
  <div class="logo-wrap">
    <svg class="logo-svg" viewBox="0 0 130 103" fill="none" xmlns="http://www.w3.org/2000/svg">
      <path d="M100.696 2.77895C84.5751 16.3168 66.2151 24.6158 45.0162 27.4579C47.1257 20.2737 46.3867 13.8284 41.9151 7.81263C61.2193 1.0421 80.6435 -1.41158 100.696 2.77895Z" fill="#eda10c"/>
      <path d="M129.828 22.2726C127.181 22.7558 124.456 23.1947 121.756 23.7632C115.238 25.1305 109.715 24.4895 103.728 20.2137C100.794 18.2526 98.1004 16.6042 95.2141 14.8074C98.3499 12.4547 101.359 10.1968 104.372 7.93579C108.278 4.84737 109.232 5.14737 111.945 6.53684C118.614 10.1179 124.529 14.5358 129.127 20.6053C129.828 21.8558 129.828 22.2789 129.828 22.2726Z" fill="#eda10c"/>
      <path d="M25.3772 35.0842C23.293 24.2368 25.0614 16.8095 35.7225 10.6674C37.5162 11.0589 40.9741 17.0274 41.5299 23.1284C38.312 29.3716 35.7951 32.7505 33.6067 33.2684C30.8751 33.9158 28.1278 34.4811 25.3804 35.0842H25.3772ZM31.4814 28.0137C33.5436 28.0137 35.1635 26.4568 35.1383 24.5053C35.113 22.4589 33.5625 20.8895 31.5572 20.88C29.5141 20.8674 27.9067 22.4242 27.9067 24.4105C27.9067 26.4316 29.4793 28.0137 31.4814 28.0137Z" fill="#eda10c"/>
      <path d="M96.0636 37.7526C92.653 38.2358 86.3941 36.4453 83.2204 34.0453C79.7183 32.0779 76.2951 30.0253 73.993 29.7663C72.5214 30.1263 71.113 30.7453 69.6793 31.2568C67.1246 32.1695 66.6604 32.0432 64.6172 29.7853C68.413 28.4368 75.932 25.8095 77.4983 26.2074C82.4025 29.2579 92.173 35.4284 96.0636 37.7526Z" fill="#eda10c"/>
      <path d="M18.2814 21.6663C12.4267 18.6758 8.9025 14.1663 6.98566 8.3621C5.94039 5.19474 6.51513 0 7.49408 0.385263C8.10355 2.12526 7.84145 9.46737 21.4741 20.1568C22.2478 20.7568 21.6572 23.8042 18.3478 24.0347C11.9246 24.4832 3.96355 33.2305 1.59197 37.9958C-0.18908 37.68 0.369867 35.9463 3.29092 28.6642C8.22671 23.64 16.1278 21.9695 18.2846 21.6663H18.2814Z" fill="#eda10c"/>
      <path d="M6.20891 55.2505V71.5895H0.000488281V44.4253H7.02365L16.57 59.4442V44.4253H22.7784V71.5895H16.57V71.5516L6.20891 55.2537V55.2505Z" fill="#F3F0E8"/>
      <path d="M40.63 43.6453C48.5089 43.6453 54.9889 50.321 54.9889 58.0042C54.9889 65.6874 48.3131 72.3632 40.63 72.3632C32.5584 72.3632 26.271 65.4568 26.271 58.0042C26.271 50.1253 32.9058 43.6453 40.63 43.6453ZM40.63 66.66C45.3258 66.66 48.5089 62.2358 48.5089 58.0074C48.5089 53.5042 45.0952 49.3547 40.63 49.3547C35.9342 49.3547 32.751 53.7411 32.751 58.0074C32.9436 62.5074 35.9721 66.66 40.63 66.66Z" fill="#F3F0E8"/>
      <path d="M55.2984 71.5863L63.7963 58.2758L54.9857 44.46L61.6994 44.4221L67.1342 52.9989L72.5657 44.4221L78.97 44.46L70.3173 58.0042L78.97 71.5863H72.2563L66.9794 63.2811L61.7026 71.5863H55.2984Z" fill="#F3F0E8"/>
      <path d="M81.6858 44.4221H87.8942V61.3421C87.8942 64.2916 89.8742 66.66 92.8615 66.66C95.8489 66.66 97.791 64.2916 97.791 61.3421V44.4221H103.999V61.1874C103.999 67.9389 99.0321 72.3632 92.8615 72.3632C86.691 72.3632 81.6858 68.2895 81.6858 61.1874V44.4221Z" fill="#F3F0E8"/>
      <path d="M123.364 64.2916C123.364 62.7379 120.995 61.7305 117.815 61.0326C113.587 60.1011 107.416 58.3547 107.416 52.38C107.416 46.4053 112.889 43.6484 117.856 43.6484C122.824 43.6484 126.743 45.9 129.266 49.3516L124.144 52.8442C123.136 51.0979 120.651 49.3516 118.011 49.3516C116.498 49.3516 113.896 50.1284 113.896 52.0674C113.896 53.7347 116.186 54.3189 119.056 55.0547C123.597 56.22 129.844 57.9253 129.844 64.0958C129.844 69.7232 123.869 72.3221 118.125 72.3221C113.467 72.3221 108.733 69.8779 106.327 66.3063L111.683 63.1232C112.807 65.0621 115.873 66.6537 118.204 66.6537C118.204 66.6537 123.364 66.7326 123.364 64.2853V64.2916Z" fill="#F3F0E8"/>
      <path d="M17.5184 97.5128C16.254 97.5128 12.0749 95.2467 11.3359 92.7097V91.7491H13.6266V92.5865C13.6266 93.424 14.7104 94.6556 17.6909 95.4684C20.2525 94.7541 21.1146 92.8821 21.1146 91.5766C19.3658 90.5914 17.9864 89.9099 16.9026 89.483C14.0454 88.2267 12.3212 86.7488 11.6315 84.4088C11.6315 82.9966 13.134 81.0836 17.2475 79.8766C20.4496 80.4924 22.5679 82.2166 23.3315 84.7783V85.5173H20.9915V84.9015C20.9915 84.0476 19.957 82.7832 17.149 81.9211C14.7843 82.5615 13.9469 84.3596 13.9469 85.6897C15.5972 86.6257 17.0012 87.2333 18.1342 87.6602C20.9669 88.9411 22.765 90.4682 23.4793 92.8082C23.4793 94.2533 21.8782 96.2566 17.5184 97.5128ZM38.1324 81.8718C38.1324 82.036 38.0503 82.1181 37.8861 82.1181H29.0433V87.611H35.3983V89.6554H29.0433V95.2714H37.8861C38.0503 95.2714 38.1324 95.3535 38.1324 95.5177V97.3158H26.6787V80.0737H37.8861C38.0503 80.0737 38.1324 80.1558 38.1324 80.32V81.8718ZM60.5531 97.3158L54.9863 80.3446L54.9617 80.2461C54.9617 80.1312 55.0356 80.0737 55.1834 80.0737H57.4741L61.6122 93.9413L65.7503 80.2707C65.7996 80.1394 65.8899 80.0737 66.0213 80.0737H67.9672L62.8438 97.1187C62.7945 97.2501 62.696 97.3158 62.5482 97.3158H60.5531ZM71.233 97.3158V80.0737H73.3513V97.3158H71.233ZM82.9272 97.5375C79.7744 96.8478 76.9171 92.9888 76.9171 85.4926C76.9171 83.399 78.1651 81.7076 79.7744 80.591C80.6939 80.1147 81.7449 79.8766 82.9272 79.8766C85.1523 80.1065 87.6565 81.6419 88.9127 85.3202V85.6158L86.7944 85.7143V85.4187C86.548 84.3678 85.5628 82.8817 82.9272 81.9211C80.267 82.8817 79.2817 84.3678 79.2817 85.4187V91.9707C79.6102 93.8674 80.267 94.5078 82.9272 95.4684C84.9059 95.1482 86.548 93.8674 86.548 91.9707V91.6998L88.6664 91.7983C88.9127 92.0446 88.9127 93.1284 88.1491 94.9265C87.6565 95.7476 86.0554 96.8478 82.9272 97.5375ZM103.801 81.8718C103.801 82.036 103.718 82.1181 103.554 82.1181H94.7115V87.611H100.82C100.984 87.611 101.066 87.6931 101.066 87.8573V89.6554H94.7115V95.2714H103.554C103.718 95.2714 103.801 95.3535 103.801 95.5177V97.3158H92.3469V80.0737H103.554C103.718 80.0737 103.801 80.1558 103.801 80.32V81.8718ZM112.388 97.5128C111.124 97.5128 106.206 93.6785 106.206 91.7491H108.497V92.5865C108.858 94.1137 111.296 95.4684 112.561 95.4684C115.123 94.7541 115.985 92.8821 115.985 91.5766C114.236 90.5914 112.856 89.9099 111.773 89.483C108.915 88.2267 106.502 84.4088 106.502 84.4088C106.502 82.9966 108.004 81.0836 112.118 79.8766C115.32 80.4924 117.438 82.2166 118.202 84.7783V85.5173H115.862V84.9015C115.517 83.3415 113.218 81.9211 112.019 81.9211C109.654 82.5615 108.817 84.3596 108.817 85.6897C110.467 86.6257 111.871 87.2333 113.004 87.6602C115.837 88.9411 117.635 90.4682 118.349 92.8082C118.349 94.2533 116.748 96.2566 112.388 97.5128Z" fill="#F3F0E8"/>
    </svg>
  </div>
  <div class="certif">Certibiocide</div>
</header>

<!-- ── HERO ── -->
<div class="hero">
  <div class="hero-tag">Portail client · Fiches de préparation</div>
  <h1>FICHES<br><span class="accent">PRÉPARATION</span></h1>
  <p class="hero-sub">Sélectionnez la fiche correspondant à votre intervention. Cochez chaque étape pour activer votre garantie résultat Noxus.</p>

  <div class="stats">
    <div class="stat">
      <div class="stat-num">3</div>
      <div class="stat-label">Étapes par fiche</div>
    </div>
    <div class="stat-divider"></div>
    <div class="stat">
      <div class="stat-num">100%</div>
      <div class="stat-label">Garantie si complété</div>
    </div>
    <div class="stat-divider"></div>
    <div class="stat">
      <div class="stat-num">3</div>
      <div class="stat-label">Passages inclus</div>
    </div>
  </div>
</div>

<!-- ── SECTION DISPONIBLE ── -->
<div class="section-label">
  <div class="section-label-text">Disponibles maintenant</div>
</div>

<div class="grid">

  <!-- PUNAISES DE LIT — FEATURED -->
  <a class="card featured disponible" href="punaises-de-lit.html"
     style="--card-color: #c8321e; --card-bg: rgba(200,50,30,0.15);">
    <div class="card-icon">🪲</div>
    <div class="card-body">
      <div class="card-nuisible">Désinsectisation</div>
      <div class="card-title">PUNAISES DE LIT</div>
      <div class="card-desc">Préparation complète avant traitement insecticide en 3 passages. Linge, mobilier, aspiration, consignes post-traitement et activation de la garantie résultat.</div>
      <div class="card-footer">
        <div class="card-steps">
          <div class="step-dot active"></div>
          <div class="step-dot active"></div>
          <div class="step-dot active"></div>
        </div>
        <div style="display:flex;align-items:center;gap:12px;">
          <span class="card-status dispo">Disponible</span>
          <div class="card-arrow" style="background: #c8321e;">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><line x1="5" y1="12" x2="19" y2="12"/><polyline points="12 5 19 12 12 19"/></svg>
          </div>
        </div>
      </div>
    </div>
  </a>

</div>

<!-- ── SECTION À VENIR ── -->
<div class="section-label">
  <div class="section-label-text">Prochainement</div>
</div>

<div class="grid">

  <!-- BLATTES -->
  <div class="card bientot" style="--card-color: #f97316; --card-bg: rgba(249,115,22,0.12);">
    <div class="card-top">
      <div class="card-icon">🪳</div>
      <span class="card-status soon">Bientôt</span>
    </div>
    <div class="card-body">
      <div class="card-nuisible">Désinsectisation</div>
      <div class="card-title">BLATTES & CAFARDS</div>
      <div class="card-desc">Protocole cuisine, gel appâts, zones humides et traitement des fissures. Idéal CHR et restauration.</div>
    </div>
    <div class="card-footer">
      <div class="card-steps">
        <div class="step-dot active"></div>
        <div class="step-dot active"></div>
        <div class="step-dot active"></div>
      </div>
      <span class="card-pages">En préparation</span>
    </div>
  </div>

  <!-- RONGEURS -->
  <div class="card bientot" style="--card-color: #7c3aed; --card-bg: rgba(124,58,237,0.12);">
    <div class="card-top">
      <div class="card-icon">🐀</div>
      <span class="card-status soon">Bientôt</span>
    </div>
    <div class="card-body">
      <div class="card-nuisible">Dératisation</div>
      <div class="card-title">RATS & SOURIS</div>
      <div class="card-desc">Sécurisation des postes d'appâts, protection enfants et animaux, traçabilité anticoagulants HACCP.</div>
    </div>
    <div class="card-footer">
      <div class="card-steps">
        <div class="step-dot active"></div>
        <div class="step-dot active"></div>
        <div class="step-dot active"></div>
      </div>
      <span class="card-pages">En préparation</span>
    </div>
  </div>

  <!-- FRELONS -->
  <div class="card bientot" style="--card-color: #eda10c; --card-bg: rgba(237,161,12,0.12);">
    <div class="card-top">
      <div class="card-icon">🐝</div>
      <span class="card-status soon">Bientôt</span>
    </div>
    <div class="card-body">
      <div class="card-nuisible">Désinsectisation</div>
      <div class="card-title">FRELONS & GUÊPES</div>
      <div class="card-desc">Consignes de sécurité, évacuation, protection EPI et délai de réintégration après traitement du nid.</div>
    </div>
    <div class="card-footer">
      <div class="card-steps">
        <div class="step-dot active"></div>
        <div class="step-dot active"></div>
        <div class="step-dot active"></div>
      </div>
      <span class="card-pages">En préparation</span>
    </div>
  </div>

  <!-- FOURMIS -->
  <div class="card bientot" style="--card-color: #0d9488; --card-bg: rgba(13,148,136,0.12);">
    <div class="card-top">
      <div class="card-icon">🐜</div>
      <span class="card-status soon">Bientôt</span>
    </div>
    <div class="card-body">
      <div class="card-nuisible">Désinsectisation</div>
      <div class="card-title">FOURMIS</div>
      <div class="card-desc">Localisation des colonies, traitement des pistes, gel appâts et prévention des réinfestations.</div>
    </div>
    <div class="card-footer">
      <div class="card-steps">
        <div class="step-dot active"></div>
        <div class="step-dot active"></div>
        <div class="step-dot active"></div>
      </div>
      <span class="card-pages">En préparation</span>
    </div>
  </div>

  <!-- MITES -->
  <div class="card bientot" style="--card-color: #db2777; --card-bg: rgba(219,39,119,0.12);">
    <div class="card-top">
      <div class="card-icon">🦋</div>
      <span class="card-status soon">Bientôt</span>
    </div>
    <div class="card-body">
      <div class="card-nuisible">Désinsectisation</div>
      <div class="card-title">MITES & CHARANÇONS</div>
      <div class="card-desc">Vider les placards, isoler les denrées alimentaires, traitement des textiles et des zones de stockage.</div>
    </div>
    <div class="card-footer">
      <div class="card-steps">
        <div class="step-dot active"></div>
        <div class="step-dot active"></div>
        <div class="step-dot active"></div>
      </div>
      <span class="card-pages">En préparation</span>
    </div>
  </div>

  <!-- PIGEONS -->
  <div class="card bientot" style="--card-color: #2d7dd2; --card-bg: rgba(45,125,210,0.12);">
    <div class="card-top">
      <div class="card-icon">🐦</div>
      <span class="card-status soon">Bientôt</span>
    </div>
    <div class="card-body">
      <div class="card-nuisible">Nuisibles volants</div>
      <div class="card-title">PIGEONS & NUISIBLES VOLANTS</div>
      <div class="card-desc">Accès toiture, protection des surfaces, consignes de sécurité et suivi post-pose des systèmes anti-nidification.</div>
    </div>
    <div class="card-footer">
      <div class="card-steps">
        <div class="step-dot active"></div>
        <div class="step-dot active"></div>
        <div class="step-dot active"></div>
      </div>
      <span class="card-pages">En préparation</span>
    </div>
  </div>

</div>

<!-- ── FOOTER ── -->
<footer>
  <div class="footer-brand">NOXUS SERVICES</div>
  <div class="footer-info">
    Portail de préparation client · Usage exclusif<br>
    <span style="font-family:'JetBrains Mono',monospace;font-size:10px;color:rgba(243,240,232,0.2);">noxus-services.fr</span>
  </div>
  <div class="footer-zones">
    <span class="zone">Villefranche-sur-Saône</span>
    <span class="zone">Beaujolais</span>
    <span class="zone">Rhône</span>
    <span class="zone">Val de Saône</span>
    <span class="zone">Ain</span>
  </div>
</footer>

</body>
</html># Pr-parations-d-interventions
