---
layout: single
title: "Evolução Contínua"
permalink: /interesses/evolucao/
author_profile: false
---

<style>

/* ==================== BASE ==================== */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Inter', 'Segoe UI', sans-serif;
  scroll-behavior: smooth;
}

/* Container principal */
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
  max-width: 1400px;
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
    radial-gradient(circle at 20% 30%, rgba(0, 119, 255, 0.05) 0%, transparent 50%),
    radial-gradient(circle at 80% 70%, rgba(0, 51, 153, 0.05) 0%, transparent 50%);
}

/* ==================== KEYFRAMES ==================== */
@keyframes neon-glow {
  from {
    text-shadow: 
      0 0 10px var(--accent-color),
      0 0 20px var(--accent-color),
      0 0 30px var(--accent-color),
      0 0 40px var(--primary-color);
  }
  to {
    text-shadow: 
      0 0 5px var(--accent-color),
      0 0 10px var(--accent-color),
      0 0 15px var(--accent-color),
      0 0 20px var(--primary-color),
      0 0 35px var(--primary-color),
      0 0 40px var(--primary-color);
  }
}

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

/* ==================== HERO SECTION ==================== */
.hero-evolucao {
  position: relative;
  text-align: center;
  padding: var(--spacing-xl) var(--spacing-md) var(--spacing-lg);
  z-index: 1;
  background: linear-gradient(135deg, #002244 0%, var(--bg-dark) 100%);
  border-radius: var(--border-radius);
  margin: var(--spacing-md) 0;
  box-shadow: var(--shadow-medium);
}

.hero-evolucao h1 {
  font-size: clamp(32px, 5vw, 56px);
  font-weight: 900;
  margin-bottom: var(--spacing-md);
  color: var(--text-primary);
  text-transform: uppercase;
  letter-spacing: 2px;
  text-shadow: 
    0 0 10px var(--accent-color),
    0 0 20px var(--accent-color),
    0 0 30px var(--accent-color),
    0 0 40px var(--primary-color);
  animation: neon-glow 2s ease-in-out infinite alternate;
}

.hero-evolucao p {
  font-size: clamp(16px, 2vw, 20px);
  color: var(--text-secondary);
  max-width: 700px;
  margin: 0 auto var(--spacing-lg);
  line-height: 1.6;
}

/* ==================== SEÇÕES DE CONTEÚDO ==================== */
.content-section {
  position: relative;
  z-index: 1;
  margin: var(--spacing-lg) 0;
  background: var(--bg-medium);
  border-radius: var(--border-radius);
  padding: var(--spacing-lg) var(--spacing-md);
  box-shadow: var(--shadow-light);
  backdrop-filter: blur(3px);
}

.section-title {
  font-size: clamp(28px, 4vw, 42px);
  color: var(--text-primary);
  text-align: center;
  margin-bottom: var(--spacing-md);
  text-shadow: 
    0 0 5px var(--accent-color),
    0 0 10px var(--accent-color),
    0 0 15px var(--accent-color),
    0 0 20px var(--secondary-color);
}

.section-subtitle {
  font-size: clamp(16px, 2vw, 18px);
  color: var(--text-secondary);
  text-align: center;
  margin-bottom: var(--spacing-xl);
  line-height: 1.8;
  max-width: 700px;
  margin-left: auto;
  margin-right: auto;
}

/* ==================== CARDS EXPANSÍVEIS ==================== */
.evolution-cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: var(--spacing-md);
  margin-bottom: var(--spacing-xl);
  animation: fadeInUp 0.6s ease backwards;
}

.evolution-card {
  background: linear-gradient(145deg, var(--bg-light), rgba(0, 119, 255, 0.1));
  border: 2px solid var(--border-color);
  border-radius: var(--border-radius);
  padding: var(--spacing-lg);
  transition: all var(--transition-medium);
  cursor: pointer;
  position: relative;
  overflow: hidden;
  animation: fadeInUp 0.6s ease backwards;
}

