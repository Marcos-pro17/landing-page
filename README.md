<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Lost Light — Juego de Terror</title>
  <style>
    /* ── RESET Y BASE ── */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background-color: #0d0d0d;
      color: #cccccc;
      font-family: Georgia, serif;
      line-height: 1.7;
    }

    /* ── NAVEGACIÓN ── */
    nav {
      background-color: #111111;
      border-bottom: 2px solid #8b0000;
      padding: 14px 0;
      position: sticky;
      top: 0;
      z-index: 100;
    }

    nav ul {
      list-style: none;
      display: flex;
      justify-content: center;
      gap: 40px;
    }

    nav ul li a {
      color: #cccccc;
      text-decoration: none;
      font-family: 'Courier New', monospace;
      font-size: 14px;
      letter-spacing: 2px;
      text-transform: uppercase;
    }

    nav ul li a:hover {
      color: #cc2200;
    }

    /* ── HERO / CABECERA ── */
    #inicio {
      text-align: center;
      padding: 80px 20px 60px;
      background-color: #0a0a0a;
      border-bottom: 1px solid #1a1a1a;
    }

    #inicio img {
      <img src="ChatGPT Image 13 d'abr. del 2026"
      width: 100%;
      max-width: 400px;
      border: 2px solid #8b0000;
      display: block;
      margin: 0 auto 30px auto;
    }

    #inicio h1 {
      font-family: 'Courier New', monospace;
      font-size: 52px;
      color: #ffffff;
      letter-spacing: 8px;
      text-transform: uppercase;
    }

    #inicio h1 span {
      color: #cc2200;
    }

    #inicio p.tagline {
      font-family: 'Courier New', monospace;
      font-size: 13px;
      letter-spacing: 4px;
      color: #666666;
      margin-top: 12px;
      text-transform: uppercase;
    }

    .btn {
      display: inline-block;
      margin-top: 30px;
      padding: 12px 32px;
      background-color: #8b0000;
      color: #ffffff;
      text-decoration: none;
      font-family: 'Courier New', monospace;
      font-size: 13px;
      letter-spacing: 2px;
      text-transform: uppercase;
      border: none;
      cursor: pointer;
      transition: background-color 0.3s;
    }

    .btn:hover {
      background-color: #cc2200;
    }

    /* ── SECCIONES GENÉRICAS ── */
    section {
      max-width: 860px;
      margin: 0 auto;
      padding: 70px 24px;
      border-bottom: 1px solid #1c1c1c;
    }

    section h2 {
      font-family: 'Courier New', monospace;
      font-size: 24px;
      color: #cc2200;
      letter-spacing: 4px;
      text-transform: uppercase;
      margin-bottom: 6px;
    }

    section .subtitulo {
      font-size: 13px;
      font-family: 'Courier New', monospace;
      color: #444444;
      letter-spacing: 2px;
      margin-bottom: 28px;
    }

    section p {
      font-size: 16px;
      color: #aaaaaa;
      margin-bottom: 16px;
    }

    section p strong {
      color: #dddddd;
    }

    /* ── TARJETAS DE MECÁNICAS ── */
    .cards {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 20px;
      margin-top: 32px;
    }

    .card {
      background-color: #141414;
      border: 1px solid #222222;
      border-left: 3px solid #8b0000;
      padding: 20px;
    }

    .card h3 {
      font-family: 'Courier New', monospace;
      font-size: 14px;
      color: #ffffff;
      letter-spacing: 2px;
      text-transform: uppercase;
      margin-bottom: 10px;
    }

    .card p {
      font-size: 14px;
      color: #888888;
      margin: 0;
    }

    /* ── STEAM ── */
    #steam {
      text-align: center;
    }

    .steam-box {
      background-color: #111111;
      border: 1px solid #222222;
      max-width: 520px;
      margin: 32px auto 0;
      padding: 32px;
      text-align: left;
    }

    .steam-box img {
      width: 100%;
      max-height: 200px;
      object-fit: cover;
      object-position: top;
      display: block;
      margin-bottom: 20px;
      border: 1px solid #1a1a1a;
    }

    .steam-box h3 {
      font-family: 'Courier New', monospace;
      font-size: 18px;
      color: #ffffff;
      letter-spacing: 3px;
      margin-bottom: 6px;
    }

    .steam-box .dev {
      font-family: 'Courier New', monospace;
      font-size: 11px;
      color: #555555;
      letter-spacing: 2px;
      margin-bottom: 16px;
    }

    .steam-box p {
      font-size: 13px;
      color: #888888;
      margin-bottom: 20px;
    }

    .steam-precio {
      display: flex;
      align-items: center;
      justify-content: space-between;
      flex-wrap: wrap;
      gap: 12px;
    }

    .precio {
      font-family: 'Courier New', monospace;
      font-size: 22px;
      color: #ffffff;
    }

    .precio small {
      font-size: 12px;
      color: #666666;
      text-decoration: line-through;
      display: block;
    }

    .etiquetas {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-bottom: 20px;
    }

    .etiqueta {
      font-family: 'Courier New', monospace;
      font-size: 10px;
      letter-spacing: 1px;
      padding: 3px 8px;
      border: 1px solid #333333;
      color: #666666;
      text-transform: uppercase;
    }

    /* ── CONCLUSIÓN ── */
    #conclusion {
      text-align: center;
    }

    .ficha {
      background-color: #111111;
      border: 1px solid #1e1e1e;
      max-width: 480px;
      margin: 32px auto 0;
      padding: 24px 32px;
      text-align: left;
    }

    .ficha table {
      width: 100%;
      border-collapse: collapse;
      font-family: 'Courier New', monospace;
      font-size: 13px;
    }

    .ficha table tr td {
      padding: 7px 0;
      border-bottom: 1px solid #1c1c1c;
    }

    .ficha table tr:last-child td {
      border-bottom: none;
    }

    .ficha table td:first-child {
      color: #555555;
      width: 40%;
      letter-spacing: 1px;
    }

    .ficha table td:last-child {
      color: #cccccc;
    }

    /* ── FOOTER ── */
    footer {
      text-align: center;
      padding: 28px;
      font-family: 'Courier New', monospace;
      font-size: 11px;
      color: #333333;
      letter-spacing: 2px;
      border-top: 1px solid #1a1a1a;
    }

    /* ── JUMPSCARE ── */
    #scare {
      display: none;
      position: fixed;
      inset: 0;
      background: #000000;
      z-index: 9999;
      justify-content: center;
      align-items: center;
      font-size: 120px;
    }

    #scare.show {
      display: flex;
      animation: shake 0.5s linear;
    }

    @keyframes shake {
      0%   { transform: translate(0,0); }
      20%  { transform: translate(-6px, 4px); }
      40%  { transform: translate(6px, -4px); }
      60%  { transform: translate(-4px, 6px); }
      80%  { transform: translate(4px, -2px); }
      100% { transform: translate(0,0); }
    }
  </style>
