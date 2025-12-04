---
layout: single
title: "Música & Leitura"
permalink: /interesses/leitura/
author_profile: false
---

<style>
/* ==================== ESTILOS GLOBAIS ==================== */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Inter', 'Segoe UI', sans-serif;
  overflow-x: hidden;
}

/* Container principal */
.initial-content {
  position: relative;
  background: rgba(10,20,40,0.85);
  padding: 30px 25px;
  border-radius: 20px;
  box-shadow: 0 8px 25px rgba(0,0,0,0.6);
  backdrop-filter: blur(3px);
  z-index: 1;
}

.page__content {
  max-width: 1400px;
  margin: 0 auto;
  padding: 0 20px;
}

/* ==================== FUNDO COM PARTÍCULAS ==================== */
.particles-bg {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 0;
  pointer-events: none;
  background: 
    radial-gradient(circle at 20% 30%, rgba(0, 234, 255, 0.03) 0%, transparent 50%),
    radial-gradient(circle at 80% 70%, rgba(0, 102, 255, 0.03) 0%, transparent 50%);
}

/* ==================== SEÇÃO HERO ==================== */
.hero-leitura {
  position: relative;
  text-align: center;
  padding: 80px 20px 60px;
  z-index: 1;
  background: linear-gradient(135deg, #0a2840 0%, #001e3c 100%);
  border-radius: 20px;
  margin: 20px 0;
  box-shadow: 0 10px 30px rgba(0,0,0,0.3);
}

.hero-leitura h1 {
  font-size: 56px;
  font-weight: 900;
  margin-bottom: 20px;
  background: #ffffff;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  text-shadow: 
    0 0 10px rgba(255, 255, 255, 0.8),
    0 0 20px rgba(255, 255, 255, 0.6),
    0 0 30px rgba(255, 255, 255, 0.4),
    0 0 40px rgba(255, 255, 255, 0.2);
  animation: whiteGlow 2s ease-in-out infinite alternate;
}

@keyframes whiteGlow {
  0% {
    text-shadow: 
      0 0 10px rgba(255, 255, 255, 0.8),
      0 0 20px rgba(255, 255, 255, 0.6),
      0 0 30px rgba(255, 255, 255, 0.4),
      0 0 40px rgba(255, 255, 255, 0.2);
  }
  100% {
    text-shadow: 
      0 0 20px rgba(255, 255, 255, 1),
      0 0 30px rgba(255, 255, 255, 0.8),
      0 0 40px rgba(255, 255, 255, 0.6),
      0 0 50px rgba(255, 255, 255, 0.4);
  }
}

.hero-leitura p {
  font-size: 20px;
  color: #b3d9ff;
  max-width: 700px;
  margin: 0 auto 40px;
  line-height: 1.6;
}

/* ==================== MENU DE NAVEGAÇÃO RÁPIDA ==================== */
.quick-nav {
  position: sticky;
  top: 0;
  z-index: 100;
  background: rgba(0, 8, 20, 0.95);
  backdrop-filter: blur(10px);
  padding: 15px 0;
  margin: 20px 0 30px 0;
  border-radius: 50px;
  box-shadow: 0 4px 15px rgba(0,0,0,0.3);
  border: 2px solid rgba(0, 102, 255, 0.3);
}

.quick-nav-container {
  max-width: 100%;
  margin: 0 auto;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 15px;
  padding: 0 30px;
}

.quick-nav-item {
  padding: 10px 25px;
  background: rgba(0, 102, 255, 0.15);
  border: 2px solid rgba(0, 102, 255, 0.3);
  border-radius: 30px;
  color: #b3d9ff;
  text-decoration: none;
  font-weight: 600;
  font-size: 15px;
  transition: all 0.3s ease;
  min-width: 140px;
  text-align: center;
  position: relative;
  overflow: hidden;
}

.quick-nav-item::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, 
    transparent, 
    rgba(0, 234, 255, 0.3), 
    transparent);
  transition: left 0.6s ease;
}

.quick-nav-item:hover::before {
  left: 100%;
}

.quick-nav-item:hover, .quick-nav-item.active {
  background: rgba(0, 234, 255, 0.25);
  border-color: #00eaff;
  color: #00eaff;
  transform: translateY(-2px);
  box-shadow: 0 5px 15px rgba(0, 234, 255, 0.3);
}

