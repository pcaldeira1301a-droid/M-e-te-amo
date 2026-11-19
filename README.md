<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Carta para a Melhor Mãe do Mundo</title>
<style>
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body {
    min-height: 100vh;
    font-family: "Segoe UI", Arial, sans-serif;
    background: linear-gradient(135deg, #1a0b2e, #5b1a6e 50%, #c2185b);
    background-attachment: fixed;
    color: #3b1030;
    overflow-x: hidden;
  }
  #bg { position: fixed; inset: 0; pointer-events: none; z-index: 0; overflow: hidden; }
  .float {
    position: absolute;
    bottom: -60px;
    animation: subir linear forwards;
    opacity: .85;
  }
  @keyframes subir {
    to { transform: translateY(-115vh) rotate(360deg); opacity: 0; }
  }
  .carta {
    position: relative;
    z-index: 1;
    max-width: 700px;
    margin: 24px auto;
    padding: 28px 22px;
    background: rgba(255, 245, 250, .94);
    border: 3px solid #ff4d88;
    border-radius: 22px;
    box-shadow: 0 0 30px rgba(255, 77, 136, .6);
  }
  h1 { text-align: center; color: #c2185b; font-size: 1.5rem; margin-bottom: 18px; }
  h2 { text-align: center; color: #e91e63; font-size: 1.2rem; margin: 14px 0; }
  p { margin: 12px 0; line-height: 1.6; font-size: 1.05rem; }
  .beneficio {
    background: #ffe3ef;
    border-left: 5px solid #ff4d88;
    border-radius: 12px;
    padding: 10px 14px;
    margin: 10px 0;
    line-height: 1.5;
  }
  .destaque { text-align: center; font-size: 1.3rem; font-weight: bold; color: #c2185b; margin: 18px 0; }
  .assinatura { text-align: center; font-weight: bold; margin-top: 20px; }
  .final { text-align: center; font-size: 1.4rem; font-weight: bold; color: #e91e63; margin-top: 18px; }
  .coracao-btn { display: block; margin: 20px auto 0; padding: 12px 24px; font-size: 1.1rem;
    border: none; border-radius: 30px; background: #ff4d88; color: #fff; cursor: pointer; }
  .coracao-btn:active { transform: scale(.95); }
</style>
</head>
<body>
<div id="bg"></div>

<div class="carta">
  <h1>💌 CARTA PARA A MELHOR MÃE DO MUNDO 💌</h1>
  <h2>❤️ MÃE, EU TENHO UM PEDIDO ESPECIAL! ❤️</h2>

  <p>Eu queria muito um PS5, e prometo que não é só por diversão! 🥹🎮</p>
  <p><strong>O PlayStation 5 tem vários benefícios:</strong></p>

  <div class="beneficio">🎮 <strong>1. Diversão em família:</strong> Podemos jogar juntos, rir e criar momentos inesquecíveis.</div>
  <div class="beneficio">🧠 <strong>2. Desenvolve habilidades:</strong> Alguns jogos ajudam a melhorar o raciocínio, a atenção e a criatividade.</div>
  <div class="beneficio">🏠 <strong>3. Diversão em casa:</strong> Não preciso sair para me divertir, posso aproveitar meu tempo em casa.</div>
  <div class="beneficio">🎯 <strong>4. Aprender inglês:</strong> Muitos jogos ajudam a aprender palavras e expressões em inglês.</div>
  <div class="beneficio">⏰ <strong>5. Compromisso:</strong> Prometo jogar somente depois das minhas responsabilidades, como estudar e ajudar em casa.</div>
  <div class="beneficio">💰 <strong>6. Um investimento duradouro:</strong> O PS5 é um console que pode durar vários anos e receber muitos jogos novos.</div>

  <p>🥺 Mãe, eu sei que você gosta de economizar, e eu respeito isso! Mas esse seria um sonho muito especial para mim. Prometo cuidar muito bem dele e valorizar cada momento.</p>

  <p class="destaque">E sabe qual seria o melhor benefício de todos?<br>Ver seu filho feliz! ❤️</p>

  <p class="assinatura">Com muito amor,<br>SEU FILHO QUE TE AMA MUITO!</p>
  <p class="final">❤️❤️❤️ TE AMO, MÃE! ❤️❤️❤️</p>

  <button class="coracao-btn" onclick="chuva()">Clique aqui, mãe! 💖</button>
</div>

<script>
  const icones = ["❤️", "💖", "💕", "🎮", "🕹️", "👾", "💗", "🎮"];
  const bg = document.getElementById("bg");

  function criar() {
    const el = document.createElement("div");
    el.className = "float";
    el.textContent = icones[Math.floor(Math.random() * icones.length)];
    el.style.left = Math.random() * 100 + "vw";
    el.style.fontSize = 18 + Math.random() * 30 + "px";
    const dur = 6 + Math.random() * 6;
    el.style.animationDuration = dur + "s";
    bg.appendChild(el);
    setTimeout(() => el.remove(), dur * 1000);
  }

  setInterval(criar, 350);
  for (let i = 0; i < 15; i++) setTimeout(criar, i * 150);

  function chuva() {
    for (let i = 0; i < 40; i++) setTimeout(criar, i * 60);
  }
</script>
</body>
</html>
