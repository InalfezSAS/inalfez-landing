<template>
  <div class="equipo d-flex flex-column mb-5">
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
      <p>Nuestro equipo</p>
    </div>
    <div class="swiper personal">
      <div class="swiper-wrapper">
        <div class="swiper-slide">
          <div class="team-card d-flex flex-column">
            <div class="team-img d-flex justify-content-center">
              <div></div>
            </div>
            <div
              class="d-flex flex-column align-items-center my-auto"
              style="height: 100%"
            >
              <p style="font-size: 18px">
                <strong>Gabriel Alferez</strong> - CEO INALFEZ S.A.S
              </p>
              <p style="font-size: 14px">
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
  height: 1080px;
  display: flex;
  justify-content: center;
  background-image: url("../assets/fondo-equipo.jpeg");
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

@media (max-width: 800px) {
  .equipo {
    background: none;
  }
}

.swiper {
  width: 500px;
  height: 400px;
  padding: 50px;
}

.swiper-slide {
  background-position: center;
  background-size: cover;
  width: 400px;
  height: 300px;
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
  height: 300px;
  background-color: white;
  box-shadow: 0px 3px 8px -1px rgba(0, 0, 0, 0.5);
  border-radius: 20px;
}

.team-img div {
  width: 200px;
  height: 200px;
  border-radius: 50%;
  position: relative;
  top: -30px;
  background-image: url("https://www.dzoom.org.es/wp-content/uploads/2020/02/portada-foto-perfil-redes-sociales-consejos.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

@media (max-width: 768px) {
  .swiper {
    width: 450px;
    height: 350px;
    padding: 0;
  }

  .swiper-slide {
    width: 100%;
    height: 100%;
  }

  .team-card {
    height: 100%;
  }

  /* .team-img div {
				width: 150px;
				height: 150px;
		} */
}

@media (max-width: 500px) {
  .swiper {
    width: 320px;
    height: 250px;
  }

  .team-img div {
    width: 100px;
    height: 100px;
  }

  .team-img div {
    width: 150px;
    height: 150px;
  }
}
</style>