.evolution-card:nth-child(1) { animation-delay: 0.1s; }
.evolution-card:nth-child(2) { animation-delay: 0.2s; }
.evolution-card:nth-child(3) { animation-delay: 0.3s; }
.evolution-card:nth-child(4) { animation-delay: 0.4s; }
.evolution-card:nth-child(5) { animation-delay: 0.5s; }
.evolution-card:nth-child(6) { animation-delay: 0.6s; }

.evolution-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(77, 171, 247, 0.1), transparent);
  transition: left 0.6s ease;
  z-index: 1;
}

.evolution-card:hover::before {
  left: 100%;
}

.evolution-card:hover {
  transform: translateY(-10px);
  border-color: var(--text-accent);
  box-shadow: var(--shadow-heavy);
}

/* ==================== CARD HEADER ==================== */
.card-header {
  display: flex;
  align-items: center;
  gap: var(--spacing-sm);
  margin-bottom: var(--spacing-sm);
  position: relative;
  z-index: 2;
}

.card-icon {
  width: 40px;
  height: 40px;
  min-width: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: linear-gradient(135deg, var(--text-accent), var(--secondary-color));
  border-radius: 10px;
  color: var(--text-primary);
  font-weight: bold;
  font-size: 20px;
  box-shadow: 0 0 15px rgba(77, 171, 247, 0.4);
}

.card-title {
  font-size: clamp(18px, 2.5vw, 22px);
  font-weight: 700;
  color: var(--text-accent);
  flex: 1;
  margin: 0;
}

.card-arrow {
  font-size: 20px;
  color: var(--secondary-color);
  transition: transform var(--transition-fast);
  flex-shrink: 0;
}

.evolution-card.expanded .card-arrow {
  transform: rotate(180deg);
}

/* ==================== CARD CONTENT ==================== */
.card-content {
  max-height: 0;
  overflow: hidden;
  transition: max-height var(--transition-medium);
  color: var(--text-secondary);
  line-height: 1.8;
  position: relative;
  z-index: 2;
}

.evolution-card.expanded .card-content {
  max-height: 1500px;
  margin-top: var(--spacing-md);
  padding-top: var(--spacing-md);
  border-top: 1px solid var(--border-color);
}

.card-content p {
  margin-bottom: var(--spacing-sm);
  font-size: 15px;
}

.card-list {
  list-style: none;
  margin: var(--spacing-sm) 0;
  padding: 0;
}

.card-list li {
  padding: var(--spacing-xs) 0;
  padding-left: 25px;
  position: relative;
  font-size: 15px;
  margin: 0;
}

.card-list li::before {
  content: '▸';
  position: absolute;
  left: 0;
  color: var(--text-accent);
  font-weight: bold;
  font-size: 18px;
}

.card-quote {
  margin-top: var(--spacing-sm);
  padding: var(--spacing-sm);
  background: rgba(77, 171, 247, 0.25);
  border-left: 3px solid var(--accent-color);
  border-radius: 8px;
  font-style: italic;
  color: #b3d9ff;
  font-size: 14px;
  line-height: 1.6;
  box-shadow: 0 4px 12px rgba(0, 119, 255, 0.2);
}

/* ==================== COMMITMENT BOX ==================== */
.commitment-box {
  background: linear-gradient(135deg, rgba(77, 171, 247, 0.1), var(--bg-light));
  border: 2px solid rgba(77, 171, 247, 0.4);
  border-radius: var(--border-radius);
  padding: var(--spacing-lg);
  text-align: center;
  margin: var(--spacing-xl) 0;
}

.commitment-values {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: var(--spacing-sm);
  margin-bottom: var(--spacing-lg);
}

.value-item {
  padding: var(--spacing-sm);
  background: rgba(77, 171, 247, 0.08);
  border: 1px solid var(--border-color);
  border-radius: 12px;
  color: var(--text-accent);
  font-weight: 600;
  font-size: 15px;
  transition: all var(--transition-fast);
  cursor: default;
}

.value-item:hover {
  background: rgba(77, 171, 247, 0.15);
  transform: translateY(-5px);
  box-shadow: 0 10px 25px rgba(77, 171, 247, 0.2);
}

