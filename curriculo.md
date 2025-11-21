---
title: "Currículo On-Line"
layout: single
permalink: /curriculo/
classes: wide
author_profile: false
---

<style>
/* Estilos Globais e de Layout */
body {
  overflow-x: hidden;
}

.page,
.page__content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  width: 100%;
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

/* Título com efeito neon azul */
.page__title {
  display: block;
  color: #00d4ff;
  font-family: 'Courier New', monospace;
  font-size: 2.5rem;
  font-weight: bold;
  text-align: center;
  margin-bottom: 20px;
  animation: neon-flicker 1.5s infinite alternate;
}

@keyframes neon-flicker {
  from {
    text-shadow: 0 0 10px #00d4ff, 0 0 20px #00d4ff, 0 0 30px #00d4ff, 0 0 40px #00a8cc;
  }
  to {
    text-shadow: 0 0 5px #00d4ff, 0 0 10px #00d4ff, 0 0 15px #00d4ff, 0 0 20px #00a8cc;
  }
}

/* Container do Terminal */
.terminal-container {
  background: #000814;
  border: 2px solid #ffffff;
  border-radius: 8px;
  padding: 20px;
  margin: 10px auto 8px auto; /* ALTERADO: Adicionado margin-bottom: 8px para espaçar */
  max-width: 95vw; /* Largura máxima de 95% da tela */
  width: 100%;
  box-shadow: 0 0 30px rgba(0, 212, 255, 0.5);
  position: relative;
}

/* Cabeçalho do Terminal */
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

/* Saída do Terminal */
.terminal-output {
  min-height: 300px; /* ALTERADO: Reduzido de 400px para 300px */
  color: #ffffff;
  font-size: 14px;
  line-height: 1.6;
  white-space: pre-wrap;
  font-family: 'Courier New', monospace;
}

.terminal-line {
  margin-bottom: 2px;
  opacity: 0;
  animation: fadeIn 0.3s forwards;
}

@keyframes fadeIn {
  to { opacity: 1; }
}

