<template>
  <section id="como-jogar" class="como-jogar-section">
    <div class="how-to-play-title">
      <img src="@/assets/images/titulo-como-jogar.webp" alt="Como Jogar" class="title-img" />
    </div>

    <div class="blue-background-section">
      <div class="container-fluid">
        <div class="content-wrapper">
          <div class="steps-grid">
            <div class="step-item">
              <img src="@/assets/images/como-participar-1.webp" alt="Passo 1" />
            </div>
            <div class="step-item">
              <img src="@/assets/images/como-participar-2.webp" alt="Passo 2" />
            </div>
            <div class="step-item">
              <img src="@/assets/images/como-participar-3.webp" alt="Passo 3" />
            </div>
          </div>

          <div class="text-box">
            <img src="@/assets/images/box-texto.webp" alt="Informações" />
          </div>
        </div>
      </div>
    </div>

    <div class="promo-section">
      <div class="promo-content">
        <img src="@/assets/images/maionese.webp" alt="Maionese" class="maionese-left" />
        
        <div class="promo-text-wrapper">
          <div class="promo-text">
            <p class="promo-line-1">GARANTA AQUI O SABOR IRRESISTÍVEL</p>
            <p class="promo-line-2">PARA A SUA GAMEPLAY</p>
          </div>
          <button class="promo-button">COMPRE AGORA</button>
        </div>
        
        <img src="@/assets/images/maionese.webp" alt="Maionese" class="maionese-right" />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'PlayGuideSection'
}
</script>

<style scoped>
.como-jogar-section {
  width: 100%;
  min-height: auto;
  display: flex;
  flex-direction: column;
  position: relative;
  padding: 0;
  background: transparent;
}

.how-to-play-title {
  position: absolute;
  top: -50px;
  left: 50%;
  transform: translateX(-50%);
  z-index: 10;
  background: transparent;
}

.title-img {
  max-width: 100%;
  height: auto;
  display: block;
}

.blue-background-section {
  background-color: #152d47;
  width: 100%;
  padding: 20px 0 40px 0;
}

.container-fluid {
  position: relative;
  max-width: 85vw;
  width: 85vw;
  padding: 0;
  margin: 0 auto;
  display: flex;
  align-items: flex-start;
  justify-content: center;
}

.content-wrapper {
  display: flex;
  flex-direction: column;
  gap: 40px;
  align-items: center;
  width: 100%;
  padding-top: 20px;
}

.steps-grid {
  position: relative;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 40px;
  background-color: #FFD700;
  padding: 50px;
  border-radius: 25px;
  width: 100%;
  max-width: none;
}

.steps-grid::before {
  content: "";
  position: absolute;
  top: 20px;
  left: 20px;
  right: 20px;
  bottom: 20px;
  border: 3px solid #0d4085;
  border-radius: 25px;
  pointer-events: none;
}

.step-item {
  display: flex;
  justify-content: center;
  align-items: center;
}

.step-item img {
  width: 100%;
  height: auto;
  max-width: none;
  border-radius: 10px;
}

.text-box {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
}

.text-box img {
  width: 100%;
  height: auto;
  max-width: 70%;
}

.promo-section {
  width: 100vw;
  background-color: #FFFFFF;
  border-radius: 0;
  margin: 0;
  padding: 0;
  box-shadow: none;
  flex-shrink: 0;
  position: relative;
  left: 50%;
  transform: translateX(-50%);
  z-index: 1;
}

.promo-content {
  display: grid;
  grid-template-columns: auto 1fr auto;
  grid-template-areas: "left-mayo content right-mayo";
  align-items: center;
  gap: 30px;
  min-height: auto;
  padding: 10px;
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
}

.maionese-left {
  grid-area: left-mayo;
  height: 250px;
  width: auto;
  object-fit: contain;
  justify-self: center;
}

.maionese-right {
  grid-area: right-mayo;
  height: 250px;
  width: auto;
  object-fit: contain;
  justify-self: center;
}

.promo-text-wrapper {
  grid-area: content;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-self: center;
  text-align: center;
}

.promo-text {
  text-align: center;
  font-family: 'DollopSerif', serif;
  color: #0e5470;
}

.promo-line-1,
.promo-line-2 {
  font-size: 3rem;
  line-height: 0.8;
  font-weight: 900;
  margin-bottom: 20px;
}

.promo-button {
  font-family: 'DollopSerif', serif;
  background: #FFD700;
  color: #0e5470;
  border: none;
  padding: 5px 35px;
  font-size: 2rem;
  font-weight: 900;
  text-transform: uppercase;
  border-radius: 50px;
  cursor: pointer;
  transition: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
  box-shadow: 3px 6px 4px rgba(58, 57, 54, 0.4);
  position: relative;
  overflow: hidden;
}

