<template >
  <div class="fondo mt-5" id="contacto"> 
    <div class="footer container ">
      <div class="footer-content d-flex flex-column d-lg-grid">
        <div class="map-container">
          <iframe src="https://www.google.com/maps/embed?pb=!1m14!1m12!1m3!1d497.3432358807377!2d-73.48691360460823!3d4.269559738516057!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!5e0!3m2!1ses!2sco!4v1634872896044!5m2!1ses!2sco" width="80%" height="100%" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
        </div>

        <div class="info-container text-center text-lg-end">
          <div class="mb-5">
            <h1 class="fw-bold text-white mb-3">Dirección</h1>
            <p class="text-white mb-0">Oficina: Calle 12 # 18-91</p>
            <p class="text-white">Centro EDS Terpel del centro de Cumaral</p>
          </div>
          <div class="mb-5">
            <h1 class="fw-bold text-white mb-3">Teléfono</h1>
            <p class="text-white mb-0">Atención al cliente: +57 318 835 31 11</p>
            <p class="text-white">Oficina: +57 314 365 22 43</p>
          </div>
          <div class="mb-5">
            <h1 class="fw-bold text-white mb-3">Correo Electrónico</h1>
            <p class="text-white">inalfezsas@gmail.com </p>
          </div>
          <div class="d-flex flex-column align-items-center flex-lg-row justify-content-lg-end">
            <a href="https://wa.link/p8kn4q" target="_blank" class="boton btn btn-light mb-5 mb-lg-0">Ventas</a>
            <a href="https://wa.link/gg36br" target="_blank" class="boton btn btn-light ms-lg-5">Oficina</a>
          </div>
        </div>
      </div>

      <div class="footer-final p-5">
        <div class="d-none d-lg-block">
          <img src="https://res.cloudinary.com/msolutionstech/image/upload/v1626917763/LOGO_BLANCO-02_pori1c.png" alt="logo">
        </div>
        <div class="d-flex align-items-center justify-content-center">
          <p class="text-white mb-4 mb-lg-0" style="font-size: 12px;">COPYRIGHT INVERSIONES ALFEREZ SAS 2022 - TERMS & CONDITIONS  PRIVACY POLICY</p>
        </div>
        <div class="d-flex justify-content-center">
          <img class="d-lg-none me-4" src="https://res.cloudinary.com/msolutionstech/image/upload/v1626917763/LOGO_BLANCO-02_pori1c.png" alt="logo">
          <Facebook class="me-4"/>
          <Instagram />
        </div>
      </div>
    </div>
  </div>
</template>
<script>

import Facebook from './icons/Facebook.vue'
import Instagram from './icons/Instagram.vue'

export default {
  names: 'Footer',
  components: {
    Facebook,
    Instagram,
  }
}
</script>
<style scoped>
  .fondo {
  width: 100%;
  background-color: #0d6efd;
}
  .footer {
  display: flex;
  flex-direction: column;
}

.footer-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
}

.map-container, .info-container {
  padding-top: 50px;
  padding-bottom: 50px;
}

.map-container iframe {
  border-radius: 30px;
}

/* .info-container {
  text-align: end;
} */

.info-container p {
  font-size: 16px;
}

.info-container h1 {
  font-size: 25px;
}

.boton {
  font-size: 14px !important;
  padding: 10px 25px !important;
  box-shadow: -10px 12px 23px -11px rgba(57, 57, 57, 0.67);
  -webkit-box-shadow: -10px 12px 23px -11px rgba(57, 57, 57, 0.67);
  -moz-box-shadow: -10px 12px 23px -11px rgba(57, 57, 57, 0.67);
  width: 200px;
  border-radius: 100px !important;
}

.footer-final {
  display: flex;
  justify-content: space-between;
  align-content: center;
}
.footer-final img {
  height: 25px;
}

@media (max-width: 992px) {
  .map-container {
    height: 400px;
  }

  .map-container {
    padding-bottom: 25px;
  }

  .info-container {
    padding-top: 25px;
    padding-bottom: 25px;
  }

  .footer-final {
    flex-direction: column;
  }
}

@media (max-width: 500px) {
  .map-container {
    height: 350px;
  }
}

@media (max-width: 375px) {
  .map-container {
    height: 300px;
  }
}
</style>