/* ==================== BOTÕES DE NAVEGAÇÃO ==================== */
.nav-buttons {
  display: flex;
  justify-content: center;
  gap: 20px;
  margin: 60px 0;
  flex-wrap: wrap;
  padding: 0 20px;
}

.nav-button {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  padding: 12px 30px;
  background: rgba(0, 102, 255, 0.1);
  border: 2px solid #00eaff;
  color: #00eaff;
  text-decoration: none;
  border-radius: 50px;
  font-weight: 600;
  transition: all 0.3s ease;
  box-shadow: 0 4px 12px rgba(0, 102, 255, 0.15);
}

.nav-button:hover {
  background: rgba(0, 234, 255, 0.2);
  transform: translateY(-3px);
  box-shadow: 0 8px 20px rgba(0, 234, 255, 0.3);
}

.nav-button.secondary {
  border-color: #00ff88;
  color: #00ff88;
  box-shadow: 0 4px 12px rgba(0, 255, 136, 0.15);
}

.nav-button.secondary:hover {
  background: rgba(0, 255, 136, 0.2);
  box-shadow: 0 8px 20px rgba(0, 255, 136, 0.3);
}

/* ==================== SEÇÕES DE CONTEÚDO ==================== */
.content-section {
  position: relative;
  z-index: 1;
  margin: 40px 0;
  background: rgba(10,20,40,0.85);
  border-radius: 20px;
  padding: 40px 30px;
  box-shadow: 0 8px 25px rgba(0,0,0,0.6);
  backdrop-filter: blur(3px);
}

.section-title {
  font-size: 42px;
  color: #00eaff;
  text-align: center;
  margin-bottom: 50px;
  text-shadow: 0 0 20px rgba(0, 234, 255, 0.5);
}

/* ==================== CARDS DAS BANDAS ==================== */
.bands-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 30px;
  margin-bottom: 60px;
  max-width: 1100px;
  margin-left: auto;
  margin-right: auto;
}

.band-card {
  background: linear-gradient(145deg, rgba(0, 102, 255, 0.08), rgba(0, 234, 255, 0.08));
  border: 2px solid rgba(0, 234, 255, 0.3);
  border-radius: 20px;
  padding: 40px 30px;
  text-align: center;
  transition: all 0.4s ease;
  position: relative;
  overflow: hidden;
}

.band-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(0, 234, 255, 0.1), transparent);
  transition: left 0.6s ease;
}

.band-card:hover::before {
  left: 100%;
}

.band-card:hover {
  transform: translateY(-10px);
  border-color: #00eaff;
  box-shadow: 0 20px 50px rgba(0, 234, 255, 0.3);
}

.band-icon {
  font-size: 64px;
  margin-bottom: 20px;
  display: block;
  filter: drop-shadow(0 0 10px rgba(0, 234, 255, 0.5));
}

.band-name {
  font-size: 26px;
  font-weight: 700;
  color: #00eaff;
  margin-bottom: 15px;
}

.band-description {
  font-size: 15px;
  color: #b3d9ff;
  line-height: 1.6;
  font-style: italic;
}

/* ==================== PLAYER SPOTIFY ==================== */
.spotify-container {
  max-width: 900px;
  margin: 0 auto 80px;
  background: linear-gradient(145deg, rgba(0, 102, 255, 0.08), rgba(0, 234, 255, 0.08));
  border: 2px solid rgba(0, 234, 255, 0.3);
  border-radius: 20px;
  padding: 40px;
  text-align: center;
}

.spotify-title {
  font-size: 28px;
  color: #00eaff;
  margin-bottom: 10px;
  font-weight: 700;
}

.spotify-subtitle {
  font-size: 16px;
  color: #b3d9ff;
  margin-bottom: 30px;
  font-style: italic;
}

.spotify-container iframe {
  border-radius: 12px;
  box-shadow: 0 10px 40px rgba(0, 234, 255, 0.2);
}

.spotify-placeholder {
  background: rgba(0, 20, 40, 0.6);
  border: 2px dashed rgba(0, 234, 255, 0.3);
  border-radius: 12px;
  padding: 60px 40px;
  text-align: center;
}

.spotify-placeholder p {
  font-size: 18px;
  color: #b3d9ff;
  margin-bottom: 15px;
}

.spotify-placeholder code {
  background: rgba(0, 234, 255, 0.1);
  padding: 4px 12px;
  border-radius: 6px;
  color: #00ff88;
  font-size: 14px;
}

