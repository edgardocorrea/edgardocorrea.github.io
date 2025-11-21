---
title: "Minhas Habilidades"
permalink: /habilidades/
layout: single
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
body.page--habilidades {
  background: var(--dark-bg);
  overflow-x: hidden;
  min-height: 100vh;
  position: relative;
}

/* Bloco inicial (initial-content) – fundo azul, sem hover animado */
.initial-content {
  position: relative;
  background: var(--darker-bg);
  padding: 30px 25px;
  border-radius: 20px;
  box-shadow: 0 8px 25px rgba(0,0,0,0.6);
  backdrop-filter: blur(3px);
  z-index: 1;
  transition: none;
  box-sizing: border-box;
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

/* ==================== CARDS DE HABILIDADES ==================== */
.notice--info,
.notice--success,
.notice--warning {
  background: var(--darker-bg);
  border-radius: 15px;
  padding: 30px 25px;
  margin-bottom: 25px;
  position: relative;
  overflow: hidden;
  box-shadow: 0 8px 30px rgba(0, 0, 0, 0.5);
  transition: all 0.4s ease;
}

/* Efeito neon apenas no card de Infraestrutura & Redes (notice--info) */
.notice--info::before {
  content: "";
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: linear-gradient(135deg, var(--primary-color), var(--secondary-color), var(--primary-color), var(--secondary-color));
  opacity: 0.2;
  transform: rotate(45deg);
  filter: blur(40px);
  animation: neonGlow 6s linear infinite;
  pointer-events: none;
  z-index: 0;
  border-radius: 20px;
}

/* Efeito hover para todos os cards */
.notice--info:hover,
.notice--success:hover,
.notice--warning:hover {
  box-shadow: 0 15px 50px rgba(77, 166, 255, 0.5);
  transform: translateY(-5px) scale(1.02);
}

/* ==================== TÍTULOS ==================== */
/* Título "Principais Habilidades" (ou h2/h3) com cor branca normal */
.intro-text, 
h2, h3 {
  color: var(--light-text);
  background: none;
  -webkit-background-clip: unset;
  -webkit-text-fill-color: unset;
  text-shadow: none;
}

/* Títulos dentro dos cards */
.notice--info h4,
.notice--success h4,
.notice--warning h4 {
  position: relative;
  z-index: 1;
  color: var(--gray-text);
  text-shadow: none;
  margin-bottom: 10px;
}

/* ==================== LISTAS ==================== */
/* Remover a bolinha padrão dos <li> */
.notice--info ul,
.notice--success ul,
.notice--warning ul {
  list-style: none;
  padding-left: 0;
}

/* Estilo personalizado para os itens da lista */
.notice--info li,
.notice--success li,
.notice--warning li {
  position: relative;
  z-index: 1;
  color: var(--gray-text);
  padding-left: 20px;
  margin-bottom: 8px;
}

/* Bolinha neon personalizada */
.notice--info li::before,
.notice--success li::before,
.notice--warning li::before {
  content: "•";
  position: absolute;
  left: 0;
  color: var(--primary-color);
  font-weight: bold;
  text-shadow:
    0 0 3px var(--primary-color),
    0 0 6px var(--secondary-color),
    0 0 10px var(--secondary-color);
}

/* ==================== ANIMAÇÕES ==================== */
@keyframes neonGlow {
  0%, 100% {
    transform: rotate(0deg) translate(-50%, -50%);
  }
  50% {
    transform: rotate(45deg) translate(-50%, -50%);
  }
}

/* ==================== RESPONSIVIDADE ==================== */
@media (max-width: 768px) {
  .initial-content,
  .notice--info,
  .notice--success,
  .notice--warning {
    padding: 20px 15px;
  }
  
  .page__title {
    font-size: 36px !important;
  }
  
  .page-title h1 {
    font-size: 42px;
  }
}
</style>

<!-- Título com Efeito Neon -->
<div class="page-title">
  <h1>Minhas Habilidades</h1>
</div>

<!-- Título Secundário -->
<h2>💻 Principais Habilidades</h2>

<!-- Cards de Habilidades -->
<div class="notice--info">
  <h4>Infraestrutura & Redes</h4>
  <ul>
    <li>Configuração de switches, routers e firewalls</li>
    <li>Mikrotik, TP-Link</li>
    <li>Protocolos: TCP/IP, VLANs, OSPF, BGP</li>
    <li>Segurança de rede e VPN</li>
  </ul>
</div>

<div class="notice--success">
  <h4>Sistemas & Virtualização</h4>
  <ul>
    <li>Linux (Slackware, Ubuntu, CentOS)</li>
    <li>Windows Server (2016/2019/2022)</li>
    <li>VMware vSphere & Hyper-V</li>
  </ul>
</div>

<div class="notice--warning">
  <h4>Automação & Scripting</h4>
  <ul>
    <li>PowerShell para automação Windows</li>
    <li>Bash scripting para Linux</li>
    <li>Python para automação de tarefas</li>
  </ul>
</div>
