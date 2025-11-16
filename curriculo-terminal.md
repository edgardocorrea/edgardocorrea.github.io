---
title: ""
layout: single
permalink: /curriculo-terminal/
classes: wide
author_profile: false
---

<style>
/* ==================== CENTRALIZAÇÃO GLOBAL ==================== */
.page,
.page__content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  width: 100%;
}

/* ==================== BACKGROUND AZUL ESCURO ==================== */
body {
  overflow-x: hidden;
  background: #0a1428 !important;
}

.initial-content {
  position: relative;
  background: rgba(10,20,40,0.85);
  padding: 30px 25px;
  border-radius: 20px;
  box-shadow: 0 8px 25px rgba(0,0,0,0.6);
  backdrop-filter: blur(3px);
  z-index: 1;
}

.page {
  background: transparent;
}

.page__content {
  background: transparent;
  padding: 20px;
  max-width: 100%;
}

.page__title {
  display: none;
}

/* ==================== TERMINAL CONTAINER ==================== */
.terminal-container {
  background: #000814;
  border: 2px solid #00d4ff;
  border-radius: 8px;
  padding: 20px;
  margin: 20px auto;
  max-width: 900px;
  width: 100%;
  box-shadow: 0 0 30px rgba(0, 212, 255, 0.5);
  position: relative;
}

/* Terminal Header */
.terminal-header {
  display: flex;
  gap: 8px;
  margin-bottom: 20px;
  padding-bottom: 10px;
  border-bottom: 1px solid #00d4ff;
}

.terminal-button {
  width: 12px;
  height: 12px;
  border-radius: 50%;
  display: inline-block;
}