/* ==================== ABAS DOS LIVROS ==================== */
.books-tabs {
  display: flex;
  justify-content: center;
  margin-bottom: 40px;
  flex-wrap: wrap;
  gap: 12px;
}

.book-tab {
  padding: 12px 30px;
  background: rgba(0, 102, 255, 0.1);
  border: 2px solid rgba(0, 102, 255, 0.3);
  border-radius: 30px;
  color: #b3d9ff;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s ease;
  font-size: 15px;
  box-shadow: 0 3px 10px rgba(0, 102, 255, 0.15);
}

.book-tab:hover {
  background: rgba(0, 102, 255, 0.2);
  transform: translateY(-2px);
  box-shadow: 0 5px 15px rgba(0, 102, 255, 0.25);
}

.book-tab.active {
  background: rgba(0, 234, 255, 0.25);
  border-color: #00eaff;
  color: #00eaff;
  box-shadow: 0 5px 20px rgba(0, 234, 255, 0.4);
}

.books-category {
  display: none;
  margin-bottom: 60px;
}

.books-category.active {
  display: block;
}

.category-title {
  font-size: 32px;
  color: #00ff88;
  margin-bottom: 30px;
  text-align: center;
  font-weight: 700;
}

.books-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  gap: 35px;
  max-width: 1200px;
  margin: 0 auto;
}

.book-card {
  background: linear-gradient(145deg, rgba(0, 20, 40, 0.8), rgba(0, 30, 50, 0.8));
  border: 2px solid rgba(0, 234, 255, 0.3);
  border-radius: 20px;
  padding: 30px;
  transition: all 0.4s ease;
  cursor: pointer;
  position: relative;
  overflow: hidden;
}

.book-card:hover {
  border-color: #00eaff;
  box-shadow: 0 15px 50px rgba(0, 234, 255, 0.3);
  transform: translateY(-8px);
}

.book-header {
  display: flex;
  gap: 20px;
  margin-bottom: 20px;
  align-items: flex-start;
}

.book-cover {
  width: 100px;
  min-width: 100px;
  height: 150px;
  border-radius: 8px;
  object-fit: cover;
  box-shadow: 0 5px 20px rgba(0, 0, 0, 0.5);
  border: 1px solid rgba(0, 234, 255, 0.2);
}

.book-info {
  flex: 1;
}

.book-title {
  font-size: 20px;
  font-weight: 700;
  color: #00eaff;
  margin-bottom: 8px;
  line-height: 1.3;
}

.book-author {
  font-size: 15px;
  color: #b3d9ff;
  margin-bottom: 10px;
  font-style: italic;
}

.book-rating {
  font-size: 18px;
  margin-bottom: 10px;
}

.book-genre {
  display: inline-block;
  background: rgba(0, 255, 136, 0.2);
  border: 1px solid #00ff88;
  color: #00ff88;
  padding: 4px 12px;
  border-radius: 12px;
  font-size: 12px;
  font-weight: 600;
}

.book-review {
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.5s ease, margin-top 0.5s ease;
  color: #b3d9ff;
  line-height: 1.7;
  font-size: 15px;
}

.book-card.expanded .book-review {
  max-height: 500px;
  margin-top: 20px;
  padding-top: 20px;
  border-top: 1px solid rgba(0, 234, 255, 0.2);
}

.read-more-btn {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  margin-top: 15px;
  padding: 8px 20px;
  background: rgba(0, 234, 255, 0.1);
  border: 1px solid #00eaff;
  color: #00eaff;
  border-radius: 20px;
  font-size: 14px;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s ease;
}

.read-more-btn:hover {
  background: rgba(0, 234, 255, 0.2);
  transform: translateX(5px);
}

.read-more-btn .arrow {
  transition: transform 0.3s ease;
}

.book-card.expanded .read-more-btn .arrow {
  transform: rotate(90deg);
}

/* ==================== RESPONSIVIDADE ==================== */
@media (max-width: 1200px) {
  .quick-nav-container {
    justify-content: space-around;
  }
  .quick-nav-item {
    min-width: 120px;
    padding: 8px 20px;
    font-size: 14px;
  }
}

