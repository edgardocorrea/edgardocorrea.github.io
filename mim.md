---
layout: single
title: "Sobre Mim"
permalink: /sobre/
author_profile: false
---

<style>
/* ==================== RESET & BASE ==================== */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background: #000814 !important;
  color: #e6faff;
  font-family: 'Inter', 'Segoe UI', sans-serif;
  overflow-x: hidden;
}

.page__content {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

/* ==================== PARTÍCULAS DE FUNDO ==================== */
.particles-bg {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 0;
  pointer-events: none;
  background: 
    radial-gradient(circle at 20% 30%, rgba(0, 234, 255, 0.03) 0%, transparent 50%),
    radial-gradient(circle at 80% 70%, rgba(0, 102, 255, 0.03) 0%, transparent 50%);
}

.particles-bg::before {
  content: '';
  position: absolute;
  width: 100%;
  height: 100%;
  background-image: 
    repeating-linear-gradient(0deg, rgba(0, 234, 255, 0.03) 0px, transparent 2px, transparent 40px),
    repeating-linear-gradient(90deg, rgba(0, 234, 255, 0.03) 0px, transparent 2px, transparent 40px);
  animation: gridMove 20s linear infinite;
}

@keyframes gridMove {
  0% { transform: translate(0, 0); }
  100% { transform: translate(40px, 40px); }
}

/* ==================== HERO SECTION ==================== */
.hero-section {
  position: relative;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 60px 20px;
  z-index: 1;
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
  text-shadow: 0 0 40px rgba(0, 234, 255, 0.5);
}

@keyframes gradient {
  0%, 100% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
}

.typewriter {
  font-size: 28px;
  color: #00ff88;
  font-weight: 600;
  margin-bottom: 30px;
  border-right: 3px solid #00ff88;
  white-space: nowrap;
  overflow: hidden;
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
  background: linear-gradient(135deg, #00ff88, #00ccaa);
  color: #000814;
  font-size: 18px;
  font-weight: 700;
  text-decoration: none;
  border-radius: 50px;
  position: relative;
  overflow: hidden;
  transition: all 0.3s ease;
  box-shadow: 0 0 30px rgba(0, 255, 136, 0.4);
  animation: ctaPulse 2s ease-in-out infinite;
}

.cta-button:hover {
  transform: translateY(-3px);
  box-shadow: 0 10px 40px rgba(0, 255, 136, 0.6);
}

@keyframes ctaPulse {
  0%, 100% { box-shadow: 0 0 30px rgba(0, 255, 136, 0.4); }
  50% { box-shadow: 0 0 50px rgba(0, 255, 136, 0.8); }
}

.scroll-indicator {
  position: absolute;
  bottom: 30px;
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

/* ==================== SEÇÕES EXPANSÍVEIS ==================== */
.content-section {
  position: relative;
  z-index: 1;
  margin: 80px 0;
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

/* ==================== TIMELINE ==================== */
.timeline {
  position: relative;
  padding: 20px 0;
}

.timeline::before {
  content: '';
  position: absolute;
  left: 50%;
  top: 0;
  bottom: 0;
  width: 3px;
  background: linear-gradient(180deg, #00eaff, #0066ff);
  box-shadow: 0 0 10px #00eaff;
}

.timeline-item {
  display: flex;
  margin-bottom: 40px;
  position: relative;
  opacity: 0;
  animation: fadeInUp 0.6s ease forwards;
}

.timeline-item:nth-child(odd) {
  flex-direction: row-reverse;
}

.timeline-item:nth-child(1) { animation-delay: 0.2s; }
.timeline-item:nth-child(2) { animation-delay: 0.4s; }
.timeline-item:nth-child(3) { animation-delay: 0.6s; }

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.timeline-content {
  width: 45%;
  background: rgba(0, 20, 40, 0.6);
  border: 1px solid rgba(0, 234, 255, 0.3);
  border-radius: 15px;
  padding: 20px;
  backdrop-filter: blur(10px);
}

.timeline-dot {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  width: 20px;
  height: 20px;
  background: #00ff88;
  border-radius: 50%;
  box-shadow: 0 0 20px #00ff88;
  animation: dotPulse 2s infinite;
}

@keyframes dotPulse {
  0%, 100% { box-shadow: 0 0 20px #00ff88; }
  50% { box-shadow: 0 0 40px #00ff88; }
}

.timeline-date {
  color: #00ff88;
  font-weight: 600;
  margin-bottom: 10px;
}

.timeline-title {
  color: #00eaff;
  font-size: 20px;
  font-weight: 700;
  margin-bottom: 10px;
}

/* ==================== SKILLS ==================== */
.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 20px;
  margin-top: 30px;
}

.skill-item {
  margin-bottom: 25px;
}

.skill-header {
  display: flex;
  justify-content: space-between;
  margin-bottom: 10px;
}

.skill-name {
  color: #00eaff;
  font-weight: 600;
}

.skill-level {
  color: #00ff88;
  font-weight: 600;
}

.skill-bar {
  height: 10px;
  background: rgba(0, 234, 255, 0.1);
  border-radius: 10px;
  overflow: hidden;
  position: relative;
}

.skill-fill {
  height: 100%;
  background: linear-gradient(90deg, #0066ff, #00eaff);
  border-radius: 10px;
  box-shadow: 0 0 15px rgba(0, 234, 255, 0.6);
  width: 0;
  transition: width 1.5s ease;
}

.section-accordion.active .skill-fill {
  animation: fillBar 1.5s ease forwards;
}

@keyframes fillBar {
  to { width: var(--skill-width); }
}

/* ==================== CARDS DE INTERESSE ==================== */
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

/* ==================== LINKS SOCIAIS ==================== */
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

/* ==================== RESPONSIVO ==================== */
@media (max-width: 768px) {
  .hero-title { font-size: 42px; }
  .typewriter { font-size: 20px; }
  .hero-description { font-size: 16px; }
  
  .timeline::before { left: 20px; }
  .timeline-item { flex-direction: column !important; margin-left: 40px; }
  .timeline-content { width: 100%; }
  .timeline-dot { left: 20px; }
  
  .accordion-title { font-size: 22px; }
  .skills-grid { grid-template-columns: 1fr; }
}
</style>

<!-- Partículas de Fundo -->
<div class="particles-bg"></div>

<!-- Hero Section -->
<section class="hero-section">
  <div class="avatar-container">
    <div class="avatar-glow"></div>
    <img src="./minha_foto.jpg" alt="Logo EC" />
  </div>
  
  <h1 class="hero-title">EDGARDO CORREA</h1>
  
  <div class="typewriter">Analista de Sistemas | Tech Enthusiast</div>
  
  <p class="hero-description">
    Transformando desafios técnicos em soluções elegantes. 
    Especializado em infraestrutura, redes e automação com paixão por inovação.
  </p>
  
  <a href="#contato" class="cta-button">Vamos Conversar! 🚀</a>
  
  <div class="scroll-indicator">
    <span style="font-size: 32px;">↓</span>
  </div>
</section>

<!-- Conteúdo Principal -->
<div class="content-section">

  <!-- Sobre Mim -->
  <div class="section-accordion">
    <div class="accordion-header" onclick="toggleAccordion(this)">
      <div class="accordion-title">
        <span class="accordion-icon">💡</span>
        <span>Sobre Mim</span>
      </div>
      <span class="accordion-arrow">▼</span>
    </div>
    <div class="accordion-content">
      <p style="color: #b3d9ff; line-height: 1.8; font-size: 16px;">
        Formado em <strong style="color: #00eaff;">Sistemas de Informação</strong> e movido pela paixão em resolver problemas complexos de forma criativa. Acredito que tecnologia é sobre pessoas — criar soluções que realmente fazem diferença no dia a dia.
      </p>
      <p style="color: #b3d9ff; line-height: 1.8; font-size: 16px; margin-top: 15px;">
        Minha filosofia: <strong style="color: #00ff88;">"Todo problema tem solução, e cada desafio é uma oportunidade de crescimento."</strong> Adoro trabalhar em equipe, compartilhar conhecimento e trazer energia positiva para os projetos.
      </p>
      <p style="color: #b3d9ff; line-height: 1.8; font-size: 16px; margin-top: 15px;">
        Quando não estou codando ou resolvendo tickets, você me encontra assistindo animes, explorando novas tecnologias ou pensando em como automatizar processos do dia a dia. 🎮✨
      </p>
    </div>
  </div>

  <!-- Experiência -->
  <div class="section-accordion">
    <div class="accordion-header" onclick="toggleAccordion(this)">
      <div class="accordion-title">
        <span class="accordion-icon">💼</span>
        <span>Jornada Profissional</span>
      </div>
      <span class="accordion-arrow">▼</span>
    </div>
    <div class="accordion-content">
      <div class="timeline">
        <div class="timeline-item">
          <div class="timeline-content">
            <div class="timeline-date">2024 - Atual</div>
            <div class="timeline-title">Analista de Suporte & Infraestrutura</div>
            <p style="color: #b3d9ff; margin-top: 10px;">
              Especialização em Service Desk, Windows Server, Active Directory e automação de processos. Foco em melhorar a experiência do usuário e reduzir tempo de resolução.
            </p>
          </div>
          <div class="timeline-dot"></div>
        </div>
        
        <div class="timeline-item">
          <div class="timeline-content">
            <div class="timeline-date">2023 - 2024</div>
            <div class="timeline-title">Desenvolvedor de Automações</div>
            <p style="color: #b3d9ff; margin-top: 10px;">
              Criação de ferramentas de automação com PowerShell, Node.js e Selenium. Projetos como desbloqueio de modems e scripts de limpeza avançada do Windows.
            </p>
          </div>
          <div class="timeline-dot"></div>
        </div>
        
        <div class="timeline-item">
          <div class="timeline-content">
            <div class="timeline-date">2019 - 2023</div>
            <div class="timeline-title">Graduação em Sistemas de Informação</div>
            <p style="color: #b3d9ff; margin-top: 10px;">
              Base sólida em infraestrutura, redes, desenvolvimento e gestão de TI. Projetos acadêmicos focados em soluções práticas para o mercado.
            </p>
          </div>
          <div class="timeline-dot"></div>
        </div>
      </div>
    </div>
  </div>

  <!-- Habilidades -->
  <div class="section-accordion">
    <div class="accordion-header" onclick="toggleAccordion(this)">
      <div class="accordion-title">
        <span class="accordion-icon">🛠️</span>
        <span>Arsenal Técnico</span>
      </div>
      <span class="accordion-arrow">▼</span>
    </div>
    <div class="accordion-content">
      <div class="skills-grid">
        <div>
          <h3 style="color: #00eaff; margin-bottom: 20px;">Infraestrutura & Redes</h3>
          
          <div class="skill-item">
            <div class="skill-header">
              <span class="skill-name">Windows Server</span>
              <span class="skill-level">90%</span>
            </div>
            <div class="skill-bar">
              <div class="skill-fill" style="--skill-width: 90%;"></div>
            </div>
          </div>
          
          <div class="skill-item">
            <div class="skill-header">
              <span class="skill-name">Active Directory</span>
              <span class="skill-level">85%</span>
            </div>
            <div class="skill-bar">
              <div class="skill-fill" style="--skill-width: 85%;"></div>
            </div>
          </div>
          
          <div class="skill-item">
            <div class="skill-header">
              <span class="skill-name">Redes & VPN</span>
              <span class="skill-level">80%</span>
            </div>
            <div class="skill-bar">
              <div class="skill-fill" style="--skill-width: 80%;"></div>
            </div>
          </div>
        </div>
        
        <div>
          <h3 style="color: #00eaff; margin-bottom: 20px;">Automação & Desenvolvimento</h3>
          
          <div class="skill-item">
            <div class="skill-header">
              <span class="skill-name">PowerShell</span>
              <span class="skill-level">85%</span>
            </div>
            <div class="skill-bar">
              <div class="skill-fill" style="--skill-width: 85%;"></div>
            </div>
          </div>
          
          <div class="skill-item">
            <div class="skill-header">
              <span class="skill-name">Node.js</span>
              <span class="skill-level">75%</span>
            </div>
            <div class="skill-bar">
              <div class="skill-fill" style="--skill-width: 75%;"></div>
            </div>
          </div>
          
          <div class="skill-item">
            <div class="skill-header">
              <span class="skill-name">JavaScript</span>
              <span class="skill-level">80%</span>
            </div>
            <div class="skill-bar">
              <div class="skill-fill" style="--skill-width: 80%;"></div>
            </div>
          </div>
        </div>
      </div>
      
      <h3 style="color: #00eaff; margin-top: 40px; margin-bottom: 20px;">Soft Skills</h3>
      <div style="display: flex; flex-wrap: wrap; gap: 10px;">
        <span style="background: rgba(0, 234, 255, 0.2); border: 1px solid #00eaff; color: #00eaff; padding: 8px 16px; border-radius: 20px;">🤝 Trabalho em Equipe</span>
        <span style="background: rgba(0, 234, 255, 0.2); border: 1px solid #00eaff; color: #00eaff; padding: 8px 16px; border-radius: 20px;">💬 Comunicação Clara</span>
        <span style="background: rgba(0, 234, 255, 0.2); border: 1px solid #00eaff; color: #00eaff; padding: 8px 16px; border-radius: 20px;">🎯 Foco em Resultados</span>
        <span style="background: rgba(0, 234, 255, 0.2); border: 1px solid #00eaff; color: #00eaff; padding: 8px 16px; border-radius: 20px;">🚀 Proatividade</span>
        <span style="background: rgba(0, 234, 255, 0.2); border: 1px solid #00eaff; color: #00eaff; padding: 8px 16px; border-radius: 20px;">😊 Otimismo</span>
        <span style="background: rgba(0, 234, 255, 0.2); border: 1px solid #00eaff; color: #00eaff; padding: 8px 16px; border-radius: 20px;">📚 Aprendizado Contínuo</span>
      </div>
    </div>
  </div>

  <!-- Interesses -->
  <div class="section-accordion">
    <div class="accordion-header" onclick="toggleAccordion(this)">
      <div class="accordion-title">
        <span class="accordion-icon">🎮</span>
        <span>Além do Código</span>
      </div>
      <span class="accordion-arrow">▼</span>
    </div>
    <div class="accordion-content">
      <div class="interests-grid">
        <div class="interest-card">
          <span class="interest-icon">📺</span>
          <div class="interest-title">Animes & Séries</div>
        </div>
        <div class="interest-card">
          <span class="interest-icon">🤖</span>
          <div class="interest-title">Inteligência Artificial</div>
        </div>
        <div class="interest-card">
          <span class="interest-icon">⚡</span>
          <div class="interest-title">Automação</div>
        </div>
        <div class="interest-card">
          <span class="interest-icon">💡</span>
          <div class="interest-title">Inovação Tech</div>
        </div>
        <div class="interest-card">
          <span class="interest-icon">🎧</span>
          <div class="interest-title">Podcasts Tech</div>
        </div>
        <div class="interest-card">
          <span class="interest-icon">🌐</span>
          <div class="interest-title">Web Development</div>
        </div>
      </div>
    </div>
  </div>

  <!-- Contato -->
  <div class="section-accordion" id="contato">
    <div class="accordion-header" onclick="toggleAccordion(this)">
      <div class="accordion-title">
        <span class="accordion-icon">📬</span>
        <span>Vamos Conectar?</span>
      </div>
      <span class="accordion-arrow">▼</span>
    </div>
    <div class="accordion-content">
      <p style="color: #b3d9ff; text-align: center; margin-bottom: 30px; font-size: 18px;">
        Sempre aberto para conversas sobre tecnologia, oportunidades ou apenas trocar ideias! 🚀
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
        
        <a href="mailto:seu-email@exemplo.com" class="social-card email">
          <span class="social-icon">📧</span>
          <div class="social-title">Email</div>
          <div class="social-description">Envie uma mensagem direta</div>
        </a>
      </div>
    </div>
  </div>

</div>

<!-- Script para Acordeão -->
<script>
function toggleAccordion(header) {
  const accordion = header.parentElement;
  const allAccordions = document.querySelectorAll('.section-accordion');
  
  // Fecha todos os outros acordeões
  allAccordions.forEach(acc => {
    if (acc !== accordion && acc.classList.contains('active')) {
      acc.classList.remove('active');
    }
  });
  
  // Toggle do acordeão clicado
  accordion.classList.toggle('active');
  
  // Smooth scroll para o acordeão
  if (accordion.classList.contains('active')) {
    setTimeout(() => {
      accordion.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
    }, 100);
  }
}

// Animação das skills quando a seção é aberta
document.querySelectorAll('.section-accordion').forEach(accordion => {
  accordion.addEventListener('transitionend', function(e) {
    if (e.propertyName === 'max-height' && this.classList.contains('active')) {
      const skills = this.querySelectorAll('.skill-fill');
      skills.forEach((skill, index) => {
        setTimeout(() => {
          skill.style.width = skill.style.getPropertyValue('--skill-width');
        }, index * 100);
      });
    }
  });
});

// Smooth scroll para âncoras
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
  anchor.addEventListener('click', function (e) {
    e.preventDefault();
    const target = document.querySelector(this.getAttribute('href'));
    if (target) {
      target.scrollIntoView({ behavior: 'smooth', block: 'start' });
      
      // Abre o acordeão se for um link para seção
      const accordion = target.closest('.section-accordion');
      if (accordion && !accordion.classList.contains('active')) {
        accordion.querySelector('.accordion-header').click();
      }
    }
  });
});

// Efeito de typewriter no hero
const typewriterText = document.querySelector('.typewriter');
if (typewriterText) {
  const text = typewriterText.textContent;
  typewriterText.textContent = '';
  typewriterText.style.width = '0';
  
  setTimeout(() => {
    typewriterText.style.width = '100%';
    let i = 0;
    const typing = setInterval(() => {
      if (i < text.length) {
        typewriterText.textContent += text.charAt(i);
        i++;
      } else {
        clearInterval(typing);
      }
    }, 100);
  }, 1000);
}

// Parallax suave no scroll
let ticking = false;
window.addEventListener('scroll', () => {
  if (!ticking) {
    window.requestAnimationFrame(() => {
      const scrolled = window.pageYOffset;
      const parallaxBg = document.querySelector('.particles-bg');
      if (parallaxBg) {
        parallaxBg.style.transform = `translateY(${scrolled * 0.5}px)`;
      }
      ticking = false;
    });
    ticking = true;
  }
});

// Intersection Observer para animações ao entrar na viewport
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

// Observa todos os cards e elementos animáveis
document.querySelectorAll('.interest-card, .social-card').forEach(el => {
  el.style.opacity = '0';
  el.style.transform = 'translateY(30px)';
  el.style.transition = 'all 0.6s ease';
  observer.observe(el);
});

// Easter Egg: Konami Code
let konamiCode = ['ArrowUp', 'ArrowUp', 'ArrowDown', 'ArrowDown', 'ArrowLeft', 'ArrowRight', 'ArrowLeft', 'ArrowRight', 'b', 'a'];
let konamiIndex = 0;

document.addEventListener('keydown', (e) => {
  if (e.key === konamiCode[konamiIndex]) {
    konamiIndex++;
    if (konamiIndex === konamiCode.length) {
      // Easter Egg ativado!
      document.body.style.animation = 'rainbow 2s linear infinite';
      setTimeout(() => {
        alert('🎉 Easter Egg encontrado! Você é curioso(a) hein! 🚀');
        document.body.style.animation = '';
      }, 100);
      konamiIndex = 0;
    }
  } else {
    konamiIndex = 0;
  }
});

// Animação rainbow para easter egg
const style = document.createElement('style');
style.textContent = `
  @keyframes rainbow {
    0% { filter: hue-rotate(0deg); }
    100% { filter: hue-rotate(360deg); }
  }
`;
document.head.appendChild(style);
</script>