</head>
<body>

<!-- JUMPSCARE -->
<div id="scare">👁️</div>

<!-- NAVEGACIÓN -->
<nav>
  <ul>
    <li><a href="#inicio">Inicio</a></li>
    <li><a href="#promocion">Promoción</a></li>
    <li><a href="#juego">El Juego</a></li>
    <li><a href="#steam">Comprar</a></li>
    <li><a href="#conclusion">Conclusión</a></li>
  </ul>
</nav>

<!-- INICIO / HERO -->
<div id="inicio">
  <img src="portada.png" alt="Lost Light portada" />
  <h1>LOST <span>LIGHT</span></h1>
  <p class="tagline">Explora · Sobrevive · No mires atrás</p>
  <a href="#steam" class="btn">Ver en Steam</a>
</div>

<!-- PROMOCIÓN -->
<section id="promocion">
  <h2>Promoción</h2>
  <p class="subtitulo">// 01 — ¿De qué va el juego?</p>

  <p>
    <strong>Lost Light</strong> es un videojuego de terror en primera persona ambientado en
    lugares oscuros y abandonados. El jugador debe explorar su entorno, encontrar objetos
    clave y avanzar por la historia mientras se enfrenta a una atmósfera cargada de tensión
    y sustos inesperados.
  </p>
  <p>
    Sin armas. Sin combate. Solo tú, una linterna con batería limitada y la sensación
    constante de que algo te observa desde la oscuridad.
  </p>
  <p>
    Diseñado para los amantes del terror que buscan una experiencia inmersiva, pausada
    y genuinamente aterradora.
  </p>
</section>

