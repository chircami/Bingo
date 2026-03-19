<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Bingo Master — README</title>
<link href="https://fonts.googleapis.com/css2?family=Fredoka+One&family=Nunito:wght@400;600;700;900&display=swap" rel="stylesheet">
<style>
  :root {
    --primary: #1a237e;
    --accent:  #e53935;
    --green:   #2e7d32;
    --gold:    #f9a825;
    --bg:      #e8eaf6;
    --white:   #ffffff;
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    font-family: 'Nunito', sans-serif;
    background: var(--bg);
    color: #1a1a2e;
    line-height: 1.7;
  }

  /* ── HERO ── */
  .hero {
    background: linear-gradient(135deg, #1a237e 0%, #283593 50%, #3949ab 100%);
    color: white;
    text-align: center;
    padding: 64px 24px 80px;
    position: relative;
    overflow: hidden;
  }
  .hero::before {
    content: '';
    position: absolute;
    inset: 0;
    background: radial-gradient(circle at 20% 50%, rgba(255,255,255,0.06) 0%, transparent 60%),
                radial-gradient(circle at 80% 20%, rgba(249,168,37,0.15) 0%, transparent 50%);
  }
  .hero-emoji { font-size: 4rem; display: block; margin-bottom: 12px; position: relative; }
  .hero h1 {
    font-family: 'Fredoka One', cursive;
    font-size: 3.2rem;
    letter-spacing: 2px;
    position: relative;
    margin-bottom: 8px;
  }
  .hero p {
    font-size: 1.15rem;
    opacity: 0.85;
    position: relative;
    max-width: 500px;
    margin: 0 auto 28px;
  }
  .badge {
    display: inline-block;
    background: rgba(255,255,255,0.15);
    border: 1px solid rgba(255,255,255,0.3);
    border-radius: 20px;
    padding: 6px 18px;
    font-size: 0.85rem;
    font-weight: 700;
    letter-spacing: 1px;
    margin: 4px;
    position: relative;
  }

  /* ── LAYOUT ── */
  .container {
    max-width: 960px;
    margin: 0 auto;
    padding: 48px 24px;
  }

  section { margin-bottom: 64px; }

  h2 {
    font-family: 'Fredoka One', cursive;
    font-size: 2rem;
    color: var(--primary);
    margin-bottom: 24px;
    display: flex;
    align-items: center;
    gap: 12px;
  }
  h2::after {
    content: '';
    flex: 1;
    height: 3px;
    background: linear-gradient(to right, var(--primary), transparent);
    border-radius: 2px;
  }

  h3 {
    font-family: 'Fredoka One', cursive;
    font-size: 1.3rem;
    color: var(--primary);
    margin-bottom: 12px;
    font-weight: normal;
  }

  p { margin-bottom: 12px; color: #333; }

  /* ── SCREENSHOTS GRID ── */
  .screens-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 28px;
    margin-top: 8px;
  }
  @media (max-width: 720px) {
    .screens-grid { grid-template-columns: 1fr; }
    .hero h1 { font-size: 2.2rem; }
  }

  .phone-frame {
    background: #1a1a2e;
    border-radius: 36px;
    padding: 14px;
    box-shadow: 0 20px 60px rgba(0,0,0,0.3), 0 0 0 2px #333;
    position: relative;
  }
  .phone-notch {
    width: 80px; height: 18px;
    background: #1a1a2e;
    border-radius: 0 0 14px 14px;
    margin: 0 auto 8px;
    position: relative;
    z-index: 2;
  }
  .phone-screen {
    background: #e8eaf6;
    border-radius: 24px;
    overflow: hidden;
    min-height: 480px;
    position: relative;
  }
  .screen-label {
    text-align: center;
    margin-top: 14px;
    font-weight: 700;
    font-size: 0.9rem;
    color: var(--primary);
  }

  /* ── MOCKUP SCREEN 1: Setup ── */
  .mock-setup {
    background: #e8eaf6;
    padding: 18px 14px;
    font-family: 'Nunito', sans-serif;
  }
  .mock-card {
    background: white;
    border-radius: 16px;
    padding: 16px 14px;
    box-shadow: 0 6px 20px rgba(0,0,0,0.1);
    text-align: center;
  }
  .mock-title {
    font-family: 'Fredoka One', cursive;
    font-size: 1.4rem;
    color: #1a237e;
    margin-bottom: 4px;
  }
  .mock-sub { font-size: 0.65rem; color: #7986cb; margin-bottom: 10px; }
  .mock-label { text-align: left; font-size: 0.6rem; font-weight: 700; color: #1a237e; margin: 8px 0 3px; }
  .mock-input {
    width: 100%; background: #f5f5f5; border: 2px solid #c5cae9;
    border-radius: 8px; padding: 6px 8px; font-size: 0.6rem; color: #555;
    margin-bottom: 4px; font-family: 'Nunito', sans-serif;
  }
  .mock-btn {
    width: 100%; background: #1a237e; color: white;
    border: none; border-radius: 10px; padding: 10px;
    font-size: 0.7rem; font-weight: 800; margin-top: 8px;
    font-family: 'Fredoka One', cursive; letter-spacing: 0.5px;
  }

  /* ── MOCKUP SCREEN 2: Game ── */
  .mock-game { background: #e8eaf6; padding: 14px 10px; }
  .mock-game-card {
    background: white; border-radius: 14px;
    padding: 12px 10px; box-shadow: 0 6px 20px rgba(0,0,0,0.1);
    text-align: center;
  }
  .mock-big-num {
    font-family: 'Fredoka One', cursive;
    font-size: 3.2rem; color: #1a237e;
    text-shadow: 2px 2px 0 #c5cae9;
    line-height: 1; margin: 6px 0;
  }
  .mock-btn-green {
    width: 100%; background: linear-gradient(135deg, #2e7d32, #43a047);
    color: white; border: none; border-radius: 10px; padding: 10px;
    font-family: 'Fredoka One', cursive; font-size: 0.9rem;
    box-shadow: 0 4px 0 #1b5e20; margin: 6px 0;
  }
  .mock-grid {
    display: grid; grid-template-columns: repeat(10, 1fr); gap: 2px; margin-top: 8px;
  }
  .mock-cell {
    aspect-ratio: 1; background: #f5f5f5; border: 1px solid #e8eaf6;
    border-radius: 3px; font-size: 0.32rem; display: flex;
    align-items: center; justify-content: center; font-weight: 700; color: #9fa8da;
  }
  .mock-cell.ex { background: #e53935; color: white; border-color: #e53935; }

  /* ── MOCKUP SCREEN 3: Player ── */
  .mock-player { background: #e8eaf6; padding: 0; }
  .mock-player-header {
    background: linear-gradient(135deg, #1a237e, #3949ab);
    color: white; text-align: center;
    padding: 14px 12px;
    font-family: 'Fredoka One', cursive; font-size: 0.9rem;
  }
  .mock-player-body { padding: 10px; }
  .mock-cartilla {
    background: white; border: 3px solid #1a237e;
    border-radius: 12px; padding: 10px; margin-bottom: 10px;
  }
  .mock-cartilla-title {
    font-family: 'Fredoka One', cursive; color: #1a237e;
    font-size: 0.7rem; margin-bottom: 8px; font-weight: normal;
  }
  .mock-nums {
    display: grid; grid-template-columns: repeat(5, 1fr); gap: 5px;
  }
  .mock-num {
    aspect-ratio: 1; border: 2px solid #c5cae9; border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-size: 0.55rem; font-weight: 900; background: #f5f5f5; color: #333;
  }
  .mock-num.marked { background: #2e7d32; color: white; border-color: #2e7d32; }

  /* ── RULES CARDS ── */
  .rules-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 20px;
  }
  .rule-card {
    background: white;
    border-radius: 16px;
    padding: 22px 20px;
    box-shadow: 0 4px 16px rgba(0,0,0,0.08);
    border-left: 5px solid var(--primary);
    transition: transform 0.2s;
  }
  .rule-card:hover { transform: translateY(-3px); }
  .rule-card.green  { border-color: var(--green); }
  .rule-card.red    { border-color: var(--accent); }
  .rule-card.gold   { border-color: var(--gold); }
  .rule-icon { font-size: 2rem; margin-bottom: 10px; display: block; }
  .rule-card h3 { margin-bottom: 8px; }
  .rule-card p  { font-size: 0.9rem; margin-bottom: 0; color: #555; }

  /* ── STEP FLOW ── */
  .steps {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 16px;
    counter-reset: step;
  }
  .step {
    background: white;
    border-radius: 14px;
    padding: 20px 16px;
    text-align: center;
    box-shadow: 0 4px 14px rgba(0,0,0,0.07);
    position: relative;
  }
  .step::before {
    counter-increment: step;
    content: counter(step);
    position: absolute;
    top: -14px; left: 50%; transform: translateX(-50%);
    width: 30px; height: 30px;
    background: var(--primary); color: white;
    border-radius: 50%; font-weight: 900; font-size: 0.85rem;
    display: flex; align-items: center; justify-content: center;
    box-shadow: 0 2px 8px rgba(26,35,126,0.4);
  }
  .step-icon { font-size: 2rem; margin: 8px 0 10px; display: block; }
  .step p { font-size: 0.88rem; color: #555; margin: 0; }
  .step h3 { font-size: 1rem; margin-bottom: 6px; }

  /* ── WIN CONDITIONS ── */
  .win-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 24px;
  }
  @media (max-width: 580px) { .win-grid { grid-template-columns: 1fr; } }

  .win-card {
    background: white;
    border-radius: 16px;
    padding: 28px 24px;
    text-align: center;
    box-shadow: 0 4px 16px rgba(0,0,0,0.08);
  }
  .win-card.linea { border-top: 5px solid var(--gold); }
  .win-card.bingo { border-top: 5px solid var(--accent); }
  .win-emoji-big { font-size: 3.5rem; display: block; margin-bottom: 12px; }
  .win-card h3 { font-size: 1.6rem; margin-bottom: 8px; }
  .win-card.linea h3 { color: #856404; }
  .win-card.bingo h3 { color: var(--accent); }

  /* mini cartilla demo */
  .mini-cartilla {
    display: grid; grid-template-columns: repeat(5, 32px);
    gap: 4px; margin: 16px auto 8px; width: fit-content;
  }
  .mc { width: 32px; height: 32px; border-radius: 50%; border: 2px solid #ddd;
    display: flex; align-items: center; justify-content: center;
    font-size: 0.7rem; font-weight: 900; background: #f5f5f5; color: #555; }
  .mc.m { background: #2e7d32; color: white; border-color: #2e7d32; }
  .mc.b { background: #e53935; color: white; border-color: #e53935; }
  .mc.h { background: #f9a825; color: #5d4037; border-color: #f9a825; }

  /* ── LANGS ── */
  .lang-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 16px;
  }
  @media (max-width: 580px) { .lang-grid { grid-template-columns: repeat(2,1fr); } }
  .lang-card {
    background: white; border-radius: 14px; padding: 20px 14px;
    text-align: center; box-shadow: 0 4px 14px rgba(0,0,0,0.07);
  }
  .lang-flag { font-size: 2.5rem; display: block; margin-bottom: 8px; }
  .lang-card h3 { font-size: 1rem; margin-bottom: 6px; }
  .lang-card p { font-size: 0.8rem; color: #888; margin: 0; }
  .linea-word { font-size: 1.1rem; font-weight: 900; color: var(--gold); }
  .bingo-word { font-size: 1.1rem; font-weight: 900; color: var(--accent); }

  /* ── FOOTER ── */
  .readme-footer {
    background: linear-gradient(135deg, #1a237e, #283593);
    color: rgba(255,255,255,0.85);
    text-align: center;
    padding: 40px 24px;
    font-size: 0.95rem;
  }
  .readme-footer span { color: #e53935; font-size: 1.1rem; }
  .readme-footer strong { color: white; }
</style>
</head>
<body>

<!-- ═══════════════════════ HERO ═══════════════════════ -->
<div class="hero">
  <span class="hero-emoji">🎱</span>
  <h1>Bingo Master</h1>
  <p>La app de bingo familiar, multijugador y multilingüe — sin instalación, directo desde el navegador</p>
  <span class="badge">🇪🇸 Español</span>
  <span class="badge">🇺🇸 English</span>
  <span class="badge">🇮🇹 Italiano</span>
  <span class="badge">🇫🇷 Français</span>
</div>

<div class="container">

  <!-- ═══════════════════════ PANTALLAZOS ═══════════════════════ -->
  <section>
    <h2>📱 Pantallas</h2>
    <div class="screens-grid">

      <!-- Pantalla 1: Configuración -->
      <div>
        <div class="phone-frame">
          <div class="phone-notch"></div>
          <div class="phone-screen">
            <div class="mock-setup">
              <div class="mock-card">
                <div class="mock-title">🎱 Bingo Master</div>
                <div class="mock-sub">¡El bingo de tu familia!</div>
                <div class="mock-label">Idioma</div>
                <div class="mock-input">🇪🇸 Español</div>
                <div class="mock-label">Nombres (separados por coma)</div>
                <div class="mock-input">Ana, Juan, Pedro, María...</div>
                <div class="mock-label">Cartillas por jugador</div>
                <div class="mock-input">1</div>
                <button class="mock-btn">Generar Juego</button>
              </div>
            </div>
          </div>
        </div>
        <div class="screen-label">① Configuración</div>
      </div>

      <!-- Pantalla 2: Bombo (Admin) -->
      <div>
        <div class="phone-frame">
          <div class="phone-notch"></div>
          <div class="phone-screen">
            <div class="mock-game">
              <div class="mock-game-card">
                <div style="font-size:0.6rem;color:#9fa8da;font-weight:700;">🎱 Número</div>
                <div class="mock-big-num">37</div>
                <div style="font-size:0.5rem;color:#c5cae9;margin-bottom:4px;">53 bolas restantes</div>
                <button class="mock-btn-green">¡Cantar!</button>
                <div class="mock-grid">
                  <!-- row 1: 1-10 -->
                  <div class="mock-cell ex">1</div><div class="mock-cell">2</div><div class="mock-cell ex">3</div>
                  <div class="mock-cell">4</div><div class="mock-cell ex">5</div><div class="mock-cell">6</div>
                  <div class="mock-cell ex">7</div><div class="mock-cell">8</div><div class="mock-cell">9</div>
                  <div class="mock-cell ex">10</div>
                  <!-- row 2 -->
                  <div class="mock-cell">11</div><div class="mock-cell ex">12</div><div class="mock-cell">13</div>
                  <div class="mock-cell">14</div><div class="mock-cell ex">15</div><div class="mock-cell">16</div>
                  <div class="mock-cell">17</div><div class="mock-cell">18</div><div class="mock-cell ex">19</div>
                  <div class="mock-cell">20</div>
                  <!-- row 3 -->
                  <div class="mock-cell ex">21</div><div class="mock-cell">22</div><div class="mock-cell">23</div>
                  <div class="mock-cell ex">24</div><div class="mock-cell">25</div><div class="mock-cell ex">26</div>
                  <div class="mock-cell">27</div><div class="mock-cell ex">28</div><div class="mock-cell">29</div>
                  <div class="mock-cell">30</div>
                  <!-- row 4 -->
                  <div class="mock-cell">31</div><div class="mock-cell ex">32</div><div class="mock-cell">33</div>
                  <div class="mock-cell">34</div><div class="mock-cell">35</div><div class="mock-cell ex">36</div>
                  <div class="mock-cell ex" style="background:#f9a825;border-color:#f9a825;color:white;">37</div>
                  <div class="mock-cell">38</div><div class="mock-cell">39</div><div class="mock-cell">40</div>
                  <!-- rows 5-9 grises -->
                  <div class="mock-cell">41</div><div class="mock-cell">42</div><div class="mock-cell">43</div>
                  <div class="mock-cell">44</div><div class="mock-cell">45</div><div class="mock-cell">46</div>
                  <div class="mock-cell">47</div><div class="mock-cell">48</div><div class="mock-cell">49</div>
                  <div class="mock-cell">50</div>
                  <div class="mock-cell">51</div><div class="mock-cell">52</div><div class="mock-cell">53</div>
                  <div class="mock-cell">54</div><div class="mock-cell">55</div><div class="mock-cell">56</div>
                  <div class="mock-cell">57</div><div class="mock-cell">58</div><div class="mock-cell">59</div>
                  <div class="mock-cell">60</div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="screen-label">② Bombo del presentador</div>
      </div>

      <!-- Pantalla 3: Cartilla del jugador -->
      <div>
        <div class="phone-frame">
          <div class="phone-notch"></div>
          <div class="phone-screen">
            <div class="mock-player">
              <div class="mock-player-header">Ana — Mis Cartillas</div>
              <div class="mock-player-body">
                <div class="mock-cartilla">
                  <div class="mock-cartilla-title">Cartilla 1</div>
                  <div class="mock-nums">
                    <div class="mock-num marked">3</div>
                    <div class="mock-num">11</div>
                    <div class="mock-num marked">19</div>
                    <div class="mock-num">28</div>
                    <div class="mock-num marked">36</div>
                    <div class="mock-num">42</div>
                    <div class="mock-num marked">51</div>
                    <div class="mock-num">58</div>
                    <div class="mock-num">63</div>
                    <div class="mock-num">70</div>
                    <div class="mock-num marked">7</div>
                    <div class="mock-num">14</div>
                    <div class="mock-num marked">21</div>
                    <div class="mock-num">32</div>
                    <div class="mock-num">45</div>
                  </div>
                </div>
                <div style="text-align:center;font-size:0.6rem;color:#9fa8da;margin-top:6px;">
                  Toca los números para marcarlos
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="screen-label">③ Cartilla del jugador</div>
      </div>

    </div>
  </section>

  <!-- ═══════════════════════ CÓMO SE JUEGA ═══════════════════════ -->
  <section>
    <h2>🎮 Cómo se juega</h2>
    <div class="steps">
      <div class="step">
        <span class="step-icon">⚙️</span>
        <h3>Configura</h3>
        <p>Elige el idioma, escribe los nombres de los jugadores y cuántas cartillas quieres por persona.</p>
      </div>
      <div class="step">
        <span class="step-icon">📲</span>
        <h3>Comparte QR</h3>
        <p>Se genera un código QR único para cada jugador. Cada uno lo escanea con su móvil y ve sus cartillas.</p>
      </div>
      <div class="step">
        <span class="step-icon">🔊</span>
        <h3>Canta números</h3>
        <p>El presentador pulsa "¡Cantar!" y la app saca un número al azar, lo muestra grande y lo dice en voz alta.</p>
      </div>
      <div class="step">
        <span class="step-icon">👆</span>
        <h3>Marca cartillas</h3>
        <p>Cada jugador toca los números en su cartilla para marcarlos. La app detecta línea y bingo automáticamente.</p>
      </div>
      <div class="step">
        <span class="step-icon">🎉</span>
        <h3>¡Gana!</h3>
        <p>Al completar una línea o la cartilla entera, explota una animación de confeti con el mensaje de victoria.</p>
      </div>
    </div>
  </section>

  <!-- ═══════════════════════ REGLAS ═══════════════════════ -->
  <section>
    <h2>📋 Reglas del juego</h2>
    <div class="rules-grid">
      <div class="rule-card">
        <span class="rule-icon">🎱</span>
        <h3>El bombo</h3>
        <p>La app sortea números del 1 al 90 sin repetición. Una vez cantado un número no vuelve a salir. El contador muestra las bolas que quedan.</p>
      </div>
      <div class="rule-card green">
        <span class="rule-icon">📋</span>
        <h3>Las cartillas</h3>
        <p>Cada cartilla tiene 15 números aleatorios del 1 al 90, distribuidos en 3 filas de 5. Cada jugador puede tener hasta 3 cartillas distintas.</p>
      </div>
      <div class="rule-card gold">
        <span class="rule-icon">✅</span>
        <h3>Marcar números</h3>
        <p>Cuando se canta un número que tienes en tu cartilla, tócalo para marcarlo. Los números marcados se muestran en verde.</p>
      </div>
      <div class="rule-card red">
        <span class="rule-icon">🎯</span>
        <h3>¡Línea!</h3>
        <p>Se consigue cuando se marcan los 5 números de una misma fila. Salen confeti y el mensaje de línea traducido al idioma del juego.</p>
      </div>
      <div class="rule-card">
        <span class="rule-icon">🏆</span>
        <h3>¡Bingo!</h3>
        <p>Se consigue cuando se marcan los 15 números de una cartilla completa. Mayor celebración con confeti y mensaje de victoria.</p>
      </div>
      <div class="rule-card green">
        <span class="rule-icon">🔁</span>
        <h3>Nueva partida</h3>
        <p>El presentador puede reiniciar todo desde el botón "Reiniciar todo". Se generan nuevas cartillas y nuevo bombo desde cero.</p>
      </div>
    </div>
  </section>

  <!-- ═══════════════════════ CONDICIONES DE VICTORIA ═══════════════════════ -->
  <section>
    <h2>🏅 Condiciones de victoria</h2>
    <div class="win-grid">

      <div class="win-card linea">
        <span class="win-emoji-big">🎯</span>
        <h3>¡LÍNEA!</h3>
        <p style="color:#555;font-size:0.9rem;margin-bottom:16px;">5 números seguidos en la misma fila</p>
        <div class="mini-cartilla">
          <div class="mc h">7</div><div class="mc h">14</div><div class="mc h">28</div><div class="mc h">45</div><div class="mc h">63</div>
          <div class="mc">3</div><div class="mc m">11</div><div class="mc">19</div><div class="mc m">32</div><div class="mc">70</div>
          <div class="mc">21</div><div class="mc">36</div><div class="mc">51</div><div class="mc">58</div><div class="mc">82</div>
        </div>
        <p style="font-size:0.8rem;color:#856404;">La fila amarilla completa = ¡Línea!</p>
      </div>

      <div class="win-card bingo">
        <span class="win-emoji-big">🏆</span>
        <h3>¡BINGO!</h3>
        <p style="color:#555;font-size:0.9rem;margin-bottom:16px;">Los 15 números de la cartilla</p>
        <div class="mini-cartilla">
          <div class="mc b">7</div><div class="mc b">14</div><div class="mc b">28</div><div class="mc b">45</div><div class="mc b">63</div>
          <div class="mc b">3</div><div class="mc b">11</div><div class="mc b">19</div><div class="mc b">32</div><div class="mc b">70</div>
          <div class="mc b">21</div><div class="mc b">36</div><div class="mc b">51</div><div class="mc b">58</div><div class="mc b">82</div>
        </div>
        <p style="font-size:0.8rem;color:#c62828;">Toda la cartilla en rojo = ¡Bingo!</p>
      </div>

    </div>
  </section>

  <!-- ═══════════════════════ IDIOMAS ═══════════════════════ -->
  <section>
    <h2>🌍 Idiomas disponibles</h2>
    <div class="lang-grid">
      <div class="lang-card">
        <span class="lang-flag">🇪🇸</span>
        <h3>Español</h3>
        <p><span class="linea-word">¡LÍNEA!</span><br><span class="bingo-word">¡BINGO!</span></p>
      </div>
      <div class="lang-card">
        <span class="lang-flag">🇬🇧</span>
        <h3>English</h3>
        <p><span class="linea-word">LINE!</span><br><span class="bingo-word">BINGO!</span></p>
      </div>
      <div class="lang-card">
        <span class="lang-flag">🇮🇹</span>
        <h3>Italiano</h3>
        <p><span class="linea-word">TERNO!</span><br><span class="bingo-word">BINGO!</span></p>
      </div>
      <div class="lang-card">
        <span class="lang-flag">🇫🇷</span>
        <h3>Français</h3>
        <p><span class="linea-word">QUINE!</span><br><span class="bingo-word">BINGO!</span></p>
      </div>
    </div>
    <p style="margin-top:16px;font-size:0.88rem;color:#666;">La voz del bombo, los mensajes de victoria y toda la interfaz se adaptan automáticamente al idioma seleccionado. Los números se pronuncian escritos en palabras para mayor claridad.</p>
  </section>

  <!-- ═══════════════════════ REQUISITOS ═══════════════════════ -->
  <section>
    <h2>💻 Requisitos</h2>
    <div class="rules-grid">
      <div class="rule-card">
        <span class="rule-icon">🌐</span>
        <h3>Sin instalación</h3>
        <p>Solo necesitas abrir el archivo <code>index.html</code> en cualquier navegador moderno. No requiere servidor ni conexión a internet.</p>
      </div>
      <div class="rule-card green">
        <span class="rule-icon">📡</span>
        <h3>Red local para QR</h3>
        <p>Para que los jugadores escaneen el QR con su móvil, todos deben estar en la misma red WiFi. El presentador abre el HTML desde un ordenador o tablet.</p>
      </div>
      <div class="rule-card gold">
        <span class="rule-icon">🔊</span>
        <h3>Voz</h3>
        <p>Usa el motor TTS del sistema operativo. Mejor calidad en iPhone, iPad y Mac. En Android, instala los paquetes de voz en Ajustes → Accesibilidad → Texto a voz.</p>
      </div>
    </div>
  </section>

</div>

<!-- ═══════════════════════ FOOTER ═══════════════════════ -->
<div class="readme-footer">
  <div style="font-size:2rem;margin-bottom:10px;">🎱</div>
  <p>Creado en BCN con <span>❤️</span> por <strong>Mirko</strong></p>
  <p style="margin-top:8px;font-size:0.8rem;opacity:0.6;">Bingo Master — para jugar en familia sin complicaciones</p>
</div>

</body>
</html>
