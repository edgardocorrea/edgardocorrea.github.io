---
layout: single
title: "Animes & Séries"
permalink: /interesses/animes/
author_profile: false
sidebar: null
---

<style>
/* ==================== BASE & RESET ==================== */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Inter', 'Segoe UI', sans-serif;
  overflow-x: hidden;
}

.page__content {
  max-width: 1400px;
  margin: 0 auto;
  padding: 0 20px;
}

/* ==================== BACKGROUND ==================== */
.particles-bg {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: 0;
  pointer-events: none;
  background: 
    radial-gradient(circle at 20% 30%, rgba(157, 78, 221, 0.15) 0%, transparent 50%),
    radial-gradient(circle at 80% 70%, rgba(255, 0, 110, 0.15) 0%, transparent 50%);
}

/* ==================== BREADCRUMB ==================== */
.breadcrumb {
  padding: 20px 0;
  color: #b3d9ff;
  font-size: 14px;
  position: relative;
  z-index: 1;
}

.breadcrumb a {
  color: #9D4EDD;
  text-decoration: none;
  transition: color 0.3s;
}

.breadcrumb a:hover {
  color: #FF006E;
  text-shadow: 0 0 10px rgba(255, 0, 110, 0.5);
}

.breadcrumb span {
  margin: 0 8px;
  color: #666;
}

/* ==================== HERO BANNER ==================== */
.hero-banner {
  position: relative;
  height: 450px;
  border-radius: 25px;
  overflow: hidden;
  margin-bottom: 60px;
  box-shadow: 0 20px 60px rgba(157, 78, 221, 0.4);
}

.hero-banner::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(180deg, transparent 0%, rgba(10, 20, 40, 0.8) 100%);
  z-index: 1;
}

.hero-banner img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.hero-content {
  position: absolute;
  bottom: 40px;
  left: 40px;
  z-index: 2;
  max-width: 600px;
}

.hero-icon {
  font-size: 64px;
  margin-bottom: 15px;
  display: block;
  animation: float 3s ease-in-out infinite;
}

@keyframes float {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-15px); }
}

