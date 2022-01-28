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
          <a :href="item.whatsApp" class="swiper-slide "  v-for="item in workers" :key="item.id" >
            <div class="team-card d-flex flex-column">
              <div class="team-img d-flex justify-content-center">  
                <img class="foto" :src="item.photo" alt="">
              </div>
              <div
                class="team-info d-flex flex-column align-items-center"
              >
                <p class="team-title" >
                  <strong>{{item.name}}</strong> - {{item.position}}
                </p>
                <p class="frase">
                  "{{item.sentence}}"
                </p>
                <button class="asesoria">
                  {{item.boton}}
                </button>
              </div>
            </div>
          </a>
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

  data(){
    return{
      workers:[
        {
          id:0,
          name:"Maria del Pilar Niño",
          photo:"https://res.cloudinary.com/ddegh9xqy/image/upload/v1643390723/WhatsApp_Image_2022-01-25_at_3.02.54_PM_eamldg.jpg",
          position:"Cordinadora de ventas",
          sentence:"Apasionada por la vida",
          whatsApp:"https://wa.link/rdfp99",
          boton:'Quiero asesoría'
        },
         {
          id:1,
          name:"Barbara Manrique",
          photo:"https://res.cloudinary.com/ddegh9xqy/image/upload/v1641515140/WhatsApp_Image_2021-12-22_at_4.49.37_PM_fg3vrd.jpg",
          position:"Asesora de ventas",
          sentence:"Me encanta superarme",
          whatsApp:"https://wa.link/37jfgy",
          boton:'Quiero asesoría'
        },

      ]
    }
  },

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

.asesoria{
    padding: 10px 30px;
    margin: 10px 0;
    background: #70C217;
    font-size: 14px;
    color: white;
    border-style: none;
    border-radius: 50px;
    text-decoration: none;
    transition: .3s;
    cursor: pointer;
}

a{
  text-decoration: none;
  color: black;
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
