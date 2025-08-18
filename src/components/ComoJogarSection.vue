<template>
  <section id="como-jogar" class="como-jogar-section">
    <div class="how-to-play-title">
      <img src="@/assets/titulo-como-jogar.webp" alt="Como Jogar" class="title-img" />
    </div>

    <div class="container-fluid">
      <div class="content-wrapper">
        <div class="steps-grid">
          <div class="step-item">
            <img src="@/assets/como-participar-1.webp" alt="Passo 1" />
          </div>
          <div class="step-item">
            <img src="@/assets/como-participar-2.webp" alt="Passo 2" />
          </div>
          <div class="step-item">
            <img src="@/assets/como-participar-3.webp" alt="Passo 3" />
          </div>
        </div>

        <div class="text-box">
          <img src="@/assets/box-texto.webp" alt="Informações" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ComoJogarSection'
}
</script>

<style scoped>
.como-jogar-section {
  background-color: #152d47;
  width: 100%;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  position: relative;
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

.container-fluid {
  position: absolute;
  top: calc(-50px + 35px);
  left: 50%;
  transform: translateX(-50%);
  max-width: 85vw;
  width: 85vw;
  padding: 0 20px;
  display: flex;
  align-items: flex-start;
  justify-content: center;
  min-height: calc(100vh - 15px);
}

.content-wrapper {
  display: flex;
  flex-direction: column;
  gap: 40px;
  align-items: center;
  width: 100%;
  padding-top: 80px;
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

@media (max-width: 1600px) {
  .steps-grid {
    gap: 35px;
    padding: 45px;
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
}

@media (min-width: 768px) and (max-width: 991.98px) {
  .como-jogar-section {
    background-color: #152d47;
    width: 100%;
    min-height: 100vh;
    }
  
  .how-to-play-title {
    top: -40px;
  }
  
  .container-fluid {
    position: relative;
    width: 100%;
    max-width: 80%;
    padding: 0 16px;
    margin: 20px auto;
    left: unset;
    transform: unset;
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
}

@media (min-width: 576px) and (max-width: 767.98px) {
  .como-jogar-section {
    background-color: #152d47;
    width: 100%;
    min-height: 100vh;
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
    left: unset;
    transform: unset;
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
}

@media (max-width: 575.98px) {
  .como-jogar-section {
    background-color: #152d47;
    width: 100%;
    min-height: 100vh;
  }

  .how-to-play-title { top: -30px; }

  .container-fluid {
    position: relative;
    width: 100%;
    max-width: 100%;
    padding: 0 10px;
    margin: 0 auto;
    left: unset;
    transform: unset;
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
}
</style>
