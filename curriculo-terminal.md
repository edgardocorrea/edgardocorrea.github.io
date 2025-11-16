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
  padding: 0;
  max-width: 100%;
}

.page__title {
  display: none;
}

/* ==================== TERMINAL SECTION ==================== */
.terminal-section {
  background: #001a33;
  padding: 40px 20px;
  position: relative;
}

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
  margin: 5px 0;
}

.skill-name {
  width: 150px;
  color: #00ffff;
}

.skill-progress {
  flex: 1;
  height: 20px;
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
  padding-right: 5px;
  color: #000;
  font-weight: bold;
  font-size: 12px;
  box-shadow: 0 0 15px rgba(0, 212, 255, 0.8);
}

/* ==================== TIMELINE SECTION ==================== */
.timeline-section {
  background: #001a33;
  padding: 80px 20px;
  position: relative;
}

.timeline-title {
  text-align: center;
  font-size: 48px;
  color: #ffffff; /* TÍTULO BRANCO BRILHANTE */
  margin-bottom: 20px;
  font-weight: 700;
  text-shadow: 0 0 20px rgba(255, 255, 255, 0.9);
}

.timeline-subtitle {
  text-align: center;
  font-size: 20px;
  color: #ffffff; /* BRANCO NORMAL */
  margin-bottom: 60px;
}

/* Timeline 3D */
.timeline-3d {
  position: relative;
  padding: 40px 0;
  max-width: 1200px;
  margin: 0 auto;
}