@media (max-width: 768px) {
  .hero-leitura h1 { font-size: 38px; }
  .section-title { font-size: 32px; }
  .bands-grid { grid-template-columns: 1fr; }
  .books-grid { grid-template-columns: 1fr; }
  .book-header { flex-direction: column; align-items: center; text-align: center; }
  .book-cover { margin-bottom: 15px; }
  .quick-nav-container { padding: 0 20px; gap: 10px; }
  .quick-nav-item { font-size: 13px; padding: 6px 15px; min-width: 100px; }
  .books-tabs { gap: 8px; }
  .book-tab { padding: 10px 20px; font-size: 14px; }
  .content-section { padding: 30px 20px; }
  .quick-nav {
    margin: 15px 0 25px 0;
    border-radius: 30px;
  }
}

@media (max-width: 480px) {
  .quick-nav-item { 
    font-size: 12px; 
    padding: 5px 12px; 
    min-width: 80px;
  }
  .book-tab { 
    padding: 8px 16px; 
    font-size: 13px; 
  }
  .quick-nav {
    border-radius: 25px;
  }
}

/* ==================== ANIMAÇÕES ==================== */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.band-card, .book-card, .spotify-container {
  animation: fadeInUp 0.6s ease backwards;
}

.band-card:nth-child(1) { animation-delay: 0.1s; }
.band-card:nth-child(2) { animation-delay: 0.2s; }
.band-card:nth-child(3) { animation-delay: 0.3s; }
.band-card:nth-child(4) { animation-delay: 0.4s; }
</style>

<!-- Partículas de Fundo -->
<div class="particles-bg"></div>

<!-- Seção Hero -->
<section class="hero-leitura">
  <h1>🎵📚 Música & Leitura</h1>
  <p>As influências que moldam minha visão de mundo, criatividade e forma de pensar</p>
</section>

<!-- Menu de Navegação Rápida -->
<nav class="quick-nav">
  <div class="quick-nav-container">
    <a href="#musica" class="quick-nav-item">🎵 Música</a>
    <a href="#leitura" class="quick-nav-item">📚 Leitura</a>
    <a href="#topo" class="quick-nav-item">⬆️ Topo</a>
  </div>
</nav>

<!-- Âncora para o link "Topo" -->
<div id="topo"></div>

<!-- SEÇÃO: MÚSICA -->
<section id="musica" class="content-section">
  <h2 class="section-title">🎵 Trilha Sonora da Vida</h2>
  
  <!-- Cards das Bandas -->
  <div class="bands-grid">
    <div class="band-card">
      <span class="band-icon">🎸</span>
      <div class="band-name">Muse</div>
      <div class="band-description">"Uprising - Resistência em forma de som"</div>
    </div>
    
    <div class="band-card">
      <span class="band-icon">🎤</span>
      <div class="band-name">Nothing But Thieves</div>
      <div class="band-description">"Amsterdam - Intensidade emocional crua"</div>
    </div>
    
    <div class="band-card">
      <span class="band-icon">🎹</span>
      <div class="band-name">The Doors</div>
      <div class="band-description">"The End - Poesia psicodélica atemporal"</div>
    </div>
    
    <div class="band-card">
      <span class="band-icon">⚡</span>
      <div class="band-name">Linkin Park</div>
      <div class="band-description">"Numb - A trilha sonora de uma geração"</div>
    </div>
  </div>
  
  <!-- Player do Spotify -->
  <div class="spotify-container">
    <div class="spotify-title">Playlist: Code & Focus</div>
    <div class="spotify-subtitle">Trilha sonora perfeita para refletir e mergulhar em projetos</div>
    
    <!-- Placeholder para o Spotify -->
	<iframe data-testid="embed-iframe" style="border-radius:12px" src="https://open.spotify.com/embed/playlist/6ujIGj23dHCnFNPTNMwBQc?utm_source=generator" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
  </div>
</section>

