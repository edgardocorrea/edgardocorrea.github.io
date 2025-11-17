---
title: "Habilidades"
permalink: /habilidades/
layout: single
---

<style>
/* ==================== ESTILIZAÇÃO PARA HABILIDADES ==================== */

/* Fundo da página */
body.page--habilidades {
  background: #142850;
  overflow-x: hidden;
  min-height: 100vh;
  position: relative;
}

/* Bloco inicial */
.initial-content {
  background: rgba(10,20,40,0.85);
  padding: 30px 25px;
  border-radius: 20px;
  box-shadow: 0 8px 25px rgba(0,0,0,0.6);
  backdrop-filter: blur(3px);
  box-sizing: border-box;
}

/* Cards */
.notice--info,
.notice--success,
.notice--warning {
  background: rgba(10, 20, 40, 0.8);
  border-radius: 15px;
  padding: 30px 25px;
  margin-bottom: 25px;
  position: relative;
  overflow: hidden;
  box-shadow: 0 8px 30px rgba(0, 0, 0, 0.5);
  transition: all 0.4s ease;
}

/* Neon animado apenas no card notice--info */
.notice--info::before {
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
  border-radius: 20px;
}

.notice--info:hover {
  box-shadow: 0 15px 50px rgba(77, 166, 255, 0.5);
  transform: translateY(-5px) scale(1.02);
}

.notice--success:hover,
.notice--warning:hover {
  box-shadow: 0 12px 40px rgba(0, 0, 0, 0.4);
  transform: translateY(-3px) scale(1.01);
}

/* Subtítulo brilhante */
.habilidade-brilhante {
  display: block;
  text-align: center;
  margin-top: 25px;
  margin-bottom: 35px;
  font-size: 32px;
  font-weight: 700;
  color: #ffffff;
  text-shadow:
    0 0 10px rgba(255, 255, 255, 0.9),
    0 0 20px rgba(0, 234, 255, 0.8),
    0 0 35px rgba(0, 234, 255, 0.6),
    0 0 50px rgba(0, 234, 255, 0.4);
}

/* Título principal (neon) */
.page__title {
  text-align: center;
  font-size: 48px !important;
  font-weight: 700;
  background: linear-gradient(90deg, #4da6ff, #00ccff);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  text-shadow: 2px 2px 10px rgba(77, 166, 255, 0.5);
}

/* Títulos dentro dos cards */
.notice--info h4,
.notice--success h4,
.notice--warning h4 {
  color: #cccccc;
  margin-bottom: 10px;
  position: relative;
}

/* Listas */
.notice--info ul,
.notice--success ul,
.notice--warning ul {
  list-style: none;
  padding-left: 0;
}

.notice--info li,
.notice--success li,
.notice--warning li {
  position: relative;
  padding-left: 20px;
  margin-bottom: 8px;
  color: #cccccc;
}

.notice--info li::before,
.notice--success li::before,
.notice--warning li::before {
  content: "•";
  position: absolute;
  left: 0;
  color: #4da6ff;
  text-shadow:
    0 0 3px #4da6ff,
    0 0 6px #00ccff,
    0 0 10px #00ccff;
}

/* Animação Neon */
@keyframes neonGlow {
  0%, 100% {
    transform: rotate(0deg);
  }
  50% {
    transform: rotate(45deg);
  }
}

/* Responsivo */
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
  .habilidade-brilhante {
    font-size: 26px;
  }
}
</style>

<!-- Subtítulo correto e no lugar certo -->
<span class="habilidade-brilhante">💻 Principais Habilidades</span>

<!-- CARDS -->
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
