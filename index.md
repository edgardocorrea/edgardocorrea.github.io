---
title: "" 
excerpt: "" 
layout: splash
header:
  overlay_color: "rgba(255,255,255,0.0)"
  overlay_filter: 0
  image_description: "" 
---

<!-- TÍTULOS PRINCIPAIS (SEO) -->
<h1 class="hero-h1">Edgardo Correa</h1>
<h2 class="hero-h2">Analista de Sistemas – Redes, Infraestrutura e Segurança</h2>

<!-- Imagem e texto customizado sobre a tela do notebook -->
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
/*       H1 e H2 - Simples e Profissional          */
/* ------------------------------------------------ */

.hero-h1 {
  text-align: center;
  font-size: 3rem;
  margin-top: 40px;
  margin-bottom: 10px;
  color: #1a1a1a; /* preto escuro */
  text-shadow: 1px 1px 2px #bbb; /* leve sombra cinza */
  font-family: "Courier New", monospace;
  font-weight: bold;
}

.hero-h2 {
  text-align: center;
  font-size: 1.6rem;
  margin-bottom: 30px;
  color: #555555; /* cinza escuro */
  font-family: "Courier New", monospace;
}

/* ------------------------------------------------ */
/* ESTILOS EXISTENTES – LIMPOS                       */
/* ------------------------------------------------ */

#noiseCanvas {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 5;
  pointer-events: none;
  mix-blend-mode: overlay;
  opacity: 0.05; /* mais sutil */
}

.hero-img {
  position: relative;
  z-index: 8;
  border-radius: 18px;
  border: 2px solid #ccc;
  box-shadow:
    0 0 6px #ddd,
    0 0 12px #eee;
}

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
  background-color: rgba(255, 255, 255, 0.85);
  border-radius: 8px;
  font-family: "Courier New", monospace;
}

.command-prompt {
  color: #333;
  font-weight: bold;
}

#typewriter {
  color: #111;
}

.hero-description .custom-excerpt {
  color: #555;
  font-size: 16px;
  line-height: 1.5;
  margin-top: 20px;
}

.cursor-blink {
  display: inline-block;
  width: 10px;
  height: 20px;
  background: #333;
  margin-left: 5px;
  animation: blinkCursor 0.9s infinite;
}

@keyframes blinkCursor {
  0%, 50% { opacity: 1; }
  51%, 100% { opacity: 0; }
}

/* Responsivo */
@media (max-width: 768px) {
  .hero-text-overlay {
    width: 70%;
    top: 40%;
    padding: 15px 20px;
  }
  #typewriter, .command-prompt {
    font-size: 14px;
  }
}

@media (max-width: 480px) {
  .hero-text-overlay {
    width: 85%;
    top: 50%;
    padding: 10px 15px;
    text-align: center;
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

function initNoiseEffect() {
  const canvas = document.getElementById('noiseCanvas');
  const ctx = canvas.getContext('2d');
  canvas.width = window.innerWidth;
  canvas.height = window.innerHeight;

  function generateNoise() {
    const imageData = ctx.createImageData(canvas.width, canvas.height);
    const buffer = new Uint32Array(imageData.data.buffer);
    for (let i = 0; i < buffer.length; i++) {
      buffer[i] = Math.random() < 0.05 ? 0xffffffff : 0xff000000;
    }
    ctx.putImageData(imageData, 0, 0);
    requestAnimationFrame(generateNoise);
  }

  generateNoise();
}

window.addEventListener('resize', () => {
  const canvas = document.getElementById('noiseCanvas');
  canvas.width = window.innerWidth;
  canvas.height = window.innerHeight;
});
</script>