<!-- SEÇÃO: LEITURA -->
<section id="leitura" class="content-section">
  <h2 class="section-title">📚 Livros que Moldaram Minha Visão</h2>
  
  <!-- Abas de Navegação -->
  <div class="books-tabs">
    <div class="book-tab active" data-tab="ficcao">🌌 Ficção Transformadora</div>
    <div class="book-tab" data-tab="tecnicos">💻 Técnicos & Carreira</div>
    <div class="book-tab" data-tab="pessoal">🧠 Desenvolvimento Pessoal</div>
  </div>
  
  <!-- CATEGORIA: FICÇÃO TRANSFORMADORA -->
  <div id="ficcao" class="books-category active">
    <h3 class="category-title">🌌 Ficção Transformadora</h3>
    <div class="books-grid">
      
      <!-- DUNA -->
      <div class="book-card" onclick="toggleBook(this)">
        <div class="book-header">
          <img src="/assets/images/interesses/livros/Duna.jpg" alt="Duna" class="book-cover">
          <div class="book-info">
            <div class="book-title">Duna</div>
            <div class="book-author">Frank Herbert</div>
            <div class="book-rating">⭐⭐⭐⭐⭐</div>
            <span class="book-genre">Ficção Científica</span>
          </div>
        </div>
        <div class="book-review">
          <strong>Por que mudou minha vida:</strong><br><br>
          Duna não é apenas ficção científica — é uma aula de complexidade. Política, ecologia, religião, estratégia... tudo entrelaçado de forma elegante. Me mostrou que sistemas complexos podem ser compreensíveis quando bem estruturados. 
          <br><br>
          Mudou completamente como vejo ficção e como penso em arquiteturas de sistemas. A ideia de que pequenas ações têm consequências massivas no futuro é algo que aplico tanto em código quanto na vida. Um universo que respira complexidade com simplicidade narrativa.
        </div>
        <div class="read-more-btn">
          <span>Leia mais</span>
          <span class="arrow">→</span>
        </div>
      </div>
      
      <!-- NEUROMANCER -->
      <div class="book-card" onclick="toggleBook(this)">
        <div class="book-header">
          <img src="/assets/images/interesses/livros/Neuromancer.jpg" alt="Neuromancer" class="book-cover">
          <div class="book-info">
            <div class="book-title">Neuromancer</div>
            <div class="book-author">William Gibson</div>
            <div class="book-rating">⭐⭐⭐⭐⭐</div>
            <span class="book-genre">Cyberpunk</span>
          </div>
        </div>
        <div class="book-review">
          <strong>O livro que definiu cyberpunk:</strong><br><br>
          Gibson previu o futuro digital antes da internet se popularizar. O conceito de "ciberespaço" nasceu aqui. A estética neon, hackers, megacorporações, IA consciente — tudo que inspira minha visão de tecnologia.
          <br><br>
          Me fez entender que tecnologia não é neutra — ela reflete poder, controle e liberdade. A fusão entre humano e máquina, a vulnerabilidade dos sistemas... tudo aqui é atemporal e profético. É impossível trabalhar com tech e não se inspirar nesse universo.
        </div>
        <div class="read-more-btn">
          <span>Leia mais</span>
          <span class="arrow">→</span>
        </div>
      </div>
      
      <!-- FUNDAÇÃO -->
      <div class="book-card" onclick="toggleBook(this)">
        <div class="book-header">
          <img src="/assets/images/interesses/livros/Fundação.jpg" alt="Fundação" class="book-cover">
          <div class="book-info">
            <div class="book-title">Fundação</div>
            <div class="book-author">Isaac Asimov</div>
            <div class="book-rating">⭐⭐⭐⭐⭐</div>
            <span class="book-genre">Ficção Científica</span>
          </div>
        </div>
        <div class="book-review">
          <strong>Matemática prevendo sociedades:</strong><br><br>
          A psicohistória de Asimov é fascinante — usar matemática para prever o comportamento de civilizações inteiras. Me inspirou a ver dados como padrões que contam histórias sobre o futuro.
          <br><br>
          A ideia de que conhecimento e planejamento podem moldar o destino da humanidade é poderosa. Asimov me ensinou que infraestrutura (seja social ou tecnológica) é a base de tudo. Um império cai, mas conhecimento bem preservado renasce. Isso mudou como penso em documentação e sistemas legados.
        </div>
        <div class="read-more-btn">
          <span>Leia mais</span>
          <span class="arrow">→</span>
        </div>
      </div>
      
    </div>
  </div>
  
  <!-- CATEGORIA: TÉCNICOS/CARREIRA -->
  <div id="tecnicos" class="books-category">
    <h3 class="category-title">💻 Técnicos & Carreira</h3>
    <div class="books-grid">
      
      <!-- CLEAN CODE -->
      <div class="book-card" onclick="toggleBook(this)">
        <div class="book-header">
          <img src="/assets/images/interesses/livros/Codigo_limpo.jpg" alt="Código Limpo" class="book-cover">
          <div class="book-info">
            <div class="book-title">Código Limpo</div>
            <div class="book-author">Robert C. Martin</div>
            <div class="book-rating">⭐⭐⭐⭐⭐</div>
            <span class="book-genre">Programação</span>
          </div>
        </div>
        <div class="book-review">
          <strong>A bíblia do código legível:</strong><br><br>
          Prof/Mestre Fernando me apresentou o Tio Bob ou Uncle Bob é transformou como escrevo cada função. "Código é lido 10x mais do que é escrito" — essa frase mudou tudo. Aprendi que clareza é mais importante que inteligência.
          <br><br>
          Nomes significativos, funções pequenas, comentários apenas quando necessário. Cada linha deve contar uma história. Aplico esses princípios na compreensão de scripts em PowerShell, automações Node.js e até em documentação. Clean Code não é sobre perfeccionismo — é sobre respeitar quem vai ler seu código depois (incluindo você mesmo) - é um excelente livro em todos os aspectos.
        </div>
        <div class="read-more-btn">
          <span>Leia mais</span>
          <span class="arrow">→</span>
        </div>
      </div>
      
      <!-- THE PRAGMATIC PROGRAMMER -->
      <div class="book-card" onclick="toggleBook(this)">
        <div class="book-header">
          <img src="/assets/images/interesses/livros/Programador.jpg" alt="O Programador Pragmático" class="book-cover">
          <div class="book-info">
            <div class="book-title">O Programador Pragmático</div>
            <div class="book-author">Hunt & Thomas</div>
            <div class="book-rating">⭐⭐⭐⭐⭐</div>
            <span class="book-genre">Desenvolvimento</span>
          </div>
        </div>
        <div class="book-review">
          <strong>Carpintaria de software:</strong><br><br>
          Cada capítulo é uma lição prática de como ser um desenvolvedor melhor. "DRY - Don't Repeat Yourself" virou meu mantra. Automatizar processos repetitivos não é preguiça — é eficiência.
          <br><br>
          Aprendi a pensar em código como artesanato: ferramentas certas, atenção aos detalhes, orgulho do trabalho. O conceito de "broken windows" (janelas quebradas) mudou como lido com dívida técnica. Um pequeno problema ignorado se torna uma avalanche. Pragmatismo é equilibrar perfeição com entrega.
        </div>
        <div class="read-more-btn">
          <span>Leia mais</span>
          <span class="arrow">→</span>
        </div>
      </div>
      
      <!-- THE PHOENIX PROJECT -->
      <div class="book-card" onclick="toggleBook(this)">
        <div class="book-header">
          <img src="/assets/images/interesses/livros/Projeto_Fenix.jpg" alt="O Projeto Fênix" class="book-cover">
          <div class="book-info">
            <div class="book-title">O Projeto Fênix</div>
            <div class="book-author">Gene Kim</div>
            <div class="book-rating">⭐⭐⭐⭐⭐</div>
            <span class="book-genre">DevOps</span>
          </div>
        </div>
        <div class="book-review">
          <strong>DevOps em forma de thriller:</strong><br><br>
          Este livro transformou infraestrutura em narrativa envolvente. Impossível parar de ler! Acompanhar o caos de TI se transformando em fluxo otimizado foi revelador.
          <br><br>
          Os "Três Caminhos" (Flow, Feedback, Continuous Learning) mudaram como vejo suporte e automação. Gargalos, trabalho não planejado, heroísmo vs processos — tudo isso virou real. Me fez entender que infraestrutura não é apenas servidores, mas fluxo de valor. Cada automação que crio hoje vem dessa filosofia.
        </div>
        <div class="read-more-btn">
          <span>Leia mais</span>
          <span class="arrow">→</span>
        </div>
      </div>
      
    </div>
  </div>
  
  <!-- CATEGORIA: DESENVOLVIMENTO PESSOAL -->
  <div id="pessoal" class="books-category">
    <h3 class="category-title">🧠 Desenvolvimento Pessoal</h3>
    <div class="books-grid">
      
      <!-- ATOMIC HABITS -->
      <div class="book-card" onclick="toggleBook(this)">
        <div class="book-header">
          <img src="/assets/images/interesses/livros/Habitos.jpg" alt="Habitos Atômicos" class="book-cover">
          <div class="book-info">
            <div class="book-title">Habitos Atômicos</div>
            <div class="book-author">James Clear</div>
            <div class="book-rating">⭐⭐⭐⭐⭐</div>
            <span class="book-genre">Produtividade</span>
          </div>
        </div>
        <div class="book-review">
          <strong>1% melhor todo dia:</strong><br><br>
          "1% melhor todo dia = 37x melhor em um ano." Essa matemática simples mudou minha vida. Não são metas ambiciosas que transformam — são sistemas consistentes.
          <br><br>
          Aprendi a focar em identidade, não em resultados. "Eu sou alguém que aprende diariamente" é mais poderoso que "quero aprender X". Aplico isso em tudo: estudar uma tecnologia nova por 30min/dia, automatizar uma tarefa por semana, documentar learnings. Hábitos compostos são mágica real.
        </div>
        <div class="read-more-btn">
          <span>Leia mais</span>
          <span class="arrow">→</span>
        </div>
      </div>
      
      <!-- DEEP WORK -->
      <div class="book-card" onclick="toggleBook(this)">
        <div class="book-header">
          <img src="/assets/images/interesses/livros/Trabalho.jpg" alt="Trabalho Focado" class="book-cover">
          <div class="book-info">
            <div class="book-title">Trabalho Focado</div>
            <div class="book-author">Cal Newport</div>
            <div class="book-rating">⭐⭐⭐⭐⭐</div>
            <span class="book-genre">Foco</span>
          </div>
        </div>
        <div class="book-review">
          <strong>Foco profundo é superpoder:</strong><br><br>
          Na era da distração constante, quem consegue focar profundamente vence. Newport prova com dados que trabalho superficial é ilusão de produtividade.
          <br><br>
          Aprendi a criar blocos de tempo ininterruptos para resolver problemas complexos. Desligar notificações, isolar-se e mergulhar em um desafio por 2-3h gera mais resultado que 8h distraídas. Mudou como estruturo meu dia: shallow work (emails, meetings) em horários específicos, deep work protegido. Automação nasceu de sessões de deep work.
        </div>
        <div class="read-more-btn">
          <span>Leia mais</span>
          <span class="arrow">→</span>
        </div>
      </div>
      
      <!-- MINDSET -->
      <div class="book-card" onclick="toggleBook(this)">
        <div class="book-header">
          <img src="/assets/images/interesses/livros/MindSet.jpg" alt="Mindset" class="book-cover">
          <div class="book-info">
            <div class="book-title">Mindset</div>
            <div class="book-author">Carol S. Dweck</div>
            <div class="book-rating">⭐⭐⭐⭐⭐</div>
            <span class="book-genre">Psicologia</span>
          </div>
        </div>
        <div class="book-review">
          <strong>Mentalidade de crescimento vs fixa:</strong><br><br>
          Dweck revolucionou como vejo desafios. Pessoas com mindset fixo acreditam que talento é inato. Pessoas com mindset de crescimento sabem que habilidades são construídas.
          <br><br>
          Mudou completamente como reajo a erros. Bugs não são falhas pessoais — são oportunidades de aprender. Cada problema de infraestrutura é uma chance de melhorar. "Ainda não sei" virou mais poderoso que "não sei". Essa mentalidade alimenta minha curiosidade e resiliência em TI, onde sempre há algo novo para aprender.
        </div>
        <div class="read-more-btn">
          <span>Leia mais</span>
          <span class="arrow">→</span>
        </div>
      </div>
      
      <!-- SAPIENS -->
      <div class="book-card" onclick="toggleBook(this)">
        <div class="book-header">
          <img src="/assets/images/interesses/livros/Sapiens.jpg" alt="Sapiens" class="book-cover">
          <div class="book-info">
            <div class="book-title">Sapiens</div>
            <div class="book-author">Yuval Noah Harari</div>
            <div class="book-rating">⭐⭐⭐⭐⭐</div>
            <span class="book-genre">História</span>
          </div>
        </div>
        <div class="book-review">
          <strong>Contexto histórico massivo:</strong><br><br>
          Harari conta a história da humanidade de forma épica e acessível. De caçadores-coletores a algoritmos dominando decisões — uma jornada fascinante.
          <br><br>
          Me deu perspectiva sobre tecnologia. IA não é o primeiro "salto cognitivo" da humanidade. Agricultura, escrita, dinheiro — tudo foi disruptivo. Entender padrões históricos me ajuda a ver o presente com clareza. Tecnologia não é apenas código — é poder, controle e evolução. Sapiens ampliou minha visão sobre o papel da tech na sociedade.
        </div>
        <div class="read-more-btn">
          <span>Leia mais</span>
          <span class="arrow">→</span>
        </div>
      </div>
      
    </div>
  </div>
