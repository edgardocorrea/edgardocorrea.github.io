---
layout: single
title: "Sobre Mim"
permalink: /sobre/
author_profile: false
sidebar: null
---
<div id="custom-sobre-page">

<style>
/* Reset & Base */
html, body {
  overflow-x: hidden;
  overflow-y: auto;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Inter', 'Segoe UI', sans-serif;
  overflow-x: hidden;
  position: relative;
}

.initial-content {
  position: relative;
  background: rgba(10,20,40,0.85);
  padding: 30px 25px;
  border-radius: 20px;
  box-shadow: 0 8px 25px rgba(0,0,0,0.6);
  backdrop-filter: blur(3px);
  z-index: 1;
}

.page__content {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

/* Particles Background */
.particles-bg {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  overflow: hidden;
  width: 100%;
  height: 100%;
  z-index: 0;
  pointer-events: none;
  background: 
  radial-gradient(circle at 20% 30%, rgba(0, 234, 255, 0.03) 0%, transparent 50%),
  radial-gradient(circle at 80% 70%, rgba(0, 102, 255, 0.03) 0%, transparent 50%);
  will-change: transform;
  transform: translateY(0) !important;
  pointer-events: none;
  overflow: hidden;
  will-change: transform;
}

.particles-bg::before {
  content: '';
  position: absolute;
  width: 100%;
  height: 100%;
  background: 
    radial-gradient(circle at 25% 20%, rgba(0, 234, 255, 0.10), transparent 60%),
    radial-gradient(circle at 80% 80%, rgba(0, 102, 255, 0.10), transparent 60%),
    radial-gradient(circle at 50% 50%, rgba(255, 255, 255, 0.06), transparent 70%);
  animation: softGlow 12s ease-in-out infinite alternate;
  filter: blur(4px);
}

@keyframes softGlow {
  0% { opacity: 0.7; transform: scale(1); }
  100% { opacity: 1; transform: scale(1.05); }
}

/* Hero Section */
.hero-section {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 60px 20px 80px 20px;
  position: relative;
  z-index: 1;
}

.neon-text {
  color: #ffffff;
  font-weight: 700;
  text-shadow:
    0 0 10px rgba(255, 255, 255, 0.9),
    0 0 20px rgba(0, 234, 255, 0.8),
    0 0 35px rgba(0, 234, 255, 0.6),
    0 0 50px rgba(0, 234, 255, 0.4);
  transition: all 0.3s ease;
}

.neon-text:hover {
  text-shadow:
    0 0 15px white,
    0 0 30px #00eaff,
    0 0 50px #00eaff,
    0 0 80px #00eaff;
}

.avatar-container {
  width: 200px;
  height: 200px;
  margin-bottom: 40px;
  position: relative;
  animation: float 3s ease-in-out infinite;
}

.avatar-glow {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 220px;
  height: 220px;
  background: radial-gradient(circle, rgba(0, 234, 255, 0.4), transparent 70%);
  animation: pulse 2s ease-in-out infinite;
  filter: blur(20px);
}

.avatar-container img {
  position: relative;
  width: 100%;
  height: 100%;
  object-fit: contain;
  filter: drop-shadow(0 0 30px rgba(0, 234, 255, 0.8));
  z-index: 2;
}

@keyframes float {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-20px); }
}

@keyframes pulse {
  0%, 100% { opacity: 0.5; transform: translate(-50%, -50%) scale(1); }
  50% { opacity: 1; transform: translate(-50%, -50%) scale(1.1); }
}

