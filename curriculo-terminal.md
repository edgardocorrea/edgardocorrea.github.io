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
}

.initial-content {
  position: relative;
  background: rgba(10,20,40,0.85);
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
  border: 2px solid #ffffff;
  border-radius: 8px;
  padding: 20px;
  margin: 20px auto;
  max-width: 900px;
  width: 100%;
  box-shadow: 0 0 30px rgba(0, 212, 255, 0.5);
  position: relative;
}

/* HEADER */
.terminal-header {
  display: flex;
  gap: 8px;
  padding-bottom: 8px;
  border-bottom: 1px solid #ffffff;
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
  color: #ffffff;
  margin-left: 10px;
  font-size: 12px;
  font-family: 'Courier New', monospace;
}

/* Terminal Output */
.terminal-output {
  min-height: 400px;
  color: #ffffff;
  font-size: 14px;
  line-height: 1.6;
  white-space: pre-wrap; /* Mantém a formatação da arte ASCII */
  font-family: 'Courier New', monospace;
}

.terminal-line {
  margin-bottom: 2px;
  opacity: 0;
  animation: fadeIn 0.3s forwards;
  letter-spacing: 0; /* Garante espaçamento consistente */
}

.success, .output, .command, .error, .warning {
  display: inline-block; /* Ajuda a manter o espaçamento consistente */
}

@keyframes fadeIn {
  to { opacity: 1; }
}

.prompt {
  color: #ffffff;
  font-weight: bold;
}

.command {
  color: #ffffff;
}

.output {
  color: #ffffff;
}

.outputw {
  color: #00FF00;
}

.error {
  color: #ff5555;
}

.success {
  color: #ffffff; /* Alterado de verde para branco */
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
  border-top: 1px solid #ffffff;
}

.terminal-input {
  background: transparent;
  border: 1px solid #ffffff;
  border-radius: 4px;
  padding: 5px;
  color: #ffffff;
  font-family: 'Courier New', monospace;
  font-size: 14px;
  flex: 1;
  outline: none;
  caret-color: #ffffff;
  box-shadow: 0 0 5px #ffffff, 0 0 10px #ffffff;
}

