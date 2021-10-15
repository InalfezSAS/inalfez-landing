<template>
  <div id="app" class="position-relative d-flex align-items-center flex-column">
    <div class="fondo-general">
      <!-- Nav -->
      <Navbar />

      <!-- Portada -->
      <div class="container mt-5">
        <div class="row">
          <div class="col-6 info">
            <h3 class="mb-0">El lugar perfecto para</h3>
            <h2 class="mb-2">LA FAMILIA</h2>
            <button type="button" class="btn btn-primary saber">
              Quiero saber más
            </button>
          </div>
          <div class="col-6 img-familia">
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
    <Equipo />

    <!-- Footer -->
    <Footer />
  </div>
</template>

<script>
import Equipo from "./components/Equipo.vue";
import QuienesSomosSwiper from "./components/QuienesSomosSwiper.vue";
import QuienesSomos from "./components/QuienesSomos.vue";
import Navbar from "./components/Navbar.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Equipo,
    QuienesSomosSwiper,
    QuienesSomos,
    Navbar,
    Footer,
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
}

.info h3 {
  font-size: 30px;
  text-shadow: 2px 2px 5px rgb(31, 31, 31);
}

.info h2 {
  font-size: 80px;
  font-weight: 800;
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

</style>