/* ==================== FINAL MESSAGE ==================== */
.final-message {
  text-align: center;
  padding: var(--spacing-lg);
  margin-top: var(--spacing-xl);
  background: rgba(0, 20, 60, 0.95);
  border: 2px solid rgba(77, 171, 247, 0.5);
  border-radius: var(--border-radius);
}

.final-message h2 {
  font-size: clamp(24px, 3.5vw, 32px);
  color: var(--text-accent);
  margin-bottom: var(--spacing-md);
  margin-top: 0;
}

.final-message p {
  font-size: clamp(15px, 2vw, 17px);
  color: var(--text-secondary);
  line-height: 1.8;
  margin-bottom: var(--spacing-md);
}

.final-quote {
  font-size: clamp(16px, 2.5vw, 18px);
  color: var(--text-accent);
  font-weight: 700;
  font-style: italic;
  margin-top: var(--spacing-lg);
}

/* ==================== BOTÕES DE NAVEGAÇÃO ==================== */
.nav-buttons {
  display: flex;
  justify-content: center;
  gap: var(--spacing-md);
  margin: var(--spacing-xl) 0;
  flex-wrap: wrap;
  padding: 0 var(--spacing-md);
}

.nav-button {
  display: inline-flex;
  align-items: center;
  gap: var(--spacing-xs);
  padding: 12px 30px;
  background: rgba(0, 51, 153, 0.1);
  border: 2px solid var(--secondary-color);
  color: var(--secondary-color);
  text-decoration: none;
  border-radius: 50px;
  font-weight: 600;
  font-size: 15px;
  transition: all var(--transition-fast);
  box-shadow: 0 4px 12px rgba(0, 51, 153, 0.15);
  cursor: pointer;
}

.nav-button:hover,
.nav-button:focus {
  background: rgba(116, 192, 252, 0.2);
  transform: translateY(-3px);
  box-shadow: 0 8px 20px rgba(116, 192, 252, 0.3);
  outline: none;
}

.nav-button.secondary {
  border-color: var(--text-accent);
  color: var(--text-accent);
  box-shadow: 0 4px 12px rgba(77, 171, 247, 0.15);
}

.nav-button.secondary:hover,
.nav-button.secondary:focus {
  background: rgba(77, 171, 247, 0.2);
}

.nav-icon {
  width: 20px;
  height: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
}

/* ==================== RESPONSIVO ==================== */
@media (max-width: 768px) {
  .hero-evolucao h1 {
    font-size: 38px;
  }
  
  .section-title {
    font-size: 32px;
  }
  
  .evolution-cards {
    grid-template-columns: 1fr;
  }
  
  .initial-content {
    padding: var(--spacing-md) var(--spacing-sm);
  }
}

@media (max-width: 480px) {
  .card-icon {
    width: 32px;
    height: 32px;
    min-width: 32px;
    font-size: 16px;
  }
  
  .card-title {
    font-size: 18px;
  }
  
  .hero-evolucao {
    padding: var(--spacing-lg) var(--spacing-sm);
  }
}

/* ==================== ACESSIBILIDADE ==================== */
@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
}

@media (prefers-contrast: more) {
  :root {
    --text-secondary: #e6f3ff;
    --border-color: rgba(77, 171, 247, 0.6);
  }
}

/* Focus visível para acessibilidade */
*:focus-visible {
  outline: 2px solid var(--accent-color);
  outline-offset: 2px;
}
</style>

<!-- Partículas de Fundo -->
<div class="particles-bg"></div>

<!-- Hero Section -->
<section class="hero-evolucao">
  <h1>Evolução Contínua</h1>
  <p>Crescimento não é um destino, é uma forma de viver. Aprender sempre, melhorar sempre, nunca estacionar.</p>
</section>

<!-- Seção: Filosofia -->
<section id="sobre" class="content-section">
  <h2 class="section-title">A Filosofia da Evolução</h2>
  <div class="section-subtitle">
    Acredito profundamente que ninguém se torna excelente apenas com talento — excelência é construída com disciplina, consistência e intenção. Este espaço documenta as ideias que moldam meu crescimento profissional e pessoal.
  </div>