.timeline-3d::before {
  content: "";
  position: absolute;
  left: 50%;
  top: 0;
  bottom: 0;
  width: 4px;
  background: linear-gradient(180deg, transparent, #00d4ff 10%, #00d4ff 90%, transparent);
  transform: translateX(-50%);
  box-shadow: 0 0 20px rgba(0, 212, 255, 0.8);
}

.timeline-item-3d {
  position: relative;
  margin-bottom: 80px;
  display: flex;
  align-items: center;
  opacity: 0;
  transform: translateY(50px);
  animation: slideUp 0.8s forwards;
}

@keyframes slideUp {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.timeline-item-3d:nth-child(1) { animation-delay: 0.2s; }
.timeline-item-3d:nth-child(2) { animation-delay: 0.4s; }
.timeline-item-3d:nth-child(3) { animation-delay: 0.6s; }
.timeline-item-3d:nth-child(4) { animation-delay: 0.8s; }

.timeline-item-3d.left {
  justify-content: flex-end;
  padding-right: calc(50% + 50px);
}

.timeline-item-3d.right {
  justify-content: flex-start;
  padding-left: calc(50% + 50px);
}

/* Card 3D */
.timeline-card-3d {
  background: linear-gradient(145deg, #001428, #000814);
  border: 2px solid #00d4ff;
  border-radius: 15px;
  padding: 30px;
  max-width: 450px;
  position: relative;
  transition: all 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  transform-style: preserve-3d;
  box-shadow: 0 10px 40px rgba(0, 0, 0, 0.8), 0 0 30px rgba(0, 212, 255, 0.3);
  cursor: pointer;
}

.timeline-card-3d:hover {
  transform: rotateY(10deg) scale(1.05);
  border-color: #00ffff;
  box-shadow: 0 20px 60px rgba(0, 212, 255, 0.6);
}

.timeline-item-3d.left .timeline-card-3d:hover {
  transform: rotateY(-10deg) scale(1.05);
}

.timeline-date-badge {
  position: absolute;
  top: -15px;
  left: 30px;
  background: linear-gradient(135deg, #00d4ff, #0088cc);
  color: #000000;
  padding: 8px 20px;
  border-radius: 20px;
  font-size: 14px;
  font-weight: 700;
  box-shadow: 0 5px 15px rgba(0, 212, 255, 0.6);
  z-index: 1;
}

.timeline-card-icon {
  font-size: 48px;
  margin-bottom: 15px;
  display: inline-block;
  filter: drop-shadow(0 0 10px rgba(0, 212, 255, 0.8));
}

.timeline-card-title {
  font-size: 24px;
  font-weight: 700;
  color: #ffffff; /* TÍTULO BRANCO BRILHANTE */
  margin: 0 0 10px 0;
  text-shadow: 0 0 10px rgba(255, 255, 255, 0.8);
}

.timeline-card-company {
  font-size: 16px;
  color: #00d4ff;
  margin: 0 0 15px 0;
  font-weight: 600;
}

.timeline-card-description {
  font-size: 15px;
  color: #ffffff; /* FONTE BRANCA NORMAL */
  line-height: 1.7;
  margin-bottom: 20px;
}

.timeline-card-skills {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin-top: 15px;
}

.skill-tag-3d {
  background: rgba(0, 212, 255, 0.1);
  border: 1px solid #00d4ff;
  color: #00ffff;
  padding: 6px 12px;
  border-radius: 15px;
  font-size: 12px;
  font-weight: 600;
  transition: all 0.3s ease;
}

.skill-tag-3d:hover {
  background: rgba(0, 212, 255, 0.3);
  transform: scale(1.1);
  box-shadow: 0 0 15px rgba(0, 212, 255, 0.8);
}

.timeline-dot {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  width: 24px;
  height: 24px;
  background: #00d4ff;
  border: 4px solid #001a33;
  border-radius: 50%;
  box-shadow: 0 0 30px rgba(0, 212, 255, 1);
  z-index: 10;
  animation: pulse 2s infinite;
}

@keyframes pulse {
  0%, 100% {
    transform: translate(-50%, -50%) scale(1);
    box-shadow: 0 0 30px rgba(0, 212, 255, 1);
  }
  50% {
    transform: translate(-50%, -50%) scale(1.3);
    box-shadow: 0 0 50px rgba(0, 212, 255, 1);
  }
}

/* ==================== DOWNLOAD SECTION ==================== */
.download-section {
  text-align: center;
  margin: 60px auto;
  padding: 40px;
  max-width: 1000px;
  background: linear-gradient(145deg, #001428, #000814);
  border: 2px solid #00d4ff;
  border-radius: 20px;
  box-shadow: 0 0 40px rgba(0, 212, 255, 0.4);
}

.download-section h3 {
  color: #ffffff; /* TÍTULO BRANCO BRILHANTE */
  font-size: 32px;
  margin-bottom: 15px;
  font-weight: 700;
  text-shadow: 0 0 15px rgba(255, 255, 255, 0.9);
}

.download-section p {
  color: #ffffff; /* BRANCO NORMAL */
  font-size: 18px;
  margin-bottom: 30px;
}

.download-btn {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  padding: 15px 40px;
  background: linear-gradient(135deg, #00d4ff, #0088cc);
  border: 2px solid #00d4ff;
  border-radius: 30px;
  color: #000000;
  font-size: 18px;
  font-weight: 700;
  text-decoration: none;
  transition: all 0.3s ease;
  box-shadow: 0 5px 30px rgba(0, 212, 255, 0.5);
}

.download-btn:hover {
  transform: translateY(-5px) scale(1.05);
  box-shadow: 0 10px 50px rgba(0, 212, 255, 0.8);
  color: #000000;
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
  
  .timeline-3d::before {
    left: 20px;
  }
  
  .timeline-item-3d.left,
  .timeline-item-3d.right {
    justify-content: flex-start;
    padding-left: 60px;
    padding-right: 20px;
  }
  
  .timeline-dot {
    left: 20px;
  }
  
  .timeline-card-3d:hover {
    transform: scale(1.02);
  }
  
  .timeline-item-3d.left .timeline-card-3d:hover {
    transform: scale(1.02);
  }
  
  .timeline-title {
    font-size: 36px;
  }
}

@media (max-width: 480px) {
  .timeline-title {
    font-size: 28px;
  }
  
  .timeline-card-3d {
    padding: 20px;
  }
}
</style>

<!-- ==================== TERMINAL SECTION ==================== -->
<div class="terminal-section">
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
        <span class="output">Sistema inicializado com sucesso...</span>
      </div>
      <div class="terminal-line" style="animation-delay: 0.8s;">
        <span class="output">Digite um comando ou clique nas sugestões abaixo ↓</span>
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
</div>

<!-- ==================== TIMELINE SECTION ==================== -->
<div class="timeline-section">
  <h2 class="timeline-title">Minha Jornada Profissional</h2>
  <p class="timeline-subtitle">🚀 Uma trajetória de evolução contínua em tecnologia</p>
  
  <div class="timeline-3d">
    
    <div class="timeline-item-3d right">
      <div class="timeline-card-3d">
        <div class="timeline-date-badge">2020 - Presente</div>
        <div class="timeline-card-icon">💼</div>
        <h3 class="timeline-card-title">Analista de Sistemas Senior</h3>
        <p class="timeline-card-company">Empresa Atual</p>
        <p class="timeline-card-description">
          Liderança técnica em projetos de infraestrutura, automação de processos críticos e implementação de soluções de alta disponibilidade.
        </p>
        <div class="timeline-card-skills">
          <span class="skill-tag-3d">Redes</span>
          <span class="skill-tag-3d">Automação</span>
          <span class="skill-tag-3d">Linux</span>
          <span class="skill-tag-3d">PowerShell</span>
        </div>
      </div>
      <div class="timeline-dot"></div>
    </div>
    
    <div class="timeline-item-3d left">
      <div class="timeline-card-3d">
        <div class="timeline-date-badge">2018 - 2020</div>
        <div class="timeline-card-icon">⚙️</div>
        <h3 class="timeline-card-title">Analista de Infraestrutura</h3>
        <p class="timeline-card-company">Empresa Anterior</p>
        <p class="timeline-card-description">
          Gerenciamento de ambientes virtualizados, configuração de redes corporativas e implementação de políticas de segurança.
        </p>
        <div class="timeline-card-skills">
          <span class="skill-tag-3d">Windows Server</span>
          <span class="skill-tag-3d">VMware</span>
          <span class="skill-tag-3d">Backup</span>
        </div>
      </div>
      <div class="timeline-dot"></div>
    </div>
    
    <div class="timeline-item-3d right">
      <div class="timeline-card-3d">
        <div class="timeline-date-badge">2016 - 2018</div>
        <div class="timeline-card-icon">🛠️</div>
        <h3 class="timeline-card-title">Técnico de Suporte</h3>
        <p class="timeline-card-company">Início da Carreira</p>
        <p class="timeline-card-description">
          Suporte técnico avançado, troubleshooting de problemas complexos e manutenção preventiva de equipamentos.
        </p>
        <div class="timeline-card-skills">
          <span class="skill-tag-3d">Suporte</span>
          <span class="skill-tag-3d">Hardware</span>
          <span class="skill-tag-3d">Troubleshooting</span>
        </div>
      </div>
      <div class="timeline-dot"></div>
    </div>
    
    <div class="timeline-item-3d left">
      <div class="timeline-card-3d">
        <div class="timeline-date-badge">2013 - 2017</div>
        <div class="timeline-card-icon">🎓</div>
        <h3 class="timeline-card-title">Bacharelado em Sistemas de Informação</h3>
        <p class="timeline-card-company">Universidade</p>
        <p class="timeline-card-description">
          Formação acadêmica sólida com foco em infraestrutura, redes de computadores e desenvolvimento de sistemas.
        </p>
        <div class="timeline-card-skills">
          <span class="skill-tag-3d">Redes</span>
          <span class="skill-tag-3d">S.O.</span>
          <span class="skill-tag-3d">Programação</span>
        </div>
      </div>
      <div class="timeline-dot"></div>
    </div>
    
  </div>
</div>

<!-- ==================== DOWNLOAD SECTION ==================== -->
<div class="download-section">
  <h3>📥 Gostou do que viu?</h3>
  <p>Baixe meu currículo completo em formato PDF</p>
  <a href="/assets/files/curriculo-edgardo-correa.pdf" class="download-btn" download>
    ⬇️ Download Currículo PDF
  </a>
</div>

<script>
// ==================== TERMINAL COMMANDS ====================
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
automação e administração de sistemas.</span>

<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>`,

  skills: `
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>
<span class="warning">HABILIDADES TÉCNICAS</span>
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>

<div id="skillsContainer"></div>

<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>`,

  experience: `
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>
<span class="warning">EXPERIÊNCIA PROFISSIONAL</span>
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>

<span class="command">📍 Analista de Sistemas Senior</span> (2020 - Presente)
   • Gerenciamento de infraestrutura
   • Automação de processos
   • Administração Linux/Windows

<span class="command">📍 Analista de Infraestrutura</span> (2018 - 2020)
   • Virtualização (VMware)
   • Redes corporativas
   • Segurança de sistemas

<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>`,

  projects: `
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>
<span class="warning">PROJETOS EM DESTAQUE</span>
<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━</span>

<span class="command">🚀 Modem VIVO Unlock</span>
   Automação para desbloqueio do modem Askey RTF8115VW
   Tech: Node.js, Selenium, PowerShell
   GitHub: github.com/edgardocorrea/modem-vivo

<span class="command">🧹 Limpeza Avançada Windows</span>
   Script de limpeza profunda do Windows
   Tech: PowerShell, Windows API
   GitHub: github.com/edgardocorrea/LimpezaAvancada

<span class="success">━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
