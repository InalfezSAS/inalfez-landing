<template>
  <div class="servicios-container" >
    <div class="servicios-content">
      <div class="title-container">
        <h2>Nuestro proyecto</h2>
        <p @click="toggleExit">X</p>
      </div>
        <div class="partners">
          <div class="partners-container">
            <div class="swiper servicios">
              <div class="swiper-button-next button">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"></path></svg>
                </div>
              <div class="swiper-button-prev button">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7"></path></svg>
              </div>
              <div class="swiper-wrapper slider-container">
                <div class="swiper-slide logo-container" v-for="(servicio, index) in servicios" :key="index" >
                  <div class="card">
                    <div class="img-card">
                      <img
                        :src="servicio.image"
                        alt=""
                      /> 
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  components: {},
  props:{
    toggle:{
      type: Boolean
    }
  },
  data() {
    return {
      servicios:[
        {
          id: 1,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503144/33_v1kezy.jpg",
        },
        {
          id: 2,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503124/41_qepsd2.jpg",
        },
       {
          id: 3,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503124/49_tzdfl6.jpg",
        },
       {
          id: 4,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503122/47_b6vbtv.jpg",
        },
        {
          id: 5,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503119/37_kc6q9q.jpg",
        },
       {
          id: 6,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503117/34_zgyahc.jpg",
        },
{
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503118/36_mjvqo8.jpg",
        },
      ],

      currentInfo:{
        title: "",
        info: "",
      }
    };
  },
  mounted() {
    const Swiper = window.Swiper;

    new Swiper(".servicios", {
      slidesPerView: 1,
      loop: true,
      autoplay: {
        delay: 1500,
        disableOnInteraction: false,
      },
      navigation: {
        nextEl: ".swiper-button-next",
        prevEl: ".swiper-button-prev",
      },
    });
  },

  methods: {
    toggleExit(){
      this.$emit("toggleClose", false)
    }
  },
};
</script>

<style scoped>

.swiper-button-next{
  color: #ffffff;
  background-color: none;
  right: 0;
  margin-left: 30;
}

.swiper-button-next::after{
  content: none;
  padding: 5px;
}
.swiper-button-prev{

  color: white;
  background-color: none;
  left: 0;
  margin-right: 30;
}
.swiper-button-prev::after{
  content: none;
  
}

.servicios-container {
  width: 100%;
  padding: 10px;
}

.servicios-content {
  max-width: 1080px;
  width: 100%;
  height: 100%;
  padding: 40px 0;
  margin-left: auto;
  margin-right: auto;
  display: flex;
  flex-direction: column;
}

.title-container {
  display: flex;
  justify-content: center;
  position: relative;
}

.title-container p{
  color: white;
  position: absolute;
  right: 40px;
  top: -30px;
  cursor: pointer;
}

.title-container h2 {
  color: white;
  font-weight: bold;
  margin-bottom: 10px;
}

.button {
  width: 30px;
  height: 30px;
  display: flex;
  justify-content: center;
  align-items: center;
  border: none;
  border-radius: 50%;
  cursor: pointer;
}

.partners {
  margin: auto 0;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.partners-container {
  width: 100%;
  height: max-content;
  display: flex;
  justify-content: center;
  align-items: center;
}

.servicios {
  /* display: grid;
  grid-template-columns: auto 1fr auto; */
  width: 100%;
  height: max-content;
}

.logo-container {
  /* width: max-content !important; */
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
}

.logo__partners {
  object-fit: contain;
  margin: 0 auto;
  transform: scale(1);
  filter: grayscale(1);
  transition: all 1000ms;
}

.logo__partners:hover {
  transform: scale(1.1);
  filter: none;
}

.card {
  width: 80%;
  height: auto;
  background: none;
  display: flex;
  justify-content: center;
  align-items: center;
}

.img-card {
  width: 100%;
  display: flex;
  justify-content: center;
}
.img-card img {
  width: 100%;
  border-radius: 10px;
}

.title-card {
  height: max-content;
  min-height: 60px;
  /* max-height: max-content; */
  padding: 5px 10px 10px;
  text-align: start;
}
.title-card p {
  color: white;
}

@media  (max-width: 992px) {
  .swiper-button-next{
    display: none;
  }
  .swiper-button-prev{
    display: none;
  }
}
</style>
