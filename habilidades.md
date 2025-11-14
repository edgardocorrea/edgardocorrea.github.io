---
title: "Minhas Habilidades"
permalink: /habilidades/
layout: single
---

/* Remover a bolinha padrão dos <li> */
.notice--info ul,
.notice--success ul,
.notice--warning ul {
  list-style: none;
  padding-left: 0; /* opcional para alinhar melhor */
}

/* Manter apenas a bolinha neon personalizada */
.notice--info li,
.notice--success li,
.notice--warning li {
  position: relative;
  z-index: 1;
  color: #cccccc;
  padding-left: 20px;
  margin-bottom: 8px;
}

.notice--info li::before,
.notice--success li::before,
.notice--warning li::before {
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