.hero-title {
  font-size: 64px;
  font-weight: 900;
  margin-bottom: 20px;
  background: linear-gradient(90deg, #00eaff, #0066ff, #00eaff);
  background-size: 200% auto;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  animation: gradient 3s ease infinite;
  /* CORREÇÃO: Usar drop-shadow para o efeito neon */
  filter: drop-shadow(0 0 40px rgba(0, 234, 255, 0.8));
}

@keyframes gradient {
  0%, 100% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
}

.typewriter {
  font-size: 28px;
  color: #ffffff;
  font-weight: 700;
  margin-bottom: 30px;
  border-right: 3px solid #ffffff;
  background: transparent !important;
  background-color: transparent !important;
  white-space: nowrap;
  overflow: hidden;
  text-shadow: none !important;
  animation: typing 3s steps(40) 1s 1 normal both, blink 0.7s infinite;
}

@keyframes typing {
  from { width: 0; }
  to { width: 100%; }
}

@keyframes blink {
  50% { border-color: transparent; }
}

.hero-description {
  font-size: 18px;
  color: #b3d9ff;
  max-width: 600px;
  line-height: 1.6;
  margin-bottom: 40px;
}

.cta-button {
  display: inline-block;
  padding: 16px 40px;
  background: #ffffff;
  color: #000;
  font-size: 18px;
  font-weight: 700;
  text-decoration: none;
  border-radius: 50px;
  position: relative;
  overflow: hidden;
  transition: all 0.3s ease;
  box-shadow: 0 0 22px rgba(255, 255, 255, 0.7),
              0 0 42px rgba(255, 255, 255, 0.9),
              inset 0 0 15px rgba(255, 255, 255, 0.5);
}

.cta-button:hover {
  transform: translateY(-3px);
  background: #fff;
  box-shadow: 
    0 0 25px rgba(255,255,255,1),
    0 0 55px rgba(255,255,255,1),
    0 0 85px rgba(0,234,255,0.9),
    inset 0 0 25px rgba(255,255,255,0.8);
}

.cta-button:active {
  transform: scale(0.96);
  box-shadow:
    0 0 35px rgba(255,255,255,1),
    0 0 70px rgba(0,234,255,1),
    inset 0 0 35px rgba(255,255,255,1);
}

.scroll-indicator {
  position: absolute;
  bottom: 20px;
  left: 50%;
  transform: translateX(-50%);
  color: #00eaff;
  animation: bounce 2s infinite;
}

@keyframes bounce {
  0%, 20%, 50%, 80%, 100% { transform: translateX(-50%) translateY(0); }
  40% { transform: translateX(-50%) translateY(-20px); }
  60% { transform: translateX(-50%) translateY(-10px); }
}

/* Expandable Sections */
.content-section {
  position: relative;
  z-index: 1;
  margin: 80px 0 40px 0;
}

.section-accordion {
  background: linear-gradient(145deg, rgba(0, 102, 255, 0.05), rgba(0, 234, 255, 0.05));
  border: 2px solid rgba(0, 234, 255, 0.3);
  border-radius: 20px;
  margin-bottom: 30px;
  overflow: hidden;
  transition: all 0.3s ease;
}

.section-accordion:hover {
  border-color: rgba(0, 234, 255, 0.6);
  box-shadow: 0 10px 40px rgba(0, 234, 255, 0.2);
}

.accordion-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 25px 30px;
  cursor: pointer;
  user-select: none;
}

.accordion-title {
  display: flex;
  align-items: center;
  gap: 15px;
  font-size: 28px;
  font-weight: 700;
  color: #00eaff;
}

.accordion-icon {
  font-size: 32px;
  transition: transform 0.3s ease;
}

.accordion-header:hover .accordion-icon {
  transform: scale(1.2);
}

.accordion-arrow {
  font-size: 24px;
  color: #00ff88;
  transition: transform 0.3s ease;
}

.section-accordion.active .accordion-arrow {
  transform: rotate(180deg);
}

.accordion-content {
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.5s ease, padding 0.5s ease;
  padding: 0 30px;
}

.section-accordion.active .accordion-content {
  max-height: 2000px;
  padding: 0 30px 30px 30px;
}

/* Interest Cards */
.interests-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 20px;
  margin-top: 30px;
}

