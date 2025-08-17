<template>
  <section class="description-section">
      <div class="row justify-content-center">
        <div class="col-12 text-center">
          
          <h2 class="description-title">
            PARTICIPE DO <span class="highlight-black">DESAFIO HELLMANN'S LOOT IRRESISTÍVEL</span><br>
            E CONCORRA A PRÊMIOS ESPECIAIS
          </h2>
          
          <div class="cta-container">
            <button class="btn-participe">
              PARTICIPE
            </button>
          </div>
          
        </div>
      </div>
  </section>
</template>

<script>
export default {
  name: 'DescriptionSection'
}
</script>

<style scoped>
@font-face {
  font-family: 'DollopSerif';
  src: url('@/assets/fonts/DollopSerif-Condensed.otf') format('opentype');
  font-weight: normal;
  font-style: normal;
}

.description-section {
  background: #FFFFFF;
  padding: 25px 0 15px;
  position: relative;
}

.description-title {
  font-family: 'DollopSerif', serif;
  font-size: 4.3rem;
  color: #0e5470;
  line-height: 1.2;
  font-weight: 900;
  margin-bottom: 10px;
  text-align: center;
}

.highlight-black {
  color: #000000;
}

.cta-container {
  margin-top: 10px;
}

.btn-participe {
  font-family: 'DollopSerif', serif;
  background: #FFD700;
  color: #0e5470;
  border: none;
  padding: 5px 45px;
  font-size: 2rem;
  font-weight: 900;
  text-transform: uppercase;
  border-radius: 50px;
  cursor: pointer;
  transition: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
  box-shadow: 3px 4px 3px rgba(58, 57, 54, 0.4);
  position: relative;
  overflow: hidden;
}

.btn-participe::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.4), transparent);
  transition: left 0.6s;
}

.btn-participe:hover::before {
  left: 100%;
}

.btn-participe:hover {
  background: linear-gradient(135deg, #FFA500 0%, #FF8C00 100%);
  transform: translateY(-3px);
  box-shadow: 0 12px 35px rgba(255, 165, 0, 0.6);
}

.btn-participe:active {
  transform: translateY(-1px);
}

@media (max-width: 1600px) {
  .description-title {
    font-family: 'DollopSerif', serif;
    font-size: 3.3rem;
  }
}

@media (min-width: 992px) and (max-width: 1199.98px) {
  .description-section {
    padding: 20px 0 10px;
  }
  
  .description-title {
    font-size: 2.7rem;
  }
  
  .btn-participe {
    padding: 10px 40px;
    font-size: 2rem;
  }
}

@media (min-width: 768px) and (max-width: 991.98px) {
  .description-section {
    padding: 15px 0 8px;
  }
  
  .description-title {
    font-size: 2rem;
  }

  .btn-participe {
    padding: 7px 20px;
    font-size: 1.5rem;
  }
}

@media (min-width: 576px) and (max-width: 767.98px) {
  .description-section {
    padding: 15px 0 8px;
  }
  
  .description-title {
    font-size: 1.5rem;
  }

  .btn-participe {
    padding: 7px 20px;
    font-size: 1rem;
  }
}

@media (max-width: 575.98px) {
  .description-section {
    padding: 15px 0 8px;
  }
  
  .description-title {
    font-size: 1rem;
  }

  .btn-participe {
    padding: 7px 20px;
    font-size: 1rem;
  }
}  
</style>