.cursor {
  display: inline-block;
  width: 8px;
  height: 16px;
  background: #ffffff;
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
  border: 1px solid #ffffff;
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
  grid-template-columns: repeat(4, 1fr);
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
  text-align: center;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

.command-item:hover {
  background: rgba(0, 212, 255, 0.2);
  transform: translateX(5px);
  border-color: #ffffff;
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
  color: #ffffff;
  font-family: 'Courier New', monospace;
}

.skill-progress {
  flex: 1;
  height: 22px;
  background: rgba(0, 212, 255, 0.1);
  border: 1px solid #ffffff;
  border-radius: 4px;
  overflow: hidden;
  position: relative;
}

.skill-fill {
  height: 100%;
  background: linear-gradient(90deg, #0a4c82, #0099ff);
  transition: width 1s ease;
  display: flex;
  align-items: center;
  justify-content: flex-end;
  padding-right: 8px;
  color: #ffffff;
  font-weight: bold;
  font-size: 12px;
  box-shadow: 0 0 15px rgba(0, 123, 255, 0.8);
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
    grid-template-columns: repeat(2, 1fr);
  }

  .skill-name {
    width: 120px;
    font-size: 12px;
  }
}

@media (max-width: 480px) {
  .command-item {
    font-size: 12px;
    padding: 6px;
  }
}
</style>

<!-- ==================== TERMINAL ==================== -->
<div class="terminal-container">
  <div class="terminal-header">
    <span class="terminal-button btn-close"></span>
    <span class="terminal-button btn-minimize"></span>
    <span class="terminal-button btn-maximize"></span>
    <span class="terminal-title">edgardo@lnx:~$</span>
  </div>

  <!-- IMPORTANTE: Deixe este div vazio. O JavaScript vai preenchê-lo. -->
  <div class="terminal-output" id="terminalOutput"></div>

  <div class="terminal-input-area">
    <span class="prompt">edgardo@lnx:~$</span>
    <input type="text" class="terminal-input" id="commandInput" placeholder="Digite um comando aqui...na duvida digite ajuda..." autofocus>
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
/* ==================== VARIÁVEIS GLOBAIS ==================== */
const terminalOutput = document.getElementById("terminalOutput");
const commandInput = document.getElementById("commandInput");

/* ==================== BANCO DE COMANDOS ==================== */
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
EXPERIÊNCIA PROFISSIONAL (RESUMO)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

📍 Analista de Suporte Técnico
• Atendimento a usuários via telefone, chat e acesso remoto
• Solução de incidentes em Windows, redes e aplicativos corporativos
• Acompanhamento e registro de chamados em sistema ITSM

📍 Assistente de Infraestrutura de TI
• Suporte em Active Directory, permissões e políticas de acesso
• Configuração básica de VPN, redes e equipamentos de conectividade
• Apoio na manutenção de servidores e monitoramento de ambientes

📍 Técnico de Service Desk
• Diagnóstico e resolução de problemas técnicos de primeira e segunda camada
• Orientação ao usuário e suporte ao uso de sistemas internos
• Instalação, manutenção e atualização de estações de trabalho e softwares

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━`,

  projetos: `
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
PROJETOS DESTAQUES
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

🚀 Modem VIVO Configuração avançada
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

Email:        edgardo.edyone-1@yahoo.com
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

/* ==================== DADOS DAS HABILIDADES ==================== */
const skills = [
  { name: 'Redes (TCP/IP, VLANs)', level: 80 },
  { name: 'Linux (Ubuntu, Slackware)', level: 65 },
  { name: 'Windows Server', level: 75 },
  { name: 'PowerShell', level: 81 },
  { name: 'Bash Scripting', level: 85 },
  { name: 'VMware / Hyper-V', level: 60 },
  { name: 'Docker', level: 75 },
  { name: 'Automação', level: 88 },
  { name: 'Segurança', level: 72 },
  { name: 'Troubleshooting', level: 92 }
];

/* ==================== FUNÇÕES PRINCIPAIS ==================== */

/**
 * Exibe a mensagem de boas-vindas no terminal.
 */
function showWelcomeMessage() {
  terminalOutput.innerHTML = ""; // Limpa o terminal antes de exibir
  addLine(`<span class="outputw">╔══════════════════════════════════════════════════════════════╗</span>`);
  addLine(`<span class="outputw">║  Bem-vindo ao Sistema de Informação de Edgardo Correa        ║</span>`);
  addLine(`<span class="outputw">║  Analista de Sistemas | Curriculo On-Line versão 1.3b        ║</span>`);
  addLine(`<span class="outputw">╚══════════════════════════════════════════════════════════════╝</span>`);
  addLine(`<span class="output">Sistema inicializado...</span>`);
  addLine(`<span class="output">Digite um comando ou clique em uma sugestão abaixo ↓</span>`);
}

/**
 * Executa o comando digitado pelo usuário.
 * @param {string} cmd - O comando a ser executado.
 */
function executeCommand(cmd) {
  cmd = cmd.toLowerCase().trim();

  // Se o comando for 'apagar', apenas mostra a mensagem de boas-vindas.
  if (cmd === "apagar") {
    showWelcomeMessage();
    commandInput.value = "";
    return;
  }

  // Para qualquer outro comando, limpa a tela primeiro.
  terminalOutput.innerHTML = '';

  // Exibe o comando que foi digitado.
  addLine(`edgardo@lnx:~$ ${cmd}`);

  // Processa e exibe o resultado do comando.
  if (cmd === "habilidades") {
    addLine(commands[cmd]);
    setTimeout(() => renderSkills(), 100);
  } else if (commands[cmd]) {
    addLine(commands[cmd]);
  } else if (cmd !== "") {
    addLine(`<span class="error">bash: ${cmd}: comando não encontrado</span>`);
    addLine(`<span class="warning">Digite "ajuda" para ver os comandos.</span>`);
  }

  // Limpa o campo de input para o próximo comando.
  commandInput.value = "";
}

/**
 * Adiciona uma linha de texto ao terminal.
 * @param {string} content - O conteúdo HTML da linha.
 */
function addLine(content) {
  const line = document.createElement("div");
  line.className = "terminal-line";
  line.innerHTML = content;
  terminalOutput.appendChild(line);
  terminalOutput.scrollTop = terminalOutput.scrollHeight;
}

/**
 * Renderiza as barras de habilidades com animação.
 */
function renderSkills() {
  const container = document.getElementById("skillsContainer");
  if (!container) return;

  container.innerHTML = "";
  
  // Cria um fragmento de documento para melhorar o desempenho
  const fragment = document.createDocumentFragment();
  
  skills.forEach((skill, index) => {
    // Cria a barra de habilidades
    const skillBar = document.createElement("div");
    skillBar.className = "skill-bar";
    
    // Cria o nome da habilidade
    const skillName = document.createElement("span");
    skillName.className = "skill-name";
    skillName.textContent = skill.name;
    
    // Cria o contêiner da barra de progresso
    const skillProgress = document.createElement("div");
    skillProgress.className = "skill-progress";
    
    // Cria a barra de preenchimento
    const skillFill = document.createElement("div");
    skillFill.className = "skill-fill";
    skillFill.style.width = "0%"; // Começa com 0% para a animação
    skillFill.textContent = skill.level + "%"; // Adiciona o texto da porcentagem
    
    // Adiciona a barra de preenchimento ao contêiner
    skillProgress.appendChild(skillFill);
    
    // Adiciona o nome e a barra ao elemento principal
    skillBar.appendChild(skillName);
    skillBar.appendChild(skillProgress);
    
    // Adiciona a barra completa ao fragmento
    fragment.appendChild(skillBar);
    
    // Anima a barra após um pequeno atraso
    setTimeout(() => {
      skillFill.style.width = skill.level + "%";
    }, 100 * index);
  });
  
  // Adiciona todas as barras ao contêiner de uma vez
  container.appendChild(fragment);
}

/* ==================== EVENT LISTENERS ==================== */

// Executa o comando ao pressionar Enter.
commandInput.addEventListener("keypress", (e) => {
  if (e.key === "Enter") {
    executeCommand(commandInput.value);
  }
});

// Inicializa o terminal quando a página carrega.
document.addEventListener("DOMContentLoaded", function() {
  commandInput.placeholder = "Digite um comando aqui...na duvida digite ajuda...";
  showWelcomeMessage();
});
</script>