.interest-card {
  background: rgba(0, 20, 40, 0.6);
  border: 2px solid rgba(0, 234, 255, 0.3);
  border-radius: 15px;
  padding: 30px;
  text-align: center;
  transition: all 0.3s ease;
  cursor: pointer;
}

.interest-card:hover {
  transform: translateY(-10px);
  border-color: #00eaff;
  box-shadow: 0 15px 40px rgba(0, 234, 255, 0.3);
}

.interest-icon {
  font-size: 48px;
  margin-bottom: 15px;
  display: block;
}

.interest-title {
  color: #00eaff;
  font-weight: 600;
  font-size: 18px;
}

/* Social Links */
.social-links {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
  margin-top: 30px;
}

.social-card {
  background: rgba(0, 20, 40, 0.6);
  border: 2px solid rgba(0, 234, 255, 0.3);
  border-radius: 15px;
  padding: 30px;
  text-align: center;
  text-decoration: none;
  display: block;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

.social-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(0, 234, 255, 0.1), transparent);
  transition: left 0.5s ease;
}

.social-card:hover::before {
  left: 100%;
}

.social-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 15px 40px rgba(0, 234, 255, 0.4);
}

.social-card.linkedin { border-color: #0077b5; }
.social-card.linkedin:hover { border-color: #0077b5; box-shadow: 0 15px 40px rgba(0, 119, 181, 0.4); }

.social-card.github { border-color: #333; }
.social-card.github:hover { border-color: #fff; box-shadow: 0 15px 40px rgba(255, 255, 255, 0.3); }

.social-card.email { border-color: #00ff88; }
.social-card.email:hover { border-color: #00ff88; box-shadow: 0 15px 40px rgba(0, 255, 136, 0.4); }

.social-icon {
  font-size: 48px;
  margin-bottom: 15px;
  display: block;
}

.social-title {
  color: #00eaff;
  font-size: 20px;
  font-weight: 700;
  margin-bottom: 10px;
}

.social-description {
  color: #b3d9ff;
  font-size: 14px;
}

/* Easter Egg Hint */
.easter-egg-hint {
  text-align: center;
  color: #666;
  font-size: 12px;
  margin-top: 40px;
  opacity: 0.6;
}

/* Responsive */
@media (max-width: 768px) {
  .hero-title { font-size: 42px; }
  .typewriter { font-size: 20px; }
  .hero-description { font-size: 16px; }
  
  .accordion-title { font-size: 22px; }
}
</style>

<!-- Background Particles -->
<div class="particles-bg"></div>

<!-- Hero Section -->
<section class="hero-section">
  <div class="avatar-container">
    <div class="avatar-glow"></div>
    <img src="/assets/images/minha_foto.png" alt="Logo EC" />
  </div>
  
  <h1 class="hero-title">EDGARDO CORREA</h1>
  
  <div class="typewriter">Analista de Sistemas</div>
  
  <p class="hero-description">
    Transformando desafios técnicos em soluções elegantes. 
    Especializado em infraestrutura, redes e automação com paixão por inovação.
  </p>
  
  <a href="#contato" class="cta-button">Entre em contato.</a>
  
  <div class="scroll-indicator">
    <span style="font-size: 32px;">↓</span>
  </div>
</section>

<!-- Main Content -->
<div class="content-section">

  <!-- About Me -->
  <div class="section-accordion">
    <div class="accordion-header" onclick="toggleAccordion(this)">
      <div class="accordion-title">
        <span class="accordion-icon">🔷</span>
        <span class="neon-text">Sobre Mim</span>
      </div>
      <span class="accordion-arrow">▼</span>
    </div>
    <div class="accordion-content">
      <p style="color: #b3d9ff; line-height: 1.8; font-size: 16px;">
        Formado em <strong style="color: #00eaff;">Sistemas de Informação</strong> e movido pela paixão em resolver problemas complexos de forma criativa. Acredito que tecnologia é sobre pessoas — criar soluções que realmente fazem diferença no dia a dia.
      </p>
      <p style="color: #b3d9ff; line-height: 1.8; font-size: 16px; margin-top: 15px;">
        Minha filosofia: <strong style="color: #00ff88;">"Todo problema tem solução, e cada desafio é uma oportunidade de crescimento."</strong> Adoro trabalhar em equipe, compartilhar conhecimento e trazer energia positiva para os projetos.
      </p>      <p style="color: #b3d9ff; line-height: 1.8; font-size: 16px; margin-top: 15px;">
        Meu slogan: <strong style="color: #00ff88;">"Simplifique e Conquiste o Certo."</strong>
      </p>
      <p style="color: #b3d9ff; line-height: 1.8; font-size: 16px; margin-top: 15px;">
        Quando não estou codando ou resolvendo tickets, você me encontra assistindo animes, explorando novas tecnologias ou pensando em como automatizar processos do dia a dia. 
      </p>
    </div>
  </div>

  <!-- Interests -->
  <div class="section-accordion">
    <div class="accordion-header" onclick="toggleAccordion(this)">
      <div class="accordion-title">
        <span class="accordion-icon">🔷</span>
        <span class="neon-text">Além do Código</span>
      </div>
      <span class="accordion-arrow">▼</span>
    </div>
    <div class="accordion-content">
      <div class="interests-grid">
        <div class="interest-card">
          <span class="interest-icon">🔹</span>
          <div class="interest-title">Animes & Séries</div>
        </div>
        <div class="interest-card">
          <span class="interest-icon">🔹</span>
          <div class="interest-title">Inteligência Artificial</div>
        </div>
        <div class="interest-card">
          <span class="interest-icon">🔹</span>
          <div class="interest-title">Automação</div>
        </div>
        <div class="interest-card">
          <span class="interest-icon">🔹</span>
          <div class="interest-title">Inovação Tech</div>
        </div>
        <div class="interest-card">
          <span class="interest-icon">🔹</span>
          <div class="interest-title">Podcasts Tech</div>
        </div>
        <div class="interest-card">
          <span class="interest-icon">🔹</span>
          <div class="interest-title">Web Development</div>
        </div>
      </div>
    </div>
  </div>

  <!-- Contact -->
  <div class="section-accordion" id="contato">
    <div class="accordion-header" onclick="toggleAccordion(this)">
      <div class="accordion-title">
        <span class="accordion-icon">🔷</span>
        <span class="neon-text">Vamos Conectar?</span>
      </div>
      <span class="accordion-arrow">▼</span>
    </div>
    <div class="accordion-content">
      <p style="color: #b3d9ff; text-align: center; margin-bottom: 30px; font-size: 18px;">
        Sempre aberto para conversas sobre tecnologia, oportunidades ou apenas trocar ideias!
      </p>
      
      <div class="social-links">
        <a href="https://linkedin.com/in/edgardocorrea" class="social-card linkedin" target="_blank">
          <span class="social-icon">💼</span>
          <div class="social-title">LinkedIn</div>
          <div class="social-description">Conecte-se profissionalmente</div>
        </a>
        
        <a href="https://github.com/edgardocorrea" class="social-card github" target="_blank">
          <span class="social-icon">💻</span>
          <div class="social-title">GitHub</div>
          <div class="social-description">Explore meus projetos</div>
        </a>
        
        <a href="mailto:edgardo.edyone-1@yahoo.com" class="social-card email">
          <span class="social-icon">📧</span>
          <div class="social-title">Email</div>
          <div class="social-description">Envie uma mensagem direta</div>
        </a>
      </div>
    </div>
  </div>

</div>

<!-- Dica para o Easter Egg -->
<p class="easter-egg-hint">Dica: Tente digitar "edy1" em qualquer lugar da página... 😉</p>

</div> <!-- End of Wrapper -->

<!-- Accordion Functionality -->
<script>
function toggleAccordion(header) {
  const accordion = header.parentElement;
  const allAccordions = document.querySelectorAll('.section-accordion');
  
  // Close all other accordions
  allAccordions.forEach(acc => {
    if (acc !== accordion && acc.classList.contains('active')) {
      acc.classList.remove('active');
    }
  });
  
  // Toggle the clicked accordion
  accordion.classList.toggle('active');
  
  // Smooth scroll to the accordion
  if (accordion.classList.contains('active')) {
    setTimeout(() => {
      accordion.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
    }, 100);
  }
}

// Smooth scroll for anchors
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
  anchor.addEventListener('click', function (e) {
    e.preventDefault();
    const target = document.querySelector(this.getAttribute('href'));
    if (target) {
      target.scrollIntoView({ behavior: 'smooth', block: 'start' });
      
      // Open accordion if it's a link to a section
      const accordion = target.closest('.section-accordion');
      if (accordion && !accordion.classList.contains('active')) {
        accordion.querySelector('.accordion-header').click();
      }
    }
  });
});

// Typewriter Effect
const typewriterElement = document.querySelector('.typewriter');
if (typewriterElement) {
  const text = typewriterElement.textContent;
  typewriterElement.textContent = '';
  typewriterElement.style.width = '0';
  
  setTimeout(() => {
    typewriterElement.style.width = '100%';
    let i = 0;
    const typingInterval = setInterval(() => {
      if (i < text.length) {
        typewriterElement.textContent += text.charAt(i);
        i++;
      } else {
        clearInterval(typingInterval);
      }
    }, 100);
  }, 1000);
}

// Parallax Effect on Scroll
let isScrollTicking = false;
window.addEventListener('scroll', () => {
  if (!isScrollTicking) {
    window.requestAnimationFrame(() => {
      const scrolled = window.pageYOffset;
      const parallaxBg = document.querySelector('.particles-bg');
      if (parallaxBg) {
        parallaxBg.style.transform = `translateY(${scrolled * 0.2}px)`;
      }
      isScrollTicking = false;
    });
    isScrollTicking = true;
  }
});

// Intersection Observer for Animations
const observerOptions = {
  threshold: 0.2,
  rootMargin: '0px 0px -100px 0px'
};

const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.style.opacity = '1';
      entry.target.style.transform = 'translateY(0)';
    }
  });
}, observerOptions);

