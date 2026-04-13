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
      color: #171515;
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
      color: #171515;
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
      color: #171515;
    }

    .ficha table tr:last-child td {
      border-bottom: none;
    }

    .ficha table td:first-child {
      color: #171515;
      width: 40%;
      letter-spacing: 1px;
    }

    .ficha table td:last-child {
      color: #171515;
      
    }

    /* ── FOOTER ── */
    footer {
      text-align: center;
      padding: 28px;
      font-family: 'Courier New', monospace;
      font-size: 11px;
      color: #FFFFFF;
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
  <img src="ChatGPT Image 13 d’abr. del 2026, 11_51_18.png" alt="Lost Light portada" />
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
    <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAoHBwgHBgoICAgLCgoLDhgQDg0NDh0VFhEYIx8lJCIfIiEmKzcvJik0KSEiMEExNDk7Pj4+JS5ESUM8SDc9Pjv/2wBDAQoLCw4NDhwQEBw7KCIoOzs7Ozs7Ozs7Ozs7Ozs7Ozs7Ozs7Ozs7Ozs7Ozs7Ozs7Ozs7Ozs7Ozs7Ozs7Ozs7Ozv/wAARCALuAlgDASIAAhEBAxEB/8QAHwAAAQUBAQEBAQEAAAAAAAAAAAECAwQFBgcICQoL/8QAtRAAAgEDAwIEAwUFBAQAAAF9AQIDAAQRBRIhMUEGE1FhByJxFDKBkaEII0KxwRVS0fAkM2JyggkKFhcYGRolJicoKSo0NTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6/8QAHwEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoL/8QAtREAAgECBAQDBAcFBAQAAQJ3AAECAxEEBSExBhJBUQdhcRMiMoEIFEKRobHBCSMzUvAVYnLRChYkNOEl8RcYGRomJygpKjU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6goOEhYaHiImKkpOUlZaXmJmaoqOkpaanqKmqsrO0tba3uLm6wsPExcbHyMnK0tPU1dbX2Nna4uPk5ebn6Onq8vP09fb3+Pn6/9oADAMBAAIRAxEAPwDydTiEE9ycU0mj/lkg+tNoAUUZpBxS96AA0CijtQAUUEUUAFFFHegAo6UtJQAUtJRQAUtJS0AJRRRQAUUUUAFFLSUALSUUUALRSUUALml7U2igBTSUUUAFLSUtACUUtJQAtFFJQAtFIKM0AFLRSUALRmiigApKKKAFoopKAFzSUtFABmig0lAC0UlLQAGiiigApKWkoAM0tJRQAtJRRQAUtJxRQAUUUUAFFLSUALRSUUAFGcUUUAHag0UdqAEpaUjFJQAoJCsKKPX6UUAH/LNfxpKX/lmv40maACig0GgAxzS0lFAC0lAooAKMUUUAFLSUUAFFFFAC0lLRQAlFFFABRQKKAFpKKKACiiigBaKSgUAFFFFABRRiigAoopRQAUmaKKAFpKKKACiiigAooooAKKWkoABS0lFAC0lFLQAlFLSUAL0ooooAKKKKACiiigAooooAKSg0UAFFFFABRRRQAUUUUAFFFFABRRRQAd6KOlFAC0UlGeBQAufXmlxnpTc0CgB38LcdqKC2UPtRQAh5VTSUv8I560gFABR3oNLQAlBoooAKKKKAFpBRRQAtFJRQAUUUUAFFFFABRRRQAUtFHSgBKKKKACiiigAooooAOKKKKACiiigAooooAKMUUUAFFFFABRRRQAUtJRQAUUUlAC0UUUAFLSUUAFFFFABQKKKAFopKWgAoopKAFopKKACijtRgjFABRSmigBMUtFJQAHmiiigAooooAKKKSgBaKSlzQAUlLRQAUUUZoAX1opP4T9KKAFx8imjtSgHYDjikNACc9qXOORSdqASDmgAHNHvR+NFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFAC9qKSloASiiigAooFFABRRRQAUUUe1AB3oo7UUAFFHaigAooNFABRRRQAlLRRQAUUUUAFFFFABRRRQAUUUUAJS0UUALSUUUAFLSUUABooooAKKBRQAUZ4Az0oooAKKKO9ABRRRQAUAUUUAFFFFABRRRQAlLRRQAUUUlAC0ds0UCgBR90n2opRyp+lFAB0jU9smmnrTv4R+NNoAKKDRQAYoooFABRRRQAUUUUAFFFFAB1opaSgAooooAWkpaSgApaKTtQAUUUlAC0lFFABRRRQAUtakPhnW7iFJ4dMneORQyuAMEHoarX+k3+l7Pt1rJB5mdm8fex1/nQBUooooAKKKKACiir+m6Lf6v5n2C387ysb/mAxnp1PtQBQordPgvxAOunnH/XVP8AGg+DNfC7jY4AGTmVP8aV0BhUUClpgJRRS4oATGKK09P8PapqlubiztxJEG2k7wOfxNWv+EN13/n0X/v6v+NK6AwqK2Lrwtq9nbSXM9sqxxLuY+YDgVj4pgFFFKoLMFHUnFACUV0I8Da3/cgH/bWnf8IJrmcbLf8A7/f/AFqV0BzlGK6T/hBNc4ylvz/01/8ArUn/AAguuf8APODj/pr/APWougOcxRit+58GaxaWstzKsHlxKWbEuTgfhWDTASilpOlAAKWkpaACiikoAKKWkoASloooAKKMUdqACig0UAFFJS0AFFFFABQaKDQAlLSUUAPX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1juFZjgDPNbS2ZxUnaav3NK44t5P901kVozXULQuofkqQOKzcVnTTS1OnGSjKSsy5p3+vb/dqzfD/RW+o/nVSykSOVi7BRt6mp7ueJ7cqrgnIwBSknzmlKUVh2r9zOooorY84O1bS/dH0rF7VrrNHtH7xenrWNXod+DaXNczJ+Z3/wB41HUkxDTORyNxqOtVscUviYUUUtMkSiiloASiiigA70UdqKACiiigAooooAOlGRnikPSkHWgB3WgUUGgAoopKAFooooAKKKKAFH3W+lFKOEaigBP4B+NJSnHlr+NJQAcUe9FFABSUUtACUUtFACUtFFABRS0lABRRRQAUUUUAFFFFAC0lL2pDQAUUUlABS0lLQAUUUUAJS0UUAFHbmiigAoopD1oAWikpaACiiigAooooAKM0UUAFFFFABS0lFAC0ZpKKACiiigBaM+vSikoAWikooAKKO1FABQaKKACikpaACiiigAooooAKTPOKWmt1oAUjjNJ1OKSjvQA4DApaZTx0oAMUUUlABQaWigAxQKKSgB2fkIopMZBz6UUAOIAiU555ptKR8i8+tJQAUUUUAFFFFABSUvaigAxSUueMZ4ooAKKKO9ABR3oooAKKKKACiiigApaSigANFFFACd6WiigAooooAKKKWgBKKKKACijtRQAlLSUtABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFAC0lLRQAlFLRQAnNFLSUAFFFFAC0lFFABRmko70ALR3pKKAFopKGPAoAM84peOlNzzmkJzQAp6mkoooAUYx0ozSUo60AOooooAOlFFHSgAoopKAHD7rduKKMDYx9qKAA/cWkpxOIlGOpNNoAO9FH0pe9ACUUUUAFHaijvQAUUUUAFFFFABRRRQAUUUtACUUZpKAFpaSigBaKSigAooooAKKSlFABRRRQAUUUUAFFFFABRRQaAFpKWkNABSikoFAC0UUlABRRS4oASlpKWgAooo/GgAopKWgA7UlLRQAlFFFABRS0lABSUtJjmgBaQ0tFACUtIaB0oAWjAoozQA08dqTmnkA0Y4oAZRQetFACgA0vY4pAcCjNACDrT6ZRnmgB9JTqKAEooooAeAPLfucUUL/qn/CigBrf6tT9aSnZ+QU2gAooooAOlH40UUAFFFFABQKKKACiiigBKXNFJQAtFFFABRRRQAUUUUAAooooAKKM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40mKAG9qSnHqabQAoyelPFNWnUABoIyKO9KOlADMEUrNuoP502gBQcUBc85pKcACOaAH9j9KKQD5TzRQArdF+lNp5HyJ+NJjNACdKTNL9aTFAC0UUUAFJjilooASjvRRQAUuaSloAKack8U7NIeOlADRwadnNNpw9qAFpKWkoAWiiigAoopaAEpaKKACikNAoAWjvRRQAGiikoAKKWjFABiiiigAooo60AJSiikoAWiikoAWiiigA7Unag8A0KaAClopD0oAWmsOaAfU0ucqeKAG0pPpSUpHpzQAq4/GlpAMDmloAD6U2nEU0DmgA+lJ3pw4NN70ALnHSgDnmlxzSjrQAhAzSDApWx7U0gkDFADuvSggZpFIx1prfeoAWig0g5oACTzzSYpT1pKAFXpTs0g4oNAATxQpOaQnigGgB2Qaawx0o6GhjmgBB704Y7U0daXp3oAUDhvYUUA/K30ooAkP3E+h/nTacc7F9MU2gA60lLikoAUdKKSloAKBSUUALR2oFIeAaACigc0UAIaM4pcUmPWgBKcDmm0p9qAFGB0paQAiloAKKDRQAUoHFJS96ACj+VHejFAAOlJS9qKACiiigAooo9qADvS0lLQAlGKKO9ABRzRRQAduaKKWgBKSl5o96ACjtRQenFACMccUi47mk6DmgY70APpCKUdOKO9ADSMUBsDFKeabg0AFKOuaQ0p56daAFYbulKP5UKuBz1pAfmxQApxTehpx9aTvQAcgUneng9qYOtADv501lG3OOafketHUetAEPtTgxAxT2GBwBUe0ntQAlKTml2Y6mkxQAlFL68UoHGeKAG0U4jBpKAHKARmkYcZpy/d/GmEk8UAJ1op33eRQ2O3NAAOvNI2O1LjIpDQAgpfxoHWg9fagBy4KN60U0d+O1FAEp4VPTHH502nsT5SemKZQAGjtQaQ0ALRRRQAlFLSUAFBPGKWmlcc5oAAQBTqZx3pxGRQAZ7UEZpCMEUuaAEpQM9KSl6dKAFozQeKKACiilxxQAUCilFACCilooASj6UtFACUtFFAAaSl60hoAKWkooAWikpaACj3oooAOKSloFABRRRQAlIRjJzS0A5zQA0nOKQClbHakBwaAHZAGKRutJnmndRmgBAcClB+Wmng0cgZ7UAFL0ORSUrelAClulIp5oC5HHNA4NADz6UnelAB564pKAHAVETip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UAWo4l28qc56VMkUHlsWADduarLdjGNp/OpI281S3THFICVbV5EDRwsy56gEitCzs4I7UyzR7JkJZWbIIxyKrW+qLbQrAYixBPOfWrKX8VwpjaNl8z5MgjjPGaTuNFW61EuylZwcDqCKgF10BcbT1FSXmkpA6LHMxBGTuHvVN7Pau7zM47YoVgFmuXEhEch2Y7UyOZ8nLmk8mTHy4I+tMaMp1b8MUxDzMx43GmMzHgnOetMJx360cjtTAcFX/JpTimZoBx2oAftUUZBNAORmjvQAtN3jsaQsfSmigCVs44phB7ijefSjfxjFACUpc0nWkoAX60UlLQAlFFAoAKKXFHSgBO9LRR3oAKSlooAKKKKACijtRQAlLRRQAUCiigA9qKKKACiijtQAUgpaKAHDmNvqKKAfkYe4ooAP4F+lJmnFPkDDkCm0AB5pKKKACiiigAooooAKOtFFAAaO9BJJpKAFpKWigApKWigAopKWgAHrS0lFABRRRQACl3c02igB+eKKZRQA4mk/CikxQAZNLQFPpTlRm5HagBtGSOAT+dSqdg2t+lP569qAEWIFc7ia1NO0wXVuriZ0+YjAGce+azM1JHLskQkttDAnH1pMDR1HTzaPGouZX3AnLduapLDuXJc/Spbu8jmdWXdwOciqm5c96EMWY+UDtb05quZC3U5xUrSKpwcn8KQzIB0P5UxDAQTyBxRtVznpQ5DjC/WosEHBoAk8rH8X6Uwc0opMAUAHIoJpCaKACilyBS0ANopSBSUAFFLSUAFFFFABSiijpQAuaTNJS0AFFFFABmiiigAooooAKKKKACiiigAooooAKKKKACiiigA60UvfPekPXNACj7jc96KAPlaigB+47F5NN6n0o52L6U2gAxiilB59RSYz0NAB3ooooAO1BoooABRRRQAUH1FFAODQAlLQwweOh6UUAFFFFABRRRQAUUUUAFFFFABiikooAXFGKKKADFFFFAC7iKUOQOKbRQApJJzS+Y3rTaKAJ4/nxk9TirsVnEy5JbP1rKpcmgC/dQpC6hScEZOTVIu2fTFMzmigBxO45NIR0pKWgABINGSTk0UUALSHFFFABiiikoAKWkpaACkpaKAEopaBQAUUUUAFFFFABSUtIaACiiigAoopaACiiigBKWkpcUAFFFFACUtJRQAtFFFABRRml5oAMUEUKaWgBP4DRSj7jfhRQAnUD6UUp/1a0lABSUUGgBQeDkDmkIwcUUqnkEnp7ZoAb3paVhzx09qbQAtFFFABSUtJQAo9DRjHBpKcTlfcfyoASikpaACiiigAoxxRRmgAoo60UAFFFGKACiiigApKWigAopKKAFopKKAFooooAKKKSgApaKSgBelFJS0AFFJS0AFJRS0AJS0lFAC0UUUAFFFFABRRRQAUUUdKACkpaKAExS0UUAFFJS0AFFFFABiiiigAoo70lAC0lFLQAUUUUAFL34ooBxQAmPSlz0ooVS2fQDmgB6jKHPTPailZyUJHyqOgxRQAzHyCkpx/1fA6Gm9MH1oAKCDQaQ0AFFJSigBQcdgfrSEdKKcvORQA2ijvS0AJRRRQAUgpaKABhg8dO1FSBd8ee4zUdABSUtJ3oAKWjgCigAoHX2oooAOO1FA4oB56UAHailP0owMj3oASijvSkAGgBKKM9aTvQAYpaKTNAC0UUGgApKWigBKKXHNFACUUuKKAEpaKSgBaSnUlABRR2ooAKKSlNABRSUUALRQKQmgBaKB/SgcmgAooOO1HtQAlLR7UCgAooPWigAoo9aKACjNFFABSUuKKADFFHbNFACgUnfmij2oAX2ooHXFOAz7AUACgHk9B1pC2RgdO1PmwCqAYAFR5oAdyYyMcCilA+Qn3FFAH/9k=" alt="Lost Light portada Steam" />
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
