---
layout: splash
title: "Edgardo Correa - Analista de Sistemas" # Título para SEO
excerpt: "Analista de Sistemas especializado em infraestrutura, redes e automação." # Descrição para SEO
# As variáveis 'overlay_image' e 'actions' foram removidas
# pois você está criando o header com HTML customizado.
---

<!-- Imagem e texto customizado posicionado sobre a tela do notebook -->
<div class="hero-image-wrapper">
  <canvas id="noiseCanvas"></canvas>
  <img src="/assets/images/banner-home.jpg" alt="Banner com notebook e código" class="hero-img">

  <div class="hero-text-overlay">
    <span class="command-prompt">edgardo@lnx:~$</span>
    <span id="typewriter"></span>
    <span class="cursor-blink"></span>

    <div class="hero-description" style="display: none;">
      <p class="custom-excerpt">
      </p>
    </div>
  </div>
</div>

<style>
/* CORREÇÃO: Faz o container do layout 'splash' ocupar a largura total da tela */
/* ATENÇÃO: Isso pode causar uma barra de rolagem horizontal em algumas telas.
   Se isso acontecer, remova este bloco de CSS. */
.page__hero {
  width: 100vw;
  margin-left: calc(-50vw + 50%);
}

/* Efeito de ruído no canvas */
#noiseCanvas {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 5;
  pointer-events: none;
  mix-blend-mode: overlay;
  opacity: 0.15;
}

/* Estilo da imagem principal com efeito neon */
.hero-img {
  position: relative;
  z-index: 8;
  border-radius: 18px;
  border: 3px solid #10192c;
  box-shadow:
    0 0 6px #10192c,
    0 0 12px #16233a,
    0 0 22px #1d3254;
  animation: neonPulse 2.5s ease-in-out infinite alternate;
}

@keyframes neonPulse {
  0% { box-shadow: 0 0 6px #10192c, 0 0 12px #16233a, 0 0 22px #1d3254; }
  100% { box-shadow: 0 0 10px #16233a, 0 0 20px #1d3254, 0 0 35px #274977; }
}

/* Container do texto sobre a imagem */
.hero-text-overlay {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 40%;
  max-width: 600px;
  text-align: left;
  z-index: 10;
  padding: 20px 30px;
  background-color: rgba(0, 0, 0, 0.3);
  border: none;
  border-radius: 8px;
  font-family: "Courier New", monospace;
  animation: flickerScreen 1.5s infinite;
}

/* Efeito flicker sutil */
@keyframes flickerScreen {
  0%, 19%, 21%, 23%, 25%, 54%, 56%, 100% { opacity: 1; }
  20%, 22%, 24%, 55% { opacity: 0.85; }
}

/* Prompt de comando */
.command-prompt { color: #00aaff; font-weight: bold; }
/* Texto da digitação */
#typewriter { color: #00eaff; }
/* Texto descritivo */
.hero-description .custom-excerpt {
  color: #b8eaff;
  font-size: 16px;
  line-height: 1.5;
  margin-top: 20px;
  text-shadow: 0 0 8px #00d4ff88;
}

/* Cursor Piscante */
.cursor-blink {
  display: inline-block;
  width: 10px;
  height: 20px;
  background: #00eaff;
  margin-left: 5px;
  animation: blinkCursor 0.9s infinite;
}
@keyframes blinkCursor { 0%, 50% { opacity: 1; } 51%, 100% { opacity: 0; } }

/* Responsivo - Tablets */
@media (max-width: 768px) {
  .hero-text-overlay { width: 70%; top: 40%; padding: 15px 20px; }
  .hero-description .custom-excerpt { font-size: 14px; }
  #typewriter, .command-prompt { font-size: 14px; }
}

/* Responsivo - Celulares */
@media (max-width: 480px) {
  .hero-text-overlay {
    width: 85%;
    top: 50%;
    padding: 10px 15px;
    text-align: center;
  }
  .hero-description .custom-excerpt { font-size: 13px; line-height: 1.4; }
  #typewriter, .command-prompt { font-size: 12px; }
  .cursor-blink { width: 6px; height: 16px; }
}
</style>

<script>
// Texto para o efeito de digitação
const typewriterText = `read -p "Analista de Sistemas com experiência em infra, redes e automação." edyone ; echo "Apaixonado por soluções eficientes :P"`;
let i = 0;

function typeWriterEffect() {
  if (i < typewriterText.length) {
    document.getElementById("typewriter").innerHTML += typewriterText.charAt(i);
    i++;
    setTimeout(typeWriterEffect, 55);
  } else {
    document.querySelector(".hero-description").style.display = "block";
  }
}

window.onload = () => {
  typeWriterEffect();
  initNoiseEffect();
};

// Inicia e anima o efeito de ruído
function initNoiseEffect() {
  const canvas = document.getElementById('noiseCanvas');
  const ctx = canvas.getContext('2d');
  canvas.width = window.innerWidth;
  canvas.height = window.innerHeight;

  function generateNoise() {
    const imageData = ctx.createImageData(canvas.width, canvas.height);
    const buffer = new Uint32Array(imageData.data.buffer);
    for (let i = 0; i < buffer.length; i++) {
      buffer[i] = Math.random() < 0.1 ? 0xffffffff : 0xff000000;
    }
    ctx.putImageData(imageData, 0, 0);
    requestAnimationFrame(generateNoise);
  }
  generateNoise();
}

// Redimensiona o canvas se a janela mudar
window.addEventListener('resize', () => {
  const canvas = document.getElementById('noiseCanvas');
  canvas.width = window.innerWidth;
  canvas.height = window.innerHeight;
});
</script>