/* Estilos de Texto do Terminal */
.prompt { color: #ffffff; font-weight: bold; }
.command { color: #ffffff; }
.output { color: #ffffff; }
.outputw { color: #00FF00; }
.error { color: #ff5555; }
.success { color: #ffffff; }
.warning { color: #ffff55; }

/* Área de Input do Terminal */
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

/* Sugestões de Comandos */
.command-suggestions {
  background: rgba(0, 212, 255, 0.05);
  border: 1px solid #ffffff;
  border-radius: 4px;
  padding: 8px; /* ALTERADO: Padding reduzido para 8px */
  margin: 0 auto 10px auto; /* ALTERADO: Margin-top 0 para colar no terminal, max-width para alinhar */
  max-width: 95vw; /* ALTERADO: Mesma largura máxima do terminal para alinhamento perfeito */
  width: 100%;
  box-sizing: border-box; /* Garante que o padding não aumente a largura total */
}

.command-suggestions h3 {
  color: #ffffff;
  margin-bottom: 6px; /* ALTERADO: Margin-bottom reduzido */
  font-size: 16px; /* ALTERADO: Tamanho do título reduzido */
  font-weight: 700;
  text-shadow: 0 0 10px rgba(255, 255, 255, 0.8);
}

.command-list {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 6px; /* ALTERADO: Espaço entre os botões reduzido */
}

.command-item {
  color: #00ffff;
  padding: 4px 6px; /* ALTERADO: Padding dos botões reduzido para mais compactação */
  background: rgba(0, 212, 255, 0.1);
  border-radius: 4px;
  cursor: pointer;
  transition: all 0.3s;
  border: 1px solid transparent;
  font-family: 'Courier New', monospace;
  font-size: 12px; /* ALTERADO: Fonte dos botões reduzida */
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

/* Barra de Habilidades */
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

/* Responsividade */
@media (max-width: 768px) {
  .terminal-container {
    margin: 10px;
    padding: 15px;
  }
  .terminal-output { font-size: 12px; }
  .command-list { grid-template-columns: repeat(2, 1fr); } /* Em telas menores, 2 colunas */
  .skill-name { width: 120px; font-size: 12px; }
}

@media (max-width: 480px) {
  .command-item { font-size: 12px; padding: 6px; }
}
</style>

<!-- Terminal Interativo -->
<div class="terminal-container">
  <div class="terminal-header">
    <span class="terminal-button btn-close"></span>
    <span class="terminal-button btn-minimize"></span>
    <span class="terminal-button btn-maximize"></span>
    <span class="terminal-title">edgardo@lnx:~$ </span>
  </div>
  <div class="terminal-output" id="terminalOutput"></div>
  <div class="terminal-input-area">
    <span class="prompt">edgardo@lnx:~$</span>
    <input type="text" class="terminal-input" id="commandInput" placeholder="Digite um comando... (na dúvida, digite 'ajuda')" autofocus>
    <span class="cursor"></span>
  </div>
</div>

<!-- Sugestões de Comandos -->
<div class="command-suggestions">
  <h3>⚡ Comandos disponíveis:</h3>
  <div class="command-list">
    <div class="command-item" onclick="processCommand('quem')">👤 quem</div>
    <div class="command-item" onclick="processCommand('habilidades')">🖥️ habilidades</div>
    <div class="command-item" onclick="processCommand('experiencia')">📊 experiência</div>
    <div class="command-item" onclick="processCommand('projetos')">📘 projetos</div>
    <div class="command-item" onclick="processCommand('contato')">📧 contato</div>
    <div class="command-item" onclick="processCommand('baixar')">⬇️ baixar</div>
    <div class="command-item" onclick="processCommand('apagar')">🗑️ apagar</div>
    <div class="command-item" onclick="processCommand('ajuda')">❓ ajuda</div>
  </div>
</div>

<script>
/* Variáveis Globais */
const terminalOutput = document.getElementById("terminalOutput");
const commandInput = document.getElementById("commandInput");

/* Banco de Respostas dos Comandos */
const commandResponses = {
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
  • Virtualização (VMware)
  • Containers (Docker)
  • Git & GitHub
  • Troubleshooting avançado

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━`,

  experiencia: `
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
EXPERIÊNCIA PROFISSIONAL (RESUMO TÉCNICO)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

📍 Analista de Suporte Técnico
• Atendimento a usuários via telefone, chat e acesso remoto
• Solução de incidentes em Windows, redes e aplicativos corporativos
• Acompanhamento e registro de chamados em sistema ERP(AICS)

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

📘 Modem VIVO Configuração avançada
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

<a href="https://www.linkedin.com/in/edgardocorrea/"
   target="_blank"
   style="
      display:inline-flex;
      align-items:center;
      gap:6px;
      padding:6px 10px;
      background:#0A66C2;
      color:white;
      border-radius:5px;
      font-size:14px;
      font-weight:600;
      text-decoration:none;
      font-family:Arial, sans-serif;
   "
>
   <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="white" viewBox="0 0 24 24">
      <path d="M4.98 3.5C4.98 4.88 3.86 6 2.5 6S0 4.88 0 3.5 1.12 1 2.5 1 4.98 2.12 4.98 3.5zM.22 8.47h4.55V24H.22V8.47zM8.54 8.47h4.36v2.11h.06c.61-1.15 2.11-2.36 4.34-2.36 4.64 0 5.5 3.05 5.5 7.02V24h-4.55v-7.77c0-1.85-.03-4.23-2.58-4.23-2.58 0-2.97 2.01-2.97 4.09V24H8.54V8.47z"/>
   </svg>
   Ver Currículo
</a>

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━`,

  apagar: "CLEAR_SCREEN"
};

/* Dados das Habilidades */
const skillsData = [
  { name: 'Redes (TCP/IP, VLANs)', level: 80 },
  { name: 'Linux (Ubuntu, Slackware)', level: 65 },
  { name: 'Windows Server', level: 75 },
  { name: 'PowerShell', level: 81 },
  { name: 'Bash Scripting', level: 85 },
  { name: 'VMware', level: 60 },
  { name: 'Docker', level: 75 },
  { name: 'Automação', level: 88 },
  { name: 'Segurança', level: 72 },
  { name: 'Troubleshooting', level: 92 }
];

/* Funções Principais */

/**
 * Exibe a mensagem de boas-vindas ao carregar a página.
 */
function displayWelcomeMessage() {
  terminalOutput.innerHTML = "";
  addLine(`<span class="outputw">╔══════════════════════════════════════════════════════════════╗</span>`);
  addLine(`<span class="outputw">║  Bem-vindo ao Sistema de Informação de Edgardo Correa        ║</span>`);
  addLine(`<span class="outputw">║  Analista de Sistemas | Currículo On-Line versão 1.3b        ║</span>`);
  addLine(`<span class="outputw">╚══════════════════════════════════════════════════════════════╝</span>`);
  addLine(`<span class="output">Sistema inicializado...</span>`);
  addLine(`<span class="output">Digite um comando ou clique em um comando disponível abaixo ↓</span>`);
}

/**
 * Processa o comando digitado pelo usuário e exibe a resposta.
 * @param {string} cmd - O comando a ser processado.
 */
function processCommand(cmd) {
  cmd = cmd.toLowerCase().trim();

  if (cmd === "apagar") {
    displayWelcomeMessage();
    commandInput.value = "";
    return;
  }

  terminalOutput.innerHTML = '';
  addLine(`edgardo@lnx:~$ ${cmd}`);

  if (cmd === "habilidades") {
    addLine(commandResponses[cmd]);
    setTimeout(() => renderSkillsBars(), 100);
  } else if (commandResponses[cmd]) {
    addLine(commandResponses[cmd]);
  } else if (cmd !== "") {
    addLine(`<span class="error">bash: ${cmd}: comando não encontrado</span>`);
    addLine(`<span class="warning">Digite "ajuda" para ver os comandos.</span>`);
  }

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
 * Renderiza as barras de progresso das habilidades com animação.
 */
function renderSkillsBars() {
  const container = document.getElementById("skillsContainer");
  if (!container) return;

  container.innerHTML = "";
  const fragment = document.createDocumentFragment();
  
  skillsData.forEach((skill, index) => {
    const skillBar = document.createElement("div");
    skillBar.className = "skill-bar";
    
    const skillName = document.createElement("span");
    skillName.className = "skill-name";
    skillName.textContent = skill.name;
    
    const skillProgress = document.createElement("div");
    skillProgress.className = "skill-progress";
    
    const skillFill = document.createElement("div");
    skillFill.className = "skill-fill";
    skillFill.style.width = "0%";
    skillFill.textContent = `${skill.level}%`;
    
    skillProgress.appendChild(skillFill);
    skillBar.appendChild(skillName);
    skillBar.appendChild(skillProgress);
    fragment.appendChild(skillBar);
    
    setTimeout(() => {
      skillFill.style.width = `${skill.level}%`;
    }, 100 * index);
  });
  
  container.appendChild(fragment);
}

/* Event Listeners */
commandInput.addEventListener("keypress", (e) => {
  if (e.key === "Enter") {
    processCommand(commandInput.value);
  }
});

document.addEventListener("DOMContentLoaded", function() {
  displayWelcomeMessage();
});
</script>
