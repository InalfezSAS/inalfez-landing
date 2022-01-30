<template>
  <div class="servicios-container" >
    <div class="servicios-content">
      <div class="title-container">
        <h2>Nuestro proyecto</h2>
        <p @click="toggleExit()">X</p>
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
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503135/14_u2vhdp.jpg",
        },
        {
          id: 1,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643388678/galeria/WhatsApp_Image_2022-01-25_at_3.00.05_PM_6_djjwtb.jpg",
        },
        {
          id: 1,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1642690646/WhatsApp_Image_2022-01-13_at_11.14.45_AM_3_lp7qor.jpg",
        },
        {
          id: 10,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643388676/galeria/WhatsApp_Image_2022-01-25_at_3.00.04_PM_4_n7r88n.jpg",
        },
        {
          id: 2,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1642690647/WhatsApp_Image_2022-01-13_at_11.14.46_AM_1_ucdi1o.jpg",
        },
        {
          id: 11,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643388676/galeria/WhatsApp_Image_2022-01-25_at_3.00.04_PM_5_ipgkou.jpg",
        },
        {
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1642690646/WhatsApp_Image_2022-01-13_at_11.14.45_AM_lqprno.jpg",
        },
        {
          id: 12,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643388676/galeria/WhatsApp_Image_2022-01-25_at_3.00.04_PM_1_elrg1u.jpg",
        },
        {
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1642690646/WhatsApp_Image_2022-01-13_at_11.14.46_AM_2_zhztbn.jpg",
        },
        {
          id: 13,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643388676/galeria/WhatsApp_Image_2022-01-25_at_3.00.04_PM_3_k7fg5i.jpg",
        },
        {
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1642690646/WhatsApp_Image_2022-01-13_at_11.14.45_AM_2_l7r3j5.jpg",
        },
        {
          id: 14,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643388676/galeria/WhatsApp_Image_2022-01-25_at_3.00.04_PM_2_ymszj1.jpg",
        },
        {
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1642690646/WhatsApp_Image_2022-01-13_at_11.14.45_AM_1_zi13hm.jpg",
        },
        {
          id: 15,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643388675/galeria/WhatsApp_Image_2022-01-25_at_3.00.03_PM_uhun6d.jpg",
        },
        {
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503124/41_qepsd2.jpg",
        },
        {
          id: 16,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1642690646/WhatsApp_Image_2022-01-13_at_11.14.46_AM_3_syl7ts.jpg",
        },
        {
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1642690645/WhatsApp_Image_2022-01-13_at_11.14.46_AM_ikif1a.jpg",
        },
        {
          id: 17,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643388675/galeria/WhatsApp_Image_2022-01-25_at_3.00.03_PM_5_uiknph.jpg",
        },
        {
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1642690645/WhatsApp_Image_2022-01-13_at_11.14.47_AM_2_flqcjl.jpg",
        },
        {
          id: 18,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643388675/galeria/WhatsApp_Image_2022-01-25_at_3.00.03_PM_3_ovon40.jpg",
        },
        {
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1642690645/WhatsApp_Image_2022-01-13_at_11.14.47_AM_kkbctr.jpg",
        },
        {
          id: 19,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643388675/galeria/WhatsApp_Image_2022-01-25_at_3.00.02_PM_6_ubcdts.jpg",
        },
        {
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1642690645/WhatsApp_Image_2022-01-13_at_11.14.47_AM_1_bcfme8.jpg",
        },
        {
          id: 20,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643388675/galeria/WhatsApp_Image_2022-01-25_at_3.00.03_PM_4_lyzkws.jpg",
        },
        {
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1642690645/WhatsApp_Image_2022-01-13_at_11.14.46_AM_4_umpi2o.jpg",
        },
        {
          id: 21,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643388675/galeria/WhatsApp_Image_2022-01-25_at_3.00.03_PM_2_mqg782.jpg",
        },
        {
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503144/33_v1kezy.jpg",
        },
        {
          id: 22,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643388675/galeria/WhatsApp_Image_2022-01-25_at_3.00.03_PM_6_uid5wa.jpg",
        },
        {
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503144/32_tooiye.jpg",
        },
        {
          id: 23,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643388675/galeria/WhatsApp_Image_2022-01-25_at_3.00.03_PM_1_r3w9ge.jpg",
        },
        {
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503142/26_apssti.jpg",
        },
        {
          id: 24,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643388674/galeria/WhatsApp_Image_2022-01-25_at_3.00.02_PM_4_tjqla8.jpg",
        },
        {
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503143/29_twpfzo.jpg",
        },
        {
          id: 25,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643388674/galeria/WhatsApp_Image_2022-01-25_at_3.00.02_PM_lhnebl.jpg",
        },
        {
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503140/24_vovl95.jpg",
        },
        {
          id: 26,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643388674/galeria/WhatsApp_Image_2022-01-25_at_3.00.01_PM_5_ek3lcm.jpg",
        },
        {
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503143/30_bmfoqy.jpg",
        },
        {
          id: 27,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643388674/galeria/WhatsApp_Image_2022-01-25_at_3.00.02_PM_5_eurd8c.jpg",
        },
        {
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503142/27_xczxjr.jpg",
        },
        {
          id: 28,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643388674/galeria/WhatsApp_Image_2022-01-25_at_3.00.02_PM_3_j64pv0.jpg",
        },
        {
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503139/25_lgrsls.jpg",
        },
        {
          id: 29,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643388674/galeria/WhatsApp_Image_2022-01-25_at_3.00.02_PM_2_vvxul0.jpg",
        },
        {
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503139/23_nr4zym.jpg",
        },
        {
          id: 30,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643494292/galeria/WhatsApp_Image_2022-01-25_at_3.00.02_PM_1_dc2esk.jpg",
        },
        {
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503138/22_z4c3sc.jpg",
        },
        {
          id: 31,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643388674/galeria/WhatsApp_Image_2022-01-25_at_3.00.01_PM_l7nmxk.jpg",
        },
        {
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503138/21_hmezao.jpg",
        },
        {
          id: 32,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643388673/galeria/WhatsApp_Image_2022-01-25_at_3.00.01_PM_1_fbgk3n.jpg",
        },
        {
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503137/19_bavyrx.jpg",
        },
        {
          id: 33,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643388673/galeria/WhatsApp_Image_2022-01-25_at_3.00.01_PM_2_nndjhw.jpg",
        },
        {
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503136/20_jmjlkb.jpg",
        },
        {
          id: 35,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643388673/galeria/WhatsApp_Image_2022-01-25_at_3.00.01_PM_7_mp13tz.jpg",
        },
        {
          id: 36,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503136/17_j44okm.jpg",
        },
        {
          id: 39,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643388672/galeria/WhatsApp_Image_2022-01-25_at_3.00.00_PM_1_qcaoe7.jpg",
        },
        {
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503135/18_ze51hj.jpg",
        },
        {
          id: 40,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643388672/galeria/WhatsApp_Image_2022-01-25_at_3.00.00_PM_5_zdl0s0.jpg",
        },
        {
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503134/16_ad3ham.jpg",
        },
        {
          id: 41,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643388672/galeria/WhatsApp_Image_2022-01-25_at_3.00.00_PM_2_yo9k7e.jpg",
        },
        {
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503133/15_igko54.jpg",
        },
        {
          id: 42,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643388672/galeria/WhatsApp_Image_2022-01-25_at_3.00.00_PM_6_v7oou1.jpg",
        },
        {
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503131/59_puyfkx.jpg",
        },
        {
          id: 43,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1643388672/galeria/WhatsApp_Image_2022-01-25_at_3.00.00_PM_4_un7bzl.jpg",
        },
        {
          id: 7,
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503130/8_dlhfjr.jpg",
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
        delay: 3000,
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
  top: 0px;
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
  height: 520px;
  display: flex;
  justify-content: center;
  align-items: center;
}

@media (max-width: 768px) {
  .partners{
    height: 420px;
  }
}
@media (max-width: 425px) {
  .partners{
    height: 320px;
  }
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
  margin: auto auto;
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
  width: 80%;
  display: flex;
  justify-content: center;
  align-items: center;
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