</section>

<!-- Seção: Pilares do Crescimento -->
<section id="pilares" class="content-section">
  <h2 class="section-title">Pilares do Crescimento</h2>
  
  <div class="evolution-cards">
    
    <!-- Card 1: Mentalidade de Crescimento -->
    <div class="evolution-card" onclick="toggleCard(this)">
      <div class="card-header">
        <div class="card-icon" aria-hidden="true">*</div>
        <h3 class="card-title">Mentalidade de Crescimento</h3>
        <span class="card-arrow" aria-hidden="true">▼</span>
      </div>
      <div class="card-content">
        <p>Ver desafios como oportunidades, fracassos como informações valiosas e limitações como temporárias.</p>
        <ul class="card-list">
          <li>Estudo constante de novas tecnologias</li>
          <li>Testes práticos e pequenos experimentos semanais</li>
          <li>Revisão periódica de habilidades fortes e fracas</li>
          <li>Paixão por aprender e compartilhar conhecimento</li>
        </ul>
        <div class="card-quote">"Melhorar 1% todos os dias sempre vence tentar ser perfeito."</div>
      </div>
    </div>

    <!-- Card 2: Hábitos Fortes -->
    <div class="evolution-card" onclick="toggleCard(this)">
      <div class="card-header">
        <div class="card-icon" aria-hidden="true">*</div>
        <h3 class="card-title">Hábitos Fortes</h3>
        <span class="card-arrow" aria-hidden="true">▼</span>
      </div>
      <div class="card-content">
        <p>Adotar pequenos comportamentos que acumulam grandes resultados ao longo do tempo.</p>
        <ul class="card-list">
          <li>Ler diariamente (mesmo que 10 minutos)</li>
          <li>Documentar tudo o que aprendo</li>
          <li>Criar pequenos projetos para validar ideias</li>
          <li>Blindar foco: evitar multitarefa</li>
          <li>Priorizar descanso, clareza mental e saúde</li>
        </ul>
        <div class="card-quote">Esses hábitos impactam direto: mais precisão, mais calma, menos retrabalho.</div>
      </div>
    </div>

    <!-- Card 3: Ferramentas e Rotinas -->
    <div class="evolution-card" onclick="toggleCard(this)">
      <div class="card-header">
        <div class="card-icon" aria-hidden="true">*</div>
        <h3 class="card-title">Ferramentas & Rotinas</h3>
        <span class="card-arrow" aria-hidden="true">▼</span>
      </div>
      <div class="card-content">
        <p>Formas simples e consistentes de acompanhar progresso e evoluir continuamente.</p>
        <ul class="card-list">
          <li><strong>Notion</strong> — organização e mapas de aprendizado</li>
          <li><strong>GitHub</strong> — evolução técnica visível em projetos</li>
          <li><strong>Método Kaizen</strong> — melhorar 1 detalhe por vez</li>
          <li><strong>Análise pós-projeto</strong> — entender o que funcionou</li>
        </ul>
        <div class="card-quote">Não acredito em mudanças gigantes. Acredito na constância bem feita.</div>
      </div>
    </div>

    <!-- Card 4: Desenvolvimento Técnico -->
    <div class="evolution-card" onclick="toggleCard(this)">
      <div class="card-header">
        <div class="card-icon" aria-hidden="true">*</div>
        <h3 class="card-title">Técnico Contínuo</h3>
        <span class="card-arrow" aria-hidden="true">▼</span>
      </div>
      <div class="card-content">
        <p>Para mim, aprender tecnologia é um processo interminável — e isso é o melhor da área.</p>
        <ul class="card-list">
          <li>Automação de processos</li>
          <li>Infraestrutura e redes</li>
          <li>Melhores práticas de documentação</li>
          <li>Arquitetura simples e eficiente</li>
          <li>Sistemas mais seguros e resilientes</li>
        </ul>
        <div class="card-quote">Cada avanço técnico faz parte de uma jornada maior, nunca um ponto final.</div>
      </div>
    </div>

    <!-- Card 5: Evolução Pessoal -->
    <div class="evolution-card" onclick="toggleCard(this)">
      <div class="card-header">
        <div class="card-icon" aria-hidden="true">*</div>
        <h3 class="card-title">Evolução Pessoal</h3>
        <span class="card-arrow" aria-hidden="true">▼</span>
      </div>
      <div class="card-content">
        <p>Profissão e vida caminham juntas. Ambas exigem crescimento contínuo.</p>
        <ul class="card-list">
          <li>Aprender a ouvir mais e falar menos</li>
          <li>Transformar frustração em combustível</li>
          <li>Aprender com pessoas mais experientes</li>
          <li>Manter humildade intelectual sempre</li>
          <li>Persistir mesmo quando falta motivação</li>
        </ul>
        <div class="card-quote">Ser a cada dia uma versão mais completa e preparada de mim.</div>
      </div>
    </div>

    <!-- Card 6: Meu Compromisso -->
    <div class="evolution-card" onclick="toggleCard(this)">
      <div class="card-header">
        <div class="card-icon" aria-hidden="true">*</div>
        <h3 class="card-title">Meu Compromisso</h3>
        <span class="card-arrow" aria-hidden="true">▼</span>
      </div>
      <div class="card-content">
        <p>Continuar crescendo, estudando e aprimorando meu trabalho com princípios sólidos.</p>
        <div class="commitment-values">
          <div class="value-item">Simplicidade</div>
          <div class="value-item">Ética</div>
          <div class="value-item">Clareza</div>
          <div class="value-item">Disciplina</div>
          <div class="value-item">Constância</div>
        </div>
        <div class="card-quote">"Pequenas melhorias diárias constroem mudanças extraordinárias."</div>
      </div>
    </div>

  </div>
