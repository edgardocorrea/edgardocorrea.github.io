---
title: "" # Força título vazio
excerpt: "" # Força excerpt vazio
layout: splash
header:
  overlay_color: "rgba(0,0,0,0.4)"
  overlay_filter: 0.3
  image_description: "" # Remove alt text
---
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
  opacity: 0.15; /* intensidade do ruído */
}

/* Estilo da imagem principal com efeito neon */
.hero-img {
  position: relative;
  z-index: 8;
  border-radius: 18px;
  border: 3px solid #10192c; /* Azul escuro */
  box-shadow:
    0 0 6px #10192c,
    0 0 12px #16233a,   /* tom levemente mais claro */
    0 0 22px #1d3254;   /* brilho externo */
  animation: neonPulse 2.5s ease-in-out infinite alternate;
}

@keyframes neonPulse {
  0% {
    box-shadow:
      0 0 6px #10192c,
      0 0 12px #16233a,
      0 0 22px #1d3254;
  }
  100% {
    box-shadow:
      0 0 10px #16233a,
      0 0 20px #1d3254,
      0 0 35px #274977; /* brilho máximo */
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
  background-color: rgba(0, 0, 0, 0.3); /* Fundo mais transparente */
  border: none; /* Remove borda azul */
  border-radius: 8px;
  box-shadow: none; /* Remove sombra */
  font-family: "Courier New", monospace;
  animation: flickerScreen 1.5s infinite;
}

/* Efeito flicker sutil */
@keyframes flickerScreen {
  0%, 19%, 21%, 23%, 25%, 54%, 56%, 100% { opacity: 1; }
  20%, 22%, 24%, 55% { opacity: 0.85; }
}

/* Prompt de comando */
.command-prompt {
  color: #00aaff;
  font-weight: bold;
}

/* Texto da digitação */
#typewriter {
  color: #00eaff;
}

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

@keyframes blinkCursor {
  0%, 50% { opacity: 1; }
  51%, 100% { opacity: 0; }
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
    width: 85%; /* Largura maior para telas pequenas */
    top: 50%;
    padding: 10px 15px;
    text-align: center; /* Centraliza o texto no mobile */
  }

  .hero-description .custom-excerpt {
    font-size: 13px; /* CORREÇÃO: Fonte legível */
    line-height: 1.4;
  }

  #typewriter, .command-prompt {
    font-size: 12px; /* CORREÇÃO: Fonte legível */
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
    setTimeout(typeWriterEffect, 55); // velocidade da digitação
  } else {
    // CORREÇÃO: Usa querySelector para a classe
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
      buffer[i] = Math.random() < 0.1 ? 0xffffffff : 0xff000000; // pixels brancos aleatórios
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
