---
title: "Minhas Habilidades"
permalink: /habilidades/
layout: single
---

<style>
/* ==================== FUNDO PADRÃO DA PÁGINA ==================== */
/* Mantém o fundo azul escuro e aplica o mesmo fundo dos cards no INITIAL-CONTENT */

body.page--certificacoes {
  background: #142850 !important;
}

/* Área principal com o mesmo gradiente dos cards */
.initial-content {
  background: linear-gradient(145deg, rgba(20,40,80,0.8), rgba(10,20,40,0.9)) !important;
  padding: 25px;
  border-radius: 15px;
  box-shadow: 0 8px 20px rgba(0,0,0,0.5);
  position: relative;
  z-index: 1;
}

/* ==================== TÍTULO EM NEON (PADRÃO PROJETOS / HABILIDADES) ==================== */
.page__title {
  text-align: center;
  font-size: 48px !important;
  background: linear-gradient(90deg, #4da6ff, #00ccff);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  margin-bottom: 25px;
  text-shadow: 2px 2px 10px rgba(77, 166, 255, 0.5);
}

/* ==================== CARDS DE CERTIFICADO - MESMO PADRÃO DOS CARDS ==================== */
/* Ajuste o nome da classe caso seus certificados tenham outra */
.cert-card {
  background: linear-gradient(145deg, rgba(20,40,80,0.8), rgba(10,20,40,0.9));
  border-radius: 15px;
  padding: 25px;
  margin-bottom: 25px;
  position: relative;
  overflow: hidden;
  box-shadow: 0 8px 20px rgba(0,0,0,0.5);
  transition: all 0.4s ease;
}

/* Camada neon animada apenas NOS CARDS */
.cert-card::before {
  content: "";
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: linear-gradient(135deg, #4da6ff, #00ccff, #4da6ff, #00ccff);
  opacity: 0.18;
  transform: rotate(45deg);
  filter: blur(45px);
  animation: neonGlow 6s linear infinite;
  pointer-events: none;
  z-index: 0;
  border-radius: 20px;
}

/* Hover com destaque NEON */
.cert-card:hover {
  box-shadow: 0 15px 50px rgba(77, 166, 255, 0.6);
  transform: translateY(-5px) scale(1.02);
}

/* ==================== TÍTULOS E TEXTOS DO CARD ==================== */

.cert-title {
  position: relative;
  z-index: 2;
  color: #ffffff;
  font-size: 24px;
  font-weight: 700;
  margin-bottom: 10px;
}

.cert-provider {
  position: relative;
  z-index: 2;
  color: #4da6ff;
  font-size: 16px;
  margin-bottom: 5px;
}

.cert-description {
  position: relative;
  z-index: 2;
  color: #cccccc;
  line-height: 1.6;
  font-size: 15px;
}

/* ==================== LISTAS DENTRO DO CARD ==================== */

.cert-card ul li {
  color: #cccccc;
  position: relative;
  z-index: 2;
  padding-left: 15px;
  margin-bottom: 6px;
}

/* bolinha neon */
.cert-card ul li::before {
  content: "•";
  color: #4da6ff;
  position: absolute;
  left: 0;
  font-size: 20px;
  line-height: 12px;
  text-shadow:
    0 0 5px #4da6ff,
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
  .cert-card {
    padding: 20px;
  }
  .page__title {
    font-size: 36px !important;
  }
  .cert-title {
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
