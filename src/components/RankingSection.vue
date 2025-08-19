<template>
  <section class="premios-section" id="ranking">
    <img src="@/assets/images/premios-balao-1.webp" alt="Balão lado esquerdo" class="balao-fixo-esquerdo">
    
    <img src="@/assets/images/premios-balao-2.webp" alt="Balão lado direito" class="balao-fixo-direito">
    
    <div class="premios-background">
      <div class="container-fluid premios-container">
        <div class="row justify-content-center">
          <div class="col-12 text-center mb-1">
            <picture>
              <source media="(max-width: 991.98px)" srcset="@/assets/images/titulo-premios-mob.webp">
              <img src="@/assets/images/titulo-premios.webp" alt="Prêmios" class="titulo-premios-img">
            </picture>
          </div>

          <div class="row w-100 mx-0 mb-1 gx-1">
            <div class="col-lg-6 col-md-6 col-sm-12 mb-1 d-flex justify-content-center">
              <img src="@/assets/images/premios-1.webp" alt="Prêmio 1º lugar" class="premio-img">
            </div>
            <div class="col-lg-6 col-md-6 col-sm-12 mb-1 d-flex justify-content-center">
              <img src="@/assets/images/premios-2.webp" alt="Prêmio 2º lugar" class="premio-img">
            </div>
          </div>

          <div class="row w-100 mx-0 gx-1">
            <div class="col-lg-6 col-md-6 col-sm-12 mb-1 d-flex justify-content-center">
              <img src="@/assets/images/premios-3.webp" alt="Prêmio 3º lugar" class="premio-img">
            </div>
            <div class="col-lg-6 col-md-6 col-sm-12 mb-1 d-flex justify-content-center">
              <img src="@/assets/images/premios-4.webp" alt="Prêmio 4º lugar" class="premio-img">
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'PremiosSection'
}
</script>

<style scoped>
.premios-section {
  position: relative;
  width: 100%;
}

.premios-background {
  position: relative;
  width: 100%;
  background-image: url('@/assets/images/bg-premios.webp');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  padding: 60px 0;
}

.premios-container {
  max-width: 1750px;
  margin: 0 auto;
  padding-left: 40px;
  padding-right: 40px;
}

.titulo-premios-img {
  max-width: 1200px;
  width: 100%;
  height: auto;
  margin-bottom: 0.25rem;
}

.premio-img {
  width: 100%;
  height: auto;
  display: block;
  margin: 0 auto;
}

@keyframes flutuar-esquerdo {
  0%, 100% {
    transform: translateY(0px) rotate(0deg);
  }
  25% {
    transform: translateY(-10px) rotate(1deg);
  }
  50% {
    transform: translateY(-5px) rotate(0deg);
  }
  75% {
    transform: translateY(-15px) rotate(-1deg);
  }
}

@keyframes flutuar-direito {
  0%, 100% {
    transform: translateY(0px) rotate(0deg);
  }
  30% {
    transform: translateY(-8px) rotate(-1deg);
  }
  60% {
    transform: translateY(-12px) rotate(1deg);
  }
  85% {
    transform: translateY(-4px) rotate(0deg);
  }
}

.balao-fixo-esquerdo {
  position: absolute;
  left: 0;
  top: -170px;
  z-index: 3;
  width: 185px !important;
  max-width: none !important;
  height: auto;
  animation: flutuar-esquerdo 4s ease-in-out infinite;
}

.balao-fixo-direito {
  position: absolute;
  right: 5.3%;
  top: 83%;
  z-index: 4;
  max-width: 100px;
  height: auto;
  animation: flutuar-direito 5s ease-in-out infinite;
}

@media (prefers-reduced-motion: reduce) {
  .balao-fixo-esquerdo,
  .balao-fixo-direito {
    animation: none;
  }
}

@media (max-width: 1600px) {
  .titulo-premios-img {
    max-width: 900px;
    margin-bottom: 0.25rem;
  }
   .balao-fixo-esquerdo {
    max-width: 150px !important;
    top: -130px;
  }
  .premio-img {
    max-width: 950px;
  }
  .premios-container {
    padding-left: 30px;
    padding-right: 30px;
  }
  .balao-fixo-direito {
    max-width: 120px;
    top: 73%;
    right: 2%;
  }
}

@media (min-width: 992px) and (max-width: 1199.98px) {
  .premios-background {
    padding: 50px 0;
  }
  .titulo-premios-img {
    max-width: 700px;
    margin-bottom: 0.25rem;
  }
  .balao-fixo-esquerdo {
    max-width: 130px !important;
    top: -85px;
  }
  .premio-img {
    max-width: 750px;
  }
  .premios-container {
    padding-left: 25px;
    padding-right: 25px;
  }
  .balao-fixo-direito {
    max-width: 105px;
    top: 72%;
    right: 2%;
  }
}

@media (min-width: 768px) and (max-width: 991.98px) {
  .premios-background {
    background-image: url('@/assets/images/bg-premios-mob.webp');
    padding: 40px 0;
  }
  .titulo-premios-img {
    max-width: 600px;
    margin-bottom: 0.25rem;
  }
  .balao-fixo-esquerdo {
    max-width: 120px !important;
    top: -75px;
  }
  .premio-img {
    max-width: 580px;
  }
  .premios-container {
    padding-left: 20px;
    padding-right: 20px;
  }
  .balao-fixo-direito {
    max-width: 90px;
    top: 72%;
    right: 2%;
  }
}

@media (min-width: 576px) and (max-width: 767.98px) {
  .premios-background {
    background-image: url('@/assets/images/bg-premios-mob.webp');
    padding: 30px 0;
  }
  .titulo-premios-img {
    max-width: 450px;
    margin-bottom: 0.125rem;
  }
  .premio-img {
    max-width: 480px;
  }
  .premios-container {
    padding-left: 15px;
    padding-right: 15px;
  }
  .row.gx-1 {
    --bs-gutter-x: 0rem;
  }
  .balao-fixo-esquerdo {
    max-width: 100px !important;
    top: -75px;
  }
  .balao-fixo-direito {
    max-width: 80px;
    top: 87%;
    right: 14%;
  }
}

@media (max-width: 575.98px) {
  .premios-background {
    background-image: url('@/assets/images/bg-premios-mob.webp');
    padding: 20px 0;
  }
  .col-12.text-center.mb-1 {
    position: relative;
    z-index: 5 !important;
  }
  .titulo-premios-img {
    max-width: 350px;
    margin-bottom: 0.125rem;
    position: relative;
    z-index: 5 !important;
  }
  .premio-img {
    max-width: 400px;
    z-index: 5 !important;
  }
  .premios-container {
    padding-left: 10px;
    padding-right: 10px;
  }
  .row.gx-1 {
    --bs-gutter-x: 0rem;
  }
  .col-sm-12.mb-1 {
    margin-bottom: 0.125rem !important;
  }
  .balao-fixo-esquerdo {
    max-width: 90px !important;
    top: -50px;
    z-index: 2 !important;
  }
  .balao-fixo-direito {
    max-width: 70px !important;
    top: 85%;
    right: 0;
    z-index: 2 !important;
  }
}
</style>