<!-- EL JUEGO -->
<section id="juego">
  <h2>El Juego</h2>
  <p class="subtitulo">// 02 — Mecánicas y características</p>

  <p>
    Lost Light combina exploración libre con resolución de puzzles y una narrativa contada
    a través del propio escenario. No hay tutoriales ni indicaciones directas: el jugador
    aprende observando.
  </p>

  <div class="cards">
    <div class="card">
      <h3>🔦 Exploración</h3>
      <p>Recorre mansiones, hospitales y bosques abandonados. Cada zona tiene sus propios secretos escondidos.</p>
    </div>
    <div class="card">
      <h3>🗝️ Objetos</h3>
      <p>Encuentra llaves, notas y artefactos que desbloquean nuevas áreas y revelan la historia del lugar.</p>
    </div>
    <div class="card">
      <h3>💀 Jumpscares</h3>
      <p>Eventos aleatorios e impredecibles que aparecen cuando menos te lo esperas. Sin avisos.</p>
    </div>
    <div class="card">
      <h3>🌑 Atmósfera</h3>
      <p>Diseño de sonido y entornos oscuros que crean una sensación constante de peligro y soledad.</p>
    </div>
    <div class="card">
      <h3>🧩 Puzzles</h3>
      <p>Enigmas integrados en el escenario que obligan al jugador a pensar y explorar con atención.</p>
    </div>
    <div class="card">
      <h3>🏁 Finales</h3>
      <p>Tus decisiones influyen en el final de la historia. Hay 5 desenlaces posibles, ninguno agradable.</p>
    </div>
  </div>
</section>

<!-- STEAM -->
<section id="steam">
  <h2>Comprar</h2>
  <p class="subtitulo">// 03 — Disponible en Steam</p>
  <p>Añade el juego a tu lista de deseos o cómpralo directamente desde la tienda de Steam.</p>

  <div class="steam-box">
    <img src="portada.png" alt="Lost Light portada Steam" />
    <h3>LOST LIGHT</h3>
    <p class="dev">DESARROLLADOR: Dark Corridor Studios &nbsp;|&nbsp; 2025</p>

    <div class="etiquetas">
      <span class="etiqueta">Terror</span>
      <span class="etiqueta">Exploración</span>
      <span class="etiqueta">Puzzle</span>
      <span class="etiqueta">Un jugador</span>
      <span class="etiqueta">Indie</span>
    </div>

    <p>Un juego de terror en primera persona. Explora lugares abandonados, recoge objetos y descubre la verdad... si eres capaz de llegar al final.</p>

    <div class="steam-precio">
      <div class="precio">
        <small>Precio normal: 19,99€</small>
        12,99€
      </div>
      <button class="btn" onclick="activarSusto()">Añadir al carrito</button>
    </div>
  </div>
</section>

<!-- CONCLUSIÓN -->
<section id="conclusion">
  <h2>Conclusión</h2>
  <p class="subtitulo">// 04 — Sobre el proyecto</p>

  <p>
    Lost Light es un proyecto de diseño web creado como parte del módulo de <strong>Sistemas
    Microinformáticos y Redes (SMX)</strong>. El objetivo ha sido diseñar una página web
    completa para un videojuego ficticio, aplicando los conocimientos de HTML y CSS
    adquiridos durante el curso.
  </p>
  <p>
    La web incluye secciones de promoción, explicación del juego, simulación de compra
    en Steam y una conclusión del proyecto. Está publicada mediante <strong>GitHub Pages</strong>.
  </p>

  <div class="ficha">
    <table>
      <tr>
        <td>Alumno</td>
        <td>SMX2B — Ciclo Medio</td>
      </tr>
      <tr>
        <td>Proyecto</td>
        <td>Web promocional de videojuego</td>
      </tr>
      <tr>
        <td>Tecnología</td>
        <td>HTML5 + CSS3</td>
      </tr>
      <tr>
        <td>Publicación</td>
        <td>GitHub Pages</td>
      </tr>
      <tr>
        <td>Juego</td>
        <td>Lost Light (concepto)</td>
      </tr>
      <tr>
        <td>Género</td>
        <td>Terror · Exploración</td>
      </tr>
    </table>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <p>LOST LIGHT &copy; 2025 · Dark Corridor Studios · Proyecto académico SMX2B</p>
</footer>

<script>
  // Jumpscare al hacer clic en "Añadir al carrito"
  function activarSusto() {
    var scare = document.getElementById('scare');
    scare.classList.add('show');
    setTimeout(function() {
      scare.classList.remove('show');
    }, 800);
  }
</script>

</body>
</html>
