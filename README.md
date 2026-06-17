[index.html](https://github.com/user-attachments/files/29059132/index.html)
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Baptiste Galon — Assistant de Production</title>
  <meta name="description" content="Portfolio de Baptiste Galon, étudiant audiovisuel option Gestion de Production." />

  <style>
    @import url('https://fonts.googleapis.com/css2?family=Helvetica+Neue:wght@700&display=swap');

    :root {
      --bg:        #e8e6e2;
      --bg2:       #dedad5;
      --bg3:       #d2cec8;
      --surface:   #e0ddd8;
      --ink:       #1a1917;
      --muted:     #6b6863;
      --subtle:    #9e9b97;
      --accent:    #1a1917;
      --border:    rgba(26,25,23,.1);
      --border2:   rgba(26,25,23,.2);
      --max:       1100px;
      --nav-h:     58px;
    }

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; -webkit-font-smoothing: antialiased; }
    body {
      background: var(--bg);
      color: var(--ink);
      font-family: Helvetica, Arial, sans-serif;
      font-size: 15px;
      line-height: 1.65;
    }
    img  { max-width: 100%; display: block; object-fit: cover; }
    a    { color: inherit; text-decoration: none; }
    ul, ol { list-style: none; }

    .container { max-width: var(--max); margin: 0 auto; padding: 0 40px; }
    .section    { padding: 100px 0; }
    .section--alt { background: var(--bg2); }

    /* ─── Type ───────────────────────────────────────────────── */
    h1 {
      font-family: Helvetica, Arial, sans-serif;
      font-size: clamp(5rem, 14vw, 11rem);
      font-weight: 700;
      line-height: .9;
      letter-spacing: -.06em;
    }
    h2 {
      font-family: Helvetica, Arial, sans-serif;
      font-size: clamp(1.6rem, 3vw, 2.2rem);
      font-weight: 700;
      letter-spacing: -.03em;
      line-height: 1.1;
    }
    h3 {
      font-family: Helvetica, Arial, sans-serif;
      font-weight: 700;
      font-size: .95rem;
      letter-spacing: -.01em;
    }
    .label {
      font-size: .62rem;
      font-weight: 700;
      letter-spacing: .18em;
      text-transform: uppercase;
      color: var(--muted);
    }

    /* ─── Nav ─────────────────────────────────────────────────── */
    .nav {
      position: fixed; top: 0; left: 0; right: 0;
      height: var(--nav-h); z-index: 100;
      background: rgba(232,230,226,.92);
      backdrop-filter: blur(20px);
      border-bottom: 1px solid var(--border);
      display: flex; align-items: center;
    }
    .nav__inner {
      width: 100%; max-width: var(--max);
      margin: 0 auto; padding: 0 40px;
      display: flex; align-items: center; justify-content: space-between;
    }
    .nav__logo {
      font-size: .72rem; font-weight: 700;
      letter-spacing: .14em; text-transform: uppercase;
      color: var(--ink);
    }
    .nav__links {
      display: flex; gap: 36px;
      font-size: .68rem; color: var(--muted);
      font-weight: 700; letter-spacing: .1em; text-transform: uppercase;
    }
    .nav__links a { transition: color .2s; }
    .nav__links a:hover { color: var(--ink); }
    .nav__cta {
      font-size: .68rem; font-weight: 700;
      letter-spacing: .1em; text-transform: uppercase;
      padding: 8px 18px;
      border: 1px solid var(--border2);
      background: transparent; color: var(--ink); transition: all .2s;
    }
    .nav__cta:hover { background: var(--ink); color: var(--bg); }

    /* ─── Hero ─────────────────────────────────────────────────── */
    .hero {
      min-height: 100svh;
      display: grid;
      grid-template-rows: auto 1fr auto;
      padding-top: var(--nav-h);
      background: var(--bg);
      border-bottom: 1px solid var(--border2);
      overflow: hidden;
    }
    .hero__title-wrap {
      padding: 52px 40px 0;
      max-width: var(--max);
      margin: 0 auto;
      width: 100%;
    }
    .hero__title-wrap h1 {
      font-size: clamp(4.5rem, 13vw, 10.5rem);
      font-weight: 700;
      line-height: .88;
      letter-spacing: .06em;
      color: var(--ink);
    }
    .hero__main {
      display: flex;
      align-items: flex-end;
      padding: 0 40px 48px;
      max-width: var(--max);
      margin: 0 auto;
      width: 100%;
    }
    .hero__meta {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      gap: 24px;
      padding-bottom: 12px;
      max-width: 480px;
    }
    .hero__role {
      font-size: .72rem;
      font-weight: 700;
      letter-spacing: .14em;
      text-transform: uppercase;
      color: var(--muted);
      text-align: left;
    }
    .hero__desc {
      font-size: .9rem;
      color: var(--muted);
      line-height: 1.75;
      text-align: left;
    }
    .hero__bar {
      border-top: 1px solid var(--border2);
      padding: 20px 40px;
      max-width: var(--max);
      margin: 0 auto;
      width: 100%;
      display: flex;
      gap: 16px;
    }
    .btn {
      display: inline-flex; align-items: center; gap: 8px;
      padding: 10px 22px;
      font-family: Helvetica, Arial, sans-serif;
      font-size: .68rem; font-weight: 700;
      letter-spacing: .1em; text-transform: uppercase;
      cursor: pointer; transition: all .2s;
      border: 1px solid var(--border2);
    }
    .btn--primary { background: var(--ink); color: var(--bg); border-color: var(--ink); }
    .btn--primary:hover { background: var(--muted); border-color: var(--muted); }
    .btn--ghost   { background: transparent; color: var(--ink); }
    .btn--ghost:hover { background: var(--ink); color: var(--bg); }

    /* ─── Section header ────────────────────────────────────── */
    .sec-head { margin-bottom: 60px; }
    .sec-head h2 { margin-top: 8px; }
    .sec-line { height: 1px; background: var(--border2); margin-top: 20px; }

    /* ─── À propos ──────────────────────────────────────────── */
    .about__grid { display: grid; grid-template-columns: 1fr 320px; gap: 80px; align-items: start; }
    .about__body {
      color: var(--muted); font-size: .93rem; line-height: 1.85; margin-bottom: 20px;
    }
    .about__body strong { color: var(--ink); font-weight: 700; }
    .skills__title {
      font-size: .58rem; font-weight: 700; letter-spacing: .18em;
      text-transform: uppercase; color: var(--subtle); margin-bottom: 12px;
    }
    .skills__list  { display: flex; flex-wrap: wrap; gap: 6px; margin-bottom: 28px; }
    .skill-pill {
      font-size: .68rem; font-weight: 700; padding: 4px 11px;
      border: 1px solid var(--border2);
      color: var(--muted); letter-spacing: .03em; transition: all .2s;
    }
    .skill-pill:hover { border-color: var(--ink); color: var(--ink); }
    .lang-row { display: flex; gap: 8px; }
    .lang-badge {
      display: flex; align-items: center; gap: 8px;
      padding: 6px 12px;
      border: 1px solid var(--border2); font-size: .78rem;
    }
    .lang-badge strong { font-weight: 700; }
    .lang-badge span   { color: var(--muted); font-size: .68rem; }

    .timeline { display: flex; flex-direction: column; margin-top: 8px; }
    .timeline-item {
      display: grid; grid-template-columns: 72px 1fr;
      gap: 16px; padding: 16px 0; border-bottom: 1px solid var(--border);
    }
    .timeline-item:last-child { border-bottom: none; }
    .timeline__date { font-size: .65rem; font-weight: 700; color: var(--subtle); letter-spacing: .06em; padding-top: 2px; }
    .timeline__body h4 { font-size: .88rem; font-weight: 700; margin-bottom: 2px; }
    .timeline__body p  { font-size: .78rem; color: var(--muted); }

    /* ─── Experience cards ──────────────────────────────────── */
    .cards-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
      gap: 1px;
      border: 1px solid var(--border2);
    }
    .exp-card {
      background: var(--surface);
      transition: background .2s;
      padding: 32px;
    }
    .exp-card:hover { background: var(--bg3); }
    .exp-card--featured { border-left: 3px solid var(--ink); }
    .exp-card__tag {
      display: inline-flex; align-items: center; gap: 6px;
      font-size: .58rem; font-weight: 700; letter-spacing: .14em;
      text-transform: uppercase; color: var(--muted); margin-bottom: 14px;
    }
    .exp-card__tag-dot {
      width: 5px; height: 5px;
      background: var(--ink); flex-shrink: 0;
    }
    .exp-card__tag-dot--live {
      animation: pulse 2.4s ease-in-out infinite;
    }
    @keyframes pulse { 0%,100%{opacity:1} 50%{opacity:.3} }
    .exp-card__title   { font-size: 1rem; font-weight: 700; margin-bottom: 4px; }
    .exp-card__company { font-size: .72rem; font-weight: 700; color: var(--muted); text-transform: uppercase; letter-spacing: .08em; margin-bottom: 3px; }
    .exp-card__period  { font-size: .68rem; color: var(--subtle); margin-bottom: 16px; }
    .exp-card__desc    { font-size: .85rem; color: var(--muted); line-height: 1.75; }
    .exp-card__chips   { display: flex; flex-wrap: wrap; gap: 5px; margin-top: 18px; }
    .chip {
      font-size: .6rem; font-weight: 700; letter-spacing: .06em;
      text-transform: uppercase; padding: 3px 8px;
      border: 1px solid var(--border2); color: var(--muted);
    }

    /* ─── Note coming soon ──────────────────────────────────── */
    .coming-soon-note {
      grid-column: 1 / -1;
      background: var(--surface);
      padding: 28px 32px;
      border-top: 1px solid var(--border);
      display: flex;
      align-items: center;
      gap: 16px;
    }
    .coming-soon-note__dash {
      width: 24px;
      height: 1px;
      background: var(--subtle);
      flex-shrink: 0;
    }
    .coming-soon-note p {
      font-size: .82rem;
      color: var(--subtle);
      font-weight: 700;
      letter-spacing: .04em;
      font-style: italic;
    }

    /* ─── Projects ─────────────────────────────────────────── */
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
      gap: 1px;
      border: 1px solid var(--border2);
    }
    .proj-card {
      background: var(--surface);
      overflow: hidden;
      transition: background .2s;
    }
    .proj-card:hover { background: var(--bg3); }

    .proj-card__media {
      width: 100%; aspect-ratio: 16/9;
      background: var(--bg3);
      overflow: hidden; position: relative;
    }
    .proj-card__media a {
      display: block;
      width: 100%; height: 100%;
      position: relative;
    }
    .proj-card__media img {
      width: 100%; height: 100%;
      object-fit: cover;
      filter: grayscale(20%);
      transition: filter .4s, transform .4s;
    }
    .proj-card:hover .proj-card__media img {
      filter: grayscale(0%);
      transform: scale(1.02);
    }
    .proj-card__play {
      position: absolute; top: 50%; left: 50%;
      transform: translate(-50%,-50%);
      width: 44px; height: 44px;
      background: rgba(26,25,23,.75);
      display: flex; align-items: center; justify-content: center;
      transition: background .2s, transform .2s;
    }
    .proj-card:hover .proj-card__play {
      background: rgba(26,25,23,.9);
      transform: translate(-50%,-50%) scale(1.08);
    }
    .proj-card__media-title {
      width: 100%; height: 100%;
      display: flex; align-items: center; justify-content: center;
      background: var(--ink); color: var(--bg);
      font-family: Helvetica, Arial, sans-serif;
      font-size: clamp(1.3rem, 2.6vw, 1.6rem); font-weight: 700;
      letter-spacing: -.01em; text-transform: uppercase;
      text-align: center; padding: 20px; line-height: 1.15;
      transition: opacity .2s;
    }
    .proj-card:hover .proj-card__media-title { opacity: .85; }
    .proj-card__body { padding: 24px; }
    .proj-card__type {
      font-size: .58rem; font-weight: 700; letter-spacing: .16em;
      text-transform: uppercase; color: var(--subtle); margin-bottom: 8px;
    }
    .proj-card__title { font-weight: 700; font-size: .95rem; margin-bottom: 10px; }
    .proj-card__desc  { font-size: .83rem; color: var(--muted); line-height: 1.75; margin-bottom: 16px; }
    .proj-card__link  {
      font-size: .65rem; font-weight: 700; color: var(--ink);
      text-transform: uppercase; letter-spacing: .1em;
      display: inline-flex; align-items: center; gap: 6px;
      border-bottom: 1px solid var(--border2);
      padding-bottom: 2px;
      transition: border-color .2s;
    }
    .proj-card__link:hover { border-color: var(--ink); }

    /* ─── Bénévolat ─────────────────────────────────────────── */
    .benev-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
      gap: 1px;
      border: 1px solid var(--border2);
    }
    .benev-card {
      background: var(--surface);
      padding: 28px;
      transition: background .2s;
    }
    .benev-card:hover { background: var(--bg3); }
    .benev-card__date  { font-size: .58rem; font-weight: 700; color: var(--subtle); letter-spacing: .14em; text-transform: uppercase; margin-bottom: 10px; }
    .benev-card__role  { font-weight: 700; font-size: .95rem; margin-bottom: 3px; }
    .benev-card__event { font-size: .72rem; font-weight: 700; color: var(--muted); text-transform: uppercase; letter-spacing: .06em; margin-bottom: 12px; }
    .benev-card__desc  { font-size: .83rem; color: var(--muted); line-height: 1.7; }

    /* ─── Contact ───────────────────────────────────────────── */
    .contact__wrap {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 80px;
      align-items: start;
    }
    .contact__body {
      color: var(--muted); font-size: .93rem; line-height: 1.85; margin-bottom: 40px;
    }
    .contact__links { display: flex; flex-direction: column; gap: 1px; border: 1px solid var(--border2); }
    .contact__link {
      display: flex; align-items: center; gap: 16px;
      padding: 16px 20px;
      background: var(--surface);
      transition: background .2s;
    }
    .contact__link:hover { background: var(--bg3); }
    .contact__link-icon {
      width: 30px; height: 30px;
      background: var(--bg3);
      border: 1px solid var(--border2);
      display: flex; align-items: center; justify-content: center;
      font-size: .78rem; flex-shrink: 0; font-weight: 700;
    }
    .contact__link-label {
      font-size: .58rem; font-weight: 700; color: var(--subtle);
      text-transform: uppercase; letter-spacing: .12em; margin-bottom: 2px;
    }
    .contact__link-val   { font-size: .85rem; font-weight: 700; }

    .contact__right {
      padding-top: 8px;
    }
    .contact__big {
      font-size: clamp(3rem, 6vw, 5rem);
      font-weight: 700;
      letter-spacing: -.05em;
      line-height: .95;
      margin-bottom: 32px;
      color: var(--ink);
    }
    .contact__tagline {
      font-size: .85rem;
      color: var(--muted);
      line-height: 1.8;
      border-left: 1px solid var(--border2);
      padding-left: 20px;
    }

    /* ─── Footer ─────────────────────────────────────────────── */
    .footer {
      background: var(--ink); color: rgba(232,230,226,.4);
      padding: 36px 0;
    }
    .footer__inner { display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 16px; }
    .footer__logo { font-size: .72rem; font-weight: 700; text-transform: uppercase; letter-spacing: .1em; color: var(--bg); }
    .footer__links {
      display: flex; gap: 28px;
      font-size: .65rem; font-weight: 700; text-transform: uppercase; letter-spacing: .08em;
    }
    .footer__links a { transition: color .2s; }
    .footer__links a:hover { color: var(--bg); }
    .footer__copy { font-size: .65rem; }

    /* ─── Reveal ─────────────────────────────────────────────── */
    .reveal { opacity: 0; transform: translateY(14px); transition: opacity .6s ease, transform .6s ease; }
    .reveal.visible { opacity: 1; transform: none; }

    /* ─── Responsive ─────────────────────────────────────────── */
    @media (max-width: 820px) {
      .hero__main { flex-direction: column; align-items: flex-start; gap: 32px; }
      .hero__meta { align-items: flex-start; text-align: left; max-width: 100%; }
      .hero__meta .hero__role, .hero__meta .hero__desc { text-align: left; }
      .about__grid, .contact__wrap { grid-template-columns: 1fr; gap: 48px; }
      .nav__links { display: none; }
      .cards-grid, .projects-grid, .benev-grid { grid-template-columns: 1fr; }
    }
  </style>
