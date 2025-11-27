<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <title>Happy Birthday, Ghulian 🎉</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <!-- Fuente (opcional) -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap" rel="stylesheet">

  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: "Poppins", system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 20px;
      background: radial-gradient(circle at top, #ffe082, #f48fb1, #7e57c2);
      overflow-x: hidden;
      color: #1f1f1f;
    }

    body.celebrate {
      animation: bgPulse 6s infinite alternate;
    }

    @keyframes bgPulse {
      0% { filter: hue-rotate(0deg); }
      100% { filter: hue-rotate(40deg); }
    }

    .card {
      position: relative;
      max-width: 900px;
      width: 100%;
      background: rgba(255, 255, 255, 0.94);
      border-radius: 28px;
      padding: 28px 24px 26px;
      box-shadow:
        0 18px 45px rgba(0, 0, 0, 0.18),
        0 0 0 1px rgba(255, 255, 255, 0.6);
      text-align: center;
      overflow: hidden;
    }

    .badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 6px 14px;
      border-radius: 999px;
      font-size: 12px;
      font-weight: 600;
      letter-spacing: 0.06em;
      text-transform: uppercase;
      background: linear-gradient(135deg, #ffca28, #ff7043);
      color: #4a2500;
      margin-bottom: 14px;
    }

    .badge span {
      font-size: 16px;
    }

    h1 {
      font-size: clamp(28px, 5vw, 34px);
      line-height: 1.1;
      margin-bottom: 8px;
      font-weight: 700;
    }

    .name {
      display: inline-block;
      padding: 4px 12px;
      border-radius: 999px;
      background: linear-gradient(135deg, #7e57c2, #42a5f5);
      color: #ffffff;
      margin-top: 6px;
      font-size: 22px;
      font-weight: 700;
      letter-spacing: 0.03em;
    }

    .subtitle {
      font-size: 14px;
      opacity: 0.8;
      margin-bottom: 16px;
    }

    .message {
      font-size: 14px;
      margin-bottom: 16px;
    }

    .bullets {
      list-style: none;
      margin-bottom: 20px;
      text-align: left;
      font-size: 13px;
      opacity: 0.9;
      max-width: 480px;
      margin-left: auto;
      margin-right: auto;
    }

    .bullets li {
      display: flex;
      align-items: center;
      gap: 8px;
      margin-bottom: 6px;
    }

    .bullets li span {
      font-size: 16px;
    }

    .cta-btn {
      border: none;
      border-radius: 999px;
      padding: 10px 22px;
      font-size: 14px;
      font-weight: 600;
      cursor: pointer;
      background: linear-gradient(135deg, #42a5f5, #ab47bc);
      color: #ffffff;
      box-shadow: 0 12px 25px rgba(0, 0, 0, 0.25);
      transition: transform 0.15s ease, box-shadow 0.15s ease, filter 0.15s ease;
      margin-bottom: 8px;
    }

    .cta-btn:hover {
      transform: translateY(-1px) scale(1.02);
      box-shadow: 0 16px 30px rgba(0, 0, 0, 0.3);
      filter: brightness(1.03);
    }

    .cta-btn:active {
      transform: translateY(0) scale(0.98);
      box-shadow: 0 8px 18px rgba(0, 0, 0, 0.22);
    }

    .hidden-message {
      margin-top: 6px;
      font-size: 14px;
      font-weight: 600;
      opacity: 0;
      transform: translateY(6px);
      transition: opacity 0.3s ease, transform 0.3s ease;
    }

    .hidden-message.visible {
      opacity: 1;
      transform: translateY(0);
    }

    .footer {
      margin-top: 14px;
      font-size: 11px;
      opacity: 0.8;
    }

    /* GALERÍA DE FOTOS */
    .gallery-title {
      margin-top: 26px;
      font-size: 18px;
      font-weight: 700;
    }

    .gallery-subtitle {
      font-size: 13px;
      opacity: 0.85;
      margin-bottom: 16px;
    }

    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
      gap: 14px;
      margin-top: 8px;
    }

    .photo-card {
      background: rgba(255, 255, 255, 0.95);
      border-radius: 18px;
      padding: 8px 8px 10px;
      box-shadow: 0 4px 14px rgba(0, 0, 0, 0.09);
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    .photo-card img {
      width: 100%;
      border-radius: 14px;
      object-fit: cover;
      max-height: 260px;
    }

    .photo-caption {
      margin-top: 6px;
      font-size: 11px;
      text-align: center;
      padding: 0 4px;
    }

    /* Globos */
    .balloon {
      position: absolute;
      width: 60px;
      height: 80px;
      border-radius: 50% 50% 45% 45%;
      opacity: 0.8;
      animation: float 10s linear infinite;
    }

    .balloon::after {
      content: "";
      position: absolute;
      bottom: -20px;
      left: 50%;
      width: 2px;
      height: 26px;
      background: rgba(0, 0, 0, 0.15);
      transform: translateX(-50%);
    }

    .balloon.pink { background: #f48fb1; }
    .balloon.blue { background: #64b5f6; }
    .balloon.yellow { background: #ffd54f; }
    .balloon.purple { background: #b39ddb; }

    .balloon.b1 { top: -20px; left: -10px; animation-delay: 0s; }
    .balloon.b2 { top: 10px; right: -15px; animation-delay: 2s; }
    .balloon.b3 { bottom: -40px; left: 20%; animation-delay: 4s; }
    .balloon.b4 { bottom: -30px; right: 15%; animation-delay: 1s; }

    @keyframes float {
      0% { transform: translateY(20px); opacity: 0.6; }
      50% { transform: translateY(-10px); opacity: 0.9; }
      100% { transform: translateY(20px); opacity: 0.6; }
    }

    /* Confetti */
    .confetti {
      position: fixed;
      top: -10px;
      width: 8px;
      height: 14px;
      opacity: 0.9;
      border-radius: 2px;
      animation: fall 3s linear forwards;
      z-index: 9999;
    }

    @keyframes fall {
      0%   { transform: translateY(0) rotateZ(0deg); }
      100% { transform: translateY(110vh) rotateZ(360deg); }
    }

    @media (max-width: 480px) {
      .card {
        padding: 22px 14px 20px;
        border-radius: 22px;
      }
      .bullets {
        font-size: 12px;
      }
    }
  </style>
</head>
<body>
  <!-- Globos decorativos -->
  <div class="balloon pink b1"></div>
  <div class="balloon blue b2"></div>
  <div class="balloon yellow b3"></div>
  <div class="balloon purple b4"></div>

  <div class="card">
    <div class="badge">
      <span>🎂</span> CELEBRANDO A LO GRANDE
    </div>

    <h1>¡Happy Birthday!</h1>
    <div class="name">Ghulian</div>

    <p class="subtitle">
      Hoy no es un día cualquiera, hoy es tu día especial ✨
    </p>

    <p class="message">
      Que este nuevo año de vida venga cargado de risas, aventuras, abrazos fuertes,
      muchas sorpresas y sueños gigantes por cumplir. 💫
    </p>

    <ul class="bullets">
      <li><span>🎁</span> Más momentos felices que regalos.</li>
      <li><span>🎉</span> Muchas aventuras con la gente que te quiere.</li>
      <li><span>⭐</span> Que nunca te falte amor, salud y magia.</li>
    </ul>

    <button class="cta-btn" onclick="celebrate()">
      ¡Haz clic para celebrar! 🥳
    </button>

    <p id="hiddenMessage" class="hidden-message">
      ✨ ¡Te queremos mucho, Ghulian! Que tu sonrisa ilumine siempre todo a tu alrededor. ✨
    </p>

    <!-- GALERÍA DE FOTOS EN ORDEN -->
    <p class="gallery-title">Tu historia en momentos 💛</p>
    <p class="gallery-subtitle">Cada foto, un pedacito de todo lo que significas para nosotros.</p>

    <div class="gallery">
      <!-- Foto 1 -->
      <div class="photo-card">
        <img src="img/ghulian-1.jpg" alt="Ghulian bebé">
        <p class="photo-caption">Desde el primer día llenaste todo de luz. ✨</p>
      </div>

      <!-- Foto 2 -->
      <div class="photo-card">
        <img src="img/ghulian-2.jpg" alt="Ghulian de niña con vestido blanco">
        <p class="photo-caption">Mi pequeña princesa, tan dulce y brillante. 👑</p>
      </div>

      <!-- Foto 3 -->
      <div class="photo-card">
        <img src="img/ghulian-3.jpg" alt="Ghulian posando de niña">
        <p class="photo-caption">Siempre coqueta y con una actitud que enamora. 💖</p>
      </div>

      <!-- Foto 4 -->
      <div class="photo-card">
        <img src="img/ghulian-4.jpg" alt="Ghulian patinando en el parque">
        <p class="photo-caption">Jugando, soñando y llenando el mundo de alegría. 🎠</p>
      </div>

      <!-- Foto 5 -->
      <div class="photo-card">
        <img src="img/ghulian-5.jpg" alt="Ghulian con vestido azul elegante">
        <p class="photo-caption">Brillando como la reina que eres. 💙</p>
      </div>

      <!-- Foto 6 -->
      <div class="photo-card">
        <img src="img/ghulian-6.jpg" alt="Ghulian en el parque con flores">
        <p class="photo-caption">Cada paso tuyo hace más lindo el camino. 🌸</p>
      </div>

      <!-- Foto 7 -->
      <div class="photo-card">
        <img src="img/ghulian-7.jpg" alt="Ghulian en Machu Picchu">
        <p class="photo-caption">Tus sueños te llevaron muy alto, y vas por más. ⛰️</p>
      </div>

      <!-- Foto 8 -->
      <div class="photo-card">
        <img src="img/ghulian-8.jpg" alt="Ghulian en sitio turístico con esculturas">
        <p class="photo-caption">Cada aventura a tu lado es única e inolvidable. 🌍</p>
      </div>

      <!-- Foto 9 -->
      <div class="photo-card">
        <img src="img/ghulian-9.jpg" alt="Ghulian cenando">
        <p class="photo-caption">Disfrutando la vida, un bocado y una sonrisa a la vez. 🍽️</p>
      </div>

      <!-- Foto 10 -->
      <div class="photo-card">
        <img src="img/ghulian-10.jpg" alt="Ghulian en el parque con edificios">
        <p class="photo-caption">Creciendo fuerte, auténtica y llena de futuro. 🌟</p>
      </div>

      <!-- Foto 11 -->
      <div class="photo-card">
        <img src="img/ghulian-11.jpg" alt="Ghulian en sesión de fotos">
        <p class="photo-caption">Lista para conquistar todo lo que te propongas. 🚀</p>
      </div>
    </div>

    <div class="footer">
      Con todo nuestro cariño, para ti, Ghulian 💛
    </div>
  </div>

  <script>
    function celebrate() {
      document.body.classList.add("celebrate");
      const msg = document.getElementById("hiddenMessage");
      msg.classList.add("visible");

      for (let i = 0; i < 80; i++) {
        createConfetti();
      }
    }

    function createConfetti() {
      const confetti = document.createElement("div");
      confetti.classList.add("confetti");

      const colors = ["#ffeb3b", "#ff7043", "#29b6f6", "#ab47bc", "#66bb6a"];
      const color = colors[Math.floor(Math.random() * colors.length)];
      confetti.style.backgroundColor = color;

      const left = Math.random() * 100;
      confetti.style.left = left + "vw";

      const duration = 2 + Math.random() * 2;
      confetti.style.animationDuration = duration + "s";

      document.body.appendChild(confetti);

      setTimeout(() => {
        confetti.remove();
      }, duration * 1000);
    }
  </script>
</body>
</html>