.promo-button:hover {
  background: linear-gradient(135deg, #FF8C42 0%, #FF6B35 100%);
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(255, 107, 53, 0.4);
}

@media (max-width: 1600px) {
  .steps-grid {
    gap: 35px;
    padding: 45px;
  }

  .promo-content {
    width: 850px;
    grid-template-columns: auto 1fr auto;
    gap: 25px;
  }

  .promo-line-1,
  .promo-line-2 {
    font-size: 42px;
    line-height: 0.5;
  }

  .maionese-left,
  .maionese-right {
    height: 180px;
  }
}

@media (min-width: 992px) and (max-width: 1199.98px) {
  .container-fluid {
    max-width: 90vw;
    width: 90vw;
  }
  
  .steps-grid {
    gap: 35px;
    padding: 45px;
  }

  .promo-content {
    width: 780px;
    grid-template-columns: auto 1fr auto;
    gap: 25px;
  }

  .promo-line-1,
  .promo-line-2 {
    font-size: 35px;
    font-weight: 700;
    line-height: 0.5;
  }

  .maionese-left,
  .maionese-right {
    height: 160px;
  }

  .promo-button {
    font-size: 16px;
    padding: 12px 25px;
  }
}

@media (min-width: 768px) and (max-width: 991.98px) {
  .blue-background-section {
    padding: 30px 0 40px 0;
  }
  
  .how-to-play-title {
    top: -40px;
  }
  
  .container-fluid {
    position: relative;
    width: 100%;
    max-width: 80%;
    padding: 0 16px;
    margin: 0 auto;
  }
  
  .content-wrapper {
    padding-top: 60px;
  }
  
  .steps-grid {
    grid-template-columns: 1fr;
    gap: 30px;
    padding: 40px 30px;
    box-shadow: inset 0 0 0 2px #1559a7;
  }
  
  .content-wrapper {
    gap: 30px;
  }

  .promo-content {
    width: 700px;
    grid-template-columns: auto 1fr auto;
    gap: 25px;
  }

  .promo-line-1,
  .promo-line-2 {
    font-size: 32px;
  }

  .maionese-left,
  .maionese-right {
    height: 140px;
  }

  .promo-button {
    font-size: 15px;
    padding: 10px 20px;
  }
}

@media (min-width: 576px) and (max-width: 767.98px) {
  .blue-background-section {
    padding: 20px 0 30px 0;
  }
  
  .how-to-play-title {
    top: -40px;
  }
  
  .container-fluid {
    position: relative;
    width: 100%;
    max-width: 80%;
    padding: 0 16px;
    margin: 0 auto;
  }
  
  .content-wrapper {
    padding-top: 50px;
  }
  
  .steps-grid {
    grid-template-columns: 1fr;
    padding: 30px 20px;
    border-radius: 15px;
    gap: 25px;
    box-shadow: inset 0 0 0 2px #1559a7;
  }
  
  .step-item img {
    max-width: none;
  }
  
  .text-box img {
    max-width: 85%;
  }

  .promo-content {
    grid-template-columns: 1fr;
    grid-template-areas: 
      "left-mayo"
      "content" 
      "right-mayo";
    gap: 15px;
    text-align: center;
    min-height: auto;
    width: 100%;
    margin: 0 auto;
  }

  .promo-line-1,
  .promo-line-2 {
    font-size: 20px;
    line-height: 1.1;
    margin-bottom: 10px;
  }

  .maionese-left,
  .maionese-right {
    height: auto;
    justify-self: center;
    align-self: center;
  }

  .promo-text-wrapper {
    grid-area: content;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 15px;
  }

  .promo-button {
    font-size: 18px;
    padding: 12px 25px;
  }
}

@media (max-width: 575.98px) {
  .blue-background-section {
    padding: 15px 0 20px 0;
  }

  .how-to-play-title { top: -30px; }

  .container-fluid {
    position: relative;
    width: 100%;
    max-width: 80%;
    padding: 0 10px;
    margin: 0 auto;
  }
  
  .content-wrapper {
    padding-top: 40px;
  }
  
  .steps-grid {
    grid-template-columns: 1fr;
    padding: 20px 15px;
    border-radius: 10px;
    box-shadow: inset 0 0 0 1px #1559a7;
    gap: 20px;
  }
  
  .step-item img {
    max-width: none;
  }
  
  .text-box img {
    max-width: 90%;
  }
  
  .content-wrapper {
    gap: 20px;
  }

  .promo-section {
    width: 100vw;
    padding: 25px 0;
    left: 50%;
    transform: translateX(-50%);
  }

  .promo-content {
    grid-template-columns: 1fr;
    grid-template-areas: 
      "left-mayo"
      "content" 
      "right-mayo";
    gap: 15px;
    text-align: center;
    min-height: auto;
    width: 100%;
    margin: 0 auto;
  }

  .promo-line-1,
  .promo-line-2 {
    font-size: 18px;
    line-height: 1.1;
    margin-bottom: 10px;
  }

  .maionese-left,
  .maionese-right {
    height: auto;
    justify-self: center;
    align-self: center;
  }

  .promo-text-wrapper {
    grid-area: content;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 15px;
  }

  .promo-button {
    font-size: 16px;
  }
}
</style>