</section>

<!-- Seção: Mensagem Final -->
<section class="final-message">
  <h2>Evolução Contínua é uma Forma de Viver</h2>
  <p>Não é um objetivo — é um caminho.</p>
  <p>É assim que cresço como profissional, como pessoa e como alguém que acredita que <strong>tecnologia deve servir para facilitar, transformar e inspirar</strong>.</p>
  <p class="final-quote">"O melhor dia para começar é hoje. O segundo melhor é agora."</p>
</section>

<!-- Botões de Navegação -->
<div class="nav-buttons">
  <a href="/" class="nav-button">
    <span>←</span>
    <span>Início</span>
  </a>
  
  <a href="/sobre/" class="nav-button secondary">
    <span>◉</span>
    <span>Voltar ao Perfil</span>
  </a>
</div>

<!-- JavaScript -->
<script>
/**
 * INICIALIZAÇÃO DA PÁGINA
 */
document.addEventListener('DOMContentLoaded', function() {
  initializeCards();
  initializeScrollAnimations();
});

/**
 * Toggle Cards: Abre/fecha cards ao clicar
 */
function toggleCard(card) {
  if (!card) return;
  
  const allCards = document.querySelectorAll('.evolution-card');
  
  // Fecha outros cards abertos
  allCards.forEach(c => {
    if (c !== card && c.classList.contains('expanded')) {
      c.classList.remove('expanded');
    }
  });
  
  // Alterna estado do card clicado
  card.classList.toggle('expanded');
  
  // Scroll suave se expandido
  if (card.classList.contains('expanded')) {
    setTimeout(() => {
      card.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
    }, 100);
  }
}

/**
 * Inicializar cards
 */
function initializeCards() {
  const cards = document.querySelectorAll('.evolution-card');
  cards.forEach(card => {
    card.addEventListener('keydown', function(e) {
      if (e.key === 'Enter' || e.key === ' ') {
        e.preventDefault();
        toggleCard(this);
      }
    });
  });
}

/**
 * Scroll Animations: Anima cards ao entrar na viewport
 */
function initializeScrollAnimations() {
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
  
  document.querySelectorAll('.evolution-card').forEach(el => {
    el.style.opacity = '0';
    el.style.transform = 'translateY(30px)';
    el.style.transition = 'all 0.6s ease';
    observer.observe(el);
  });
}

// Tornar a função toggleCard global para onclick
window.toggleCard = toggleCard;
</script>
