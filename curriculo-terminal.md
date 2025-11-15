---
title: "$ whoami"
layout: single
permalink: /curriculo-terminal/
classes: wide
author_profile: false
---

<style>
/* ==================== TERMINAL HACKER STYLE ==================== */
body {
  background: #0a0a0a;
  color: #00ff00;
  font-family: 'Courier New', monospace;
  overflow-x: hidden;
}

.page {
  background: #0a0a0a;
}

.page__content {
  background: #000000;
  padding: 0;
  max-width: 100%;
}

.page__title {
  display: none;
}

/* Terminal Container */
.terminal-container {
  background: #000000;
  border: 2px solid #00ff00;
  border-radius: 8px;
  padding: 20px;
  margin: 20px auto;
  max-width: 1000px;
  box-shadow: 0 0 30px rgba(0, 255, 0, 0.3);
  position: relative;
}

/* Terminal Header */
.terminal-header {
  display: flex;
  gap: 8px;
  margin-bottom: 20px;
  padding-bottom: 10px;
  border-bottom: 1px solid #00ff00;
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

/* Terminal Output */
.terminal-output {
  min-height: 400px;
  color: #00ff00;
  font-size: 14px;
  line-height: 1.6;
  white-space: pre-wrap;
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
  color: #00ff00;
  font-weight: bold;
}

.command {
  color: #00ffff;
}

.output {
  color: #ffffff;
  margin-left: 20px;
}

.error {
  color: #ff5555;
}

.success {
  color: #55ff55;
}

.warning {
  color: #ffff55;
}

/* Input Area */
.terminal-input-area {
  display: flex;
  align-items: center;
  margin-top: 20px;
  padding-top: 20px;
  border-top: 1px solid #00ff00;
}

.terminal-input {
  background: transparent;
  border: none;
  color: #00ff00;
  font-family: 'Courier New', monospace;
  font-size: 14px;
  flex: 1;
  outline: none;
  caret-color: #00ff00;
}

.cursor {
  display: inline-block;
  width: 8px;
  height: 16px;
  background: #00ff00;
  animation: blink 1s infinite;
  margin-left: 2px;
}

@keyframes blink {
  0%, 50% { opacity: 1; }
  51%, 100% { opacity: 0; }
}

/* Command Suggestions */
.command-suggestions {
  background: rgba(0, 255, 0, 0.1);
  border: 1px solid #00ff00;
  border-radius: 4px;
  padding: 15px;
  margin-top: 20px;
  max-width: 1000px;
  margin-left: auto;
  margin-right: auto;
}

.command-suggestions h3 {
  color: #00ff00;
  margin-bottom: 10px;
  font-size: 16px;
}

.command-list {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 10px;
}

.command-item {
  color: #00ffff;
  padding: 8px;
  background: rgba(0, 255, 255, 0.1);
  border-radius: 4px;
  cursor: pointer;
  transition: all 0.3s;
}

.command-item:hover {
  background: rgba(0, 255, 255, 0.2);
  transform: translateX(5px);
}

/* Skills Bar */
.skill-bar {
  display: flex;
  align-items: center;
  margin: 5px 0;
}

.skill-name {
  width: 150px;
  color: #00ffff;
}

.skill-progress {
  flex: 1;
  height: 20px;
  background: rgba(0, 255, 0, 0.1);
  border: 1px solid #00ff00;
  border-radius: 4px;
  overflow: hidden;
  position: relative;
}

.skill-fill {
  height: 100%;
  background: linear-gradient(90deg, #00ff00, #00ffff);
  transition: width 1s ease;
  display: flex;
  align-items: center;
  justify-content: flex-end;
  padding-right: 5px;
  color: #000;
  font-weight: bold;
  font-size: 12px;
}

/* Responsivo */
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
}

/* Matrix Effect Background */
.matrix-bg {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: -1;
  opacity: 0.1;
  pointer-events: none;
}
</style>

<!-- Matrix Background Canvas -->
<canvas class="matrix-bg" id="matrixCanvas"></canvas>

<!-- Terminal Container -->
<div class="terminal-container">
  <div class="terminal-header">
    <span class="terminal-button btn-close"></span>
    <span class="terminal-button btn-minimize"></span>
    <span class="terminal-button btn-maximize"></span>
    <span style="color: #00ff00; margin-left: 10px; font-size: 12px;">edgardo@career:~$</span>
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
      <span class="output">Sistema inicializado com sucesso...</span>
    </div>
    <div class="terminal-line" style="animation-delay: 0.8s;">
      <span class="output">Digite <span class="command">help</span> para ver os comandos disponíveis.</span>
    </div>
    <div class="terminal-line" style="animation-delay: 1s;">
      <span class="output">Ou clique em um comando sugerido abaixo ↓</span>
    </div>
  </div>
  
  <div class="terminal-input-area">
    <span class="prompt">edgardo@career:~$</span>
    <input type="text" class="terminal-input" id="commandInput" placeholder="Digite um comando..." autofocus>
    <span class="cursor"></span>
  </div>
</div>

<!-- Command Suggestions -->
<div class="command-suggestions">
  <h3>⚡ Comandos Rápidos:</h3>
  <div class="command-list">
    <div class="command-item" onclick="executeCommand('whoami')">📋 whoami</div>
    <div class="command-item" onclick="executeCommand('skills')">💻 skills --list</div>
    <div class="command-item" onclick="executeCommand('experience')">📊 experience</div>
    <div class="command-item" onclick="executeCommand('projects')">🚀 projects</div>
    <div class="command-item" onclick="executeCommand('education')">🎓 education</div>
    <div class="command-item" onclick="executeCommand('contact')">📧 contact</div>
    <div class="command-item" onclick="executeCommand('social')">🌐 social</div>
    <div class="command-item" onclick="executeCommand('download')">⬇️  download-cv</div>
  </div>
</div>

<script>
// ==================== MATRIX BACKGROUND ====================
const canvas = document.getElementById('matrixCanvas');
const ctx = canvas.getContext('2d');

canvas.width = window.innerWidth;
canvas.height = window.innerHeight;

const matrix = "ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789@#$%^&*()*&^%";
const fontSize = 10;
const columns = canvas.width / fontSize;
const drops = [];

for (let i = 0; i < columns; i++) {
  drops[i] = 1;
}

function drawMatrix() {
  ctx.fillStyle = 'rgba(0, 0, 0, 0.05)';
  ctx.fillRect(0, 0, canvas.width, canvas.height);
  
  ctx.fillStyle = '#00ff00';
  ctx.font = fontSize + 'px monospace';
  
  for (let i = 0; i < drops.length; i++) {
    const text = matrix[Math.floor(Math.random() * matrix.length)];
    ctx.fillText(text, i * fontSize, drops[i] * fontSize);
    
    if (drops[i] * fontSize > canvas.height && Math.random() > 0.975) {
      drops[i] = 0;
    }
    drops[i]++;
  }
}

setInterval(drawMatrix, 35);

window.addEventListener('resize', () => {
  canvas.width = window.innerWidth;
  canvas.height = window.innerHeight;
});

// ==================== TERMINAL LOGIC ====================
const terminalOutput = document.getElementById('terminalOutput');
const commandInput = document.getElementById('commandInput');

const commands = {
  help: `
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>
<span class="warning">COMANDOS DISPONÍVEIS:</span>
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>

  <span class="command">whoami</span>              Exibe informações pessoais
  <span class="command">skills</span>              Lista todas as habilidades técnicas
  <span class="command">experience</span>          Mostra experiência profissional
  <span class="command">projects</span>            Lista projetos em destaque
  <span class="command">education</span>           Formação acadêmica
  <span class="command">certifications</span>      Certificações obtidas
  <span class="command">contact</span>             Informações de contato
  <span class="command">social</span>              Redes sociais
  <span class="command">download-cv</span>         Baixa currículo em PDF
  <span class="command">clear</span>               Limpa o terminal
  <span class="command">help</span>                Exibe esta mensagem

<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>`,

  whoami: `
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>
<span class="warning">INFORMAÇÕES PESSOAIS</span>
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>

<span class="command">Nome:</span>        Edgardo Correa
<span class="command">Cargo:</span>       Analista de Sistemas
<span class="command">Especialidade:</span> Infraestrutura de TI & Automação
<span class="command">Localização:</span> São Paulo, SP - Brasil
<span class="command">Experiência:</span> 5+ anos

<span class="output">💡 Profissional com foco em infraestrutura de redes, 
   automação de processos e administração de sistemas.
   Apaixonado por transformar desafios técnicos em 
   soluções eficientes e escaláveis.</span>

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
  • Documentação técnica

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
   • Segurança e monitoramento de sistemas

<span class="command">📍 Analista de Infraestrutura</span>
   Período: 2018 - 2020
   • Configuração de switches e routers
   • Gestão de ambientes virtualizados
   • Suporte a servidores e aplicações
   • Implementação de backups automatizados

<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>`,

  projects: `
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>
<span class="warning">PROJETOS EM DESTAQUE</span>
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>

<span class="command">🚀 Modem VIVO Unlock</span>
   Ferramenta de automação para desbloqueio de 
   configurações avançadas do modem Askey RTF8115VW
   
   <span class="output">Tech Stack:</span> Node.js, Selenium WebDriver, PowerShell
   <span class="output">GitHub:</span> github.com/edgardocorrea/modem-vivo

<span class="command">🧹 Limpeza Avançada Windows</span>
   Script automatizado para limpeza profunda do Windows
   
   <span class="output">Tech Stack:</span> PowerShell, Windows API, Batch
   <span class="output">GitHub:</span> github.com/edgardocorrea/LimpezaAvancada

<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>`,

  education: `
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>
<span class="warning">FORMAÇÃO ACADÊMICA</span>
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>

<span class="command">🎓 Bacharelado em Sistemas de Informação</span>
   Instituição: [Nome da Universidade]
   Período: [Ano Início] - [Ano Conclusão]
   
   Principais áreas de estudo:
   • Redes de Computadores
   • Sistemas Operacionais
   • Engenharia de Software
   • Banco de Dados

<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>`,

  certifications: `
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>
<span class="warning">CERTIFICAÇÕES</span>
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>

<span class="command">🏆 Certificações Obtidas:</span>
   • [Nome da Certificação 1]
   • [Nome da Certificação 2]
   • [Nome da Certificação 3]
   
   <span class="output">Credly Profile:</span> credly.com/users/edgardo.correa

<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>`,

  contact: `
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>
<span class="warning">INFORMAÇÕES DE CONTATO</span>
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>

<span class="command">📧 Email:</span>      edgardo.correa@email.com
<span class="command">📍 Localização:</span> São Paulo, SP - Brasil
<span class="command">🌐 Website:</span>    edgardocorrea.github.io

<span class="output">Disponível para oportunidades em:
• Infraestrutura de TI
• Automação de Processos
• Administração de Redes
• Consultoria Técnica</span>

<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>`,

  social: `
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>
<span class="warning">REDES SOCIAIS</span>
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>

<span class="command">💼 LinkedIn:</span>  linkedin.com/in/edgardocorrea
<span class="command">💻 GitHub:</span>    github.com/edgardocorrea
<span class="command">🏆 Credly:</span>    credly.com/users/edgardo.correa

<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>`,

  download: `
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>
<span class="warning">DOWNLOAD DO CURRÍCULO</span>
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>

<span class="output">🔄 Preparando download...</span>
<span class="success">✓ Currículo em formato PDF</span>
<span class="success">✓ Versão atualizada: ${new Date().toLocaleDateString('pt-BR')}</span>

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
  { name: 'Automação', level: 88 }
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
    addLine(`<span class="error">bash: ${cmd}: command not found</span>`);
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
