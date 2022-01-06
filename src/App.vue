<template>
  <div id="app" class=" d-flex align-items-center flex-column">
    <div class="fondo-general">
      <!-- Nav -->
      <Navbar />

      <!-- Portada -->
      <div class="container inicio">
        <div class="inicio-container">
          <div class=" info">
            <h3 class="mb-0">El lugar perfecto para</h3>
            <h2 class="mb-2">LA FAMILIA</h2>
            <a href="#la-reserva" class="btn btn-primary saber">
              Quiero saber más
            </a>
          </div>
          <div class=" img-familia">
            <img
              src="https://res.cloudinary.com/ddegh9xqy/image/upload/v1632381164/familia_ao6edf.png"
              alt="Familia"
              class="familia"
            />
          </div>
        </div>
      </div>
    </div>

    <!-- ¿Quiénes somos? -->
    <QuienesSomos />
    <QuienesSomosSwiper />

    <!-- Proyecto -->
    <Proyecto />

    <!-- Equipo -->

    <Vender/>


    <Equipo />

    <Simulador/>

    
    <!-- Footer -->
    <Footer />
    <a href="#head" class="btn-flotante" style="display: flex;
    align-items: center;
    font-size: 16px;
    text-transform: uppercase;
    text-decoration: none;
    font-weight: bold;
    color: #ffffff;
    border-radius: 50px;
    letter-spacing: 2px;
    background-color: #70C217;
    padding:12px;
    position: fixed;
    bottom: 20px;
    right: 20px;
    transition: all 300ms ease 0ms;
    box-shadow: 0px 8px 15px rgba(0, 0, 0, 0.1);
    z-index: 99;">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" style="
        width: 20px;"  fill="none" viewBox="0 0 24 24" stroke="currentColor">
  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 11l5-5m0 0l5 5m-5-5v12" /></svg>
    </a>
  </div>
</template>

<script>
import Equipo from "./components/Equipo.vue";
import QuienesSomosSwiper from "./components/QuienesSomosSwiper.vue";
import QuienesSomos from "./components/QuienesSomos.vue";
import Navbar from "./components/Navbar.vue";
import Footer from "./components/Footer.vue";
import Proyecto from "./components/Proyecto.vue";
import Vender from "./components/Vender.vue";
import Simulador from "./components/Simulador.vue"

export default {
  name: "App",
  components: {
    Equipo,
    QuienesSomosSwiper,
    QuienesSomos,
    Navbar,
    Footer,
    Proyecto,
    Vender,
    Simulador
  },  
};
</script>

<style>
#app {
  font-family: "Poppins", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0;
  padding: 0;
}

html {
  font-size: 62.5%;
}

.inicio {
  margin-top: 30px;
}

.inicio-container {
  display: grid;
  grid-template-columns: 1fr 1fr;
}

.fondo-general {
  background: url("https://res.cloudinary.com/ddegh9xqy/image/upload/v1632982503/fondo_landing_wbmqbx.png");
  width: 100%;
  max-width: 1920px;
  height: 780px;
  background-size: cover;
}

.info {
  display: flex;
  flex-direction: column;
  color: white;
  justify-content: center;
  padding-bottom: 100px;
  text-align: start;
}

.info h3 {
  font-size: 30px;
  text-shadow: 2px 2px 5px rgb(31, 31, 31);
}

.info h2 {
  font-size: 80px;
  font-weight: bold;
  text-shadow: 2px 2px 10px rgb(31, 31, 31);
}

.saber {
  font-size: 14px !important;
  padding: 10px 25px !important;
  box-shadow: -10px 12px 23px -11px rgba(57, 57, 57, 0.67);
  -webkit-box-shadow: -10px 12px 23px -11px rgba(57, 57, 57, 0.67);
  -moz-box-shadow: -10px 12px 23px -11px rgba(57, 57, 57, 0.67);
  width: 200px;
  border-radius: 100px !important;
}

.img-familia {
  display: flex;
  justify-content: center;
  align-items: flex-end;
  padding: 10px;
}

.img-familia img {
  width: 100%;
  max-width: 425px;
}

@media (max-width: 992px) {
  .inicio {
    margin-top: 60px;
  }

  .inicio-container {
    display: flex;
    flex-direction: column;
  }

  .fondo-general {
    height: max-content;
  }

  .img-familia img {
    max-width: 300px;
  }

  .info {
    align-items: center;
    text-align: center;
    padding-bottom: 50px;
  }

  .saber {
    margin-top: 50px;
  }
}

@media (max-width: 600px) {
  .info h3 {
  font-size: 25px;
}

.info h2 {
  font-size: 60px;
}
}

@media (max-width: 425px) {
  .info h3 {
  font-size: 20px;
}

.info h2 {
  font-size: 50px;
}
}

</style>
