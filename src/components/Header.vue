<template>
  <header class="app-header">
    <nav class="navbar navbar-expand-lg">
      <div class="container-fluid">
        <div class="mobile-nav-left d-lg-none">
          <button 
            class="navbar-toggler" 
            type="button" 
            @click="toggleMobileMenu"
            :class="{ 'active': showMobileMenu }"
          >
            <span class="hamburger-icon">
              <span class="line line1"></span>
              <span class="line line2"></span>
              <span class="line line3"></span>
            </span>
          </button>

          <div class="mobile-logo">
            <img src="@/assets/images/logo-mobile.png" alt="Logo" />
          </div>
        </div>

        <a 
          class="mobile-participe-btn d-lg-none"
          href="#participe" 
          @click="setActiveItem('participe')"
        >
          PARTICIPE
        </a>

        <div class="navbar-collapse" :class="{ 'show': showMobileMenu }">
          <ul class="navbar-nav nav-menu">
            <li class="nav-item">
              <a 
                class="nav-link" 
                :class="{ 'active': activeItem === 'home' }"
                href="#home" 
                @click="setActiveItem('home')"
              >
                HOME
              </a>
            </li>
            <li class="nav-item">
              <a 
                class="nav-link" 
                :class="{ 'active': activeItem === 'premios' }"
                href="#ranking" 
                @click="setActiveItem('premios')"
              >
                PRÊMIOS
              </a>
            </li>
            <li class="nav-item">
              <a 
                class="nav-link" 
                :class="{ 'active': activeItem === 'como-participar' }"
                href="#como-participar" 
                @click="setActiveItem('como-participar')"
              >
                COMO PARTICIPAR
              </a>
            </li>
            <li class="nav-item">
              <a 
                class="nav-link" 
                :class="{ 'active': activeItem === 'ranking' }"
                href="#ranking" 
                @click="setActiveItem('ranking')"
              >
                RANKING
              </a>
            </li>
            <li class="nav-item d-none d-lg-block">
              <a 
                class="nav-link nav-participe" 
                :class="{ 'active': activeItem === 'participe' }"
                href="#participe" 
                @click="setActiveItem('participe')"
              >
                PARTICIPE
              </a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'AppHeader',
  data() {
    return {
      showMobileMenu: false,
      activeItem: null
    }
  },
  methods: {
    toggleMobileMenu() {
      this.showMobileMenu = !this.showMobileMenu
    },
    closeMenu() {
      this.showMobileMenu = false
    },
    setActiveItem(item) {
      this.activeItem = item
      this.closeMenu()
      this.$nextTick(() => {
        const el = document.getElementById(item)
        if (el) {
          el.scrollIntoView({ behavior: 'smooth' })
        }
      })
    }
  },
  mounted() {
    document.addEventListener('click', (e) => {
      if (!this.$el.contains(e.target)) {
        this.closeMenu()
      }
    })
  }
}
</script>

<style scoped>
.app-header {
  width: 100vw;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1000;
}

