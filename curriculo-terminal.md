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
  width: 100%;
}

/* ---------------- BACKGROUND ---------------- */
body {
  overflow-x: hidden;
  background: #0a1428 !important;
}

.page__title { display: none; }

/* ---------------- TERMINAL ---------------- */
.terminal-container {
  background: #000814;
  border: 2px solid #00d4ff;
  border-radius: 10px;
  padding: 20px;
  margin-top: 15px;
  width: 95%;
  max-width: 900px;
  box-shadow: 0 0 30px rgba(0, 212, 255, 0.5);
}

/* HEADER */
.terminal-header {
  display: flex;
  gap: 8px;
  padding-bottom: 8px;
  border-bottom: 1px solid #00d4ff;
}

.terminal-button {
  width: 12px;
  height: 12px;
  border-radius: 50%;
}

.btn-close { background: #ff5555; }
.btn-minimize { background: #ffff55; }
.btn-maximize { background: #55ff55; }

.terminal-title {
  color: #00d4ff;
  margin-left: 10px;
  font-size: 12px;
  font-family: "Courier New", monospace;
}

/* OUTPUT */
.terminal-output {
  min-height: 250px;
  color: #00d4ff;
  font-size: 14px;
  white-space: pre;
  font-family: "Courier New", monospace;
}

/* Diminuir espaçamento vertical do ASCII */
.terminal-line {
  opacity: 0;
  animation: fadeIn 0.3s forwards;
  margin-bottom: 2px; /* antes era 10 → reduzido */
}

@keyframes fadeIn {
  to { opacity: 1; }
}

.prompt { color: #00d4ff; font-weight: bold; }
.command { color: #00ffff; }
.output { color: #ffffff; }
.error { color: #ff5555; }
.success { color: #00ff88; }
.warning { color: #ffff55; }

/* INPUT */
.terminal-input-area {
  display: flex;
  align-items: center;
  margin-top: 10px;
  padding-top: 15px;
  border-top: 1px solid #00d4ff;
}

.terminal-input {
  flex: 1;
  background: transparent;
  border: none;
  color: #00d4ff;
  outline: none;
  font-size: 14px;
  font-family: "Courier New", monospace;
}

.cursor {
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

/* -------------------- COMANDOS DISPONÍVEIS EM HORIZONTAL -------------------- */
.command-suggestions {
  margin-top: 15px;
  width: 95%;
  max-width: 900px;
}

.command-list {
  display: flex;
  gap: 10px;
  overflow-x: auto;
  padding: 10px 5px;
  scrollbar-width: thin;
}

.command-item {
  white-space: nowrap;
  padding: 8px 14px;
  background: rgba(0, 212, 255, 0.1);
  border-radius: 5px;
  border: 1px solid #00d4ff;
  color: #00ffff;
  font-family: "Courier New", monospace;
  cursor: pointer;
  transition: 0.2s;
}

.command-item:hover {
  background: rgba(0, 212, 255, 0.25);
  transform: translateY(-2px);
  box-shadow: 0 0 12px rgba(0, 212, 255, 0.5);
}

/* SKILLS */
.skill-bar {
  display: flex;
  align-items: center;
  margin: 5px 0;
}

.skill-name {
  width: 180px;
  color: #00ffff;
}

.skill-progress {
  flex: 1;
  height: 20px;
  background: rgba(0, 212, 255, 0.1);
  border: 1px solid #00d4ff;
  border-radius: 4px;
}

.skill-fill {
  height: 100%;
  background: linear-gradient(90deg, #00d4ff, #00ffff);
  color: #000;
  font-size: 12px;
  display: flex;
  justify-content: flex-end;
  padding-right: 5px;
  border-radius: 4px;
  font-weight: bold;
}

</style>

<!-- ---------------- TERMINAL HTML ---------------- -->
<div class="terminal-container">
  <div class="terminal-header">
    <span class="terminal-button btn-close"></span>
    <span class="terminal-button btn-minimize"></span>
    <span class="terminal-button btn-maximize"></span>
    <span class="terminal-title">edgardo@carreira:~$</span>
  </div>

  <div class="terminal-output" id="terminalOutput">
    <div class="terminal-line"><span class="success">╔══════════════════════════════════════════════════════════════╗</span></div>
    <div class="terminal-line"><span class="success">║  Bem-vindo ao Sistema de Carreira de Edgardo Correa           ║</span></div>
    <div class="terminal-line"><span class="success">║  Analista de Sistemas | Infraestrutura & Automação            ║</span></div>
    <div class="terminal-line"><span class="success">╚══════════════════════════════════════════════════════════════╝</span></div>

    <div class="terminal-line"><span class="output">Digite um comando para começar...</span></div>
  </div>

  <div class="terminal-input-area">
    <span class="prompt">edgardo@carreira:~$</span>
    <input type="text" id="commandInput" class="terminal-input" placeholder="">
    <span class="cursor"></span>
  </div>
</div>

<!-- ---------------- COMANDOS DISPONÍVEIS ---------------- -->
<div class="command-suggestions">
  <div class="command-list">
    <div class="command-item" onclick="executeCommand('quem')">quem</div>
    <div class="command-item" onclick="executeCommand('habilidades')">habilidades</div>
    <div class="command-item" onclick="executeCommand('experiencia')">experiência</div>
    <div class="command-item" onclick="executeCommand('projetos')">projetos</div>
    <div class="command-item" onclick="executeCommand('contato')">contato</div>
    <div class="command-item" onclick="executeCommand('baixar')">baixar</div>
    <div class="command-item" onclick="executeCommand('apagar')">apagar</div>
    <div class="command-item" onclick="executeCommand('ajuda')">ajuda</div>
  </div>
</div>

<script>
/* ---------------- COMANDOS EM PORTUGUÊS ---------------- */
const terminalOutput = document.getElementById("terminalOutput");
const commandInput = document.getElementById("commandInput");

const commands = {
  ajuda: `
Comandos disponíveis:
  quem
  habilidades
  experiencia
  projetos
  contato
  baixar
  apagar
  ajuda`,

  quem: `
Nome:        Edgardo Correa
Cargo:       Analista de Sistemas
Área:        Infraestrutura & Automação
Local:       São Paulo - SP
Experiência: 5+ anos`,

  habilidades: `
HABILIDADES TÉCNICAS
<div id="skillsContainer"></div>`,

  experiencia: `
EXPERIÊNCIA PROFISSIONAL

Analista de Sistemas Senior (2020 - Atual)
• Redes e automação
• Linux e Windows Server`,

  projetos: `
PROJETOS DESTACADOS

• Modem VIVO Unlock
• Limpeza Avançada Windows`,

  contato: `
Email:  edgardo.correa@email.com
GitHub: github.com/edgardocorrea
LinkedIn: linkedin.com/in/edgardocorrea`,

  baixar: `
Baixar currículo PDF:
👉 /assets/files/curriculo-edgardo-correa.pdf`,

  apagar: "CLEAR_SCREEN"
};

/* ---------------- LISTA DAS SKILLS ---------------- */
const skills = [
  { name: "Redes (TCP/IP, VLANs)", level: 90 },
  { name: "Linux", level: 95 },
  { name: "Windows Server", level: 85 },
  { name: "PowerShell", level: 90 },
  { name: "Bash", level: 85 },
  { name: "VMware / Hyper-V", level: 80 },
];

/* ---------------- EXECUTAR COMANDO ---------------- */
function executeCommand(cmd) {
  cmd = cmd.toLowerCase().trim();

  addLine(`edgardo@carreira:~$ ${cmd}`);

  if (cmd === "apagar") {
    terminalOutput.innerHTML = "";
    return;
  }

  if (cmd === "habilidades") {
    addLine(commands[cmd]);
    setTimeout(renderSkills, 100);
    return;
  }

  if (commands[cmd]) addLine(commands[cmd]);
  else addLine(`Comando não encontrado. Digite "ajuda".`);

  terminalOutput.scrollTop = terminalOutput.scrollHeight;
}

function addLine(text) {
  const div = document.createElement("div");
  div.className = "terminal-line";
  div.textContent = text;
  terminalOutput.appendChild(div);
}

/* ---------------- RENDER SKILLS ---------------- */
function renderSkills() {
  const container = document.getElementById("skillsContainer");
  if (!container) return;

  skills.forEach(s => {
    container.innerHTML += `
      <div class="skill-bar">
        <span class="skill-name">${s.name}</span>
        <div class="skill-progress">
          <div class="skill-fill" style="width:${s.level}%">${s.level}%</div>
        </div>
      </div>`;
  });
}

/* ---------------- ENTER PARA ENVIAR ---------------- */
commandInput.addEventListener("keypress", e => {
  if (e.key === "Enter") {
    executeCommand(commandInput.value);
    commandInput.value = "";
  }
});
</script>
