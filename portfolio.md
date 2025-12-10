---
title: "Meus Projetos"
layout: single
permalink: /portfolio/
author_profile: false
sidebar: null
---

<style>
/* ==================== VARIÁVEIS CSS ==================== */
:root {
  --primary-color: #4da6ff;
  --secondary-color: #0088cc;
  --dark-bg: #142850;
  --darker-bg: #0a1428;
  --light-text: #ffffff;
  --gray-text: #cccccc;
  --card-bg-start: rgba(20, 40, 80, 0.8);
  --card-bg-end: rgba(10, 20, 40, 0.9);
  --success-gradient: linear-gradient(135deg, #00cc66, #00aa55);
  --warning-gradient: linear-gradient(135deg, #ffcc00, #ff9900);
}

/* ==================== CONFIGURAÇÕES GERAIS ==================== */
.initial-content {
  position: relative;
  background: rgba(10,20,40,0.85);
  padding: 30px 25px;
  border-radius: 20px;
  box-shadow: 0 8px 25px rgba(0,0,0,0.6);
  backdrop-filter: blur(3px);
  z-index: 1;
}

/* Ocultar barra lateral */
.sidebar, .sidebar__wrapper {
  display: none !important;
}

/* Forçar conteúdo principal a ocupar largura total */
.page--portfolio main.grid__item {
  grid-column: 1 / -1;
  margin-left: auto;
  margin-right: auto;
  max-width: 1100px;
  padding-left: 20px;
  padding-right: 20px;
}

/* Configuração de fundo para página de portfólio */
body.page--portfolio {
  background-color: var(--dark-bg) !important;
}

body.page--portfolio main.grid__item {
  background-color: var(--dark-bg) !important;
}

/* ==================== TÍTULO COM EFEITO NEON ==================== */
.page-title {
  text-align: center;
  margin: 40px 0;
  position: relative;
}

.page-title h1 {
  font-size: 56px;
  font-weight: 900;
  color: var(--light-text);
  text-transform: uppercase;
  letter-spacing: 2px;
  text-shadow: 
    0 0 10px var(--primary-color),
    0 0 20px var(--primary-color),
    0 0 30px var(--primary-color),
    0 0 40px var(--secondary-color);
  animation: neon-glow 2s ease-in-out infinite alternate;
}

@keyframes neon-glow {
  from {
    text-shadow: 
      0 0 10px var(--primary-color),
      0 0 20px var(--primary-color),
      0 0 30px var(--primary-color),
      0 0 40px var(--secondary-color);
  }
  to {
    text-shadow: 
      0 0 5px var(--primary-color),
      0 0 10px var(--primary-color),
      0 0 15px var(--primary-color),
      0 0 20px var(--secondary-color),
      0 0 35px var(--secondary-color),
      0 0 40px var(--secondary-color);
  }
}

/* Manter regra duplicada conforme solicitado */
.page__title {
  text-align: center;
  font-size: 48px !important;
  color: var(--light-text) !important;
  margin-bottom: 20px !important;
  text-shadow: 2px 2px 10px rgba(77, 166, 255, 0.5);
  background: linear-gradient(90deg, var(--primary-color), #00ccff);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

/* ==================== CONTEÚDO INTRODUTÓRIO ==================== */
.intro-text {
  text-align: center;
  font-size: 20px;
  color: var(--gray-text);
  margin-bottom: 50px;
  max-width: 800px;
  margin-left: auto;
  margin-right: auto;
}

/* ==================== GRID DE PROJETOS ==================== */
.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 30px;
  margin: 40px 0;
  width: 100%;
  box-sizing: border-box;
}

/* ==================== CARDS DE PROJETOS ==================== */
.project-card {
  width: 100%;
  box-sizing: border-box;
  background: linear-gradient(145deg, var(--card-bg-start), var(--card-bg-end));
  border: 2px solid transparent;
  border-radius: 15px;
  padding: 30px;
  transition: all 0.4s ease;
  position: relative;
  overflow: hidden;
  box-shadow: 0 8px 30px rgba(0, 0, 0, 0.5);
}

.project-card::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  border-radius: 15px;
  padding: 2px;
  background: linear-gradient(135deg, var(--primary-color), #00ccff, var(--primary-color));
  -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
  -webkit-mask-composite: xor;
  mask-composite: exclude;
  opacity: 0;
  transition: opacity 0.4s ease;
  pointer-events: none; 
}

.project-card:hover::before {
  opacity: 1;
}

.project-card:hover {
  transform: translateY(-10px) scale(1.02);
  box-shadow: 0 15px 50px rgba(77, 166, 255, 0.4);
}

/* ==================== ÍCONES E TÍTULOS DE PROJETOS ==================== */
.project-icon {
  width: 80px;
  height: 80px;
  margin: 0 auto 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
  border-radius: 20px;
  font-size: 40px;
  box-shadow: 0 5px 20px rgba(77, 166, 255, 0.3);
}

.project-title {
  font-size: 28px !important;
  color: var(--light-text) !important;
  margin: 20px 0 15px 0 !important;
  text-align: center;
  font-weight: 700;
}

.project-description {
  color: var(--gray-text);
  font-size: 16px; /* Espaço corrigido */
  line-height: 1.6;
  margin-bottom: 20px;
  text-align: center;
}

/* ==================== TAGS DE TECNOLOGIA ==================== */
.tech-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  justify-content: center;
  margin: 20px 0;
}

.tech-tag {
  background: rgba(77, 166, 255, 0.2);
  border: 1px solid var(--primary-color);
  color: var(--primary-color);
  padding: 6px 12px;
  border-radius: 20px;
  font-size: 13px; /* Espaço corrigido */
  font-weight: 600;
  transition: all 0.3s ease;
}

.tech-tag:hover {
  background: rgba(77, 166, 255, 0.3);
  transform: scale(1.05);
}

/* ==================== BOTÕES E INTERAÇÕES ==================== */
.project-buttons {
  display: flex;
  flex-direction: column;
  gap: 10px;
  align-items: center;
  margin-top: 25px;
}

.btn-custom {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
  padding: 12px 24px;
  border-radius: 8px;
  font-size: 15px;
  font-weight: 600;
  text-decoration: none;
  transition: all 0.3s ease;
  border: 2px solid;
  width: 100%;
  max-width: 240px;
  text-align: center;
}

.btn-github {
  background: linear-gradient(135deg, #333333, #1a1a1a);
  color: var(--light-text);
  border-color: #333333;
}

.btn-demo {
  background: transparent;
  color: var(--primary-color);
  border-color: var(--primary-color);
}

/* Consolidar efeitos hover para otimização */
.btn-github:hover,
.btn-demo:hover,
.project-card:hover {
  transform: translateY(-2px);
  box-shadow: 0 5px 20px rgba(77, 166, 255, 0.4);
}

.btn-github:hover {
  background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
  border-color: var(--primary-color);
}

.btn-demo:hover {
  background: rgba(77, 166, 255, 0.1);
}

/* ==================== BADGES DE STATUS ==================== */
.status-badge {
  position: absolute;
  top: 20px;
  right: 20px;
  background: var(--success-gradient);
  color: var(--light-text);
  padding: 6px 12px;
  border-radius: 20px;
  font-size: 12px;
  font-weight: 700;
  box-shadow: 0 3px 10px rgba(0, 204, 102, 0.3);
}

/* ==================== ANIMAÇÕES ==================== */
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

.project-card {
  animation: fadeInUp 0.6s ease backwards;
}

.project-card:nth-child(1) { animation-delay: 0.1s; }
.project-card:nth-child(2) { animation-delay: 0.2s; }
.project-card:nth-child(3) { animation-delay: 0.3s; }
.project-card:nth-child(4) { animation-delay: 0.4s; }

/* ==================== RESPONSIVIDADE ==================== */
@media (max-width: 768px) {
  .page--portfolio main.grid__item {
    padding-left: 15px;
    padding-right: 15px;
  }

  .projects-grid {
    grid-template-columns: 1fr;
    gap: 25px;
  }
  
  .page__title {
    font-size: 36px !important;
  }
  
  .page-title h1 {
    font-size: 42px;
  }
  
  .intro-text {
    font-size: 18px;
  }
  
  .project-card {
    padding: 25px;
  }
  
  .btn-custom {
    width: 100%;
  }
}
</style>

<!-- Título com Efeito Neon -->
<div class="page-title">
  <h1>Meus Projetos</h1>
</div>

<!-- Introdução -->
<p class="intro-text">
  Confira alguns dos meus projetos mais relevantes em <strong>infraestrutura, redes e automação</strong>. Cada projeto foi desenvolvido com foco em eficiência, automação e boas práticas de desenvolvimento.
</p>

<!-- Grid de Projetos -->
<div class="projects-grid">

  <!-- Projeto 1: Modem VIVO -->
  <div class="project-card">
    <span class="status-badge">✓ Ativo</span>
    
    <div class="project-icon">
      📶
    </div>
    
    <h2 class="project-title">Modem VIVO</h2>
    
    <p class="project-description">
      Ferramenta de automação completa para desbloqueio de configurações avançadas do modem Askey RTF8115VW REV5 (VIVO). Desenvolvida com Node.js e Selenium WebDriver para automatizar o processo de forma segura e eficiente.
    </p>
    
    <div class="tech-tags">
      <span class="tech-tag">Node.js</span>
      <span class="tech-tag">Selenium</span>
      <span class="tech-tag">PowerShell</span>
      <span class="tech-tag">ChromeDriver</span>
      <span class="tech-tag">JavaScript</span>
    </div>
    
    <div class="project-buttons">
      <a href="https://github.com/edgardocorrea/modem-vivo" class="btn-custom btn-github" target="_blank">
        <i class="fab fa-github"></i> Ver no GitHub
      </a>
      <a href="https://github.com/edgardocorrea/modem-vivo#readme" class="btn-custom btn-demo" target="_blank">
        <i class="fas fa-book"></i> Documentação
      </a>
    </div>
  </div>

  <!-- Projeto 2: Limpeza Avançada Windows -->
  <div class="project-card">
    <span class="status-badge">✓ Ativo</span>
    
    <div class="project-icon">
      🧹
    </div>
    
    <h2 class="project-title">Limpeza Avançada Windows</h2>
    
    <p class="project-description">
      Script Gráfico automatizado para limpeza profunda do Windows. Remove arquivos temporários, cache, logs e otimiza o sistema operacional com interface intuitiva e opções avançadas de personalização.
    </p>
    
    <div class="tech-tags">
      <span class="tech-tag">PowerShell</span>
      <span class="tech-tag">Windows API</span>
      <span class="tech-tag">Batch</span>
      <span class="tech-tag">Automação</span>
    </div>
    
    <div class="project-buttons">
      <a href="https://github.com/edgardocorrea/LimpezaAvancada" class="btn-custom btn-github" target="_blank">
        <i class="fab fa-github"></i> Ver no GitHub
      </a>
      <a href="https://github.com/edgardocorrea/LimpezaAvancada#readme" class="btn-custom btn-demo" target="_blank">
        <i class="fas fa-book"></i> Documentação
      </a>
    </div>
  </div>

  <!-- Projeto 3: Outros Projetos -->
  <div class="project-card">
    <span class="status-badge" style="background: var(--warning-gradient);">⏳ Em Breve</span>
    
    <div class="project-icon">
      🔧
    </div>
    
    <h2 class="project-title">Outros Projetos</h2>
    
    <p class="project-description">
      Novos projetos com N8N, automação e desenvolvimento em andamento. Mais atualizações em breve!
    </p>
    
    <div class="tech-tags">
      <span class="tech-tag">Em Desenvolvimento</span>
    </div>
    
    <div class="project-buttons">
      <a href="https://github.com/edgardocorrea" class="btn-custom btn-github" target="_blank">
        <i class="fab fa-github"></i> Ver GitHub
      </a>
    </div>
  </div>

</div>
