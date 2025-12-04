---
layout: single
title: "Crescimento Corporativo"
permalink: /interesses/evolucao/
author_profile: false
---

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Inter', 'Segoe UI', sans-serif;
  overflow-x: hidden;
  scroll-behavior: smooth;
}

:target {
  scroll-margin-top: 100px;
}

.page__content {
  max-width: 1400px;
  margin: 0 auto;
  padding: 0 20px;
}

/* Background Premium */
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

/* Hero Section */
.hero-evolucao {
  position: relative;
  text-align: center;
  padding: 80px 20px 60px;
  z-index: 1;
  background: linear-gradient(135deg, #0a2840 0%, #001e3c 100%);
  border-radius: 20px;
  margin: 20px 0;
  box-shadow: 0 10px 30px rgba(0,0,0,0.3);
}

.hero-evolucao h1 {
  font-size: 56px;
  font-weight: 900;
  margin-bottom: 20px;
  background: linear-gradient(90deg, #00eaff, #00bfff, #00eaff);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: growthGlow 3s ease-in-out infinite;
}

@keyframes growthGlow {
  0%, 100% {
    text-shadow: 0 0 10px rgba(0, 234, 255, 0.6), 0 0 20px rgba(0, 191, 255, 0.4);
  }
  50% {
    text-shadow: 0 0 20px rgba(0, 234, 255, 0.9), 0 0 40px rgba(0, 191, 255, 0.6);
  }
}

.hero-evolucao p {
  font-size: 20px;
  color: #b3d9ff;
  max-width: 700px;
  margin: 0 auto 40px;
  line-height: 1.6;
}

/* Quick Nav */
.quick-nav {
  position: sticky;
  top: 0;
  z-index: 100;
  background: rgba(0, 8, 20, 0.95);
  backdrop-filter: blur(10px);
  padding: 15px 0;
  margin: 20px 0 30px 0;
  border-radius: 50px;
  box-shadow: 0 4px 15px rgba(0,0,0,0.3);
  border: 2px solid rgba(0, 102, 255, 0.3);
}

.quick-nav-container {
  max-width: 100%;
  margin: 0 auto;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 15px;
  padding: 0 30px;
}

.quick-nav-item {
  padding: 10px 25px;
  background: rgba(0, 102, 255, 0.15);
  border: 2px solid rgba(0, 102, 255, 0.3);
  border-radius: 30px;
  color: #b3d9ff;
  text-decoration: none;
  font-weight: 600;
  font-size: 15px;
  transition: all 0.3s ease;
  text-align: center;
  position: relative;
  overflow: hidden;
}

.quick-nav-item::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(0, 234, 255, 0.3), transparent);
  transition: left 0.6s ease;
}

.quick-nav-item:hover::before {
  left: 100%;
}

.quick-nav-item:hover, .quick-nav-item.active {
  background: rgba(0, 234, 255, 0.25);
  border-color: #00eaff;
  color: #00eaff;
  transform: translateY(-2px);
  box-shadow: 0 5px 15px rgba(0, 234, 255, 0.3);
}

/* Content Sections */
.content-section {
  position: relative;
  z-index: 1;
  margin: 40px 0;
  background: rgba(10,20,40,0.85);
  border-radius: 20px;
  padding: 40px 30px;
  box-shadow: 0 8px 25px rgba(0,0,0,0.6);
  backdrop-filter: blur(3px);
}

/* Cards */
.evolution-cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 30px;
  margin-bottom: 60px;
}

.evolution-card {
  background: linear-gradient(145deg, rgba(0, 191, 255, 0.08), rgba(0, 234, 255, 0.08));
  border: 2px solid rgba(0, 234, 255, 0.3);
  border-radius: 20px;
  padding: 30px;
  transition: all 0.4s ease;
  cursor: pointer;
  position: relative;
  overflow: hidden;
}

.evolution-card:hover {
  transform: translateY(-10px);
  border-color: #00eaff;
  box-shadow: 0 20px 50px rgba(0, 234, 255, 0.3);
}

.card-header {
  display: flex;
  align-items: center;
  gap: 15px;
  margin-bottom: 20px;
}

