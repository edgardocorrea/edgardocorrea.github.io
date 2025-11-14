---
title: "" # Força título vazio
excerpt: "" # Força excerpt vazio
header:
  overlay_color: "rgba(0, 0, 0, 0.3)"
  overlay_image: /assets/images/banner-home.jpg
  image_description: "" # Remove alt text
---
<!-- Texto customizado posicionado sobre a tela do notebook -->
<div class="custom-hero-text">
  <p class="custom-excerpt">
    Analista de Sistemas com base em infraestrutura de TI com sólida experiência em redes, sistemas e automação. Apaixonado por construir soluções robustas e eficientes.
  </p>
</div>

.custom-hero-text {
  position: absolute;
  top: 50%;   /* CENTRALIZA NA TELA DO NOTEBOOK */
  left: 50%;
  transform: translate(-50%, -50%);
  width: 40%;
  max-width: 600px;
  text-align: center;
  z-index: 10;
  padding: 20px 30px;
  background-color: rgba(0, 0, 0, 0.7);
  border: 3px solid #ffcc00;
  border-radius: 8px;
  box-shadow: 0 8px 30px rgba(255, 204, 0, 0.3);
}

.custom-title {
  font-size: 28px !important;
  line-height: 1.2 !important;
  color: #ffffff !important;
  margin: 0 0 15px 0 !important;
  font-weight: 700;
  text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.9);
}

.custom-excerpt {
  font-size: 16px !important;
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
    padding: 15px 20px;
  }
  
  .custom-title {
    font-size: 24px !important;
  }
  
  .custom-excerpt {
    font-size: 14px !important;
  }
}

/* Responsivo - Celulares */
@media (max-width: 480px) {
  .custom-hero-text {
    width: 85%;
    top: 45%;
    left: 50%;
    padding: 12px 15px;
    border-width: 2px;
  }
  
  .custom-title {
    font-size: 20px !important;
    margin-bottom: 10px !important;
  }
  
  .custom-excerpt {
    font-size: 13px !important;
    line-height: 1.4 !important;
  }
}
</style>


