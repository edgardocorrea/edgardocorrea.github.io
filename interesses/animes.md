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
  background: #0a1428;
}

.page__content {
  max-width: 1400px;
  margin: 0 auto;
  padding: 0 20px;
}

/* ==================== BACKGROUND ==================== */
.initial-content {
  position: relative;
  background: rgba(10,20,40,0.85);
  padding: 30px 25px;
  border-radius: 20px;
  box-shadow: 0 8px 25px rgba(0,0,0,0.6);
  backdrop-filter: blur(3px);
  z-index: 1;
}

/* ==================== BREADCRUMB ==================== */
.breadcrumb {
  padding: 20px 0;
  color: #e0eaff;
  font-size: 14px;
}

.breadcrumb a {
  color: #00eaff;
  text-decoration: none;
  transition: color 0.3s;
}

.breadcrumb a:hover {
  color: #ffffff;
  text-shadow: 0 0 10px rgba(0, 238, 255, 0.7);
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
  box-shadow: 0 15px 40px rgba(0, 20, 40, 0.85);
}

.hero-banner img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.hero-banner::before {
  content: '';
  position: absolute;
  inset: 0;
  background: linear-gradient(180deg, transparent 0%, rgba(10, 20, 40, 0.85) 100%);
  z-index: 1;
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

.hero-title {
  font-size: 56px;
  font-weight: 900;
  background: linear-gradient(90deg, #ffffff, #00eaff, #ffffff);
  background-size: 200% auto;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  animation: gradient 3s ease infinite;
  text-shadow: 0 0 30px rgba(0, 238, 255, 0.4);
}

.hero-subtitle {
  font-size: 20px;
  color: #e0eaff;
  font-weight: 300;
}

/* ==================== CONTENT WRAPPER ==================== */
.content-wrapper {
  background: rgba(10, 20, 40, 0.9);
  padding: 50px 40px;
  border-radius: 25px;
  box-shadow: 0 10px 40px rgba(0, 238, 255, 0.15);
  backdrop-filter: blur(10px);
}

/* ==================== INTRO SECTION ==================== */
.intro-text {
  font-size: 20px;
  color: #e0eaff;
  line-height: 1.8;
}

.intro-text strong {
  color: #ffffff;
  text-shadow: 0 0 10px #00eaff;
}

/* ==================== ANIME CARDS ==================== */
.anime-card {
  background: linear-gradient(145deg, rgba(0, 238, 255, 0.1), rgba(255, 255, 255, 0.05));
  border: 2px solid rgba(0, 238, 255, 0.5);
  border-radius: 25px;
  padding: 50px 45px;
  margin-bottom: 70px;
  transition: 0.4s ease;
}

.anime-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 20px 50px rgba(0, 238, 255, 0.4);
}

.anime-title {
  font-size: 36px;
  font-weight: 900;
  color: #ffffff;
  text-shadow: 0 0 20px rgba(0, 238, 255, 0.6);
}

.anime-subtitle {
  font-size: 16px;
  color: #00eaff;
  font-weight: 600;
}

/* ==================== SLIDESHOW ==================== */
.slideshow-container {
  position: relative;
  overflow: hidden;
  border-radius: 20px;
  margin-top: 25px;
  box-shadow: 0 15px 40px rgba(0, 238, 255, 0.25);
}

.slide {
  display: none;
}

.slide.active {
  display: block;
}

.slide img {
  width: 100%;
  border-radius: 20px;
}

.slide-caption {
  position: absolute;
  bottom: 0;
  width: 100%;
  padding: 15px;
  background: linear-gradient(transparent, rgba(0, 0, 0, 0.85));
  color: #ffffff;
  font-size: 16px;
  letter-spacing: 1px;
}

.slide-arrow {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background: rgba(0, 238, 255, 0.2);
  border: none;
  font-size: 40px;
  color: #ffffff;
  padding: 10px 18px;
  cursor: pointer;
  transition: 0.3s;
}

.slide-arrow:hover {
  background: rgba(0, 238, 255, 0.5);
}

.prev {
  left: 10px;
}

.next {
  right: 10px;
}

.slide-nav {
  text-align: center;
  margin-top: 10px;
}

.slide-dot {
  height: 12px;
  width: 12px;
  margin: 4px;
  background: rgba(0, 238, 255, 0.3);
  border-radius: 50%;
  display: inline-block;
  transition: 0.3s;
  cursor: pointer;
}

.slide-dot.active {
  background: #00eaff;
  box-shadow: 0 0 15px #00eaff;
}

/* ==================== VIDEO EMBED ==================== */
.video-container {
  margin: 25px 0 35px;
  aspect-ratio: 16 / 9;
  border-radius: 20px;
  overflow: hidden;
  box-shadow: 0 15px 40px rgba(0, 238, 255, 0.25);
}

/* ==================== CONTENT BLOCKS ==================== */
.content-block h3 {
  font-size: 28px;
  color: #ffffff;
  border-left: 4px solid #00eaff;
  padding-left: 15px;
  margin-bottom: 10px;
  text-shadow: 0 0 8px #00eaff;
}

.content-block p {
  font-size: 18px;
  color: #e0eaff;
  margin-bottom: 12px;
  line-height: 1.75;
}

/* ==================== HIGHLIGHT BOX ==================== */
.highlight-box {
  background: rgba(0, 238, 255, 0.18);
  border-left: 4px solid #00eaff;
  padding: 25px;
  border-radius: 15px;
  margin: 30px 0;
}

.highlight-box p {
  color: #f8fbff;
  line-height: 1.75;
}

.highlight-box strong {
  color: #ffffff;
}

/* ==================== TAGS ==================== */
.tag {
  display: inline-block;
  padding: 6px 14px;
  margin: 6px;
  border-radius: 12px;
  background: rgba(0, 238, 255, 0.2);
  border: 1px solid #00eaff;
  color: #00eaff;
  font-size: 14px;
  transition: 0.3s;
}

.tag:hover {
  background: rgba(0, 238, 255, 0.4);
  box-shadow: 0 0 15px rgba(0, 238, 255, 0.7);
}

/* ==================== BACK BUTTON ==================== */
.back-button {
  display: inline-block;
  padding: 14px 24px;
  background: linear-gradient(135deg, #00eaff, #0f1b31);
  color: #ffffff;
  border-radius: 12px;
  text-decoration: none;
  box-shadow: 0 5px 20px rgba(0, 238, 255, 0.35);
  transition: 0.3s;
}

.back-button:hover {
  box-shadow: 0 10px 30px rgba(0, 238, 255, 0.6);
}

/* ==================== RESPONSIVIDADE ==================== */
@media (max-width: 768px) {
  .hero-title { font-size: 38px; }
  .hero-subtitle { font-size: 16px; }
  .anime-title { font-size: 30px; }
  .anime-card { padding: 35px 25px; }
  .slide-arrow { font-size: 28px; padding: 6px 10px; }
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
// ==================== SLIDESHOW ====================
let currentSlide = {};

function initSlideshow(containerId) {
  currentSlide[containerId] = 0;
  const container = document.getElementById(containerId);
  const slides = container.querySelectorAll('.slide');
  const nav = document.getElementById(containerId.replace('-slideshow', '-nav'));

  slides[0].classList.add('active');

  slides.forEach((_, index) => {
    const dot = document.createElement('span');
    dot.className = 'slide-dot';
    if (index === 0) dot.classList.add('active');
    dot.onclick = () => goToSlide(containerId, index);
    nav.appendChild(dot);
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

  slides[index].classList.add('active');
  dots[index].classList.add('active');
}

function autoPlay(containerId, interval = 5500) {
  setInterval(() => changeSlide(containerId, 1), interval);
}

// ==================== PAGE INIT ====================
document.addEventListener('DOMContentLoaded', () => {
  initSlideshow('bleach-slideshow');
  autoPlay('bleach-slideshow');

  initSlideshow('arquivox-slideshow');
  autoPlay('arquivox-slideshow');

  // Animation entrance
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
</script>
