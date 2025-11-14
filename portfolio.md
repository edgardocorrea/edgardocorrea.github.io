<style>
/* ==================== FUNDO ESCURO APENAS PARA O PORTFOLIO ==================== */
body.page--portfolio .initial-content {
  background-color: #000000 !important;
  background-image: none !important;
}

/* ====================MUDANÇA FEITA ==================== */

/* Customizações só para /portfolio/ */
.page--portfolio {
  /* CORREÇÃO PRINCIPAL: Centralizar a COLUNA INTEIRA (título + conteúdo) */
  main.grid__item {
    margin-left: auto !important;
    margin-right: auto !important;
    max-width: 1100px; /* Largura máxima desejada para todo o bloco */
    padding-left: 20px;  /* Espaçamento nas laterais */
    padding-right: 20px;
    box-sizing: border-box;
  }

  /* CORREÇÃO DOS BOTÕES: Organizar verticalmente */
  .project-buttons {
    display: flex;
    flex-direction: column; /* Garante que os botões fiquem em coluna */
    gap: 10px;
    align-items: center;
    margin-top: 25px;
  }

  .btn-custom {
    width: 100%;
    max-width: 240px;
    text-align: center;
  }
}


/* ==================== TÍTULO PRINCIPAL ==================== */
.page__title {
  text-align: center;
  font-size: 48px !important;
  color: #ffffff !important;
  margin-bottom: 20px !important;
  text-shadow: 2px 2px 10px rgba(77, 166, 255, 0.5);
  background: linear-gradient(90deg, #4da6ff, #00ccff);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

/* ==================== SUBTÍTULO ==================== */
.intro-text {
  text-align: center;
  font-size: 20px;
  color: #cccccc;
  margin-bottom: 50px;
  max-width: 800px;
  margin-left: auto;
  margin-right: auto;
}

/* ==================== GRID DE PROJETOS ==================== */
.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 30px;
  margin: 40px 0; /* Margem vertical ajustada, pois o padding está no pai */
  width: 100%;
  box-sizing: border-box;
}

/* ==================== CARD DE PROJETO ==================== */
.project-card {
  width: 100%;
  box-sizing: border-box;
  background: linear-gradient(145deg, rgba(20, 40, 80, 0.8), rgba(10, 20, 40, 0.9));
  border: 2px solid transparent;
  border-radius: 15px;
  padding: 30px;
  transition: all 0.4s ease;
  position: relative;
  overflow: hidden;
  box-shadow: 0 8px 30px rgba(0, 0, 0, 0.5);
}

.project-card::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  border-radius: 15px;
  padding: 2px;
  background: linear-gradient(135deg, #4da6ff, #00ccff, #4da6ff);
  -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
  -webkit-mask-composite: xor;
  mask-composite: exclude;
  opacity: 0;
  transition: opacity 0.4s ease;
  pointer-events: none;
}

.project-card:hover::before {
  opacity: 1;
}

.project-card:hover {
  transform: translateY(-10px) scale(1.02);
  box-shadow: 0 15px 50px rgba(77, 166, 255, 0.4);
}

/* ==================== ÍCONE DO PROJETO ==================== */
.project-icon {
  width: 80px;
  height: 80px;
  margin: 0 auto 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: linear-gradient(135deg, #4da6ff, #0088cc);
  border-radius: 20px;
  font-size: 40px;
  box-shadow: 0 5px 20px rgba(77, 166, 255, 0.3);
}

/* ==================== TÍTULO DO PROJETO ==================== */
.project-title {
  font-size: 28px !important;
  color: #ffffff !important;
  margin: 20px 0 15px 0 !important;
  text-align: center;
  font-weight: 700;
}

/* ==================== DESCRIÇÃO ==================== */
.project-description {
  color: #cccccc;
  font-size: 16px;
  line-height: 1.6;
  margin-bottom: 20px;
  text-align: center;
}

/* ==================== TAGS DE TECNOLOGIA ==================== */
.tech-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  justify-content: center;
  margin: 20px 0;
}

.tech-tag {
  background: rgba(77, 166, 255, 0.2);
  border: 1px solid #4da6ff;
  color: #4da6ff;
  padding: 6px 12px;
  border-radius: 20px;
  font-size: 13px;
  font-weight: 600;
  transition: all 0.3s ease;
}

.tech-tag:hover {
  background: rgba(77, 166, 255, 0.3);
  transform: scale(1.05);
}

/* ==================== BOTÕES ==================== */
.btn-custom {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
  padding: 12px 24px;
  border-radius: 8px;
  font-size: 15px;
  font-weight: 600;
  text-decoration: none;
  transition: all 0.3s ease;
  border: 2px solid;
}

.btn-github {
  background: linear-gradient(135deg, #333333, #1a1a1a);
  color: #ffffff;
  border-color: #333333;
}

.btn-github:hover {
  background: linear-gradient(135deg, #4da6ff, #0088cc);
  border-color: #4da6ff;
  transform: translateY(-2px);
  box-shadow: 0 5px 20px rgba(77, 166, 255, 0.4);
}

.btn-demo {
  background: transparent;
  color: #4da6ff;
  border-color: #4da6ff;
}

.btn-demo:hover {
  background: rgba(77, 166, 255, 0.1);
  transform: translateY(-2px);
}

/* ==================== STATUS BADGE ==================== */
.status-badge {
  position: absolute;
  top: 20px;
  right: 20px;
  background: linear-gradient(135deg, #00cc66, #00aa55);
  color: #ffffff;
  padding: 6px 12px;
  border-radius: 20px;
  font-size: 12px;
  font-weight: 700;
  box-shadow: 0 3px 10px rgba(0, 204, 102, 0.3);
}

/* ==================== RESPONSIVO ==================== */
@media (max-width: 768px) {
  .page--portfolio main.grid__item {
    padding-left: 15px;
    padding-right: 15px;
  }

  .projects-grid {
    grid-template-columns: 1fr;
    gap: 25px;
  }
  
  .page__title {
    font-size: 36px !important;
  }
  
  .intro-text {
    font-size: 18px;
  }
  
  .project-card {
    padding: 25px;
  }
  
  .btn-custom {
    width: 100%;
  }
}

/* ==================== ANIMAÇÃO DE ENTRADA ==================== */
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

.project-card {
  animation: fadeInUp 0.6s ease backwards;
}

.project-card:nth-child(1) { animation-delay: 0.1s; }
.project-card:nth-child(2) { animation-delay: 0.2s; }
.project-card:nth-child(3) { animation-delay: 0.3s; }
.project-card:nth-child(4) { animation-delay: 0.4s; }
</style>