</head>
<body>

  <!-- ═══ NAV ══════════════════════════════════════════════ -->
  <nav class="nav">
    <div class="nav__inner">
      <span class="nav__logo">Baptiste Galon</span>
      <ul class="nav__links">
        <li><a href="#apropos">Profil</a></li>
        <li><a href="#pro">Expériences</a></li>
        <li><a href="#projets">Projets</a></li>
        <li><a href="#benevolat">Bénévolat</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
      <a href="#contact" class="nav__cta">Me contacter</a>
    </div>
  </nav>

  <!-- ═══ HERO ══════════════════════════════════════════════ -->
  <section class="hero" id="accueil">
    <div class="hero__title-wrap">
      <h1>Baptiste<br>Galon</h1>
    </div>
    <div class="hero__main">
      <div class="hero__meta">
        <div class="hero__role">Assistant de production<br>Étudiant audiovisuel</div>
        <p class="hero__desc">
          Passionné par le cinéma et sa phase de production. J'ai accompagné des équipes dans des structures variées : courts métrages, documentaires, festivals. Je construis mon parcours projet après projet.
        </p>
      </div>
    </div>
    <div class="hero__bar">
      <a href="#pro" class="btn btn--primary">Mes expériences</a>
      <a href="#contact" class="btn btn--ghost">Me contacter</a>
    </div>
  </section>

  <!-- ═══ PROFIL ════════════════════════════════════════════ -->
  <section class="section section--alt" id="apropos">
    <div class="container">
      <div class="sec-head reveal">
        <div><span class="label">Profil</span><h2>Qui suis-je</h2></div>
        <div class="sec-line"></div>
      </div>

      <div class="about__grid">
        <div class="reveal">
          <p class="about__body">
            Actuellement en fin de <strong>BTS Métiers de l'Audiovisuel option Gestion de Production,</strong>
            je me forme aux métiers qui font exister les projets : de la recherche de financement à la coordination logistique sur le terrain. Je recherche actuellement une alternance à Paris pour le mois de septembre 2026.
          </p>
          <p class="about__body">
            Mon parcours est à la croisée de la culture cinématographique et de l'organisation :
            stages, apprentissage en sociétés de production, bénévolat dans des festivals,
            et un travail personnel autour de la critique visuelle avec <strong>@BANECI_FRANCE</strong>.
          </p>
          <p class="about__body">
            Avant l'audiovisuel, j'ai suivi une <strong>Licence Histoire et Science-Politique,</strong>
            ce qui nourrit ma lecture des projets et ma capacité d'analyse.
          </p>
          <div style="margin-top:40px">
            <div class="skills__title">Parcours</div>
            <div class="timeline">
              <div class="timeline-item">
                <span class="timeline__date">2026–27</span>
                <div class="timeline__body">
                  <h4>Licence Gestion de la production audiovisuelle</h4>
                  <p>Animation, cinéma et télévision — GOBELINS, Paris</p>
                </div>
              </div>
              <div class="timeline-item">
                <span class="timeline__date">2024–26</span>
                <div class="timeline__body">
                  <h4>BTS Audiovisuel — Gestion de production</h4>
                  <p>Studio M, Angers</p>
                </div>
              </div>
              <div class="timeline-item">
                <span class="timeline__date">2022–24</span>
                <div class="timeline__body">
                  <h4>Licence Histoire &amp; Science-Politique (Bac+1)</h4>
                  <p>Institut Catholique de Rennes</p>
                </div>
              </div>
              <div class="timeline-item">
                <span class="timeline__date">2022</span>
                <div class="timeline__body">
                  <h4>Certificate Kaplan</h4>
                  <p>Séjour linguistique d'un mois au Canada</p>
                </div>
              </div>
              <div class="timeline-item">
                <span class="timeline__date">2019–22</span>
                <div class="timeline__body">
                  <h4>Bac général HGGSP / SES</h4>
                  <p>Lycée Sévigné, Rennes</p>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="reveal" style="transition-delay:.1s">
          <div class="skills__title">Compétences métier</div>
          <div class="skills__list">
            <span class="skill-pill">Gestion de production</span>
            <span class="skill-pill">Recherche de financement</span>
            <span class="skill-pill">Comptabilité</span>
            <span class="skill-pill">Budget</span>
            <span class="skill-pill">Fiches de lecture</span>
            <span class="skill-pill">Distribution festivals</span>
            <span class="skill-pill">Logistique</span>
          </div>
          <div class="skills__title" style="margin-top:24px">Outils</div>
          <div class="skills__list">
            <span class="skill-pill">Premiere Pro</span>
            <span class="skill-pill">DaVinci Resolve</span>
            <span class="skill-pill">Photoshop</span>
            <span class="skill-pill">Canva</span>
            <span class="skill-pill">AirTable</span>
            <span class="skill-pill">WordPress</span>
            <span class="skill-pill">Suite Microsoft</span>
          </div>
          <div class="skills__title" style="margin-top:24px">Langues</div>
          <div class="lang-row">
            <div class="lang-badge"><strong>Anglais</strong><span>B2</span></div>
            <div class="lang-badge"><strong>Espagnol</strong><span>B1</span></div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ═══ EXPÉRIENCES PRO ══════════════════════════════════ -->
  <section class="section" id="pro">
    <div class="container">
      <div class="sec-head reveal">
        <div><span class="label">Expériences professionnelles</span><h2>Stages &amp; alternance</h2></div>
        <div class="sec-line"></div>
      </div>

      <div class="cards-grid reveal">

        <!-- Contrat d'apprentissage -->
        <div class="exp-card exp-card--featured">
          <div class="exp-card__tag">
            <span class="exp-card__tag-dot exp-card__tag-dot--live"></span>
            Contrat d'apprentissage · En cours
          </div>
          <div class="exp-card__title">Coorigines Production</div>
          <div class="exp-card__company">Rennes</div>
          <div class="exp-card__period">Septembre 2025 – Août 2026</div>
          <p class="exp-card__desc">Optimisation et gestion des fichiers de projections. Préparation logistique et technique. Distribution des films dans les festivals. Dépôt des dossiers de production. Chargé de mission au Festival International de Court Métrage de Clermont-Ferrand.</p>
          <div class="exp-card__chips">
            <span class="chip">Production</span>
            <span class="chip">Distribution</span>
            <span class="chip">Festival</span>
            <span class="chip">Cinéma</span>
          </div>
        </div>

        <!-- Coorigines Production -->
        <div class="exp-card">
          <div class="exp-card__tag">
            <span class="exp-card__tag-dot"></span>
            Stage · Assistant de production
          </div>
          <div class="exp-card__title">Coorigines Production</div>
          <div class="exp-card__company">Rennes</div>
          <div class="exp-card__period">Juin – Juillet 2025</div>
          <p class="exp-card__desc">Optimisation et gestion des fichiers de projections. Préparation logistique et technique. Distribution des films dans les festivals. Dépôt des dossiers de production.</p>
          <div class="exp-card__chips">
            <span class="chip">Distribution</span>
            <span class="chip">Logistique</span>
            <span class="chip">Festival</span>
            <span class="chip">Cinéma</span>
          </div>
        </div>

        <!-- Puffin Pictures -->
        <div class="exp-card">
          <div class="exp-card__tag">
            <span class="exp-card__tag-dot"></span>
            Stage · Assistant de production
          </div>
          <div class="exp-card__title">Puffin Pictures</div>
          <div class="exp-card__company">Rennes</div>
          <div class="exp-card__period">Mars – Mai 2025</div>
          <p class="exp-card__desc">Lecture et analyse de scénarios (fiches de lecture). Montage de dossiers de production. Recherche de financements pour les projets en développement.</p>
          <div class="exp-card__chips">
            <span class="chip">Fiches de lecture</span>
            <span class="chip">Développement</span>
            <span class="chip">Financement</span>
          </div>
        </div>

      </div>
    </div>
  </section>

  <!-- ═══ PROJETS ══════════════════════════════════════════ -->
  <section class="section section--alt" id="projets">
    <div class="container">
      <div class="sec-head reveal">
        <div><span class="label">Créations &amp; réalisations</span><h2>Projets</h2></div>
        <div class="sec-line"></div>
      </div>

      <div class="projects-grid reveal">

        <!-- Projet 1 — Raphaëlle -->
        <div class="proj-card">
          <div class="proj-card__media">
            <a href="https://youtu.be/blX6DaO5GJ4" target="_blank" rel="noopener">
              <img src="https://img.youtube.com/vi/blX6DaO5GJ4/hqdefault.jpg" alt="Raphaëlle EPK" />
              <div class="proj-card__play">
                <svg width="14" height="14" viewBox="0 0 24 24" fill="white"><polygon points="5 3 19 12 5 21 5 3"/></svg>
              </div>
            </a>
          </div>
          <div class="proj-card__body">
            <div class="proj-card__type">EPK</div>
            <div class="proj-card__title">Raphaëlle [Chargé de production]</div>
            <p class="proj-card__desc">Originaire d'Angers, Raphaëlle est une artiste singulière à la croisée de la chanson française, de la pop et du jazz. À l'approche de la sortie de son EP, cet EPK lève le voile sur une artiste en plein essor, révélant les coulisses de son univers et ses inspirations profondes.</p>
            <a href="https://youtu.be/blX6DaO5GJ4" target="_blank" rel="noopener" class="proj-card__link">Voir le projet →</a>
          </div>
        </div>

        <!-- Projet 2 — Rugby Santé -->
        <div class="proj-card">
          <div class="proj-card__media">
            <a href="https://youtu.be/iW7Z_VvA4IE" target="_blank" rel="noopener">
              <img src="https://img.youtube.com/vi/iW7Z_VvA4IE/hqdefault.jpg" alt="Rugby Santé" />
              <div class="proj-card__play">
                <svg width="14" height="14" viewBox="0 0 24 24" fill="white"><polygon points="5 3 19 12 5 21 5 3"/></svg>
              </div>
            </a>
          </div>
          <div class="proj-card__body">
            <div class="proj-card__type">Reportage</div>
            <div class="proj-card__title">Rugby Santé [Chargé de production]</div>
            <p class="proj-card__desc">Le rugby comme remède. En six minutes, ce reportage part à la rencontre de l'association Rugby Santé de Saumur, où le sport adapté transforme des vies.</p>
            <a href="https://youtu.be/iW7Z_VvA4IE" target="_blank" rel="noopener" class="proj-card__link">Voir le projet →</a>
          </div>
        </div>

        <!-- Projet 3 — La poursuite -->
        <div class="proj-card">
          <div class="proj-card__media">
            <a href="https://youtu.be/k9oW1TIZlVo" target="_blank" rel="noopener">
              <img src="https://img.youtube.com/vi/k9oW1TIZlVo/hqdefault.jpg" alt="La poursuite" />
              <div class="proj-card__play">
                <svg width="14" height="14" viewBox="0 0 24 24" fill="white"><polygon points="5 3 19 12 5 21 5 3"/></svg>
              </div>
            </a>
          </div>
          <div class="proj-card__body">
            <div class="proj-card__type">Court-métrage</div>
            <div class="proj-card__title">La poursuite [Réalisateur]</div>
            <p class="proj-card__desc">Dans un silence oppressant, un homme court — mais ce qui le traque est peut-être moins extérieur qu'il n'y paraît.</p>
            <a href="https://youtu.be/k9oW1TIZlVo" target="_blank" rel="noopener" class="proj-card__link">Voir le projet →</a>
          </div>
        </div>

        <!-- Projet 4 — Casse-tête -->
        <div class="proj-card">
          <div class="proj-card__media">
            <a href="https://youtu.be/w4LWra-mdzs" target="_blank" rel="noopener">
              <img src="https://img.youtube.com/vi/w4LWra-mdzs/hqdefault.jpg" alt="Casse-tête" />
              <div class="proj-card__play">
                <svg width="14" height="14" viewBox="0 0 24 24" fill="white"><polygon points="5 3 19 12 5 21 5 3"/></svg>
              </div>
            </a>
          </div>
          <div class="proj-card__body">
            <div class="proj-card__type">Court-métrage</div>
            <div class="proj-card__title">Casse-tête [Réalisateur]</div>
            <p class="proj-card__desc">Un homme face à un problème insoluble — et quand la solution tarde, c'est sa tête qui finit par en faire les frais.</p>
            <a href="https://youtu.be/w4LWra-mdzs" target="_blank" rel="noopener" class="proj-card__link">Voir le projet →</a>
          </div>
        </div>

        <!-- Projet 5 — Myself -->
        <div class="proj-card">
          <div class="proj-card__media">
            <a href="https://youtu.be/ADorjM_h134" target="_blank" rel="noopener">
              <img src="https://img.youtube.com/vi/ADorjM_h134/hqdefault.jpg" alt="Myself" />
              <div class="proj-card__play">
                <svg width="14" height="14" viewBox="0 0 24 24" fill="white"><polygon points="5 3 19 12 5 21 5 3"/></svg>
              </div>
            </a>
          </div>
          <div class="proj-card__body">
            <div class="proj-card__type">Court-métrage</div>
            <div class="proj-card__title">Myself [Réalisateur]</div>
            <p class="proj-card__desc">Réviser ou profiter ? Un dilemme banal… jusqu'à ce que le vrai problème se révèle être lui-même.</p>
            <a href="https://youtu.be/ADorjM_h134" target="_blank" rel="noopener" class="proj-card__link">Voir le projet →</a>
          </div>
        </div>

        <!-- Documentaire Sama — Coorigines Production -->
        <div class="proj-card">
          <div class="proj-card__media">
            <a href="https://vimeo.com/1200387367" target="_blank" rel="noopener">
              <div class="proj-card__media-title">Sama</div>
              <div class="proj-card__play">
                <svg width="14" height="14" viewBox="0 0 24 24" fill="white"><polygon points="5 3 19 12 5 21 5 3"/></svg>
              </div>
            </a>
          </div>
          <div class="proj-card__body">
            <div class="proj-card__type">Documentaire — Coorigines Production</div>
            <div class="proj-card__title">Sama [Assistant de production]</div>
            <p class="proj-card__desc">Réalisé par Rabab Khamis. À seulement dix ans, Sama survit dans les ruines de Gaza en ramassant des déchets pour subvenir aux besoins de sa famille, tout en rêvant d'un avenir où elle pourra retourner à l'école et retrouver son enfance.</p>
            <a href="https://vimeo.com/1200387367" target="_blank" rel="noopener" class="proj-card__link">Voir le projet →</a>
          </div>
        </div>

        <!-- Documentaire Citizen Osama — Coorigines Production -->
        <div class="proj-card">
          <div class="proj-card__media">
            <a href="https://vimeo.com/1188123173" target="_blank" rel="noopener">
              <div class="proj-card__media-title">Citizen Osama</div>
              <div class="proj-card__play">
                <svg width="14" height="14" viewBox="0 0 24 24" fill="white"><polygon points="5 3 19 12 5 21 5 3"/></svg>
              </div>
            </a>
          </div>
          <div class="proj-card__body">
            <div class="proj-card__type">Documentaire — Coorigines Production</div>
            <div class="proj-card__title">Citizen Osama [Assistant de production]</div>
            <p class="proj-card__desc">Réalisé par Ahmed Hassouna. Oussama, un journaliste dépêché à Gaza, devient père alors qu'il documente le génocide Palestinien en cours. Ce portrait révèle douze mois de conflit vus par ceux qui ne détournent pas le regard.</p>
            <a href="https://vimeo.com/1188123173" target="_blank" rel="noopener" class="proj-card__link">Voir le projet →</a>
          </div>
        </div>

      </div>
    </div>
  </section>

  <!-- ═══ BÉNÉVOLAT ════════════════════════════════════════ -->
  <section class="section" id="benevolat">
    <div class="container">
      <div class="sec-head reveal">
        <div><span class="label">Engagement &amp; festivals</span><h2>Bénévolat</h2></div>
        <div class="sec-line"></div>
      </div>

      <div class="benev-grid reveal">

        <div class="benev-card">
          <div class="benev-card__date">En cours</div>
          <div class="benev-card__role">Création de contenu</div>
          <div class="benev-card__event">@BANECI_FRANCE — Instagram</div>
          <p class="benev-card__desc">Réalisation de photomontages et critiques cinématographiques.</p>
        </div>

        <div class="benev-card">
          <div class="benev-card__date">Avril 2025</div>
          <div class="benev-card__role">Agent d'accueil</div>
          <div class="benev-card__event">Festival National du Film d'Animation — TNB Rennes</div>
          <p class="benev-card__desc">Accueil des spectateurs au Théâtre National de Bretagne lors du festival dédié au cinéma d'animation.</p>
        </div>

        <div class="benev-card">
          <div class="benev-card__date">Septembre 2024</div>
          <div class="benev-card__role">Logistique</div>
          <div class="benev-card__event">Festival Emgav — Rennes</div>
          <p class="benev-card__desc">Aide pour la logistique du festival de musique. Montage et démontage du dispositif scénique.</p>
        </div>

        <div class="benev-card">
          <div class="benev-card__date">Mars 2024</div>
          <div class="benev-card__role">Agent d'accueil</div>
          <div class="benev-card__event">Festival Cinéma du Réel — MK2 Paris</div>
          <p class="benev-card__desc">Accueil des artistes et spectateurs au cinéma MK2 lors du festival dédié au cinéma documentaire.</p>
        </div>

      </div>
    </div>
  </section>

  <!-- ═══ CONTACT ══════════════════════════════════════════ -->
  <section class="section section--alt" id="contact">
    <div class="container">
      <div class="sec-head reveal">
        <div><span class="label">Contact</span><h2>Me contacter</h2></div>
        <div class="sec-line"></div>
      </div>

      <div class="contact__wrap reveal">
        <div>
          <p class="contact__body">
            Disponible pour échanger sur un projet, une collaboration ou toute opportunité dans le secteur audiovisuel.
          </p>
          <div class="contact__links">
            <a href="mailto:galonbaptiste0@gmail.com" class="contact__link">
              <div class="contact__link-icon">✉</div>
              <div>
                <div class="contact__link-label">Email</div>
                <div class="contact__link-val">galonbaptiste0@gmail.com</div>
              </div>
            </a>
            <a href="tel:+33615765661" class="contact__link">
              <div class="contact__link-icon">☏</div>
              <div>
                <div class="contact__link-label">Téléphone</div>
                <div class="contact__link-val">06 15 76 56 61</div>
              </div>
            </a>
            <a href="https://www.linkedin.com/in/baptiste-galon" target="_blank" rel="noopener" class="contact__link">
              <div class="contact__link-icon" style="font-size:.65rem;font-weight:900">in</div>
              <div>
                <div class="contact__link-label">LinkedIn</div>
                <div class="contact__link-val">baptiste-galon</div>
              </div>
            </a>
            <a href="https://www.instagram.com/baneci_france" target="_blank" rel="noopener" class="contact__link">
              <div class="contact__link-icon">◈</div>
              <div>
                <div class="contact__link-label">Instagram</div>
                <div class="contact__link-val">@BANECI_FRANCE</div>
              </div>
            </a>
          </div>
        </div>

        <div class="contact__right">
          <div class="contact__big">Travaillons<br>ensemble.</div>
          <p class="contact__tagline">
            En fin de BTS audiovisuel, j'intègre en septembre 2026 la Licence Gestion de la production audiovisuelle aux GOBELINS. Dans ce cadre, je suis à la recherche d'une alternance. N'hésitez pas à me contacter, je réponds rapidement.
          </p>
        </div>
      </div>
    </div>
  </section>

  <!-- ═══ FOOTER ════════════════════════════════════════════ -->
  <footer class="footer">
    <div class="container">
      <div class="footer__inner">
        <span class="footer__logo">Baptiste Galon</span>
        <nav class="footer__links" aria-label="Liens footer">
          <a href="#apropos">Profil</a>
          <a href="#pro">Expériences</a>
          <a href="#projets">Projets</a>
          <a href="#benevolat">Bénévolat</a>
          <a href="#contact">Contact</a>
        </nav>
        <span class="footer__copy">© <span id="year"></span> Baptiste Galon</span>
      </div>
    </div>
  </footer>

  <script>
    document.getElementById('year').textContent = new Date().getFullYear();

    const observer = new IntersectionObserver(entries => {
      entries.forEach(e => {
        if (e.isIntersecting) { e.target.classList.add('visible'); observer.unobserve(e.target); }
      });
    }, { threshold: 0.08 });
    document.querySelectorAll('.reveal').forEach(el => observer.observe(el));

    const sections = document.querySelectorAll('section[id]');
    const navLinks  = document.querySelectorAll('.nav__links a');
    window.addEventListener('scroll', () => {
      let current = '';
      sections.forEach(s => { if (window.scrollY >= s.offsetTop - 80) current = s.id; });
      navLinks.forEach(a => {
        a.style.color = a.getAttribute('href') === '#' + current ? 'var(--ink)' : '';
      });
    }, { passive: true });
  </script>
</body>
</html>
