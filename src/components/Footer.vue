<template>
  <footer class="footer-section">
    <div class="decoration-full-width mb-4">
      <div class="decoration-container">
        <div class="line-left"></div>
        <img src="@/assets/images/laco.png" alt="Decoração" class="footer-decoration">
        <div class="line-right"></div>
      </div>
      <div class="footer-links">
        <a href="#duvidas" class="footer-link">DÚVIDAS</a>
        <a href="#regulamento" class="footer-link">REGULAMENTO</a>
      </div>
    </div>
    
    <div class="container">
      <div class="row justify-content-center mb-4">
        <div class="col-12 text-center">
          <div class="social-links">
            <a href="#" class="social-link" aria-label="Twitter">
              <img src="@/assets/images/redes-twitter.png" alt="Twitter" class="social-icon">
            </a>
            <a href="#" class="social-link" aria-label="Facebook">
              <img src="@/assets/images/redes-facebook.png" alt="Facebook" class="social-icon">
            </a>
            <a href="#" class="social-link" aria-label="Instagram">
              <img src="@/assets/images/redes-instagram.png" alt="Instagram" class="social-icon">
            </a>
            <a href="#" class="social-link" aria-label="YouTube">
              <img src="@/assets/images/redes-yt.png" alt="YouTube" class="social-icon">
            </a>
          </div>
        </div>
      </div>
      
      <div class="row justify-content-center mb-4">
        <div class="col-lg-12 col-12 p-1 text-center">
          <p class="footer-text mb-2">
            Esta promoção não é patrocinada, endossada nem administrada pela Epic Games, Inc.
          </p>
          <p class="footer-text mb-2">
            Ao participar deste evento, na extensão permitida pela lei aplicável, os participantes concordam em ilibar e isentar a Epic Games, Inc., seus licenciadores, seus respectivos afiliados e<br>
            funcionários, executivos, diretores, agentes, contratados e outros representantes de toda e qualquer reclamação, exigência, ação, perda, responsabilidade e despesas relacionadas à promoção.
          </p>
          <p class="footer-text mb-2">
            As informações dos participantes fornecidas ligadas a esta promoção são entregues ao patrocinador, não a Epic Games, Inc.
          </p>
          <p class="footer-text">
            Participe de 11 a 25.11.24. Veja regulamento e Certificado de Autorização em loot.hellmanns.com.br. Imagens ilustrativas.
          </p>
        </div>
      </div>
      
      <!-- Logo Unilever -->
      <div class="row justify-content-center">
        <div class="col-12 text-center">
          <img src="@/assets/images/unilever.png" alt="Unilever" class="unilever-logo">
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'SiteFooter'
}
</script>

<style scoped>
.footer-section {
  background: #074A75;
  color: white;
  padding: 20px 0;
}

.decoration-full-width {
  width: 100%;
  text-align: center;
  padding: 0 100px;
}

.footer-decoration {
  max-width: 250px!important;
  height: auto;
  flex-shrink: 0;
}

.footer-nav {
  margin-bottom: 20px;
}

.decoration-container {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 30px;
  gap: 7px;
}

.footer-decoration {
  max-width: 100px;
  height: auto;
  flex-shrink: 0;
}

.line-left,
.line-right {
  height: 2px;
  background: white;
  flex-grow: 1;
}

.footer-links {
  display: flex;
  justify-content: center;
  gap: 80px;
  flex-wrap: wrap;
}

.footer-link {
  color: white;
  text-decoration: none;
  font-weight: bold;
  font-size: 1.1rem;
  transition: opacity 0.3s ease;
}

.footer-link:hover {
  color: white;
  opacity: 0.8;
  text-decoration: none;
}

.social-links {
  display: flex;
  justify-content: center;
  gap: 80px;
  flex-wrap: wrap;
  margin: 15px 0;
}

.social-link {
  transition: transform 0.3s ease;
}

.social-link:hover {
  transform: scale(1.1);
}

.social-icon {
  width: 40px;
  height: 40px;
  object-fit: contain;
}

.footer-text {
  color: white;
  font-size: 0.9rem;
  line-height: 1.5;
  margin-bottom: 8px;
  width: 100%;
  margin-left: auto;
  margin-right: auto;
}

.unilever-logo {
  max-width: 120px;
  height: auto;
  margin-top: 10px;
}

@media (max-width: 767px) {
  .footer-section {
    padding: 30px 0;
  }
  
  .decoration-full-width {
    padding: 0 15px;
  }
  
  .decoration-container {
    gap: 15px;
  }
  
  .footer-decoration {
    max-width: 120px;
  }
  
  .footer-links {
    gap: 20px;
    flex-direction: column;
    align-items: center;
  }
  
  .footer-link {
    font-size: 1rem;
  }
  
  .social-links {
    gap: 15px;
  }
  
  .social-icon {
    width: 35px;
    height: 35px;
  }
  
  .footer-text {
    font-size: 0.8rem;
    padding: 0 10px;
  }
  
  .unilever-logo {
    max-width: 100px;
  }
}

@media (max-width: 575px) {
  .footer-section {
    padding: 20px 0;
  }
  
  .decoration-full-width {
    padding: 0 10px;
  }
  
  .decoration-container {
    gap: 10px;
  }
  
  .footer-decoration {
    max-width: 90px;
  }
  
  .social-icon {
    width: 30px;
    height: 30px;
  }
  
  .footer-text {
    font-size: 0.75rem;
    padding: 0 15px;
  }
  
  .unilever-logo {
    max-width: 80px;
  }
}
</style>