.card-icon { font-size: 40px; }
.card-title { font-size: 24px; font-weight: 700; color: #00eaff; }
.card-arrow { margin-left: auto; font-size: 20px; color: #00bfff; transition: transform 0.3s ease; }

.evolution-card.expanded .card-arrow { transform: rotate(180deg); }

.card-content {
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.5s ease;
  color: #b3d9ff;
  line-height: 1.8;
}

.evolution-card.expanded .card-content {
  max-height: 1000px;
  margin-top: 20px;
  padding-top: 20px;
  border-top: 1px solid rgba(0, 234, 255, 0.2);
}

.card-list { list-style: none; margin: 15px 0; }
.card-list li {
  padding: 8px 0;
  padding-left: 25px;
  position: relative;
}
.card-list li::before { content: '▸'; position: absolute; left: 0; color: #00eaff; font-weight: bold; }

.card-quote {
  margin-top: 15px;
  padding: 15px;
  background: rgba(0, 234, 255, 0.1);
  border-left: 3px solid #00eaff;
  border-radius: 8px;
  font-style: italic;
  color: #00eaff;
  animation: fadeInQuote 1s ease forwards;
}

@keyframes fadeInQuote {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Section Title */
.section-title {
  font-size: 42px;
  color: #00eaff;
  text-align: center;
  margin-bottom: 50px;
  text-shadow: 0 0 20px rgba(0, 234, 255, 0.5);
}

.section-subtitle {
  font-size: 18px;
  color: #b3d9ff;
  text-align: center;
  margin-bottom: 50px;
  line-height: 1.8;
  max-width: 700px;
  margin-left: auto;
  margin-right: auto;
}

/* Final Message */
.final-message {
  text-align: center;
  padding: 40px;
  margin-top: 60px;
  background: linear-gradient(145deg, rgba(0, 102, 255, 0.08), rgba(0, 234, 255, 0.08));
  border: 2px solid rgba(0, 234, 255, 0.3);
  border-radius: 20px;
}

.final-message h2 { font-size: 32px; color: #00eaff; margin-bottom: 20px; }
.final-message p { font-size: 18px; color: #b3d9ff; line-height: 1.8; margin-bottom: 20px; }
.final-quote { font-size: 20px; color: #00eaff; font-weight: 700; font-style: italic; margin-top: 30px; }

/* Nav Buttons */
.nav-buttons {
  display: flex;
  justify-content: center;
  gap: 20px;
  margin: 60px 0;
  flex-wrap: wrap;
  padding: 0 20px;
}

.nav-button {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  padding: 12px 30px;
  background: rgba(0, 102, 255, 0.1);
  border: 2px solid #00eaff;
  color: #00eaff;
  text-decoration: none;
  border-radius: 50px;
  font-weight: 600;
  transition: all 0.3s ease;
  box-shadow: 0 4px 12px rgba(0, 102, 255, 0.15);
}

.nav-button:hover { background: rgba(0, 234, 255, 0.2); transform: translateY(-3px); box-shadow: 0 8px 20px rgba(0, 234, 255, 0.3); }

.nav-button.secondary { border-color: #00eaff; color: #00eaff; }
.nav-button.secondary:hover { background: rgba(0, 191, 255, 0.2); }

@media (max-width: 768px) {
  .hero-evolucao h1 { font-size: 38px; }
  .section-title { font-size: 32px; }
  .evolution-cards { grid-template-columns: 1fr; }
  .quick-nav-item { font-size: 13px; padding: 6px 15px; }
}

/* Animations */
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(30px); }
  to { opacity: 1; transform: translateY(0); }
}

.evolution-card { animation: fadeInUp 0.6s ease backwards; }
.evolution-card:nth-child(1) { animation-delay: 0.1s; }
.evolution-card:nth-child(2) { animation-delay: 0.2s; }
.evolution-card:nth-child(3) { animation-delay: 0.3s; }
.evolution-card:nth-child(4) { animation-delay: 0.4s; }
.evolution-card:nth-child(5) { animation-delay: 0.5s; }
.evolution-card:nth-child(6) { animation-delay: 0.6s; }
</style>

<!-- Partículas de Fundo -->
<div class="particles-bg"></div>

<!-- Hero -->
<section class="hero-evolucao">
  <h1>🚀 Crescimento Corporativo</h1>
  <p>Excelência, inovação e resultados — um compromisso diário com evolução e performance.</p>
</section>

<!-- Quick Nav -->
<nav class="quick-nav">
  <div class="quick-nav-container">
    <a href="#sobre" class="quick-nav-item">📖 Filosofia</a>
    <a href="#cards" class="quick-nav-item">🚀 Áreas</a>
  </div>
</nav>

<!-- Filosofia -->
<section id="sobre" class="content-section">
  <h2 class="section-title">📖 Filosofia Corporativa</h2>
  <div class="section-subtitle">
    A excelência corporativa é construída diariamente, combinando inovação, disciplina e estratégia bem aplicada.
  </div>
</section>

<!-- Cards Corporativos -->
<section id="cards" class="content-section">
  <h2 class="section-title">🚀 Pilares do Crescimento Corporativo</h2>
  
  <div class="evolution-cards">
    <!-- Card 1 -->
    <div class="evolution-card">
      <div class="card-header" onclick="toggleCard(this.parentElement)">
        <span class="card-icon">💡</span>
        <span class="card-title">Inovação Contínua</span>
        <span class="card-arrow">▼</span>
      </div>
      <div class="card-content">
        <ul class="card-list">
          <li>Processos ágeis e eficientes</li>
          <li>Incentivo à criatividade da equipe</li>
          <li>Feedback constante e construtivo</li>
        </ul>
        <div class="card-quote">"A inovação distingue um líder de um seguidor." – Steve Jobs</div>
      </div>
    </div>

    <!-- Card 2 -->
    <div class="evolution-card">
      <div class="card-header" onclick="toggleCard(this.parentElement)">
        <span class="card-icon">📊</span>
        <span class="card-title">Crescimento Corporativo</span>
        <span class="card-arrow">▼</span>
      </div>
      <div class="card-content">
        <ul class="card-list">
          <li>Metas claras e mensuráveis</li>
          <li>Expansão estratégica de mercado</li>
          <li>Investimento contínuo em talentos</li>
        </ul>
        <div class="card-quote">"O crescimento é o resultado de uma estratégia bem executada." – Indra Nooyi</div>
      </div>
    </div>

    <!-- Card 3 -->
    <div class="evolution-card">
      <div class="card-header" onclick="toggleCard(this.parentElement)">
        <span class="card-icon">🤝</span>
        <span class="card-title">Liderança Eficaz</span>
        <span class="card-arrow">▼</span>
      </div>
      <div class="card-content">
        <ul class="card-list">
          <li>Tomada de decisão transparente</li>
          <li>Inspirar confiança e motivação</li>
          <li>Desenvolvimento de líderes internos</li>
        </ul>
        <div class="card-quote">"A liderança é ação, não posição." – Donald McGannon</div>
      </div>
    </div>

    <!-- Card 4 -->
    <div class="evolution-card">
      <div class="card-header" onclick="toggleCard(this.parentElement)">
        <span class="card-icon">⚙️</span>
        <span class="card-title">Eficiência Operacional</span>
        <span class="card-arrow">▼</span>
      </div>
      <div class="card-content">
        <ul class="card-list">
          <li>Automatização de processos-chave</li>
          <li>Redução de desperdícios</li>
          <li>Monitoramento constante de performance</li>
        </ul>
        <div class="card-quote">"Eficiência é fazer as coisas corretamente; eficácia é fazer as coisas certas." – Peter Drucker</div>
      </div>
    </div>

    <!-- Card 5 -->
    <div class="evolution-card">
      <div class="card-header" onclick="toggleCard(this.parentElement)">
        <span class="card-icon">🌱</span>
        <span class="card-title">Sustentabilidade</span>
        <span class="card-arrow">▼</span>
      </div>
      <div class="card-content">
        <ul class="card-list">
          <li>Redução da pegada ambiental</li>
          <li>Programas sociais corporativos</li>
          <li>Processos éticos e responsáveis</li>
        </ul>
        <div class="card-quote">"Sustentabilidade não é apenas um objetivo, é uma responsabilidade." – Paul Polman</div>
      </div>
    </div>

    <!-- Card 6 -->
    <div class="evolution-card">
      <div class="card-header" onclick="toggleCard(this.parentElement)">
        <span class="card-icon">📈</span>
        <span class="card-title">Transformação Digital</span>
        <span class="card-arrow">▼</span>
      </div>
      <div class="card-content">
        <ul class="card-list">
          <li>Adaptação tecnológica contínua</li>
          <li>Uso de dados para decisões estratégicas</li>
          <li>Inovação em produtos e serviços</li>
        </ul>
        <div class="card-quote">"A tecnologia sozinha não basta. É preciso estratégia e pessoas." – Satya Nadella</div>
      </div>
    </div>

  </div>
</section>

<!-- Mensagem Final -->
<section class="final-message">
  <h2>🌟 Estamos Sempre Evoluindo</h2>
  <p>Nosso compromisso com a excelência não termina. Cada desafio é uma oportunidade de crescimento e aprendizado contínuo.</p>
  <p class="final-quote">"O sucesso corporativo é a soma de pequenas melhorias diárias." – Autor Desconhecido</p>
</section>

<!-- Navegação Final -->
<div class="nav-buttons">
  <a href="/interesses/" class="nav-button">⬅️ Voltar</a>
  <a href="/contato/" class="nav-button secondary">📩 Contato</a>
</div>

<script>
// Toggle Cards
function toggleCard(card) {
  card.classList.toggle('expanded');
}
</script>
