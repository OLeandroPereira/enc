<template>
  <section class="hero-section" id="home">
    <div class="hero-background">
      <div class="container-fluid">
        <div class="row justify-content-center align-items-center min-vh-100">
          <div class="col-12 text-center">
            
            <div class="promo-logo-container">
              <img 
                src="@/assets/images/logo-promo.webp" 
                alt="Loot Irresistível" 
                class="logo-promo"
              >
            </div>

          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'HeroSection'
}
</script>

<style scoped>
.hero-section {
  position: relative;
  width: 100%;
  margin-top: 30px;
}

.hero-background {
  position: relative;
  width: 100%;
  min-height: calc(100vh - 80px);
  background-image: url('@/assets/images/bg-home.webp');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

.promo-logo-container {
  animation: fadeInDown 1s ease-out 0.2s both;
}

.logo-promo {
  max-width: 1010px;
  width: 100%;
  margin-right: 140px;
  margin-bottom: 80px;
  
}

@keyframes fadeInDown {
  from {
    opacity: 0;
    transform: translateY(-30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@media (max-width: 1600px) {
  .hero-section {
    margin-top: 50px;
  }

  .logo-promo {
    max-width: 780px;
    width: 100%;
    margin-right: 110px;
    margin-bottom: 80px;
  }
}

@media (min-width: 992px) and (max-width: 1199.98px) {
  .hero-background {
    background-image: url('@/assets/images/bg-home-mob.webp');
  }

  .hero-section {
    margin-top: 46px;
  }

  .hero-background {
    min-height: calc(100vh - 70px);
  }
  
  .logo-promo {
    max-width: 650px;
    margin: 0 0 150px 0;
  }
}

@media (min-width: 768px) and (max-width: 991.98px) {
  .hero-background {
    background-image: url('@/assets/images/bg-home-mob.webp');
  }

  .hero-section {
    margin-top: 46px;
  }
  
  .hero-background {
    min-height: calc(100vh - 70px);
  }
  
  .logo-promo {
    max-width: 600px;
    margin: 0 0 150px 0;
  }
}

@media (min-width: 576px) and (max-width: 767.98px) {

  .hero-background {
    background-image: url('@/assets/images/bg-home-mob.webp');
  }

  .hero-section {
    margin-top: 50px;
  }

  .hero-background {
    min-height: calc(100vh - 70px);
  }

  .logo-promo {
    max-width: 550px;
    margin: 0 0 150px 0;
  }
}

@media (max-width: 575.98px) {
  .hero-background {
    background-image: url('@/assets/images/bg-home-mob.webp');
  }

  .hero-section {
    margin-top: 45px;
  }

  .hero-background {
    min-height: calc(100vh - 70px);
  }

  .logo-promo {
    max-width: 450px;
    margin: 0 0 150px 0;
  }
}

</style>
