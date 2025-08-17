<template>
  <section class="hero-section">
    <div class="hero-background">
      <div class="container-fluid">
        <div class="row justify-content-center align-items-center min-vh-100">
          <div class="col-12 text-center">
            
            <div class="promo-logo-container">
              <img 
                src="@/assets/logo-promo.webp" 
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
  margin-top: 51px;
}

.hero-background {
  position: relative;
  width: 100%;
  min-height: calc(100vh - 80px);
  background-image: url('@/assets/bg-home.webp');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

.promo-logo-container {
  animation: fadeInDown 1s ease-out 0.2s both;
}

.logo-promo {
  max-width: 850px;
  width: 100%;
  height: auto;
  filter: drop-shadow(0 4px 8px rgba(0, 0, 0, 0.3));
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

@media (max-width: 991.98px) {
  .hero-background {
    background-image: url('@/assets/bg-home-mob.webp');
  }
  
  .logo-promo {
    max-width: 550px;
  }
}

@media (max-width: 576px) {
  .hero-section {
    margin-top: 46px;
  }
  
  .hero-background {
    min-height: calc(100vh - 70px);
  }
  
  .logo-promo {
    max-width: 280px;
  }
}

</style>
