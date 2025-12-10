---
title: "" # Força título vazio
excerpt: "" # Força excerpt vazio
layout: splash
header:
  overlay_color: "rgba(0,0,0,0.5)"
  overlay_filter: 0.4
  image_description: "" # Remove alt text
---

<!-- TÍTULOS PRINCIPAIS (SEO) -->
<h1 class="hero-h1">Edgardo Correa</h1>
<h2 class="hero-h2">Analista de Sistemas – Redes, Infraestrutura e Segurança</h2>

<!-- Imagem e texto customizado posicionado sobre a tela do notebook -->
<div class="hero-image-wrapper">
  <canvas id="noiseCanvas"></canvas>
  <img src="/assets/images/banner-home.jpg" alt="Notebook Banner" class="hero-img">

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

/* ------------------------------------------------ */
/*       H1 e H2 - Tema Dourado/Cobre          */
/* ------------------------------------------------ */

.hero-h1 {
  text-align: center;
  font-size: 3rem;
  margin-top: 40px;
  margin-bottom: 10px;
  color: #d4af37; /* Dourado */
  text-shadow:
    0 0 4px #d4af37,
    0 0 8px #b8860b,
    0 0 15px #a67c00,
    0 0 25px #8b6914;
  font-family: "Courier New", monospace;
  font-weight: bold;
  animation: goldGlow 3s ease-in-out infinite alternate;
}

.hero-h2 {
  text-align: center;
  font-size: 1.6rem;
  margin-bottom: 30px;
  color: #f0e68c; /* Amarelo claro */
  text-shadow:
    0 0 3px #f0e68c,
    0 0 6px #daa520,
    0 0 12px #b8860b;
  font-family: "Courier New", monospace;
  animation: goldGlow 3.5s ease-in-out infinite alternate;
}

@keyframes goldGlow {
  0% {
    text-shadow:
      0 0 4px #d4af37,
      0 0 8px #b8860b,
      0 0 15px #a67c00,
      0 0 25px #8b6914;
  }
  100% {
    text-shadow:
      0 0 6px #d4af37,
      0 0 12px #b8860b,
      0 0 20px #a67c00,
      0 0 30px #8b6914;
  }
}

/* ------------------------------------------------ */
/* ESTILOS EXISTENTES – MELHORADOS COM TEMA DOURADO     */
/* ------------------------------------------------ */

/* Efeito de ruído no canvas - mais sutil */
#noiseCanvas {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 5;
  pointer-events: none;
  mix-blend-mode: overlay;
  opacity: 0.15; /* mais sutil */
}

/* Estilo da imagem principal com efeito dourado */
.hero-img {
  position: relative;
  z-index: 8;
  border-radius: 18px;
  border: 3px solid #1a1a1a; /* Preto mais profundo */
  box-shadow:
    0 0 8px #1a1a1a,
    0 0 16px #2a2a2a,
    0 0 30px #3a3a3a,
    0 0 45px rgba(212, 175, 55, 0.2); /* brilho dourado sutil */
  animation: goldPulse 4s ease-in-out infinite alternate;
}

@keyframes goldPulse {
  0% {
    box-shadow:
      0 0 8px #1a1a1a,
      0 0 16px #2a2a2a,
      0 0 30px #3a3a3a,
      0 0 45px rgba(212, 175, 55, 0.2);
  }
  100% {
    box-shadow:
      0 0 12px #1a1a1a,
      0 0 25px #2a2a2a,
      0 0 40px #3a3a3a,
      0 0 55px rgba(212, 175, 55, 0.3); /* brilho dourado máximo */
  }
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
  background-color: rgba(0, 0, 0, 0.4);
  border: none;
  border-radius: 8px;
  box-shadow: none;
  font-family: "Courier New", monospace;
  animation: flickerScreen 2s infinite;
}

/* Prompt de comando - dourado */
.command-prompt {
  color: #d4af37;
  font-weight: bold;
}

/* Texto da digitação - dourado */
#typewriter {
  color: #f0e68c;
  text-shadow: 0 0 4px #d4af37;
}

/* Texto descritivo - amarelo claro */
.hero-description .custom-excerpt {
  color: #f0e68c;
  font-size: 16px;
  line-height: 1.5;
  margin-top: 20px;
  text-shadow: 0 0 6px #d4af3788;
}

/* Cursor Piscante - dourado */
.cursor-blink {
  display: inline-block;
  width: 10px;
  height: 20px;
  background: #d4af37;
  margin-left: 5px;
  animation: blinkCursor 0.9s infinite;
  box-shadow: 0 0 4px #d4af37;
}

/* Responsivo - Tablets */
@media (max-width: 768px) {
  .hero-text-overlay {
    width: 70%;
    top: 40%;
    padding: 15px 20px;
  }
  .hero-description .custom-excerpt {
    font-size: 14px;
  }
  #typewriter, .command-prompt {
    font-size: 14px;
  }
}

/* Responsivo - Celulares */
@media (max-width: 480px) {
  .hero-text-overlay {
    width: 85%;
    top: 50%;
    padding: 10px 15px;
    text-align: center;
  }

  .hero-description .custom-excerpt {
    font-size: 13px;
    line-height: 1.4;
  }

  #typewriter, .command-prompt {
    font-size: 12px;
  }

  .cursor-blink {
    width: 6px;
    height: 16px;
  }
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
