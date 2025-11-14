---
title: "Meus Projetos"
layout: single
permalink: /portfolio/
classes: wide
author_profile: false
---

<style>
/* ====================MUDANÇA FEITA ==================== */


/* Customizações só para /portfolio/ */
.page--portfolio {
  /* CORREÇÃO 1: Forçar a página a usar uma coluna e centralizar o conteúdo */
  .grid__wrapper {
    display: block; /* Ignora o layout de grade do tema */
    width: 100%;
    max-width: 100%;
  }

  .page__content {
    margin-left: auto !important; /* Usar !important para garantir que sobrescreva o tema */
    margin-right: auto !important;
    max-width: 1100px;
    padding-left: 20px;
    padding-right: 20px;
    box-sizing: border-box;
  }

  /* CORREÇÃO 2: Centralizar e organizar os botões verticalmente */
  .project-buttons {
    display: flex;
    flex-direction: column; /* Garante que os botões fiquem em coluna */
    gap: 10px;
    align-items: center;
    margin-top: 25px; /* Mantido da regra antiga */
  }

  .btn-custom {
    width: 100%;
    max-width: 240px;
    text-align: center;
  }
}


/* ==================== TÍTULO PRINCIPAL ==================== */
.page__title {
  text-align: center;
  font-size: 48px !important;
  color: #ffffff !important;
  margin-bottom: 20px !important;
  text-shadow: 2px 2px 10px rgba(77, 166, 255, 0.5);
  background: linear-gradient(90deg, #4da6ff, #00ccff);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

/* ==================== SUBTÍTULO ==================== */
.intro-text {
  text-align: center;
  font-size: 20px;
  color: #cccccc;
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
  margin: 40px auto;
  padding: 0 15px; /* evita overflow horizontal */
  width: 100%;
  box-sizing: border-box; /* importante para padding */
}

/* ==================== CARD DE PROJETO ==================== */
.project-card {
  width: 100%; /* garante que não ultrapasse a coluna */
  box-sizing: border-box;
  background: linear-gradient(145deg, rgba(20, 40, 80, 0.8), rgba(10, 20, 40, 0.9));
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
  background: linear-gradient(135deg, #4da6ff, #00ccff, #4da6ff);
  -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
  -webkit-mask-composite: xor;
  mask-composite: exclude;
  opacity: 0;
  transition: opacity 0.4s ease;
}

.project-card:hover::before {
  opacity: 1;
}

.project-card:hover {
  transform: translateY(-10px) scale(1.02);
  box-shadow: 0 15px 50px rgba(77, 166, 255, 0.4);
}

/* ==================== ÍCONE DO PROJETO ==================== */
.project-icon {
  width: 80px;
  height: 80px;
  margin: 0 auto 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: linear-gradient(135deg, #4da6ff, #0088cc);
  border-radius: 20px;
  font-size: 40px;
  box-shadow: 0 5px 20px rgba(77, 166, 255, 0.3);
}

/* ==================== TÍTULO DO PROJETO ==================== */
.project-title {
  font-size: 28px !important;
  color: #ffffff !important;
  margin: 20px 0 15px 0 !important;
  text-align: center;
  font-weight: 700;
}

/* ==================== DESCRIÇÃO ==================== */
.project-description {
  color: #cccccc;
  font-size: 16px;
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
  border: 1px solid #4da6ff;
  color: #4da6ff;
  padding: 6px 12px;
  border-radius: 20px;
  font-size: 13px;
  font-weight: 600;
  transition: all 0.3s ease;
}

.tech-tag:hover {
  background: rgba(77, 166, 255, 0.3);
  transform: scale(1.05);
}

/* ==================== BOTÕES ==================== */
/* A regra .project-buttons foi movida para dentro de .page--portfolio para evitar conflitos e garantir a especificidade. */

.btn-custom {
  display: inline-flex;
  align-items: center;
  justify-content: center; /* Centraliza o texto e o ícone dentro do botão */
  gap: 8px;
  padding: 12px 24px;
  border-radius: 8px;
  font-size: 15px;
  font-weight: 600;
  text-decoration: none;
  transition: all 0.3s ease;
  border: 2px solid;
}

.btn-github {
  background: linear-gradient(135deg, #333333, #1a1a1a);
  color: #ffffff;
  border-color: #333333;
}

.btn-github:hover {
  background: linear-gradient(135deg, #4da6ff, #0088cc);
  border-color: #4da6ff;
  transform: translateY(-2px);
  box-shadow: 0 5px 20px rgba(77, 166, 255, 0.4);
}

.btn-demo {
  background: transparent;
  color: #4da6ff;
  border-color: #4da6ff;
}

.btn-demo:hover {
  background: rgba(77, 166, 255, 0.1);
  transform: translateY(-2px);
}

/* ==================== STATUS BADGE ==================== */
.status-badge {
  position: absolute;
  top: 20px;
  right: 20px;
  background: linear-gradient(135deg, #00cc66, #00aa55);
  color: #ffffff;
  padding: 6px 12px;
  border-radius: 20px;
  font-size: 12px;
  font-weight: 700;
  box-shadow: 0 3px 10px rgba(0, 204, 102, 0.3);
}

/* ==================== RESPONSIVO ==================== */
@media (max-width: 768px) {
  .projects-grid {
    grid-template-columns: 1fr;
    gap: 25px;
    padding: 0 15px;
  }
  
  .page__title {
    font-size: 36px !important;
  }
  
  .intro-text {
    font-size: 18px;
  }
  
  .project-card {
    padding: 25px;
  }
  
  /* A regra abaixo já está implícita na nova regra principal, mas pode ser mantida para clareza */
  .project-buttons {
    flex-direction: column;
  }
  
  .btn-custom {
    width: 100%;
  }
}

/* ==================== ANIMAÇÃO DE ENTRADA ==================== */
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
</style>

<!-- Introdução -->
<p class="intro-text">
  🚀 Confira alguns dos meus projetos mais relevantes em <strong>infraestrutura, redes e automação</strong>. Cada projeto foi desenvolvido com foco em eficiência, automação e boas práticas de desenvolvimento.
</p>

<!-- Grid de Projetos -->
<div class="projects-grid">

  <!-- Projeto 1: Modem VIVO Unlock -->
  <div class="project-card">
    <span class="status-badge">✓ Ativo</span>
    
    <div class="project-icon">
      📡
    </div>
    
    <h2 class="project-title">Modem VIVO Unlock</h2>
    
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
      Script PowerShell automatizado para limpeza profunda do Windows. Remove arquivos temporários, cache, logs e otimiza o sistema operacional com interface intuitiva e opções avançadas de personalização.
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

  <!-- Projeto 3: (Adicione mais projetos aqui) -->
  <div class="project-card">
    <span class="status-badge" style="background: linear-gradient(135deg, #ffcc00, #ff9900);">⏳ Em Breve</span>
    
    <div class="project-icon">
      🔧
    </div>
    
    <h2 class="project-title">Outros Projetos</h2>
    
    <p class="project-description">
      Novos projetos de infraestrutura, automação e desenvolvimento em andamento. Fique atento para mais atualizações em breve!
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