.btn-close { background: #ff5555; }
.btn-minimize { background: #ffff55; }
.btn-maximize { background: #55ff55; }

.terminal-title {
  color: #00d4ff;
  margin-left: 10px;
  font-size: 12px;
  font-family: 'Courier New', monospace;
}

/* Terminal Output */
.terminal-output {
  min-height: 400px;
  color: #00d4ff;
  font-size: 14px;
  line-height: 1.6;
  white-space: pre; /* ← ARRUMA A CAIXA ASCII */
  font-family: 'Courier New', monospace;
}

.terminal-line {
  margin-bottom: 10px;
  opacity: 0;
  animation: fadeIn 0.3s forwards;
}

@keyframes fadeIn {
  to { opacity: 1; }
}

.prompt {
  color: #00d4ff;
  font-weight: bold;
}

.command {
  color: #00ffff;
}

.output {
  color: #ffffff;
}

.error {
  color: #ff5555;
}

.success {
  color: #00ff88;
}

.warning {
  color: #ffff55;
}

/* Terminal Input */
.terminal-input-area {
  display: flex;
  align-items: center;
  margin-top: 20px;
  padding-top: 20px;
  border-top: 1px solid #00d4ff;
}

.terminal-input {
  background: transparent;
  border: none;
  color: #00d4ff;
  font-family: 'Courier New', monospace;
  font-size: 14px;
  flex: 1;
  outline: none;
  caret-color: #00d4ff;
}

.cursor {
  display: inline-block;
  width: 8px;
  height: 16px;
  background: #00d4ff;
  animation: blink 1s infinite;
  margin-left: 2px;
}

@keyframes blink {
  0%, 50% { opacity: 1; }
  51%, 100% { opacity: 0; }
}

/* Command Suggestions */
.command-suggestions {
  background: rgba(0, 212, 255, 0.05);
  border: 1px solid #00d4ff;
  border-radius: 4px;
  padding: 15px;
  margin-top: 20px;
  max-width: 900px;
  margin-left: auto;
  margin-right: auto;
}

.command-suggestions h3 {
  color: #ffffff;
  margin-bottom: 10px;
  font-size: 18px;
  font-weight: 700;
  text-shadow: 0 0 10px rgba(255, 255, 255, 0.8);
}

.command-list {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 10px;
}

.command-item {
  color: #00ffff;
  padding: 8px;
  background: rgba(0, 212, 255, 0.1);
  border-radius: 4px;
  cursor: pointer;
  transition: all 0.3s;
  border: 1px solid transparent;
  font-family: 'Courier New', monospace;
}

.command-item:hover {
  background: rgba(0, 212, 255, 0.2);
  transform: translateX(5px);
  border-color: #00d4ff;
  box-shadow: 0 0 15px rgba(0, 212, 255, 0.5);
}

/* Skills Bar */
.skill-bar {
  display: flex;
  align-items: center;
  margin: 8px 0;
}

.skill-name {
  width: 180px;
  color: #00ffff;
  font-family: 'Courier New', monospace;
}

.skill-progress {
  flex: 1;
  height: 22px;
  background: rgba(0, 212, 255, 0.1);
  border: 1px solid #00d4ff;
  border-radius: 4px;
  overflow: hidden;
  position: relative;
}

.skill-fill {
  height: 100%;
  background: linear-gradient(90deg, #00d4ff, #00ffff);
  transition: width 1s ease;
  display: flex;
  align-items: center;
  justify-content: flex-end;
  padding-right: 8px;
  color: #000;
  font-weight: bold;
  font-size: 12px;
  box-shadow: 0 0 15px rgba(0, 212, 255, 0.8);
}

/* RESPONSIVE */
@media (max-width: 768px) {
  .terminal-container {
    margin: 10px;
    padding: 15px;
  }

  .terminal-output {
    font-size: 12px;
  }

  .command-list {
    grid-template-columns: 1fr;
  }

  .skill-name {
    width: 120px;
    font-size: 12px;
  }
}
</style>

<!-- ==================== TERMINAL ==================== -->
<div class="terminal-container">
  <div class="terminal-header">
    <span class="terminal-button btn-close"></span>
    <span class="terminal-button btn-minimize"></span>
    <span class="terminal-button btn-maximize"></span>
    <span class="terminal-title">edgardo@carreira:~$</span>
  </div>

  <div class="terminal-output" id="terminalOutput">
    <div class="terminal-line"><span class="success">╔══════════════════════════════════════════════════════════════════════╗</span></div>
    <div class="terminal-line"><span class="success">║  Bem-vindo ao Sistema de Carreira de Edgardo Correa                   ║</span></div>
    <div class="terminal-line"><span class="success">║  Analista de Sistemas | Infraestrutura & Automação                    ║</span></div>
    <div class="terminal-line"><span class="success">╚══════════════════════════════════════════════════════════════════════╝</span></div>
    <div class="terminal-line"><span class="output">Sistema inicializado...</span></div>
    <div class="terminal-line"><span class="output">Digite um comando ou clique em uma sugestão abaixo ↓</span></div>
  </div>

  <div class="terminal-input-area">
    <span class="prompt">edgardo@carreira:~$</span>
    <input type="text" class="terminal-input" id="commandInput" placeholder="Digite um comando..." autofocus>
    <span class="cursor"></span>
  </div>
</div>

<!-- ==================== SUGESTÕES ==================== -->
<div class="command-suggestions">
  <h3>⚡ Comandos disponíveis:</h3>
  <div class="command-list">
    <div class="command-item" onclick="executeCommand('quem')">📋 quem</div>
    <div class="command-item" onclick="executeCommand('habilidades')">💻 habilidades</div>
    <div class="command-item" onclick="executeCommand('experiencia')">📊 experiência</div>
    <div class="command-item" onclick="executeCommand('projetos')">🚀 projetos</div>
    <div class="command-item" onclick="executeCommand('contato')">📧 contato</div>
    <div class="command-item" onclick="executeCommand('baixar')">⬇️ baixar</div>
    <div class="command-item" onclick="executeCommand('apagar')">🗑️ apagar</div>
    <div class="command-item" onclick="executeCommand('ajuda')">❓ ajuda</div>
  </div>
</div>

<script>
/* ==================== MIGRAÇÃO PARA COMANDOS EM PORTUGUÊS ==================== */
const terminalOutput = document.getElementById("terminalOutput");
const commandInput = document.getElementById("commandInput");

const commands = {
  ajuda: `
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
COMANDOS DISPONÍVEIS:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  quem           Informações pessoais
  habilidades    Habilidades técnicas
  experiencia    Experiência profissional
  projetos       Projetos realizados
  contato        Formas de contato
  baixar         Baixar currículo PDF
  apagar         Limpar terminal
  ajuda          Exibir ajuda

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━`,

  quem: `
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
INFORMAÇÕES PESSOAIS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Nome:          Edgardo Correa
Cargo:         Analista de Sistemas
Área:          Infraestrutura & Automação
Local:         São Paulo, SP - Brasil
Experiência:   5+ anos

Profissional especializado em redes, automação e
administração de sistemas Linux e Windows.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━`,

  habilidades: `
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
HABILIDADES TÉCNICAS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

<div id="skillsContainer"></div>

Outras competências:
  • Virtualização (VMware, Hyper-V)
  • Containers (Docker)
  • Git & GitHub
  • Troubleshooting avançado

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━`,

  experiencia: `
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
EXPERIÊNCIA PROFISSIONAL
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

📍 Analista de Sistemas Senior (2020 - Presente)
• Gerenciamento de infraestrutura de rede
• Implementação de automações
• Administração de servidores Linux/Windows

📍 Analista de Infraestrutura (2018 - 2020)
• Configuração de switches e routers
• Ambientes virtualizados
• Backups automatizados

📍 Técnico de Suporte (2016 - 2018)
• Suporte técnico avançado
• Diagnóstico de falhas
• Manutenção de equipamentos

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━`,

  projetos: `
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
PROJETOS DESTAQUES
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

🚀 Modem VIVO Unlock
Desbloqueio automatizado de configurações do modem Askey
RTF8115VW REV5.

Tecnologias: Node.js, Selenium, PowerShell  
GitHub: github.com/edgardocorrea/modem-vivo

🧹 Limpeza Avançada Windows
Script avançado para limpeza profunda do sistema.

Tecnologias: PowerShell  
GitHub: github.com/edgardocorrea/LimpezaAvancada

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━`,

  contato: `
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
CONTATO
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Email:        edgardo.correa@email.com
Localização:  São Paulo, SP - Brasil
LinkedIn:     linkedin.com/in/edgardocorrea
GitHub:       github.com/edgardocorrea
Site:         edgardocorrea.github.io

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━`,

  baixar: `
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
DOWNLOAD DO CURRÍCULO
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Preparando download...
✓ Currículo atualizado

Clique no link abaixo:
👉 <a href="/assets/files/curriculo-edgardo-correa.pdf" style="color:#00ffff" download>Baixar PDF</a>

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━`,

  apagar: "CLEAR_SCREEN"
};

/* ==================== HABILIDADES COM BARRA ==================== */
const skills = [
  { name: 'Redes (TCP/IP, VLANs)', level: 90 },
  { name: 'Linux (Ubuntu, CentOS)', level: 95 },
  { name: 'Windows Server', level: 85 },
  { name: 'PowerShell', level: 90 },
  { name: 'Bash Scripting', level: 85 },
  { name: 'VMware / Hyper-V', level: 80 },
  { name: 'Docker', level: 75 },
  { name: 'Automação', level: 88 },
  { name: 'Segurança', level: 82 },
  { name: 'Troubleshooting', level: 92 }
];

/* ==================== EXECUTAR COMANDO ==================== */
function executeCommand(cmd) {
  cmd = cmd.toLowerCase().trim();

  addLine(`edgardo@carreira:~$ ${cmd}`);

  if (cmd === "apagar") {
    terminalOutput.innerHTML = "";
    return;
  }

  if (cmd === "habilidades") {
    addLine(commands[cmd]);
    setTimeout(() => renderSkills(), 100);
    return;
  }

  if (commands[cmd]) {
    addLine(commands[cmd]);
  } else if (cmd !== "") {
    addLine(`bash: ${cmd}: comando não encontrado`);
    addLine(`Digite "ajuda" para ver os comandos.`);
  }
}

function addLine(content) {
  const line = document.createElement("div");
  line.className = "terminal-line";
  line.innerHTML = content;
  terminalOutput.appendChild(line);
  terminalOutput.scrollTop = terminalOutput.scrollHeight;
}

function renderSkills() {
  const container = document.getElementById("skillsContainer");
  if (!container) return;

  container.innerHTML = "";
  skills.forEach((s, i) => {
    setTimeout(() => {
      container.innerHTML += `
        <div class="skill-bar">
          <span class="skill-name">${s.name}</span>
          <div class="skill-progress">
            <div class="skill-fill" style="width:${s.level}%">${s.level}%</div>
          </div>
        </div>`;
    }, i * 100);
  });
}

commandInput.addEventListener("keypress", (e) => {
  if (e.key === "Enter") {
    executeCommand(commandInput.value);
    commandInput.value = "";
  }
});

/* AUTOEXECUTAR "quem" AO INICIAR */
setTimeout(() => executeCommand("quem"), 1500);
</script>