.navbar {
  background: linear-gradient(90deg, #F4C430 0%, #FFD700 100%);
  padding: 0;
  min-height: 50px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
}

.container-fluid {
  padding: 0;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 50px;
}

.nav-menu {
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  width: 100%;
  margin: 0;
  padding: 0;
}

.nav-item {
  font-family: 'DollopSerif', serif;
  margin: 0;
  text-align: center;
}

.nav-item > a {
  font-weight: 900;
}

.nav-link {
  color: #1559a7  !important;
  font-weight: 700;
  font-size: 14px;
  text-transform: uppercase;
  letter-spacing: 0.5px;
  padding: 15px 20px !important;
  text-decoration: none;
  display: block;
  transition: all 0.1s cubic-bezier(0.25, 0.46, 0.45, 0.94);
  border: none;
  background: transparent;
  white-space: nowrap;
}

.nav-link:hover {
  background-color: #0d4085 !important;
  color: #FFD700 !important;
}

.nav-link.active {
  background-color: #0d4085 !important;
  color: #FFD700 !important;
}

.nav-link.nav-participe {
  background-color: #1559a7 !important;
  color: #FFD700 !important;
}

.nav-link.nav-participe:hover {
  background-color: #0d4085 !important;
  color: #FFD700 !important;
}

.nav-link.nav-participe.active {
  background-color: #0d4085 !important;
  color: #FFD700 !important;
}

.mobile-nav-left {
  display: flex;
  align-items: center;
  gap: 15px;
  padding-left: 15px;
}

.mobile-participe-btn {
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #1559a7 !important;
  color: #FFD700 !important;
  font-family: 'DollopSerif', serif;
  font-weight: 900;
  font-size: 12px;
  text-transform: uppercase;
  letter-spacing: 0.5px;
  padding: 0 15px;
  text-decoration: none;
  transition: all 0.2s ease;
  white-space: nowrap;
  z-index: 1002;
  height: 50px;
  margin-right: 15px;
}

.mobile-participe-btn:hover {
  background-color: #0d4085 !important;
  color: #FFD700 !important;
}

.mobile-logo {
  display: flex;
  align-items: center;
}

.mobile-logo img {
  height: 35px;
  width: auto;
}


.navbar-toggler {
  border: none;
  padding: 10px;
  background: transparent;
  position: relative;
  z-index: 1001;
}

.navbar-toggler:focus {
  box-shadow: none;
}

.hamburger-icon {
  display: inline-block;
  position: relative;
  width: 25px;
  height: 20px;
}

.line {
  display: block;
  position: absolute;
  height: 3px;
  width: 100%;
  background: #1559a7;
  border-radius: 2px;
  opacity: 1;
  left: 0;
  transform: rotate(0deg);
  transition: all 0.3s cubic-bezier(0.25, 0.46, 0.45, 0.94);
}

.line1 {
  top: 0px;
}

.line2 {
  top: 8px;
}

.line3 {
  top: 16px;
}

.navbar-toggler.active .line1 {
  top: 8px;
  transform: rotate(135deg);
}

.navbar-toggler.active .line2 {
  opacity: 0;
  left: -60px;
}

.navbar-toggler.active .line3 {
  top: 8px;
  transform: rotate(-135deg);
}

@media (max-width: 991.98px) {
  .navbar-collapse {
    position: absolute;
    top: 100%;
    left: 0;
    right: 0;
    background: linear-gradient(90deg, #F4C430 0%, #FFD700 100%);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
    padding: 0;
    max-height: 0;
    overflow: hidden;
    transition: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
    opacity: 0;
    transform: translateY(-10px);
  }

  .navbar-collapse.show {
    max-height: 400px;
    opacity: 1;
    transform: translateY(0);
  }

  .nav-menu {
    flex-direction: column;
    justify-content: flex-start;
    padding: 0;
    width: 100%;
  }

  .nav-item {
    width: 100%;
    opacity: 0;
    transform: translateX(-20px);
    animation: slideInLeft 0.3s ease forwards;
  }

  .navbar-collapse.show .nav-item:nth-child(1) { animation-delay: 0.1s; }
  .navbar-collapse.show .nav-item:nth-child(2) { animation-delay: 0.2s; }
  .navbar-collapse.show .nav-item:nth-child(3) { animation-delay: 0.3s; }
  .navbar-collapse.show .nav-item:nth-child(4) { animation-delay: 0.4s; }

  .nav-link {
    padding: 15px 20px !important;
    text-align: center;
    border-bottom: 1px solid rgba(0, 102, 204, 0.1);
  }

  .nav-link:last-child {
    border-bottom: none;
  }
}

@keyframes slideInLeft {
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@media (max-width: 576px) {
  .navbar {
    min-height: 45px;
  }

  .container-fluid {
    height: 45px;
  }
  
  .nav-link {
    font-size: 13px;
    padding: 12px 15px !important;
  }

  .mobile-participe-btn {
    font-size: 11px;
    padding: 0 12px;
    height: 45px;
    margin-right: 10px;
  }

  .mobile-nav-left {
    padding-left: 10px;
    gap: 10px;
  }

  .mobile-logo img {
    height: 30px;
  }
}
</style>