// Observe all animatable cards
document.querySelectorAll('.interest-card, .social-card').forEach(el => {
  el.style.opacity = '0';
  el.style.transform = 'translateY(30px)';
  el.style.transition = 'all 0.6s ease';
  observer.observe(el);
});

// Easter Egg: "edy1" code
const easterEggCode = 'edy1';
let typedString = '';
let easterEggTimeout;

document.addEventListener('keydown', (e) => {
  // Limpa o timeout anterior
  clearTimeout(easterEggTimeout);

  // Adiciona a tecla pressionada à string
  typedString += e.key;

  // Verifica se o código foi digitado (ignorando maiúsculas/minúsculas)
  if (typedString.toLowerCase().includes(easterEggCode)) {
    triggerEasterEgg();
    typedString = ''; // Reseta a string após ativar
  }

  // Reseta a string se o usuário parar de digitar por 2 segundos
  easterEggTimeout = setTimeout(() => {
    typedString = '';
  }, 2000);
});

function triggerEasterEgg() {
  document.body.style.animation = 'rainbow 2s linear infinite';
  setTimeout(() => {
    alert('🎉 Parabéns! Você ativou o modo arco-íris! 🚀');
    document.body.style.animation = '';
  }, 100);
}

// Rainbow Animation for Easter Egg
const style = document.createElement('style');
style.textContent = `
  @keyframes rainbow {
    0% { filter: hue-rotate(0deg); }
    100% { filter: hue-rotate(360deg); }
  }
`;
document.head.appendChild(style);
</script>