.hero-title {
  font-size: 56px;
  font-weight: 900;
  background: linear-gradient(90deg, #9D4EDD, #FF006E, #9D4EDD);
  background-size: 200% auto;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  animation: gradient 3s ease infinite;
  margin-bottom: 15px;
  text-shadow: 0 0 40px rgba(157, 78, 221, 0.6);
}

@keyframes gradient {
  0%, 100% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
}

.hero-subtitle {
  font-size: 20px;
  color: #b3d9ff;
  font-weight: 300;
}

/* ==================== CONTENT WRAPPER ==================== */
.content-wrapper {
  position: relative;
  z-index: 1;
  background: rgba(10, 20, 40, 0.85);
  padding: 50px 40px;
  border-radius: 25px;
  box-shadow: 0 10px 40px rgba(0, 0, 0, 0.6);
  backdrop-filter: blur(10px);
  margin-bottom: 40px;
}

/* ==================== INTRO SECTION ==================== */
.intro-section {
  text-align: center;
  margin-bottom: 80px;
}

.intro-text {
  font-size: 20px;
  color: #b3d9ff;
  line-height: 1.8;
  max-width: 800px;
  margin: 0 auto;
}

.intro-text strong {
  color: #FF006E;
  font-weight: 700;
}

/* ==================== ANIME CARDS ==================== */
.anime-section {
  margin-bottom: 80px;
}

.anime-card {
  background: linear-gradient(145deg, rgba(157, 78, 221, 0.1), rgba(255, 0, 110, 0.1));
  border: 2px solid rgba(157, 78, 221, 0.3);
  border-radius: 25px;
  padding: 40px;
  margin-bottom: 50px;
  transition: all 0.4s ease;
}

.anime-card:hover {
  transform: translateY(-10px);
  border-color: #9D4EDD;
  box-shadow: 0 20px 50px rgba(157, 78, 221, 0.4);
}

.anime-header {
  display: flex;
  align-items: center;
  gap: 20px;
  margin-bottom: 30px;
  padding-bottom: 20px;
  border-bottom: 2px solid rgba(157, 78, 221, 0.3);
}

.anime-logo {
  font-size: 48px;
}

.anime-title {
  font-size: 36px;
  font-weight: 900;
  color: #9D4EDD;
  text-shadow: 0 0 20px rgba(157, 78, 221, 0.5);
}

.anime-subtitle {
  font-size: 16px;
  color: #FF006E;
  font-weight: 600;
  margin-top: 5px;
}

/* ==================== SLIDESHOW ==================== */
.slideshow-container {
  position: relative;
  width: 100%;
  max-width: 900px;
  margin: 30px auto;
  border-radius: 15px;
  overflow: hidden;
  box-shadow: 0 15px 40px rgba(157, 78, 221, 0.3);
}

.slide {
  display: none;
  position: relative;
}

.slide.active {
  display: block;
  animation: fadeIn 0.8s ease;
}

@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

.slide img {
  width: 100%;
  height: 500px;
  object-fit: cover;
}

.slide-caption {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  background: linear-gradient(transparent, rgba(0, 0, 0, 0.9));
  color: white;
  padding: 30px 20px 20px;
  font-size: 16px;
  text-align: center;
}

.slide-nav {
  display: flex;
  justify-content: center;
  gap: 10px;
  margin-top: 20px;
}

.slide-dot {
  width: 12px;
  height: 12px;
  border-radius: 50%;
  background: rgba(157, 78, 221, 0.3);
  cursor: pointer;
  transition: all 0.3s;
}

.slide-dot.active {
  background: #9D4EDD;
  box-shadow: 0 0 15px #9D4EDD;
  transform: scale(1.3);
}

.slide-arrow {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background: rgba(157, 78, 221, 0.8);
  color: white;
  border: none;
  font-size: 24px;
  padding: 15px 20px;
  cursor: pointer;
  transition: all 0.3s;
  z-index: 10;
}

.slide-arrow:hover {
  background: #9D4EDD;
  box-shadow: 0 0 20px #9D4EDD;
}

.slide-arrow.prev { left: 10px; border-radius: 0 10px 10px 0; }
.slide-arrow.next { right: 10px; border-radius: 10px 0 0 10px; }

/* ==================== VIDEO EMBED ==================== */
.video-container {
  position: relative;
  width: 100%;
  max-width: 900px;
  margin: 30px auto;
  padding-bottom: 56.25%; /* 16:9 aspect ratio */
  height: 0;
  border-radius: 15px;
  overflow: hidden;
  box-shadow: 0 15px 40px rgba(255, 0, 110, 0.3);
}

.video-container iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

/* ==================== CONTENT BLOCKS ==================== */
.content-block {
  margin: 30px 0;
}

.content-block h3 {
  font-size: 28px;
  color: #FF006E;
  margin-bottom: 20px;
  padding-left: 20px;
  border-left: 4px solid #9D4EDD;
}

.content-block p {
  font-size: 18px;
  color: #b3d9ff;
  line-height: 1.8;
  margin-bottom: 15px;
}

.highlight-box {
  background: rgba(157, 78, 221, 0.15);
  border-left: 4px solid #9D4EDD;
  padding: 20px 25px;
  margin: 25px 0;
  border-radius: 10px;
}

.highlight-box strong {
  color: #FF006E;
}

/* ==================== TAGS ==================== */
.tags-container {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin: 25px 0;
}

.tag {
  background: rgba(157, 78, 221, 0.2);
  border: 1px solid #9D4EDD;
  color: #9D4EDD;
  padding: 8px 16px;
  border-radius: 20px;
  font-size: 14px;
  font-weight: 600;
  transition: all 0.3s;
}

.tag:hover {
  background: rgba(157, 78, 221, 0.4);
  box-shadow: 0 0 15px rgba(157, 78, 221, 0.5);
  transform: translateY(-2px);
}

/* ==================== BACK BUTTON ==================== */
.back-button {
  display: inline-block;
  margin-top: 40px;
  padding: 15px 35px;
  background: linear-gradient(135deg, #9D4EDD, #FF006E);
  color: white;
  text-decoration: none;
  border-radius: 50px;
  font-weight: 700;
  font-size: 16px;
  transition: all 0.3s;
  box-shadow: 0 5px 20px rgba(157, 78, 221, 0.4);
}

.back-button:hover {
  transform: translateY(-3px);
  box-shadow: 0 10px 30px rgba(157, 78, 221, 0.6);
}

/* ==================== RESPONSIVE ==================== */
@media (max-width: 768px) {
  .hero-banner { height: 300px; }
  .hero-title { font-size: 36px; }
  .hero-content { left: 20px; bottom: 20px; }
  .content-wrapper { padding: 30px 20px; }
  .anime-card { padding: 25px; }
  .anime-title { font-size: 28px; }
  .slide img { height: 300px; }
}
</style>

<div class="particles-bg"></div>

<!-- Breadcrumb -->
<nav class="breadcrumb">
  <a href="/">Início</a>
  <span>›</span>
  <a href="/sobre/#contato">Interesses</a>
  <span>›</span>
  <span>Animes & Séries</span>
</nav>

<!-- Hero Banner -->
<div class="hero-banner">
  <img src="/assets/images/interesses/animes-banner.jpg" alt="Animes Banner">
  <div class="hero-content">
    <span class="hero-icon">🎭</span>
    <h1 class="hero-title">Animes & Séries</h1>
    <p class="hero-subtitle">Histórias que transcendem a tela e inspiram a vida</p>
  </div>
</div>

<!-- Content Wrapper -->
<div class="content-wrapper">

  <!-- Intro -->
  <section class="intro-section">
    <p class="intro-text">
      Os animes não são apenas entretenimento para mim — são <strong>fontes de inspiração</strong>, 
      filosofia de vida e lições sobre <strong>perseverança, propósito e humanidade</strong>. 
      Cada história que me marca traz reflexões profundas que aplico no meu trabalho e na minha jornada pessoal.
    </p>
  </section>

  <!-- BLEACH -->
  <section class="anime-section">
    <div class="anime-card">
      <div class="anime-header">
        <span class="anime-logo">⚔️</span>
        <div>
          <h2 class="anime-title">BLEACH</h2>
          <p class="anime-subtitle">A Jornada do Protetor</p>
        </div>
      </div>

      <!-- Slideshow -->
      <div class="slideshow-container" id="bleach-slideshow">
        <div class="slide active">
          <img src="/assets/images/interesses/bleach-1.jpg" alt="Ichigo Kurosaki">
          <div class="slide-caption">Ichigo Kurosaki - O Protetor</div>
        </div>
        <div class="slide">
          <img src="/assets/images/interesses/bleach-2.jpg" alt="Soul Society">
          <div class="slide-caption">Soul Society - O Mundo Espiritual</div>
        </div>
        <div class="slide">
          <img src="/assets/images/interesses/bleach-3.jpg" alt="Bankai">
          <div class="slide-caption">Bankai - O Poder Interior</div>
        </div>
        <button class="slide-arrow prev" onclick="changeSlide('bleach-slideshow', -1)">‹</button>
        <button class="slide-arrow next" onclick="changeSlide('bleach-slideshow', 1)">›</button>
      </div>
      <div class="slide-nav" id="bleach-nav"></div>

      <!-- Resumo -->
      <div class="content-block">
        <h3>📖 Resumo</h3>
        <p>
          Bleach conta a história de <strong>Ichigo Kurosaki</strong>, um adolescente que obtém poderes 
          de Shinigami (ceifador de almas) para proteger os vivos de espíritos malignos e guiar as almas 
          dos mortos para a Soul Society. O anime explora temas de <strong>sacrifício, identidade e o peso da responsabilidade</strong>.
        </p>
      </div>

      <!-- O que representa -->
      <div class="highlight-box">
        <h3>💭 O que Bleach representa para mim</h3>
        <p>
          <strong>"Proteger aqueles que amo, mesmo quando ninguém reconhece."</strong>
        </p>
        <p>
          Bleach me ensinou que <strong>força verdadeira não vem de poder, mas de propósito</strong>. 
          Ichigo luta não pela glória, mas para proteger seus amigos e familiares. Essa filosofia 
          se reflete no meu trabalho: <strong>resolver problemas de infraestrutura e automação</strong> 
          muitas vezes é invisível, mas essencial para que tudo funcione.
        </p>
      </div>

      <!-- Momentos importantes -->
      <div class="content-block">
        <h3>⭐ Momentos Mais Marcantes</h3>
        <p><strong>1. A Salvação de Rukia:</strong> Ichigo invade a Soul Society para salvar Rukia, 
        mostrando lealdade absoluta e coragem contra um sistema inteiro.</p>
        
        <p><strong>2. Conquista do Bankai:</strong> O treinamento com Yoruichi representa 
        <strong>superação através de disciplina e dedicação</strong> — valores que aplico ao aprender novas tecnologias.</p>
        
        <p><strong>3. Confronto com Aizen:</strong> A batalha final ensina que <strong>nem tudo pode ser resolvido 
        apenas com poder</strong>, mas com estratégia, trabalho em equipe e confiança.</p>
      </div>

      <!-- Tags -->
      <div class="tags-container">
        <span class="tag">#Ação</span>
        <span class="tag">#Sobrenatural</span>
        <span class="tag">#Amizade</span>
        <span class="tag">#Superação</span>
        <span class="tag">#Espadas</span>
        <span class="tag">#Shounen</span>
      </div>
    </div>
  </section>

  <!-- EVANGELION -->
  <section class="anime-section">
    <div class="anime-card">
      <div class="anime-header">
        <span class="anime-logo">🤖</span>
        <div>
          <h2 class="anime-title">NEON GENESIS EVANGELION</h2>
          <p class="anime-subtitle">A Complexidade da Existência Humana</p>
        </div>
      </div>

      <!-- Video Embed -->
      <div class="video-container">
        <iframe 
          src="https://www.youtube.com/embed/13nSISwxrY4" 
          title="Evangelion Trailer" 
          frameborder="0" 
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
          allowfullscreen>
        </iframe>
      </div>

      <!-- Resumo -->
      <div class="content-block">
        <h3>📖 Resumo</h3>
        <p>
          Evangelion segue <strong>Shinji Ikari</strong>, um adolescente relutante recrutado para pilotar 
          um mecha gigante (EVA) contra seres misteriosos chamados Anjos. Mas o anime vai além da ação: 
          é uma <strong>análise psicológica profunda sobre trauma, solidão, aceitação e o significado da conexão humana</strong>.
        </p>
      </div>

      <!-- O que representa -->
      <div class="highlight-box">
        <h3>💭 O que Evangelion representa para mim</h3>
        <p>
          <strong>"Enfrentar nossos medos internos é mais difícil que qualquer desafio externo."</strong>
        </p>
        <p>
          Evangelion me fez refletir sobre <strong>saúde mental, vulnerabilidade e aceitação</strong>. 
          Shinji luta com depressão e medo de rejeição — sentimentos que muitos de nós enfrentamos. 
          O anime me ensinou que <strong>está tudo bem não estar bem</strong>, e que buscar ajuda 
          e conexão humana é um ato de coragem, não fraqueza.
        </p>
      </div>

      <!-- Momentos importantes -->
      <div class="content-block">
        <h3>⭐ Momentos Mais Marcantes</h3>
        <p><strong>1. "Você merece amor" (Episódio 26):</strong> A mensagem final de autoaceitação 
        e amor próprio é <strong>libertadora e transformadora</strong>.</p>
        
        <p><strong>2. Batalha contra Ramiel:</strong> Trabalho em equipe perfeito entre Shinji e Rei, 
        mostrando que <strong>colaboração e confiança superam desafios impossíveis</strong>.</p>
        
        <p><strong>3. End of Evangelion:</strong> O confronto final com a psique humana questiona 
        <strong>individualidade vs. coletividade</strong> — uma reflexão sobre como equilibramos 
        autonomia e conexão no mundo tech.</p>
      </div>

      <!-- Tags -->
      <div class="tags-container">
        <span class="tag">#Psicológico</span>
        <span class="tag">#Mecha</span>
        <span class="tag">#Filosofia</span>
        <span class="tag">#Drama</span>
        <span class="tag">#Complexo</span>
        <span class="tag">#Cult Classic</span>
      </div>
    </div>
  </section>

  <!-- ARQUIVO X -->
  <section class="anime-section">
    <div class="anime-card">
      <div class="anime-header">
        <span class="anime-logo">🔦</span>
        <div>
          <h2 class="anime-title">ARQUIVO X</h2>
          <p class="anime-subtitle">A Verdade Está Lá Fora</p>
        </div>
      </div>

      <!-- Slideshow -->
      <div class="slideshow-container" id="arquivox-slideshow">
        <div class="slide active">
          <img src="/assets/images/interesses/arquivox-1.jpg" alt="Mulder e Scully">
          <div class="slide-caption">Mulder & Scully - A Dupla Icônica</div>
        </div>
        <div class="slide">
          <img src="/assets/images/interesses/arquivox-2.jpg" alt="X-Files Investigation">
          <div class="slide-caption">Investigações Sobrenaturais</div>
        </div>
        <div class="slide">
          <img src="/assets/images/interesses/arquivox-3.jpg" alt="The Truth is Out There">
          <div class="slide-caption">"A Verdade Está Lá Fora"</div>
        </div>
        <button class="slide-arrow prev" onclick="changeSlide('arquivox-slideshow', -1)">‹</button>
        <button class="slide-arrow next" onclick="changeSlide('arquivox-slideshow', 1)">›</button>
      </div>
      <div class="slide-nav" id="arquivox-nav"></div>

      <!-- Resumo -->
      <div class="content-block">
        <h3>📖 Resumo</h3>
        <p>
          Arquivo X segue os agentes do FBI <strong>Fox Mulder</strong> e <strong>Dana Scully</strong> 
          investigando casos não solucionados envolvendo fenômenos paranormais. Mulder, o crente, e Scully, 
          a cética, formam uma dupla que equilibra <strong>fé e ciência, intuição e lógica</strong>. 
          A série explora conspiração governamental, alienígenas e os limites do inexplicável.
        </p>
      </div>

      <!-- O que representa -->
      <div class="highlight-box">
        <h3>💭 O que Arquivo X representa para mim</h3>
        <p>
          <strong>"Questione tudo, mas mantenha a mente aberta."</strong>
        </p>
        <p>
          Arquivo X me ensinou a importância do <strong>pensamento crítico e da investigação metódica</strong>. 
          Como Analista de Sistemas, preciso ser como Scully: <strong>cético, analítico e baseado em evidências</strong>. 
          Mas também preciso ter a mente aberta de Mulder para <strong>explorar soluções não convencionais</strong> 
          quando os métodos tradicionais falham. A série me inspira a nunca aceitar respostas superficiais 
          e sempre buscar a raiz do problema.
        </p>
      </div>

      <!-- Momentos importantes -->
      <div class="content-block">
        <h3>⭐ Momentos Mais Marcantes</h3>
        <p><strong>1. "Pilot" (Episódio 1):</strong> O início da parceria Mulder/Scully estabelece 
        a dinâmica perfeita entre <strong>crença e ceticismo</strong> que define toda a série.</p>
        
        <p><strong>2. "Clyde Bruckman's Final Repose":</strong> Um episódio que explora 
        <strong>destino vs. livre arbítrio</strong>, mostrando que mesmo sabendo o futuro, 
        nossas escolhas ainda importam — assim como no planejamento de infraestrutura.</p>
        
        <p><strong>3. "Home" (Temporada 4):</strong> O episódio mais perturbador da série 
        prova que <strong>o verdadeiro terror muitas vezes é humano</strong>, não sobrenatural.</p>
      </div>

      <!-- Tags -->
      <div class="tags-container">
        <span class="tag">#Ficção Científica</span>
        <span class="tag">#Investigação</span>
        <span class="tag">#Conspiração</span>
        <span class="tag">#Sobrenatural</span>
        <span class="tag">#Clássico 90s</span>
        <span class="tag">#Mistério</span>
      </div>
    </div>
  </section>

  <!-- BLACK MIRROR -->
  <section class="anime-section">
    <div class="anime-card">
      <div class="anime-header">
        <span class="anime-logo">📱</span>
        <div>
          <h2 class="anime-title">BLACK MIRROR</h2>
          <p class="anime-subtitle">O Lado Sombrio da Tecnologia</p>
        </div>
      </div>

      <!-- Video Embed -->
      <div class="video-container">
        <iframe 
          src="https://www.youtube.com/embed/jROLrhQkK78" 
          title="Black Mirror Trailer" 
          frameborder="0" 
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
          allowfullscreen>
        </iframe>
      </div>

      <!-- Resumo -->
      <div class="content-block">
        <h3>📖 Resumo</h3>
        <p>
          Black Mirror é uma série antológica que explora as <strong>consequências não intencionais da tecnologia</strong> 
          na sociedade moderna. Cada episódio é uma história independente que funciona como um <strong>espelho distorcido</strong> 
          da nossa relação com tecnologia, mostrando futuros distópicos que estão assustadoramente próximos da realidade.
        </p>
      </div>

      <!-- O que representa -->
      <div class="highlight-box">
        <h3>💭 O que Black Mirror representa para mim</h3>
        <p>
          <strong>"Tecnologia é neutra. O perigo está em como a usamos."</strong>
        </p>
        <p>
          Como profissional de tecnologia, Black Mirror é um <strong>alerta constante sobre responsabilidade ética</strong>. 
          A série me lembra que cada sistema que implemento, cada automação que crio, tem <strong>impacto real 
          na vida das pessoas</strong>. Me motiva a sempre perguntar: "Isso está facilitando ou controlando? 
          Está libertando ou aprisionando?" A tecnologia deve servir à humanidade, não o contrário.
        </p>
      </div>

      <!-- Momentos importantes -->
      <div class="content-block">
        <h3>⭐ Episódios Mais Impactantes</h3>
        <p><strong>1. "San Junipero":</strong> Prova que Black Mirror não é só distopia — 
        mostra como tecnologia pode ser usada para <strong>preservar amor, memória e esperança</strong>. 
        Um dos episódios mais emocionantes da TV moderna.</p>
        
        <p><strong>2. "Nosedive" (Queda Livre):</strong> Crítica devastadora às redes sociais 
        e à <strong>tirania da validação online</strong>. Me faz refletir sobre como medimos 
        nosso valor pessoal e profissional.</p>
        
        <p><strong>3. "USS Callister":</strong> Explora <strong>poder, abuso e ética em ambientes virtuais</strong>. 
        Como desenvolvedor, questiona: onde termina o controle sobre meu código e onde começam 
        as consequências morais?</p>

        <p><strong>4. "White Christmas":</strong> Três histórias interligadas que exploram 
        <strong>consciência digital e isolamento</strong> — levanta questões filosóficas sobre 
        o que significa ser "humano" na era digital.</p>
      </div>

      <!-- Tags -->
      <div class="tags-container">
        <span class="tag">#Distopia</span>
        <span class="tag">#Tecnologia</span>
        <span class="tag">#Ficção Científica</span>
        <span class="tag">#Suspense</span>
        <span class="tag">#Reflexivo</span>
        <span class="tag">#Antologia</span>
      </div>
    </div>
  </section>

  <!-- Reflexão Final -->
  <section class="intro-section" style="margin-top: 60px;">
    <p class="intro-text">
      Essas séries e animes moldaram minha visão de mundo: <strong>Bleach</strong> me ensinou a proteger e lutar 
      pelo que importa, <strong>Evangelion</strong> me mostrou a importância de enfrentar nossos demônios internos, 
      <strong>Arquivo X</strong> me treinou a questionar e investigar profundamente, e <strong>Black Mirror</strong> 
      me alerta sobre a responsabilidade ética na tecnologia. Cada uma delas me inspira a ser melhor, 
      profissional e pessoalmente.
    </p>
  </section>

  <!-- Back Button -->
  <div style="text-align: center;">
    <a href="/sobre/#contato" class="back-button">← Voltar aos Interesses</a>
  </div>

</div>

<!-- JavaScript -->
<script>
// Slideshow functionality
let currentSlide = {};

function initSlideshow(containerId) {
  currentSlide[containerId] = 0;
  const container = document.getElementById(containerId);
  const slides = container.querySelectorAll('.slide');
  const navContainer = document.getElementById(containerId.replace('-slideshow', '-nav'));
  
  // Create dots
  slides.forEach((_, index) => {
    const dot = document.createElement('span');
    dot.className = 'slide-dot';
    if (index === 0) dot.classList.add('active');
    dot.onclick = () => goToSlide(containerId, index);
    navContainer.appendChild(dot);
  });
}

function changeSlide(containerId, direction) {
  const container = document.getElementById(containerId);
  const slides = container.querySelectorAll('.slide');
  const dots = document.getElementById(containerId.replace('-slideshow', '-nav')).querySelectorAll('.slide-dot');
  
  slides[currentSlide[containerId]].classList.remove('active');
  dots[currentSlide[containerId]].classList.remove('active');
  
  currentSlide[containerId] += direction;
  
  if (currentSlide[containerId] >= slides.length) currentSlide[containerId] = 0;
  if (currentSlide[containerId] < 0) currentSlide[containerId] = slides.length - 1;
  
  slides[currentSlide[containerId]].classList.add('active');
  dots[currentSlide[containerId]].classList.add('active');
}

function goToSlide(containerId, index) {
  const container = document.getElementById(containerId);
  const slides = container.querySelectorAll('.slide');
  const dots = document.getElementById(containerId.replace('-slideshow', '-nav')).querySelectorAll('.slide-dot');
  
  slides[currentSlide[containerId]].classList.remove('active');
  dots[currentSlide[containerId]].classList.remove('active');
  
  currentSlide[containerId] = index;
  
  slides[currentSlide[containerId]].classList.add('active');
  dots[currentSlide[containerId]].classList.add('active');
}

// Auto-play slideshow
function autoPlaySlideshow(containerId, interval = 5000) {
  setInterval(() => {
    changeSlide(containerId, 1);
  }, interval);
}

// Initialize on load
document.addEventListener('DOMContentLoaded', () => {
  initSlideshow('bleach-slideshow');
  autoPlaySlideshow('bleach-slideshow', 5000);
  
  // Scroll animations
  const cards = document.querySelectorAll('.anime-card');
  cards.forEach((card, index) => {
    card.style.opacity = '0';
    card.style.transform = 'translateY(30px)';
    setTimeout(() => {
      card.style.transition = 'all 0.8s ease';
      card.style.opacity = '1';
      card.style.transform = 'translateY(0)';
    }, index * 200);
  });
});

// Parallax effect
let ticking = false;
window.addEventListener('scroll', () => {
  if (!ticking) {
    window.requestAnimationFrame(() => {
      const scrolled = window.pageYOffset;
      const parallaxBg = document.querySelector('.particles-bg');
      if (parallaxBg) {
        parallaxBg.style.transform = `translateY(${scrolled * 0.2}px)`;
      }
      ticking = false;
    });
    ticking = true;
  }
});
</script>
