---
title: "Olá, eu sou Edgardo Correa"
layout: splash
date: 2025-11-12T12:00:00-03:00
header:
  overlay_color: "rgba(0, 0, 0, 0.5)" # Sobreposição escura para dar contraste
  overlay_image: /assets/images/banner-home.jpg
  actions:
    - label: "Ver Meus Projetos"
      url: "/portfolio/"
excerpt: "Analista de Sistemas com base em infraestrutura de TI com sólida experiência em redes, sistemas e automação. Apaixonado por construir soluções robustas e eficientes."
---
<div class="text-wrapper">
  <h1 class="page__title">{{ page.title }}</h1>
  <p class="page__lead">{{ page.excerpt | markdownify }}</p>
  {% if page.header.actions %}
    <p>{% include custom-actions.html %}</p>
  {% endif %}
</div>



