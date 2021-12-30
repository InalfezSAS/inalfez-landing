<template>
  <div class="equipo d-flex flex-column px-5">
    <div class="container">
      <div
        class="
          team-title
          d-flex
          justify-content-center
          align-items-center
          py-5
          mb-5 mb-md-0
        "
      >
        <p>Nuestro equipoo</p>
      </div>
      <div class="swiper personal">
        <div class="swiper-wrapper">
          <div class="swiper-slide">
            <div class="team-card d-flex flex-column">
              <div class="team-img d-flex justify-content-center">
                <img class="foto" src="https://www.dzoom.org.es/wp-content/uploads/2020/02/portada-foto-perfil-redes-sociales-consejos.jpg" alt="">
              </div>
              <div
                class="team-info d-flex flex-column align-items-center"
              >
                <p class="team-title" >
                  <strong>Gabriel Alferez</strong> - CEO INALFEZ S.A.S
                </p>
                <p class="frase">
                  “Amo mi trabajo como si fuera mi vida”
                </p>
              </div>
            </div>
          </div>
        </div>
        <div class="d-none d-md-block">
          <div class="swiper-button-next"></div>
          <div class="swiper-button-prev"></div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Equipo",

  mounted() {
    const Swiper = window.Swiper;
    new Swiper(".personal", {
      effect: "flip",
      grabCursor: true,
      loop: true,
      autoplay: {
        delay: 5000,
        disableOnInteraction: false,
      },
      pagination: {
        el: ".swiper-pagination",
      },
      navigation: {
        nextEl: ".swiper-button-next",
        prevEl: ".swiper-button-prev",
      },
    });
  },
};
</script>
<style scoped>
.equipo {
  width: 100%;
  max-width: 1920px;
  height: 1080px;
  justify-content: center;
  background-image: url("https://res.cloudinary.com/ddegh9xqy/image/upload/v1635412131/fondo_equoi_Mesa_de_trabajo_1_dztvfy.png"); 
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

@media (max-width: 1600px) {
  .equipo {
    height: 900px;
  }
}

@media (max-width: 1300px) {
  .equipo {
    height: 768px;
  }
}

@media (max-width: 1000px) {
  .equipo {
    height: 600px;
  }
}


.swiper {
  width: 700px;
  padding: 50px;
}

.swiper-slide {
  background-position: center;
  background-size: cover;
  width: 100%;
  height: 100%;
}

.button-container {
  width: 40px;
  height: 40px;
  border-radius: 50%;
}

.team-title p {
  font-size: 25px;
  font-weight: bold;
}

.team-card {
  width: 100%;
  height: 100%;
  background-color: white;
  box-shadow: 0px 3px 8px -1px rgba(0, 0, 0, 0.5);
  border-radius: 20px;
}

.foto {
  width: 250px;
  height: 250px;
  border-radius: 100%;
  position: relative;
  top: -30px;
  object-fit: cover;
}

.team-info {
  height: 100%;
  padding: 5px;
}

.team-title {
    font-size: 25px;
  }

  .frase {
    font-size: 21px;
  }

@media (max-width: 1440px) {
  .swiper {
    width: 600px;
  }

  .team-title {
    font-size: 18px;
  }

  .frase {
    font-size: 14px;
  }
}

@media (max-width: 768px) {
  .swiper {
    width: 100%;
  padding: 0;
}

.foto {
  width: 200px;
  height: 200px;
}


}

@media (max-width: 425px) {
  


.foto  {
  width: 150px;
  height: 150px;
}
}

</style>
