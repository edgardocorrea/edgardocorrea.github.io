---
title: "Minhas Habilidades"
permalink: /habilidades/
layout: single
---

<style>
/* ==================== FUNDO NEON ANIMADO PARA HABILIDADES ==================== */
body.page--habilidades {
  background: #142850;
  overflow-x: hidden;
}

/* Conteúdo principal e blocos de habilidades com estilo de cards */
body.page--habilidades .initial-content,
body.page--habilidades .notice--info,
body.page--habilidades .notice--success,
body.page--habilidades .notice--warning {
  background: linear-gradient(145deg, rgba(20, 40, 80, 0.8), rgba(10, 20, 40, 0.9));
  border-radius: 15px;
  padding: 30px 25px;
  margin-bottom: 25px;
  position: relative;
  overflow: hidden;
  box-shadow: 0 8px 30px rgba(0, 0, 0, 0.5);
  transition: all 0.4s ease;
}

/* Camada neon animada */
body.page--habilidades .initial-content::before,
body.page--habilidades .notice--info::before,
body.page--habilidades .notice--success::before,
body.page--habilidades .notice--warning::before {
  content: "";
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: linear-gradient(135deg, #4da6ff, #00ccff, #4da6ff, #00ccff);
  opacity: 0.2;
  transform: rotate(45deg);
  filter: blur(40px);
  animation: neonGlow 6s linear infinite;
  pointer-events: none;
  z-index: 0;
  border-radius: 20px;
}

/* Hover nos blocos */
body.page--habilidades .initial-content:hover,
body.page--habilidades .notice--info:hover,
body.page--habilidades .notice--success:hover,
body.page--habilidades .notice--warning:hover {
  box-shadow: 0 15px 50px rgba(77, 166, 255, 0.5);
  transform: translateY(-5px) scale(1.02);
}

/* ==================== TÍTULOS DAS HABILIDADES ==================== */
body.page--habilidades h4 {
  position: relative;
  z-index: 1;
  color: #4da6ff;
  text-shadow:
    0 0 5px #4da6ff,
    0 0 10px #00ccff,
    0 0 20px #00ccff,
    0 0 40px #0088cc;
  margin-bottom: 10px;
}

/* ==================== ITENS DE LISTA ==================== */
body.page--habilidades li {
  position: relative;
  z-index: 1;
  color: #cccccc;
  padding-left: 15px;
  margin-bottom: 8px;
}

/* Marcador neon antes do item */
body.page--habilidades li::before {
  content: "•";
  position: absolute;
  left: 0;
  color: #4da6ff;
  font-weight: bold;
  text-shadow:
    0 0 3px #4da6ff,
    0 0 6px #00ccff,
    0 0 10px #00ccff;
}

/* ==================== ANIMAÇÃO NEON ==================== */
@keyframes neonGlow {
  0%, 100% {
    transform: rotate(0deg) translate(-50%, -50%);
  }
  50% {
    transform: rotate(45deg) translate(-50%, -50%);
  }
}

/* ==================== RESPONSIVO ==================== */
@media (max-width: 768px) {
  body.page--habilidades .initial-content,
  body.page--habilidades .notice--info,
  body.page--habilidades .notice--success,
  body.page--habilidades .notice--warning {
    padding: 20px 15px;
  }

  body.page--habilidades h4 {
    font-size: 20px;
  }
}
</style>


## 💻 Principais Habilidades

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
