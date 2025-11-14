---
title: "Certificações e Badges"
permalink: /certificacoes/
layout: single
---

<style>
/* ==================== FUNDO PADRÃO DA PÁGINA ==================== */
/* Mantém o fundo azul escuro e aplica o mesmo fundo dos cards no INITIAL-CONTENT */

body.page--certificacoes {
  background: #142850 !important;
}

/* Área principal com o mesmo gradiente dos cards */
.initial-content {
  background: linear-gradient(145deg, rgba(20,40,80,0.8), rgba(10,20,40,0.9)) !important;
  padding: 25px;
  border-radius: 15px;
  box-shadow: 0 8px 20px rgba(0,0,0,0.5);
  position: relative;
  z-index: 1;
}

/* ==================== TÍTULO EM NEON (PADRÃO PROJETOS / HABILIDADES) ==================== */
.page__title {
  text-align: center;
  font-size: 48px !important;
  background: linear-gradient(90deg, #4da6ff, #00ccff);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  margin-bottom: 25px;
  text-shadow: 2px 2px 10px rgba(77, 166, 255, 0.5);
}

/* ==================== CARDS DE CERTIFICADO - MESMO PADRÃO DOS CARDS ==================== */
/* Ajuste o nome da classe caso seus certificados tenham outra */
.cert-card {
  background: linear-gradient(145deg, rgba(20,40,80,0.8), rgba(10,20,40,0.9));
  border-radius: 15px;
  padding: 25px;
  margin-bottom: 25px;
  position: relative;
  overflow: hidden;
  box-shadow: 0 8px 20px rgba(0,0,0,0.5);
  transition: all 0.4s ease;
}

/* Camada neon animada apenas NOS CARDS */
.cert-card::before {
  content: "";
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: linear-gradient(135deg, #4da6ff, #00ccff, #4da6ff, #00ccff);
  opacity: 0.18;
  transform: rotate(45deg);
  filter: blur(45px);
  animation: neonGlow 6s linear infinite;
  pointer-events: none;
  z-index: 0;
  border-radius: 20px;
}

/* Hover com destaque NEON */
.cert-card:hover {
  box-shadow: 0 15px 50px rgba(77, 166, 255, 0.6);
  transform: translateY(-5px) scale(1.02);
}

/* ==================== TÍTULOS E TEXTOS DO CARD ==================== */

.cert-title {
  position: relative;
  z-index: 2;
  color: #ffffff;
  font-size: 24px;
  font-weight: 700;
  margin-bottom: 10px;
}

.cert-provider {
  position: relative;
  z-index: 2;
  color: #4da6ff;
  font-size: 16px;
  margin-bottom: 5px;
}

.cert-description {
  position: relative;
  z-index: 2;
  color: #cccccc;
  line-height: 1.6;
  font-size: 15px;
}

/* ==================== LISTAS DENTRO DO CARD ==================== */

.cert-card ul li {
  color: #cccccc;
  position: relative;
  z-index: 2;
  padding-left: 15px;
  margin-bottom: 6px;
}

/* bolinha neon */
.cert-card ul li::before {
  content: "•";
  color: #4da6ff;
  position: absolute;
  left: 0;
  font-size: 20px;
  line-height: 12px;
  text-shadow:
    0 0 5px #4da6ff,
    0 0 10px #00ccff;
}

/* ==================== ANIMAÇÃO NEON ==================== */

@keyframes neonGlow {
  0%, 100% {
    transform: rotate(0deg) translate(-50%, -50%);
  }
  50% {
    transform: rotate(45deg) translate(-50%, -50%);
  }
}

/* ==================== RESPONSIVO ==================== */
@media (max-width: 768px) {
  .cert-card {
    padding: 20px;
  }
  .page__title {
    font-size: 36px !important;
  }
  .cert-title {
    font-size: 20px;
  }
}
</style>



Nesta página, apresento as minhas certificações profissionais, que validam as minhas competências em diversas áreas da tecnologia. Para mais detalhes ou para verificar a autenticidade, visite meu perfil completo no [Credly](https://www.credly.com/users/edgardo.correa).

---

## Redes

<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="232a032a-8675-4fbd-9752-b74219f08ad8" data-share-badge-host="https://www.credly.com"></div>

<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="5c6077c7-6f57-4196-b648-e7d3b5b82624" data-share-badge-host="https://www.credly.com"></div>

<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="e0ee1601-18f3-41d2-97f3-67a836bfe4c9" data-share-badge-host="https://www.credly.com"></div>

---

## Segurança da Informação

<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="d44d5772-1fee-4491-9326-ab1aa4a908ca" data-share-badge-host="https://www.credly.com"></div>

<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="02abd07a-71a8-4024-8316-0dd40691fa74" data-share-badge-host="https://www.credly.com"></div>

---

## Inteligência Artificial e Metodologias Ágeis

<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="aa5e1665-af74-4d59-9567-409b890991f4" data-share-badge-host="https://www.credly.com"></div>

<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="bdb8bcd3-8357-4d2e-8894-f1fe4e36e079" data-share-badge-host="https://www.credly.com"></div>

<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="24f3cc92-a5fb-469b-820d-d2d85b4d487c" data-share-badge-host="https://www.credly.com"></div>

<!-- Script do Credly para renderizar todos os badges acima. Apenas um é necessário por página. -->
<script type="text/javascript" async src="//cdn.credly.com/assets/utilities/embed.js"></script>
