---
title: "Certificações e Badges"
layout: single
permalink: /certificacoes/
author_profile: false
sidebar: null
---

<style>
/* ==================== VARIÁVEIS CSS ==================== */
:root {
  --primary-color: #4da6ff;
  --secondary-color: #00ccff;
  --dark-bg: #142850;
  --darker-bg: rgba(10, 20, 40, 0.85);
  --light-text: #ffffff;
  --gray-text: #cccccc;
}

/* ==================== CONFIGURAÇÕES GERAIS ==================== */
body.page--certificacoes {
  background: var(--dark-bg) !important;
  overflow-x: hidden;
  position: relative;
}

.initial-content {
  position: relative;
  background: var(--darker-bg);
  padding: 30px 25px;
  border-radius: 20px;
  box-shadow: 0 8px 25px rgba(0,0,0,0.6);
  backdrop-filter: blur(3px);
  z-index: 1;
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

/* Manter regra existente para compatibilidade */
.page__title {
  text-align: center;
  font-size: 48px !important;
  font-weight: 700;
  background: linear-gradient(90deg, var(--primary-color), var(--secondary-color));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  text-shadow: 2px 2px 10px rgba(77, 166, 255, 0.5);
}

/* ==================== CONTEÚDO INTRODUTÓRIO ==================== */
.initial-content p {
  color: var(--light-text) !important;
}

.initial-content a {
  color: var(--light-text);
  text-decoration: none;
  transition: all 0.3s ease;
}

.initial-content a:hover {
  text-decoration: underline;
  color: var(--primary-color);
}

/* ==================== SEÇÕES DE CERTIFICAÇÕES ==================== */
.cert-section {
  margin-top: 35px;
  margin-bottom: 15px;
}

.cert-section h2 {
  color: var(--light-text) !important;
  font-weight: 700;
  text-shadow: 0 0 6px rgba(255,255,255,0.3);
}

/* ==================== BADGES DO CREDLY - ESTILOS FORÇADOS ==================== */
/* Container principal do badge */
.cert-badge {
  display: inline-block;
  margin: 12px;
  color: var(--light-text);
  text-align: center;
  transition: transform 0.3s ease;
  vertical-align: top;
}

.cert-badge:hover {
  transform: scale(1.05);
}

/* FORÇAR ESTILOS DOS ELEMENTOS INTERNOS DO BADGE */
/* Nome do certificado */
.cert-badge .badge-name,
.cert-badge [id*="badge-name"],
.cert-badge [class*="badge-name"],
.credly-badge .badge-name,
.credly-badge [id*="badge-name"],
.credly-badge [class*="badge-name"] {
  color: var(--light-text) !important;
  font-weight: 600 !important;
  font-size: 14px !important;
  line-height: 1.3 !important;
  margin-bottom: 4px !important;
  display: block !important;
}

/* Emissor do certificado */
.cert-badge .badge-issuer,
.cert-badge [id*="badge-issuer"],
.cert-badge [class*="badge-issuer"],
.credly-badge .badge-issuer,
.credly-badge [id*="badge-issuer"],
.credly-badge [class*="badge-issuer"] {
  color: var(--light-text) !important;
  font-weight: 400 !important;
  font-size: 12px !important;
  opacity: 0.9 !important;
  display: block !important;
}

/* Data do certificado */
.cert-badge .badge-date,
.cert-badge [id*="badge-date"],
.cert-badge [class*="badge-date"],
.credly-badge .badge-date,
.credly-badge [id*="badge-date"],
.credly-badge [class*="badge-date"] {
  color: var(--light-text) !important;
  font-weight: 400 !important;
  font-size: 11px !important;
  opacity: 0.8 !important;
  display: block !important;
  margin-top: 2px !important;
}

/* Estilo geral para todos os elementos dentro do badge */
.cert-badge *,
.cert-badge div,
.cert-badge span,
.credly-badge *,
.credly-badge div,
.credly-badge span {
  color: var(--light-text) !important;
  font-family: 'Inter', 'Segoe UI', sans-serif !important;
}

/* ==================== IFRAMES DO CREDLY ==================== */
/* Forçar estilos dentro dos iframes */
.cert-badge iframe,
.credly-badge iframe {
  border: none !important;
  background: transparent !important;
}

/* Estilos para o conteúdo dentro do iframe */
.cert-badge iframe body,
.cert-badge iframe html,
.credly-badge iframe body,
.credly-badge iframe html {
  background: transparent !important;
  color: var(--light-text) !important;
}

/* ==================== RESPONSIVIDADE ==================== */
@media (max-width: 768px) {
  .page__title { 
    font-size: 36px !important; 
  }
  
  .page-title h1 {
    font-size: 42px;
  }
  
  .cert-badge {
    margin: 8px;
  }
}
</style>

<!-- Título com Efeito Neon -->
<div class="page-title">
  <h1>Certificações e Badges</h1>
</div>

<div class="initial-content">
  <p>Apresento aqui minhas certificações profissionais, que validam competências em diversas áreas da tecnologia. Para mais detalhes ou para verificar a autenticidade, visite meu perfil completo no <a href="https://www.credly.com/users/edgardo.correa" target="_blank">Credly</a>.</p>

  <!-- Seção de Redes -->
  <div class="cert-section">
    <h2>Redes</h2>
    <div class="cert-badge" data-iframe-width="150" data-iframe-height="270" data-share-badge-id="232a032a-8675-4fbd-9752-b74219f08ad8" data-share-badge-host="https://www.credly.com"></div>
    <div class="cert-badge" data-iframe-width="150" data-iframe-height="270" data-share-badge-id="5c6077c7-6f57-4196-b648-e7d3b5b82624" data-share-badge-host="https://www.credly.com"></div>
    <div class="cert-badge" data-iframe-width="150" data-iframe-height="270" data-share-badge-id="e0ee1601-18f3-41d2-97f3-67a836bfe4c9" data-share-badge-host="https://www.credly.com"></div>
  </div>

  <!-- Seção de Segurança -->
  <div class="cert-section">
    <h2>Segurança da Informação</h2>
    <div class="cert-badge" data-iframe-width="150" data-iframe-height="270" data-share-badge-id="d44d5772-1fee-4491-9326-ab1aa4a908ca" data-share-badge-host="https://www.credly.com"></div>
    <div class="cert-badge" data-iframe-width="150" data-iframe-height="270" data-share-badge-id="02abd07a-71a8-4024-8316-0dd40691fa74" data-share-badge-host="https://www.credly.com"></div>
  </div>

  <!-- Seção de IA e Metodologias Ágeis -->
  <div class="cert-section">
    <h2>Inteligência Artificial e Metodologias Ágeis</h2>
    <div class="cert-badge" data-iframe-width="150" data-iframe-height="270" data-share-badge-id="aa5e1665-af74-4d59-9567-409b890991f4" data-share-badge-host="https://www.credly.com"></div>
    <div class="cert-badge" data-iframe-width="150" data-iframe-height="270" data-share-badge-id="bdb8bcd3-8357-4d2e-8894-f1fe4e36e079" data-share-badge-host="https://www.credly.com"></div>
    <div class="cert-badge" data-iframe-width="150" data-iframe-height="270" data-share-badge-id="24f3cc92-a5fb-469b-820d-d2d85b4d487c" data-share-badge-host="https://www.credly.com"></div>
  </div>
</div>

<!-- Script do Credly para renderizar os badges -->
<script type="text/javascript" async src="//cdn.credly.com/assets/utilities/embed.js"></script>

<!-- Script adicional para forçar estilos após carregamento dos badges -->
<script>
document.addEventListener('DOMContentLoaded', function() {
  // Esperar um pouco para o script do Credly carregar
  setTimeout(function() {
    // Tentar aplicar estilos diretamente nos elementos criados
    const badges = document.querySelectorAll('.cert-badge iframe, .credly-badge iframe');
    
    badges.forEach(function(badge) {
      try {
        // Tentar acessar o conteúdo do iframe
        const badgeDoc = badge.contentDocument || badge.contentWindow.document;
        if (badgeDoc) {
          // Aplicar estilos diretamente no documento do iframe
          const style = badgeDoc.createElement('style');
          style.textContent = `
            body, html {
              background: transparent !important;
              color: #ffffff !important;
              font-family: 'Inter', 'Segoe UI', sans-serif !important;
            }
            .badge-name {
              color: #ffffff !important;
              font-weight: 600 !important;
            }
            .badge-issuer {
              color: #ffffff !important;
              font-weight: 400 !important;
            }
            .badge-date {
              color: #ffffff !important;
              font-weight: 400 !important;
            }
            * {
              color: #ffffff !important;
            }
          `;
          badgeDoc.head.appendChild(style);
        }
      } catch (e) {
        // Se não conseguir acessar o iframe (cross-origin), aplicar estilos externos
        console.log('Não foi possível acessar o iframe do badge:', e);
      }
    });
  }, 2000);
});
</script>
