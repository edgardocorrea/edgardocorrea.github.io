---
title: "$ whoami"
layout: single
permalink: /curriculo-terminal/
classes: wide
author_profile: false
---

<style>
/* ==================== BACKGROUND AZUL ESCURO ==================== */
body {
  background: linear-gradient(135deg, #0a0a0a 0%, #001a33 100%);
  color: #ffffff;
  overflow-x: hidden;
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
  max-width: 1000px;
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
  white-space: pre-wrap;
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
  color: #ffffff; /* FONTE BRANCA NORMAL */
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
  max-width: 1000px;
  margin-left: auto;
  margin-right: auto;
}

.command-suggestions h3 {
  color: #ffffff; /* TÍTULO BRANCO BRILHANTE */
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

/* ==================== RESPONSIVO ==================== */
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
    <span class="terminal-title">edgardo@career:~$</span>
  </div>
  
  <div class="terminal-output" id="terminalOutput">
    <div class="terminal-line" style="animation-delay: 0.1s;">
      <span class="success">╔════════════════════════════════════════════════════════════╗</span>
    </div>
    <div class="terminal-line" style="animation-delay: 0.2s;">
      <span class="success">║  Bem-vindo ao Sistema de Carreira de Edgardo Correa       ║</span>
    </div>
    <div class="terminal-line" style="animation-delay: 0.3s;">
      <span class="success">║  Analista de Sistemas | Infraestrutura & Automação        ║</span>
    </div>
    <div class="terminal-line" style="animation-delay: 0.4s;">
      <span class="success">╚════════════════════════════════════════════════════════════╝</span>
    </div>
    <div class="terminal-line" style="animation-delay: 0.6s;">
      <span class="output">Sistema inicializado...</span>
    </div>
    <div class="terminal-line" style="animation-delay: 0.8s;">
      <span class="output">Digite um comando ou clique nas sugestões ↓</span>
    </div>
  </div>
  
  <div class="terminal-input-area">
    <span class="prompt">edgardo@career:~$</span>
    <input type="text" class="terminal-input" id="commandInput" placeholder="Digite um comando..." autofocus>
    <span class="cursor"></span>
  </div>
</div>

<div class="command-suggestions">
  <h3>⚡ Comandos Disponíveis:</h3>
  <div class="command-list">
    <div class="command-item" onclick="executeCommand('whoami')">📋 whoami</div>
    <div class="command-item" onclick="executeCommand('skills')">💻 skills</div>
    <div class="command-item" onclick="executeCommand('experience')">📊 experience</div>
    <div class="command-item" onclick="executeCommand('projects')">🚀 projects</div>
    <div class="command-item" onclick="executeCommand('contact')">📧 contact</div>
    <div class="command-item" onclick="executeCommand('download')">⬇️ download</div>
    <div class="command-item" onclick="executeCommand('clear')">🗑️ clear</div>
    <div class="command-item" onclick="executeCommand('help')">❓ help</div>
  </div>
</div>

<script>
// ==================== TERMINAL LOGIC ====================
const terminalOutput = document.getElementById('terminalOutput');
const commandInput = document.getElementById('commandInput');

const commands = {
  help: `
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>
<span class="warning">COMANDOS DISPONÍVEIS:</span>
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>

  <span class="command">whoami</span>       Informações pessoais
  <span class="command">skills</span>       Habilidades técnicas
  <span class="command">experience</span>   Experiência profissional
  <span class="command">projects</span>     Projetos em destaque
  <span class="command">contact</span>      Informações de contato
  <span class="command">download</span>     Baixar currículo PDF
  <span class="command">clear</span>        Limpar terminal
  <span class="command">help</span>         Exibir esta mensagem

<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>`,

  whoami: `
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>
<span class="warning">INFORMAÇÕES PESSOAIS</span>
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>

<span class="command">Nome:</span>        Edgardo Correa
<span class="command">Cargo:</span>       Analista de Sistemas
<span class="command">Área:</span>        Infraestrutura & Automação
<span class="command">Local:</span>       São Paulo, SP - Brasil
<span class="command">Experiência:</span> 5+ anos

<span class="output">Profissional com foco em infraestrutura de redes,
automação e administração de sistemas Linux/Windows.</span>

<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>`,

  skills: `
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>
<span class="warning">HABILIDADES TÉCNICAS</span>
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>

<div id="skillsContainer"></div>

<span class="command">📦 Outras Competências:</span>
  • Virtualização (VMware, Hyper-V)
  • Containers (Docker)
  • Git & GitHub
  • Troubleshooting avançado

<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>`,

  experience: `
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>
<span class="warning">EXPERIÊNCIA PROFISSIONAL</span>
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>

<span class="command">📍 Analista de Sistemas Senior</span>
   Período: 2020 - Presente
   • Gerenciamento de infraestrutura de rede
   • Implementação de soluções de automação
   • Administração de servidores Linux/Windows

<span class="command">📍 Analista de Infraestrutura</span>
   Período: 2018 - 2020
   • Configuração de switches e routers
   • Gestão de ambientes virtualizados
   • Implementação de backups automatizados

<span class="command">📍 Técnico de Suporte</span>
   Período: 2016 - 2018
   • Suporte técnico avançado
   • Troubleshooting de problemas complexos
   • Manutenção de equipamentos

<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>`,

  projects: `
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>
<span class="warning">PROJETOS EM DESTAQUE</span>
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>

<span class="command">🚀 Modem VIVO Unlock</span>
   Automação para desbloqueio de configurações
   do modem Askey RTF8115VW REV5
   
   <span class="output">Tech:</span> Node.js, Selenium, PowerShell
   <span class="output">GitHub:</span> github.com/edgardocorrea/modem-vivo

<span class="command">🧹 Limpeza Avançada Windows</span>
   Script automatizado para limpeza profunda
   
   <span class="output">Tech:</span> PowerShell, Windows API
   <span class="output">GitHub:</span> github.com/edgardocorrea/LimpezaAvancada

<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>`,

  contact: `
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>
<span class="warning">INFORMAÇÕES DE CONTATO</span>
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>

<span class="command">📧 Email:</span>      edgardo.correa@email.com
<span class="command">📍 Localização:</span> São Paulo, SP - Brasil
<span class="command">💼 LinkedIn:</span>   linkedin.com/in/edgardocorrea
<span class="command">💻 GitHub:</span>     github.com/edgardocorrea
<span class="command">🌐 Website:</span>    edgardocorrea.github.io

<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>`,

  download: `
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>
<span class="warning">DOWNLOAD DO CURRÍCULO</span>
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>

<span class="output">🔄 Preparando download...</span>
<span class="success">✓ Currículo em formato PDF</span>
<span class="success">✓ Versão atualizada</span>

<span class="command">📥 Clique no link abaixo:</span>
   <a href="/assets/files/curriculo-edgardo-correa.pdf" style="color: #00ffff;" download>
     → Baixar Currículo PDF
   </a>

<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>`,

  clear: 'CLEAR_SCREEN'
};

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

function executeCommand(cmd) {
  cmd = cmd.toLowerCase().trim();
  
  // Add command to output
  addLine(`<span class="prompt">edgardo@career:~$</span> <span class="command">${cmd}</span>`);
  
  if (cmd === 'clear') {
    terminalOutput.innerHTML = '';
    return;
  }
  
  if (cmd === 'skills' || cmd === 'skills --list') {
    addLine(commands.skills);
    setTimeout(() => renderSkills(), 100);
    return;
  }
  
  if (commands[cmd]) {
    addLine(commands[cmd]);
  } else if (cmd === '') {
    // Do nothing
  } else {
    addLine(`<span class="error">bash: ${cmd}: comando não encontrado</span>`);
    addLine(`<span class="output">Digite <span class="command">help</span> para ver os comandos disponíveis.</span>`);
  }
  
  // Scroll to bottom
  terminalOutput.scrollTop = terminalOutput.scrollHeight;
}

function addLine(content) {
  const line = document.createElement('div');
  line.className = 'terminal-line';
  line.innerHTML = content;
  terminalOutput.appendChild(line);
}

function renderSkills() {
  const container = document.getElementById('skillsContainer');
  if (!container) return;
  
  container.innerHTML = '';
  skills.forEach((skill, index) => {
    setTimeout(() => {
      const skillHtml = `
        <div class="skill-bar">
          <span class="skill-name">${skill.name}</span>
          <div class="skill-progress">
            <div class="skill-fill" style="width: ${skill.level}%">${skill.level}%</div>
          </div>
        </div>
      `;
      container.innerHTML += skillHtml;
    }, index * 100);
  });
}

// Handle Enter key
commandInput.addEventListener('keypress', (e) => {
  if (e.key === 'Enter') {
    const cmd = commandInput.value;
    executeCommand(cmd);
    commandInput.value = '';
  }
});

// Auto-execute whoami on load
setTimeout(() => {
  executeCommand('whoami');
}, 1500);
</script>