</section>

<!-- Botões de Navegação -->
<div class="nav-buttons">
  <a href="/" class="nav-button">
    <span>🏠</span>
    <span>Inicio</span>
  </a>
  
  <a href="/sobre/" class="nav-button secondary">
    <span>←</span>
    <span>Voltar ao Perfil</span>
  </a>
</div>

<!-- JavaScript Simplificado -->
<script>
/**
 * INICIALIZAÇÃO DA PÁGINA
 * Executado quando o DOM está completamente carregado
 */
document.addEventListener('DOMContentLoaded', function() {
  
  /**
   * FUNÇÃO: Alternar abas dos livros
   * Controla a exibição das categorias de livros
   */
  const initBookTabs = function() {
    const tabs = document.querySelectorAll('.book-tab');
    const categories = document.querySelectorAll('.books-category');
    
    tabs.forEach(tab => {
      tab.addEventListener('click', function() {
        // Remove a classe active de todas as abas e categorias
        tabs.forEach(t => t.classList.remove('active'));
        categories.forEach(c => c.classList.remove('active'));
        
        // Adiciona a classe active à aba clicada e à categoria correspondente
        this.classList.add('active');
        const tabId = this.getAttribute('data-tab');
        const targetCategory = document.getElementById(tabId);
        
        if (targetCategory) {
          targetCategory.classList.add('active');
        }
      });
    });
  };
  
  /**
   * FUNÇÃO: Configurar navegação rápida
   * Implementa o comportamento de scroll suave para os links do menu
   */
  const setupQuickNav = function() {
    const quickNavItems = document.querySelectorAll('.quick-nav-item');
    
    quickNavItems.forEach(item => {
      item.addEventListener('click', function(e) {
        e.preventDefault();
        const targetId = this.getAttribute('href').substring(1);
        const targetElement = document.getElementById(targetId);
        
        if (targetElement) {
          // Rola suavemente até o elemento
          window.scrollTo({
            top: targetElement.offsetTop - 80,
            behavior: 'smooth'
          });
        }
      });
    });
  };
  
  /**
   * FUNÇÃO: Alternar cards de livros
   * Controla a exibição das resenhas dos livros
   */
  const toggleBook = function(card) {
    // Fecha outros cards abertos
    const allCards = document.querySelectorAll('.book-card');
    allCards.forEach(c => {
      if (c !== card && c.classList.contains('expanded')) {
        c.classList.remove('expanded');
      }
    });
    
    // Alterna o estado do card clicado
    card.classList.toggle('expanded');
    
    // Rola suavemente para o card se foi expandido
    if (card.classList.contains('expanded')) {
      setTimeout(() => {
        card.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
      }, 100);
    }
  };
  
  /**
   * FUNÇÃO: Configurar animações de entrada
   * Adiciona animações quando os elementos entram na viewport
   */
  const setupScrollAnimations = function() {
    const observerOptions = {
      threshold: 0.1,
      rootMargin: '0px 0px -50px 0px'
    };
    
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.style.opacity = '1';
          entry.target.style.transform = 'translateY(0)';
        }
      });
    }, observerOptions);
    
    // Prepara elementos para animação
    document.querySelectorAll('.book-card, .band-card').forEach(el => {
      el.style.opacity = '0';
      el.style.transform = 'translateY(30px)';
      el.style.transition = 'all 0.6s ease';
      observer.observe(el);
    });
  };
  
  /**
   * FUNÇÃO: Atualizar navegação ativa
   * Destaca o item do menu correspondente à seção visível
   */
  const setupActiveNavigation = function() {
    const quickNavItems = document.querySelectorAll('.quick-nav-item');
    
    window.addEventListener('scroll', function() {
      let current = '';
      const sections = document.querySelectorAll('section[id], div[id]');
      
      sections.forEach(section => {
        const sectionTop = section.offsetTop - 100;
        if (window.pageYOffset >= sectionTop) {
          current = section.getAttribute('id');
        }
      });
      
      quickNavItems.forEach(item => {
        item.classList.remove('active');
        if (item.getAttribute('href') === `#${current}`) {
          item.classList.add('active');
        }
      });
    });
  };
  
  // Inicializa todas as funcionalidades
  initBookTabs();
  setupQuickNav();
  setupScrollAnimations();
  setupActiveNavigation();
  
  // Torna a função toggleBook global para acesso via onclick
  window.toggleBook = toggleBook;
});
</script>
