<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ATRIC SARL – African Trade and Industry Company</title>
<meta name="description" content="ATRIC SARL connecte l'Afrique aux opportunités internationales. Construction, Agro, Cosmétiques, Digital – Expertise multisectorielle africaine au Cameroun.">
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@300;400;600;700&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --or: #C9A84C; --or-light: #E8C97A;
    --noir: #0A0A0A; --gris: #111111; --gris2: #1A1A1A; --gris3: #2A2A2A;
    --blanc: #F8F5EF; --texte: #C8C0B0;
  }
  * { margin: 0; padding: 0; box-sizing: border-box; }
  html { scroll-behavior: smooth; }
  body { background: var(--noir); color: var(--blanc); font-family: 'DM Sans', sans-serif; font-weight: 300; overflow-x: hidden; }

  /* NAV */
  nav { position: fixed; top: 0; left: 0; right: 0; z-index: 100; display: flex; justify-content: space-between; align-items: center; padding: 1.2rem 5%; background: rgba(10,10,10,0.96); backdrop-filter: blur(12px); border-bottom: 1px solid rgba(201,168,76,0.15); }
  .logo { font-family: 'Cormorant Garamond', serif; font-size: 1.4rem; font-weight: 700; letter-spacing: 0.15em; color: var(--or); }
  .logo span { color: var(--blanc); font-weight: 300; font-size: 0.68rem; display: block; letter-spacing: 0.3em; margin-top: -2px; }
  nav ul { list-style: none; display: flex; gap: 1.8rem; }
  nav ul a { color: var(--texte); text-decoration: none; font-size: 0.72rem; letter-spacing: 0.12em; text-transform: uppercase; transition: color 0.3s; }
  nav ul a:hover { color: var(--or); }

  /* HERO */
  #accueil { min-height: 100vh; display: flex; align-items: center; padding: 0 5%; position: relative; overflow: hidden; }
  .hero-bg { position: absolute; inset: 0; background: radial-gradient(ellipse at 70% 50%, rgba(201,168,76,0.07) 0%, transparent 60%); }
  .hero-img { position: absolute; right: 0; top: 0; bottom: 0; width: 45%; background: url('https://images.unsplash.com/photo-1541888946425-d81bb19240f5?w=900&q=80') center/cover no-repeat; opacity: 0.18; }
  .hero-img::after { content: ''; position: absolute; inset: 0; background: linear-gradient(to right, var(--noir) 0%, transparent 70%); }
  .hero-line { position: absolute; top: 0; right: 20%; width: 1px; height: 100%; background: linear-gradient(to bottom, transparent, rgba(201,168,76,0.2), transparent); }
  .hero-content { max-width: 700px; position: relative; z-index: 1; padding-top: 5rem; }
  .hero-tag { font-size: 0.65rem; letter-spacing: 0.4em; text-transform: uppercase; color: var(--or); margin-bottom: 2rem; display: flex; align-items: center; gap: 1rem; }
  .hero-tag::before { content: ''; width: 40px; height: 1px; background: var(--or); }
  h1 { font-family: 'Cormorant Garamond', serif; font-size: clamp(2.8rem, 5.5vw, 5rem); font-weight: 300; line-height: 1.1; margin-bottom: 1rem; }
  h1 em { color: var(--or); font-style: normal; }
  .hero-subtitle { font-size: 1.1rem; color: var(--texte); margin-bottom: 1.5rem; font-family: 'Cormorant Garamond', serif; font-style: italic; }
  .hero-liste { list-style: none; margin-bottom: 2.5rem; display: flex; flex-direction: column; gap: 0.6rem; }
  .hero-liste li { font-size: 0.88rem; color: var(--texte); display: flex; align-items: center; gap: 0.8rem; }
  .hero-liste li::before { content: '→'; color: var(--or); font-size: 0.9rem; }
  .hero-cta-group { display: flex; gap: 1rem; flex-wrap: wrap; }
  .btn { display: inline-flex; align-items: center; gap: 0.8rem; padding: 1rem 2.5rem; border: 1px solid var(--or); color: var(--or); text-decoration: none; font-size: 0.75rem; letter-spacing: 0.2em; text-transform: uppercase; transition: all 0.3s; position: relative; overflow: hidden; cursor: pointer; }
  .btn::before { content: ''; position: absolute; inset: 0; background: var(--or); transform: translateX(-101%); transition: transform 0.3s; z-index: -1; }
  .btn:hover { color: var(--noir); }
  .btn:hover::before { transform: translateX(0); }
  .btn-outline { background: transparent; border-color: var(--gris3); color: var(--texte); }
  .btn-outline:hover { color: var(--blanc); border-color: var(--blanc); }
  .btn-outline::before { background: var(--gris3); }
  .hero-stats { position: absolute; right: 5%; bottom: 10%; display: flex; flex-direction: column; gap: 2.5rem; }
  .stat { text-align: right; }
  .stat-num { font-family: 'Cormorant Garamond', serif; font-size: 2.5rem; color: var(--or); line-height: 1; }
  .stat-label { font-size: 0.65rem; letter-spacing: 0.25em; color: var(--texte); text-transform: uppercase; }

  /* SECTIONS */
  section { padding: 7rem 5%; }
  .section-tag { font-size: 0.65rem; letter-spacing: 0.4em; text-transform: uppercase; color: var(--or); margin-bottom: 1.5rem; display: flex; align-items: center; gap: 1rem; }
  .section-tag::before { content: ''; width: 30px; height: 1px; background: var(--or); }
  h2 { font-family: 'Cormorant Garamond', serif; font-size: clamp(2rem, 4vw, 3.2rem); font-weight: 300; line-height: 1.15; margin-bottom: 1.5rem; }
  .divider { width: 50px; height: 1px; background: var(--or); margin: 1.5rem 0; }

  /* PROBLÈMES / SOLUTIONS */
  #problemes { background: var(--gris2); }
  .prob-sol-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 3rem; margin-top: 3rem; }
  .prob-col, .sol-col { padding: 2.5rem; }
  .prob-col { border: 1px solid rgba(220,50,50,0.2); background: rgba(220,50,50,0.03); }
  .sol-col { border: 1px solid rgba(201,168,76,0.2); background: rgba(201,168,76,0.03); }
  .prob-col h3 { font-family: 'Cormorant Garamond', serif; font-size: 1.4rem; color: #f08080; margin-bottom: 1.5rem; }
  .sol-col h3 { font-family: 'Cormorant Garamond', serif; font-size: 1.4rem; color: var(--or); margin-bottom: 1.5rem; }
  .prob-col ul, .sol-col ul { list-style: none; display: flex; flex-direction: column; gap: 0.8rem; }
  .prob-col li, .sol-col li { font-size: 0.88rem; color: var(--texte); display: flex; align-items: flex-start; gap: 0.8rem; line-height: 1.6; }
  .prob-col li::before { content: '✗'; color: #f08080; flex-shrink: 0; }
  .sol-col li::before { content: '✓'; color: var(--or); flex-shrink: 0; }

  /* SERVICES */
  #services { background: var(--noir); }
  .services-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.5px; margin-top: 3rem; }
  .service-card { background: var(--gris); padding: 2.5rem; position: relative; overflow: hidden; transition: background 0.3s; }
  .service-card::after { content: ''; position: absolute; bottom: 0; left: 0; width: 0; height: 2px; background: var(--or); transition: width 0.4s; }
  .service-card:hover { background: var(--gris2); }
  .service-card:hover::after { width: 100%; }
  .service-num { font-family: 'Cormorant Garamond', serif; font-size: 3rem; color: rgba(201,168,76,0.15); line-height: 1; margin-bottom: 1rem; }
  .service-icon { font-size: 1.8rem; margin-bottom: 1rem; display: block; }
  .service-card h3 { font-family: 'Cormorant Garamond', serif; font-size: 1.3rem; font-weight: 400; color: var(--blanc); margin-bottom: 1rem; }
  .service-card ul { list-style: none; margin-bottom: 1.5rem; }
  .service-card li { font-size: 0.82rem; color: var(--texte); padding: 0.35rem 0; border-bottom: 1px solid rgba(255,255,255,0.04); display: flex; align-items: flex-start; gap: 0.5rem; line-height: 1.5; }
  .service-card li::before { content: '–'; color: var(--or); flex-shrink: 0; }
  .service-card li:last-child { border-bottom: none; }
  .service-impact { margin-top: 1.5rem; padding: 1rem; background: rgba(201,168,76,0.06); border-left: 2px solid var(--or); font-size: 0.8rem; color: var(--or); line-height: 1.6; font-style: italic; }

  /* POURQUOI NOUS */
  #pourquoi { background: var(--gris); }
  .pourquoi-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.5rem; margin-top: 3rem; }
  .pourquoi-card { background: var(--noir); border-top: 2px solid var(--or); padding: 2rem; }
  .pourquoi-icon { font-size: 1.8rem; margin-bottom: 1rem; }
  .pourquoi-card h3 { font-family: 'Cormorant Garamond', serif; font-size: 1.1rem; color: var(--or); margin-bottom: 0.8rem; }
  .pourquoi-card p { font-size: 0.85rem; color: var(--texte); line-height: 1.8; }

  /* CLIENTS */
  #clients { background: var(--noir); }
  .clients-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 1.5rem; margin-top: 3rem; }
  .client-card { background: var(--gris); border: 1px solid var(--gris3); padding: 2rem; text-align: center; transition: border-color 0.3s; }
  .client-card:hover { border-color: var(--or); }
  .client-icon { font-size: 2rem; margin-bottom: 1rem; }
  .client-card p { font-size: 0.85rem; color: var(--texte); line-height: 1.7; }

  /* À PROPOS */
  #apropos { background: var(--gris); }
  .apropos-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 5rem; align-items: start; margin-top: 3rem; }
  .apropos-text p { font-size: 0.92rem; line-height: 1.9; color: var(--texte); margin-bottom: 1.2rem; }
  .apropos-right { border-left: 1px solid var(--gris3); padding-left: 3rem; }
  .info-block { margin-bottom: 1.8rem; }
  .info-label { font-size: 0.65rem; letter-spacing: 0.3em; color: var(--or); text-transform: uppercase; margin-bottom: 0.4rem; }
  .info-value { font-size: 0.92rem; color: var(--blanc); }
  .valeurs-row { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.5rem; margin-top: 3rem; }
  .valeur-bloc { padding: 2rem; border-top: 2px solid var(--or); background: var(--gris2); }
  .valeur-num { font-family: 'Cormorant Garamond', serif; font-size: 2.5rem; color: rgba(201,168,76,0.2); line-height: 1; margin-bottom: 0.5rem; }
  .valeur-titre { font-size: 0.95rem; color: var(--or); margin-bottom: 0.8rem; font-weight: 500; }
  .valeur-bloc p { font-size: 0.82rem; color: var(--texte); line-height: 1.8; }
  .mission-box { margin-top: 2rem; padding: 2rem; border: 1px solid rgba(201,168,76,0.2); background: rgba(201,168,76,0.03); }
  .mission-box h3 { font-family: 'Cormorant Garamond', serif; font-size: 1.3rem; color: var(--or); margin-bottom: 1rem; }
  .mission-box p { font-size: 0.88rem; color: var(--texte); line-height: 1.8; }
  .aide-liste { list-style: none; margin-top: 1rem; }
  .aide-liste li { font-size: 0.88rem; color: var(--texte); padding: 0.4rem 0; display: flex; align-items: center; gap: 0.7rem; border-bottom: 1px solid rgba(255,255,255,0.05); }
  .aide-liste li::before { content: '✓'; color: var(--or); }
  .aide-liste li:last-child { border-bottom: none; }

  /* AUDIT CTA */
  #audit { background: linear-gradient(135deg, rgba(201,168,76,0.08) 0%, var(--gris2) 100%); border-top: 1px solid rgba(201,168,76,0.2); border-bottom: 1px solid rgba(201,168,76,0.2); padding: 6rem 5%; text-align: center; }
  #audit h2 { margin-bottom: 1rem; }
  #audit p { font-size: 1rem; color: var(--texte); max-width: 600px; margin: 0 auto 2.5rem; line-height: 1.8; }
  .audit-btns { display: flex; justify-content: center; gap: 1.5rem; flex-wrap: wrap; }

  /* CONTACT */
  #contact { background: var(--noir); }
  .contact-grid { display: grid; grid-template-columns: 1fr 1.2fr; gap: 5rem; margin-top: 3rem; align-items: start; }
  .contact-info p { font-size: 0.92rem; color: var(--texte); line-height: 1.9; margin-bottom: 2rem; }
  .contact-block { margin-bottom: 1.5rem; }
  .contact-block-label { font-size: 0.65rem; letter-spacing: 0.3em; color: var(--or); text-transform: uppercase; margin-bottom: 0.6rem; }
  .contact-links { display: flex; flex-direction: column; gap: 0.6rem; }
  .contact-link { display: flex; align-items: center; gap: 0.8rem; font-size: 0.88rem; color: var(--blanc); text-decoration: none; padding: 0.75rem 1rem; border: 1px solid var(--gris3); transition: border-color 0.3s, color 0.3s; }
  .contact-link:hover { border-color: var(--or); color: var(--or-light); }
  .contact-link.wa { border-color: rgba(37,211,102,0.25); color: #a8f0c0; }
  .contact-link.wa:hover { border-color: #25D166; color: #25D166; }
  form { display: flex; flex-direction: column; gap: 1.2rem; }
  input, textarea, select { background: var(--gris2); border: 1px solid var(--gris3); color: var(--blanc); padding: 1rem 1.2rem; font-family: 'DM Sans', sans-serif; font-size: 0.85rem; outline: none; transition: border-color 0.3s; width: 100%; }
  input:focus, textarea:focus, select:focus { border-color: var(--or); }
  input::placeholder, textarea::placeholder { color: rgba(200,192,176,0.35); }
  select option { background: var(--gris2); color: var(--blanc); }
  textarea { resize: vertical; min-height: 130px; }
  .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; }
  button[type="submit"] { background: transparent; border: 1px solid var(--or); color: var(--or); padding: 1rem 2.5rem; font-family: 'DM Sans', sans-serif; font-size: 0.75rem; letter-spacing: 0.2em; text-transform: uppercase; cursor: pointer; transition: all 0.3s; position: relative; overflow: hidden; align-self: flex-start; }
  button[type="submit"]::before { content: ''; position: absolute; inset: 0; background: var(--or); transform: translateX(-101%); transition: transform 0.3s; z-index: -1; }
  button[type="submit"]:hover { color: var(--noir); }
  button[type="submit"]:hover::before { transform: translateX(0); }
  button[type="submit"]:disabled { opacity: 0.6; cursor: not-allowed; }
  .success-msg { display: none; background: rgba(201,168,76,0.08); border: 1px solid rgba(201,168,76,0.4); padding: 1rem 1.5rem; font-size: 0.82rem; color: var(--or); }
  .error-msg { display: none; background: rgba(220,50,50,0.08); border: 1px solid rgba(220,50,50,0.4); padding: 1rem 1.5rem; font-size: 0.82rem; color: #f08080; }

  /* FOOTER */
  footer { background: var(--gris); border-top: 1px solid var(--gris3); padding: 3rem 5%; display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 1.5rem; }
  .footer-logo { font-family: 'Cormorant Garamond', serif; font-size: 1.2rem; font-weight: 700; color: var(--or); letter-spacing: 0.1em; }
  .footer-logo span { font-weight: 300; font-size: 0.68rem; display: block; color: var(--texte); letter-spacing: 0.2em; }
  .footer-links { display: flex; gap: 1.5rem; flex-wrap: wrap; }
  .footer-links a { font-size: 0.72rem; color: var(--texte); text-decoration: none; letter-spacing: 0.1em; transition: color 0.3s; }
  .footer-links a:hover { color: var(--or); }
  .copy { font-size: 0.72rem; color: var(--texte); }


  /* PHOTO DG */
  .dg-section { display: flex; align-items: center; gap: 3rem; margin-bottom: 3rem; padding: 2.5rem; background: var(--gris2); border: 1px solid var(--gris3); border-left: 3px solid var(--or); }
  .dg-photo { width: 140px; height: 140px; border-radius: 50%; object-fit: cover; object-position: top; border: 3px solid var(--or); flex-shrink: 0; filter: grayscale(20%); }
  .dg-info { flex: 1; }
  .dg-name { font-family: 'Cormorant Garamond', serif; font-size: 1.6rem; font-weight: 600; color: var(--blanc); margin-bottom: 0.3rem; }
  .dg-title { font-size: 0.75rem; letter-spacing: 0.25em; color: var(--or); text-transform: uppercase; margin-bottom: 0.8rem; }
  .dg-desc { font-size: 0.88rem; color: var(--texte); line-height: 1.8; }
  .dg-badge { display: inline-flex; align-items: center; gap: 0.4rem; margin-top: 0.8rem; padding: 0.4rem 0.8rem; border: 1px solid rgba(201,168,76,0.3); font-size: 0.7rem; color: var(--or); letter-spacing: 0.15em; }
  /* FADE IN */
  .fade-in { opacity: 0; transform: translateY(25px); transition: opacity 0.8s ease, transform 0.8s ease; }
  .fade-in.visible { opacity: 1; transform: translateY(0); }

  /* RESPONSIVE */
  @media (max-width: 960px) {
    .apropos-grid, .contact-grid, .prob-sol-grid { grid-template-columns: 1fr; gap: 2.5rem; }
    .apropos-right { border-left: none; padding-left: 0; border-top: 1px solid var(--gris3); padding-top: 2rem; }
    .services-grid, .pourquoi-grid { grid-template-columns: 1fr 1fr; }
    .clients-grid { grid-template-columns: 1fr 1fr; }
    .valeurs-row { grid-template-columns: 1fr; }
    .hero-stats { display: none; }
    footer { justify-content: center; text-align: center; }
    .form-row { grid-template-columns: 1fr; }
  }
  @media (max-width: 600px) {
    nav ul { display: none; }
    .services-grid, .pourquoi-grid, .clients-grid { grid-template-columns: 1fr; }
    .audit-btns { flex-direction: column; align-items: center; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="logo">
    ATRIC SARL
    <span>African Trade and Industry Company</span>
  </div>
  <ul>
    <li><a href="#accueil">Accueil</a></li>
    <li><a href="#services">Services</a></li>
    <li><a href="#pourquoi">Pourquoi nous</a></li>
    <li><a href="#apropos">À propos</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<section id="accueil">
  <div class="hero-bg"></div>
  <div class="hero-img"></div>
  <div class="hero-line"></div>
  <div class="hero-content fade-in">
    <div class="hero-tag">Cameroun · Afrique · International</div>
    <h1><em>Groupe ATRIC</em><br>Expertise africaine<br>orientée rentabilité</h1>
    <p class="hero-subtitle">Groupe stratégique africain – Structuration, développement et optimisation de projets à forte rentabilité</p>
    <ul class="hero-liste">
      <li>Commerce international &amp; distribution optimisée</li>
      <li>Construction &amp; architecture moderne</li>
      <li>Agro-industrie rentable</li>
      <li>Conseil stratégique &amp; financement de projets</li>
      <li>Développement digital &amp; innovation</li>
      <li>Analyse &amp; montage des dossiers d'appels d'offres</li>
    </ul>
    <div style="margin-bottom:1.5rem;padding:1rem 1.5rem;border-left:2px solid var(--or);background:rgba(201,168,76,0.05);">
      <div style="font-size:0.8rem;color:var(--or);margin-bottom:0.3rem;">🎯 NOTRE MISSION</div>
      <div style="font-size:0.88rem;color:var(--texte);line-height:1.7;">Transformer les opportunités en investissements performants.</div>
      <div style="font-size:0.8rem;color:var(--or);margin-top:0.8rem;margin-bottom:0.3rem;">🚀 NOTRE VISION</div>
      <div style="font-size:0.88rem;color:var(--texte);line-height:1.7;">Bâtir un groupe africain de référence dans le commerce, l'industrie et l'innovation.</div>
    </div>
    <div class="hero-cta-group">
      <a href="#contact" class="btn">Contactez un expert ATRIC →</a>
      <a href="#services" class="btn btn-outline">Nos pôles stratégiques</a>
    </div>
  </div>
  <div class="hero-stats">
    <div class="stat">
      <div class="stat-num">4</div>
      <div class="stat-label">Secteurs stratégiques</div>
    </div>
    <div class="stat">
      <div class="stat-num">1</div>
      <div class="stat-label">Vision continentale</div>
    </div>
    <div class="stat">
      <div class="stat-num">∞</div>
      <div class="stat-label">Opportunités</div>
    </div>
  </div>
</section>

<!-- PROBLÈMES / SOLUTIONS -->
<section id="problemes">
  <div class="section-tag">Le problème que nous résolvons</div>
  <h2>Vos défis,<br>nos <em style="color:var(--or);font-style:normal;">solutions</em></h2>
  <div class="prob-sol-grid fade-in">
    <div class="prob-col">
      <h3>❌ Les problèmes fréquents</h3>
      <ul>
        <li>Difficulté à trouver des fournisseurs fiables</li>
        <li>Risque de pertes sur importation</li>
        <li>Faible visibilité digitale</li>
        <li>Projets non structurés et non rentables</li>
        <li>Délais et malfaçons dans la construction</li>
      </ul>
    </div>
    <div class="sol-col">
      <h3>✅ Notre solution ATRIC</h3>
      <ul>
        <li>Fournisseurs fiables, marges optimisées</li>
        <li>Sécurité douanière et logistique maîtrisée</li>
        <li>Visibilité digitale et acquisition clients</li>
        <li>Projets structurés, bancables et rentables</li>
        <li>Construction clé en main, dans les délais et le budget</li>
      </ul>
    </div>
  </div>
</section>

<!-- SERVICES -->
<section id="services">
  <div class="section-tag">Nos services</div>
  <h2>Ce que nous<br>faisons pour vous</h2>
  <div class="services-grid fade-in">

    <div class="service-card">
      <div class="service-num">01</div>
      <span class="service-icon">🏗️</span>
      <h3>Architecture & Construction</h3>
      <ul>
        <li>Conception et suivi de projets résidentiels, commerciaux et industriels</li>
        <li>Gestion complète des chantiers (plans, matériaux, fournisseurs)</li>
        <li>Construction clé en main ou sur mesure</li>
        <li>Conseil en investissement immobilier</li>
      </ul>
      <div class="service-impact">💡 Projet sûr, durable et livré dans les délais et le budget prévu</div>
    </div>

    <div class="service-card">
      <div class="service-num">02</div>
      <span class="service-icon">🌍</span>
      <h3>Import – Export & Distribution</h3>
      <ul>
        <li>Cheveux naturels (Inde, Vietnam)</li>
        <li>Cosmétiques et produits de beauté</li>
        <li>Compléments alimentaires et parfums</li>
        <li>Produits agroalimentaires</li>
      </ul>
      <div class="service-impact">💡 Fournisseurs fiables, marges optimisées, sécurité douanière et logistique</div>
    </div>

    <div class="service-card">
      <div class="service-num">03</div>
      <span class="service-icon">📊</span>
      <h3>Structuration de projets</h3>
      <ul>
        <li>Études de rentabilité et plan stratégique</li>
        <li>Optimisation des achats et coûts</li>
        <li>Plan de distribution et suivi performance</li>
      </ul>
      <div class="service-impact">💡 Transformer vos idées en projets viables et rentables</div>
    </div>

    <div class="service-card">
      <div class="service-num">04</div>
      <span class="service-icon">🌾</span>
      <h3>Développement agro-industriel</h3>
      <ul>
        <li>Projets agricoles et avicoles</li>
        <li>Montage et structuration du projet</li>
        <li>Conseil en financement et gestion stratégique</li>
      </ul>
      <div class="service-impact">💡 Projet rentable, structuré et prêt à croître</div>
    </div>

    <div class="service-card">
      <div class="service-num">05</div>
      <span class="service-icon">💻</span>
      <h3>Services Digitaux</h3>
      <ul>
        <li>Création de sites web professionnels</li>
        <li>Gestion de pages et réseaux sociaux</li>
        <li>Branding et marketing digital</li>
        <li>Accompagnement stratégique digital</li>
      </ul>
      <div class="service-impact">💡 Visibilité accrue, acquisition clients et digitalisation complète</div>
    </div>

    <div class="service-card">
      <div class="service-num">06</div>
      <span class="service-icon">💄</span>
      <h3>Cosmétiques & Beauté</h3>
      <ul>
        <li>Import et distribution de produits de soins</li>
        <li>Cosmétiques certifiés et adaptés au marché africain</li>
        <li>Conseil en référencement et distribution</li>
      </ul>
      <div class="service-impact">💡 Produits de qualité, marges optimisées, distribution sécurisée</div>
    </div>

    <div class="service-card" style="border-top: 2px solid var(--or); grid-column: 1 / -1;">
      <div class="service-num">07</div>
      <span class="service-icon">📋</span>
      <h3>Analyse & Montage des Dossiers d'Appels d'Offres</h3>
      <p style="font-size:0.88rem;color:var(--texte);margin-bottom:1rem;line-height:1.7;">ATRIC accompagne entreprises et investisseurs dans la conquête des marchés publics et privés. Nous transformons les opportunités institutionnelles en contrats remportés.</p>
      <ul>
        <li>Analyse des DAO (Dossier d'Appel d'Offres) et vérification des critères administratifs et techniques</li>
        <li>Montage complet des dossiers de soumission (technique et financier)</li>
        <li>Rédaction des offres techniques et financières optimisées</li>
        <li>Optimisation stratégique pour maximiser les chances d'attribution</li>
        <li>Suivi post-dépôt et accompagnement jusqu'à l'attribution du marché</li>
        <li>Partenariats institutionnels : projets publics, ONG, collectivités, partenaires internationaux</li>
      </ul>
      <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:1rem;margin-top:1.5rem;">
        <div style="padding:1rem;background:rgba(201,168,76,0.05);border:1px solid rgba(201,168,76,0.2);">
          <div style="font-size:0.7rem;letter-spacing:0.2em;color:var(--or);margin-bottom:0.5rem;">VALEUR AJOUTÉE</div>
          <ul style="list-style:none;">
            <li style="font-size:0.8rem;color:var(--texte);padding:0.25rem 0;display:flex;gap:0.5rem;"><span style="color:var(--or);">✓</span> Lecture stratégique du cahier des charges</li>
            <li style="font-size:0.8rem;color:var(--texte);padding:0.25rem 0;display:flex;gap:0.5rem;"><span style="color:var(--or);">✓</span> Structuration technique et financière optimisée</li>
            <li style="font-size:0.8rem;color:var(--texte);padding:0.25rem 0;display:flex;gap:0.5rem;"><span style="color:var(--or);">✓</span> Réduction des risques de rejet administratif</li>
          </ul>
        </div>
        <div style="padding:1rem;background:rgba(201,168,76,0.05);border:1px solid rgba(201,168,76,0.2);">
          <div style="font-size:0.7rem;letter-spacing:0.2em;color:var(--or);margin-bottom:0.5rem;">MARCHÉS CIBLÉS</div>
          <ul style="list-style:none;">
            <li style="font-size:0.8rem;color:var(--texte);padding:0.25rem 0;display:flex;gap:0.5rem;"><span style="color:var(--or);">→</span> Projets publics & collectivités</li>
            <li style="font-size:0.8rem;color:var(--texte);padding:0.25rem 0;display:flex;gap:0.5rem;"><span style="color:var(--or);">→</span> ONG & partenaires internationaux</li>
            <li style="font-size:0.8rem;color:var(--texte);padding:0.25rem 0;display:flex;gap:0.5rem;"><span style="color:var(--or);">→</span> Grandes entreprises privées</li>
          </ul>
        </div>
      </div>
      <div class="service-impact">🎯 Objectif : Transformer les opportunités publiques et privées en marchés remportés — ATRIC comme cabinet stratégique institutionnel</div>
    </div>

  </div>
</section>


<!-- ATRIC PUBLIC & INSTITUTIONAL -->
<section style="background:var(--noir);padding:5rem 5%;border-top:1px solid var(--gris3);">
  <div class="section-tag">Pôle institutionnel</div>
  <h2>ATRIC Public &<br><em style="color:var(--or);font-style:normal;">Institutional Services</em></h2>
  <p style="font-size:0.95rem;color:var(--texte);max-width:650px;line-height:1.9;margin-bottom:3rem;">Une branche spécialisée d'ATRIC SARL dédiée aux marchés institutionnels. Nous positionnons nos clients au niveau des grands projets publics, ONG et partenariats internationaux.</p>
  <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:1.5rem;margin-bottom:3rem;">
    <div style="background:var(--gris);border:1px solid var(--gris3);border-top:2px solid var(--or);padding:2rem;">
      <div style="font-size:1.8rem;margin-bottom:1rem;">🏛️</div>
      <h3 style="font-family:'Cormorant Garamond',serif;font-size:1.2rem;color:var(--or);margin-bottom:0.8rem;">Appels d'offres publics</h3>
      <p style="font-size:0.83rem;color:var(--texte);line-height:1.7;">Analyse, montage et soumission de dossiers pour les marchés publics locaux et nationaux.</p>
    </div>
    <div style="background:var(--gris);border:1px solid var(--gris3);border-top:2px solid var(--or);padding:2rem;">
      <div style="font-size:1.8rem;margin-bottom:1rem;">🤝</div>
      <h3 style="font-family:'Cormorant Garamond',serif;font-size:1.2rem;color:var(--or);margin-bottom:0.8rem;">Partenariats institutionnels</h3>
      <p style="font-size:0.83rem;color:var(--texte);line-height:1.7;">Facilitation de partenariats avec ONG, organisations internationales et collectivités territoriales.</p>
    </div>
    <div style="background:var(--gris);border:1px solid var(--gris3);border-top:2px solid var(--or);padding:2rem;">
      <div style="font-size:1.8rem;margin-bottom:1rem;">💰</div>
      <h3 style="font-family:'Cormorant Garamond',serif;font-size:1.2rem;color:var(--or);margin-bottom:0.8rem;">Montage de projets financés</h3>
      <p style="font-size:0.83rem;color:var(--texte);line-height:1.7;">Structuration de projets éligibles aux financements publics et aux investisseurs privés.</p>
    </div>
    <div style="background:var(--gris);border:1px solid var(--gris3);border-top:2px solid var(--or);padding:2rem;">
      <div style="font-size:1.8rem;margin-bottom:1rem;">📊</div>
      <h3 style="font-family:'Cormorant Garamond',serif;font-size:1.2rem;color:var(--or);margin-bottom:0.8rem;">Stratégie pour investisseurs</h3>
      <p style="font-size:0.83rem;color:var(--texte);line-height:1.7;">Identifier des marchés sécurisés → monter le dossier → proposer aux investisseurs → partager les bénéfices.</p>
    </div>
  </div>
  <div style="background:rgba(201,168,76,0.06);border:1px solid rgba(201,168,76,0.2);padding:2.5rem;text-align:center;">
    <div style="font-family:'Cormorant Garamond',serif;font-size:1.8rem;color:var(--blanc);margin-bottom:1rem;">ATRIC devient votre <em style="color:var(--or);">plateforme stratégique</em></div>
    <div style="display:flex;justify-content:center;gap:2rem;flex-wrap:wrap;margin-top:1.5rem;">
      <div style="text-align:center;"><div style="font-size:1.5rem;">🏢</div><div style="font-size:0.75rem;color:var(--or);letter-spacing:0.15em;margin-top:0.4rem;">GROUPE MULTISECTORIEL</div></div>
      <div style="text-align:center;"><div style="font-size:1.5rem;">💼</div><div style="font-size:0.75rem;color:var(--or);letter-spacing:0.15em;margin-top:0.4rem;">CABINET STRATÉGIQUE</div></div>
      <div style="text-align:center;"><div style="font-size:1.5rem;">🌍</div><div style="font-size:0.75rem;color:var(--or);letter-spacing:0.15em;margin-top:0.4rem;">FACILITATEUR D'INVESTISSEMENTS</div></div>
      <div style="text-align:center;"><div style="font-size:1.5rem;">🏛️</div><div style="font-size:0.75rem;color:var(--or);letter-spacing:0.15em;margin-top:0.4rem;">ACTEUR MARCHÉS PUBLICS</div></div>
    </div>
  </div>
</section>
<!-- POURQUOI NOUS -->
<section id="pourquoi">
  <div class="section-tag">Pourquoi nous choisir</div>
  <h2>La force<br><em style="color:var(--or);font-style:normal;">ATRIC SARL</em></h2>
  <p style="font-size:0.95rem;color:var(--texte);max-width:600px;line-height:1.9;margin-bottom:3rem;">ATRIC n'est pas juste une entreprise. C'est une <strong style="color:var(--blanc);">structure opportuniste stratégique</strong> — multisectorielle, fiable et tournée vers l'international.</p>
  <div class="pourquoi-grid fade-in">
    <div class="pourquoi-card">
      <div class="pourquoi-icon">🌍</div>
      <h3>Vision internationale</h3>
      <p>Connecter le local et le global. Nous pensons à l'échelle africaine et internationale pour maximiser vos opportunités.</p>
    </div>
    <div class="pourquoi-card">
      <div class="pourquoi-icon">💼</div>
      <h3>Approche stratégique</h3>
      <p>Rentabilité avant tout. Chaque projet est analysé, structuré et optimisé pour garantir des résultats mesurables.</p>
    </div>
    <div class="pourquoi-card">
      <div class="pourquoi-icon">🤝</div>
      <h3>Fiabilité & transparence</h3>
      <p>Engagement respecté. Parole donnée = parole tenue. La confiance est le fondement de chaque collaboration.</p>
    </div>
    <div class="pourquoi-card">
      <div class="pourquoi-icon">💡</div>
      <h3>Innovation stratégique</h3>
      <p>Solutions modernes et adaptées. Utilisation du digital et des meilleures pratiques internationales.</p>
    </div>
    <div class="pourquoi-card">
      <div class="pourquoi-icon">🏗️</div>
      <h3>Excellence en construction</h3>
      <p>Qualité et résultats mesurables. Chaque chantier est géré avec rigueur, dans les délais et le budget définis.</p>
    </div>
    <div class="pourquoi-card">
      <div class="pourquoi-icon">🎯</div>
      <h3>Expertise locale africaine</h3>
      <p>Nous connaissons le marché camerounais en profondeur. Notre ancrage local est notre avantage le plus puissant.</p>
    </div>
  </div>
  <div style="text-align:center;margin-top:3rem;">
    <a href="#contact" class="btn">Contactez-nous pour votre audit gratuit →</a>
  </div>
</section>


<!-- GROUPE ATRIC -->
<section style="background:var(--gris2);padding:6rem 5%;">
  <div class="section-tag">Structure du groupe</div>
  <h2>Le <em style="color:var(--or);font-style:normal;">Groupe ATRIC</em><br>Holding stratégique africaine</h2>
  <p style="font-size:0.95rem;color:var(--texte);max-width:650px;line-height:1.9;margin-bottom:3rem;">On passe de PME multisectorielle à <strong style="color:var(--blanc);">groupe stratégique africain structuré</strong>. Une holding avec 5 branches spécialisées qui attire banques, investisseurs et partenaires institutionnels.</p>
  <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:1.5rem;margin-bottom:3rem;">
    <div style="background:var(--noir);border:1px solid var(--gris3);border-top:3px solid var(--or);padding:2rem;transition:transform 0.3s;" onmouseover="this.style.transform='translateY(-4px)'" onmouseout="this.style.transform='translateY(0)'">
      <div style="font-size:1.8rem;margin-bottom:0.8rem;">🌍</div>
      <div style="font-size:0.65rem;letter-spacing:0.25em;color:var(--or);margin-bottom:0.5rem;">BRANCHE 01</div>
      <h3 style="font-family:'Cormorant Garamond',serif;font-size:1.15rem;color:var(--blanc);margin-bottom:0.6rem;">ATRIC Trade</h3>
      <p style="font-size:0.8rem;color:var(--texte);line-height:1.7;">Import-Export &amp; Distribution — Sourcing international, optimisation douanière, marges jusqu'à 100%</p>
    </div>
    <div style="background:var(--noir);border:1px solid var(--gris3);border-top:3px solid var(--or);padding:2rem;transition:transform 0.3s;" onmouseover="this.style.transform='translateY(-4px)'" onmouseout="this.style.transform='translateY(0)'">
      <div style="font-size:1.8rem;margin-bottom:0.8rem;">🏗️</div>
      <div style="font-size:0.65rem;letter-spacing:0.25em;color:var(--or);margin-bottom:0.5rem;">BRANCHE 02</div>
      <h3 style="font-family:'Cormorant Garamond',serif;font-size:1.15rem;color:var(--blanc);margin-bottom:0.6rem;">ATRIC Construction</h3>
      <p style="font-size:0.8rem;color:var(--texte);line-height:1.7;">Construction &amp; Engineering — Conception 2D/3D, suivi chantiers, projets résidentiels &amp; industriels</p>
    </div>
    <div style="background:var(--noir);border:1px solid var(--gris3);border-top:3px solid var(--or);padding:2rem;transition:transform 0.3s;" onmouseover="this.style.transform='translateY(-4px)'" onmouseout="this.style.transform='translateY(0)'">
      <div style="font-size:1.8rem;margin-bottom:0.8rem;">🌾</div>
      <div style="font-size:0.65rem;letter-spacing:0.25em;color:var(--or);margin-bottom:0.5rem;">BRANCHE 03</div>
      <h3 style="font-family:'Cormorant Garamond',serif;font-size:1.15rem;color:var(--blanc);margin-bottom:0.6rem;">ATRIC Agro</h3>
      <p style="font-size:0.8rem;color:var(--texte);line-height:1.7;">Agro-industrie &amp; Industry — Projets agricoles, avicoles, transformation locale, chaîne de valeur</p>
    </div>
    <div style="background:var(--noir);border:1px solid var(--gris3);border-top:3px solid var(--or);padding:2rem;transition:transform 0.3s;" onmouseover="this.style.transform='translateY(-4px)'" onmouseout="this.style.transform='translateY(0)'">
      <div style="font-size:1.8rem;margin-bottom:0.8rem;">💼</div>
      <div style="font-size:0.65rem;letter-spacing:0.25em;color:var(--or);margin-bottom:0.5rem;">BRANCHE 04</div>
      <h3 style="font-family:'Cormorant Garamond',serif;font-size:1.15rem;color:var(--blanc);margin-bottom:0.6rem;">ATRIC Consulting</h3>
      <p style="font-size:0.8rem;color:var(--texte);line-height:1.7;">Conseil &amp; Finance — Business plan, étude rentabilité, montage dossier bancaire, recherche investisseurs</p>
    </div>
    <div style="background:var(--noir);border:1px solid var(--gris3);border-top:3px solid var(--or);padding:2rem;transition:transform 0.3s;" onmouseover="this.style.transform='translateY(-4px)'" onmouseout="this.style.transform='translateY(0)'">
      <div style="font-size:1.8rem;margin-bottom:0.8rem;">💻</div>
      <div style="font-size:0.65rem;letter-spacing:0.25em;color:var(--or);margin-bottom:0.5rem;">BRANCHE 05</div>
      <h3 style="font-family:'Cormorant Garamond',serif;font-size:1.15rem;color:var(--blanc);margin-bottom:0.6rem;">ATRIC Digital</h3>
      <p style="font-size:0.8rem;color:var(--texte);line-height:1.7;">Digital Solutions — Sites web, réseaux sociaux, marketing digital, transformation numérique</p>
    </div>
  </div>
  <div style="background:rgba(201,168,76,0.06);border:1px solid rgba(201,168,76,0.2);padding:2rem;display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:1.5rem;">
    <div>
      <div style="font-family:'Cormorant Garamond',serif;font-size:1.4rem;color:var(--blanc);margin-bottom:0.5rem;">Cette structure attire :</div>
      <div style="display:flex;gap:1.5rem;flex-wrap:wrap;">
        <span style="font-size:0.8rem;color:var(--texte);">🏦 Banques</span>
        <span style="font-size:0.8rem;color:var(--texte);">💰 Investisseurs diaspora</span>
        <span style="font-size:0.8rem;color:var(--texte);">🌍 Partenaires internationaux</span>
        <span style="font-size:0.8rem;color:var(--texte);">🏛️ Institutions publiques</span>
      </div>
    </div>
    <a href="#contact" class="btn">Devenir partenaire →</a>
  </div>
</section>
<!-- CLIENTS -->
<section id="clients">
  <div class="section-tag">Nos clients &amp; partenaires</div>
  <h2>Nous accompagnons<br><em style="color:var(--or);font-style:normal;">4 profils</em> d'investisseurs</h2>
  <div class="clients-grid fade-in">
    <div class="client-card">
      <div class="client-icon">🏢</div>
      <p>PME locales et internationales cherchant à croître et se structurer</p>
    </div>
    <div class="client-card">
      <div class="client-icon">🛒</div>
      <p>Commerçants et distributeurs souhaitant optimiser leurs imports</p>
    </div>
    <div class="client-card">
      <div class="client-icon">💰</div>
      <p>Investisseurs et institutions à la recherche de projets rentables</p>
    </div>
    <div class="client-card">
      <div class="client-icon">🚀</div>
      <p>Particuliers ambitieux voulant bâtir un patrimoine durable</p>
    </div>
  </div>
</section>

<!-- À PROPOS -->
<section id="apropos">
  <div class="section-tag">À propos</div>
  <h2>Notre force principale :<br><em style="color:var(--or);font-style:normal;">Expertise multisectorielle africaine</em></h2>

      <!-- PHOTO DG -->
      <div class="dg-section fade-in">
        <img class="dg-photo" src="data:image/jpeg;base64,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" alt="M. Minkala Bilogue Victor Christian – Directeur Général ATRIC SARL">
        <div class="dg-info">
          <div class="dg-name">M. Minkala Bilogue Victor Christian</div>
          <div class="dg-title">Directeur Général – ATRIC SARL</div>
          <p class="dg-desc">Entrepreneur visionnaire et expert en stratégie multisectorielle africaine. Fort d'une expérience dans la construction, le commerce international, l'agro-industrie et le digital.</p>
          <div class="dg-badge">🤖 Expert IA & Innovation Stratégique</div>
        </div>
      </div>
  <div class="apropos-grid fade-in">
    <div class="apropos-text">
      <p>African Trade and Industry Company SARL (ATRIC SARL) est une société à responsabilité limitée fondée au Cameroun, animée par une vision claire : bâtir un groupe multisectoriel structuré, innovant et rentable au service du développement économique de l'Afrique.</p>
      <p>Nous aidons nos clients à :</p>
      <ul class="aide-liste">
        <li>Optimiser leurs marges</li>
        <li>Réduire les risques</li>
        <li>Développer des projets durables</li>
      </ul>
      <div class="mission-box">
        <h3>Notre Mission</h3>
        <p>Transformer vos idées en projets bancables et rentables, tout en construisant un patrimoine familial et un futur groupe solide.</p>
      </div>
      <div class="valeurs-row" style="margin-top:2rem;">
        <div class="valeur-bloc">
          <div class="valeur-num">01</div>
          <div class="valeur-titre">🤝 Fiabilité</div>
          <p>Respect des engagements. Transparence absolue. Parole donnée = parole respectée.</p>
        </div>
        <div class="valeur-bloc">
          <div class="valeur-num">02</div>
          <div class="valeur-titre">💡 Innovation</div>
          <p>Capacité d'adaptation. Utilisation du digital. Recherche constante d'opportunités.</p>
        </div>
        <div class="valeur-bloc">
          <div class="valeur-num">03</div>
          <div class="valeur-titre">🏆 Excellence</div>
          <p>Dans la construction, le digital, la gestion et les relations clients.</p>
        </div>
      </div>
    </div>
    <div class="apropos-right">
      <div class="info-block">
        <div class="info-label">Raison sociale</div>
        <div class="info-value">African Trade and Industry Company SARL</div>
      </div>
      <div class="info-block">
        <div class="info-label">Sigle</div>
        <div class="info-value">ATRIC SARL</div>
      </div>
      <div class="info-block">
        <div class="info-label">Forme juridique</div>
        <div class="info-value">Société à Responsabilité Limitée</div>
      </div>
      <div class="info-block">
        <div class="info-label">Siège social</div>
        <div class="info-value">Cameroun, Afrique centrale</div>
      </div>
      <div class="info-block">
        <div class="info-label">Directeur Général</div>
        <div class="info-value">M. Minkala Bilogue Victor Christian</div>
      </div>
      <div class="info-block">
        <div class="info-label">Email</div>
        <div class="info-value"><a href="/cdn-cgi/l/email-protection#d6b5b9b8a2b7b5a296b7a2a4bfb5a5b7a4baf8b5b9bb" style="color:var(--or);text-decoration:none;"><span class="__cf_email__" data-cfemail="5635393822373522163722243f352537243a7835393b">[email&#160;protected]</span></a></div>
      </div>
      <div class="info-block">
        <div class="info-label">WhatsApp</div>
        <div class="info-value"><a href="https://wa.me/639279344642" style="color:var(--or);text-decoration:none;">+63 927 934 4642</a></div>
      </div>
      <div class="info-block">
        <div class="info-label">Secteurs d'activité</div>
        <div class="info-value">Construction · Agro · Beauté · Digital</div>
      </div>
    </div>
  </div>
</section>

<!-- AUDIT CTA -->
<section id="audit">
  <div class="section-tag">Passez à l'action</div>
  <h2>Demandez votre<br><em style="color:var(--or);font-style:normal;">audit gratuit</em> aujourd'hui</h2>
  <p>Vous avez un projet ? Une idée ? Un besoin ? Parlons-en. Notre équipe analyse votre situation et vous propose une stratégie claire et rentable — sans engagement.</p>
  <div class="audit-btns">
    <a href="#contact" class="btn">Demander mon audit gratuit →</a>
    <a href="https://wa.me/639279344642" target="_blank" class="btn btn-outline">💬 Écrire sur WhatsApp</a>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="section-tag">Contact</div>
  <h2>Parlons de<br>votre projet</h2>
  <div class="contact-grid fade-in">
    <div class="contact-info">
      <p>Vous souhaitez collaborer avec ATRIC SARL, obtenir un devis ou demander votre audit gratuit ? Notre équipe est à votre disposition.</p>
      <div class="divider"></div>
      <div class="contact-block">
        <div class="contact-block-label">📧 Email</div>
        <div class="contact-links">
          <a href="/cdn-cgi/l/email-protection#096a66677d686a7d49687d7b606a7a687b65276a6664" class="contact-link">
            <span>✉️</span> <span class="__cf_email__" data-cfemail="a9cac6c7ddc8cadde9c8dddbc0cadac8dbc587cac6c4">[email&#160;protected]</span>
          </a>
        </div>
      </div>
      <div class="contact-block">
        <div class="contact-block-label">💬 WhatsApp</div>
        <div class="contact-links">
          <a href="https://wa.me/639279344642" target="_blank" class="contact-link wa">
            <span>💬</span> +63 927 934 4642
          </a>
        </div>
      </div>
      <div class="contact-block">
        <div class="contact-block-label">📞 Téléphone</div>
        <div class="contact-links">
          <a href="tel:+237620719040" class="contact-link"><span>📞</span> +237 6 20 71 90 40</a>
          <a href="tel:+237656714402" class="contact-link"><span>📞</span> +237 656 714 402</a>
        </div>
      </div>
      <div class="contact-block">
        <div class="contact-block-label">📍 Siège social</div>
        <div style="font-size:0.9rem;color:var(--blanc);">Cameroun, Afrique centrale</div>
      </div>
    </div>
    <div>
      <form id="contactForm" onsubmit="handleSubmit(event)">
        <div class="form-row">
          <input type="text" name="nom" placeholder="Votre nom" required>
          <input type="email" name="email" placeholder="Votre email" required>
        </div>
        <div class="form-row">
          <input type="text" name="societe" placeholder="Société (optionnel)">
          <input type="tel" name="telephone" placeholder="Votre téléphone">
        </div>
        <select name="departement">
          <option value="" disabled selected>Service concerné</option>
          <option>Architecture &amp; Construction</option>
          <option>Import – Export &amp; Distribution</option>
          <option>Structuration de projets</option>
          <option>Développement agro-industriel</option>
          <option>Services Digitaux</option>
          <option>Cosmétiques &amp; Beauté</option>
          <option>Audit gratuit</option>
          <option>Direction Générale</option>
        </select>
        <textarea name="message" placeholder="Décrivez votre projet ou votre demande..."></textarea>
        <div class="success-msg" id="successMsg">✓ Votre message a bien été envoyé. Nous vous répondrons dans les plus brefs délais.</div>
        <div class="error-msg" id="errorMsg">✗ Une erreur s'est produite. Contactez-nous directement par WhatsApp ou téléphone.</div>
        <button type="submit">Envoyer ma demande →</button>
      </form>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-logo">
    ATRIC SARL
    <span>African Trade and Industry Company</span>
  </div>
  <div class="footer-links">
    <a href="#accueil">Accueil</a>
    <a href="#services">Services</a>
    <a href="#pourquoi">Pourquoi nous</a>
    <a href="#apropos">À propos</a>
    <a href="#contact">Contact</a>
    <a href="https://wa.me/639279344642" target="_blank">💬 WhatsApp</a>
  </div>
  <p class="copy">© 2026 ATRIC SARL · Cameroun · Tous droits réservés</p>
</footer>

<!-- EmailJS -->
<script data-cfasync="false" src="/cdn-cgi/scripts/5c5dd728/cloudflare-static/email-decode.min.js"></script><script src="https://cdn.jsdelivr.net/npm/@emailjs/browser@4/dist/email.min.js"></script>
<script>
  emailjs.init('yfOY9Xmgxf1QGLbbv');

  const observer = new IntersectionObserver((entries) => {
    entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); });
  }, { threshold: 0.08 });
  document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));
  setTimeout(() => {
    const h = document.querySelector('#accueil .fade-in');
    if (h) h.classList.add('visible');
  }, 100);

  function handleSubmit(e) {
    e.preventDefault();
    const form = e.target;
    const btn = form.querySelector('button[type="submit"]');
    const successMsg = document.getElementById('successMsg');
    const errorMsg = document.getElementById('errorMsg');
    const templateParams = {
      nom: form.nom.value.trim(),
      email: form.email.value.trim(),
      societe: form.societe.value.trim() || 'Non renseignée',
      telephone: form.telephone.value.trim() || 'Non renseigné',
      departement: form.departement.value || 'Non précisé',
      message: form.message.value.trim()
    };
    successMsg.style.display = 'none';
    errorMsg.style.display = 'none';
    btn.textContent = 'Envoi en cours...';
    btn.disabled = true;
    emailjs.send('service_dwlllnf', 'template_z1ka86p', templateParams)
      .then(() => {
        successMsg.style.display = 'block';
        btn.textContent = 'Message envoyé ✓';
        btn.style.background = 'var(--or)';
        btn.style.color = 'var(--noir)';
        form.reset();
        setTimeout(() => {
          successMsg.style