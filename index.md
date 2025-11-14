---
layout: splash
title: "" # Força título vazio
excerpt: "" # Força excerpt vazio
header:
  overlay_color: "rgba(0, 0, 0, 0.5)"
  overlay_image: /assets/images/banner-home.jpg
  image_description: "" # Remove alt text
  actions:
    - label: "Ver Meus Projetos"
      url: "/portfolio/"
---

<!-- Texto customizado posicionado sobre a tela do notebook -->
<div class="custom-hero-text">
  <h1 class="custom-title">Olá, eu sou Edgardo Correa</h1>
  <p class="custom-excerpt">
    Analista de Sistemas com base em infraestrutura de TI com sólida experiência em redes, sistemas e automação. Apaixonado por construir soluções robustas e eficientes.
  </p>
</div>

<style>
/* CENTRALIZA A IMAGEM DE FUNDO */
.page__hero--overlay {
  background-position: center center !important; /* Centraliza horizontal e vertical */
  background-size: cover !important; /* Cobre toda área mantendo proporção */
}

/* Remove qualquer título/excerpt que apareça */
.page__hero-caption,
.page__title,
.page__lead,
h1.page__title,
.page__hero--overlay h1,
.page__hero--overlay p {
  display: none !important;
  visibility: hidden !important;
}

/* Estilo para o texto customizado */
.custom-hero-text {
  position: absolute;
  top: 45%; /* AJUSTADO: Mais abaixo para afastar da tela */
  left: 50%; /* AJUSTADO: Centralizado horizontalmente */
  transform: translate(-50%, -50%);
  width: 50%; /* REDUZIDO: Menos largura */
  max-width: 600px; /* REDUZIDO: Para não invadir a tela */
  text-align: center;
  z-index: 10;
  padding: 20px 30px; /* REDUZIDO: Menos padding */
  background-color: rgba(0, 0, 0, 0.80); /* Fundo mais escuro */
  border: 3px solid #ffcc00; /* Borda amarela como na imagem */
  border-radius: 8px;
  box-shadow: 0 8px 30px rgba(255, 204, 0, 0.3);
}

.custom-title {
  font-size: 28px !important; /* REDUZIDO: Para caber melhor */
  line-height: 1.3 !important;
  color: #ffffff !important;
  margin: 0 0 15px 0 !important;
  font-weight: 700;
  text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.9);
}

.custom-excerpt {
  font-size: 16px !important; /* REDUZIDO: Para caber melhor */
  line-height: 1.5 !important;
  color: #e6e6e6 !important;
  margin: 0 !important;
  text-shadow: 1px 1px 5px rgba(0, 0, 0, 0.8);
  text-align: left;
}

/* Responsivo - Tablets */
@media (max-width: 768px) {
  .custom-hero-text {
    width: 70%;
    top: 40%;
    left: 50%;
    padding: 20px 25px;
  }
  
  .custom-title {
    font-size: 26px !important;
  }
  
  .custom-excerpt {
    font-size: 16px !important;
  }
}

/* Responsivo - Celulares */
@media (max-width: 480px) {
  .custom-hero-text {
    width: 85%;
    top: 45%;
    left: 50%;
    padding: 15px 18px;
    border-width: 2px;
  }
  
  .custom-title {
    font-size: 22px !important;
    margin-bottom: 12px !important;
  }
  
  .custom-excerpt {
    font-size: 14px !important;
    line-height: 1.5 !important;
  }
}
</style>
