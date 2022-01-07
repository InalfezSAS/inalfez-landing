<template >
  <div class="quienesSomos-container container w-full d-flex mb-5 d-lg-none" id="quienes-somos">
    <div class="swiper quienesSomos p-0">
      <div class="swiper-wrapper">
        <div
          v-for="item in items"
          :key="item.id"
          class="swiper-slide"
          @click="toggleModalS(item.title, item.text)"
        >
          <div>
            <div>
              <div class="row row-cols-1">
                <div class="col">
                  <img
                    :src="item.image"
                    alt=""
                    class="img-quienes"
                  />
                </div>
                <div class="col text-start">
                  <h2>{{ item.title }}</h2>
                  <p class="con">
                    {{ item.text }}
                  </p>
                  <span>Ver más...</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="ventana" v-if="statusModal">
    <div class="tarjetica">
      <header class="d-flex justify-content-end">
        <label for="modal-mision" class="btn btn-primary-outline" @click="toggleModalS"
          >X</label
        >
      </header>
      <div class="contenido-mision">
        <h1>{{currentTitle}}</h1>
        <p class="sin">
          {{currentText}}
        </p>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Equipo",

  data() {
    return {
      statusModal: false,
      currentTitle: "",
      currentText: "",
      items: [
        {
          id: 0,
          title: "¿Quienes somos?",
          image:"https://res.cloudinary.com/ddegh9xqy/image/upload/v1632465595/WhatsApp_Image_2021-08-20_at_11.04.56_AM_1_fwacmf.jpg",
          text:
            "Nuestra empresa INVERSIONES ALFÉREZ FERNÁNDEZ S.A.S (Inalfez s.a.s), es una empresa legalmente constituida identificada con número NIT 901228858-0. el cual abrió sus ofertas al mercado el 26 de octubre 2018, es una empresa dedicada a la compra y venta de inmuebles, ejecución de proyectos propios y de terceros de vivienda, urbanismos y toda clase de ejecución de obras civiles, la cual comenzó la operación de un nuevo proyecto a finales de noviembre del 2020, ofreciendo al mercado su nuevo proyecto llamado URBANIZACIÓN LA RESERVA, ubicada en la zona urbana de Cumaral - Meta.",
        },
        {
          id: 1,
          title: "Misión",
          image:"https://res.cloudinary.com/ddegh9xqy/image/upload/v1641541408/business-team-planning-marketing-strategy_ocrn2g.jpg",
          text:
            "INVERSIONES ALFEREZ Y FERNANDEZ S.A.S, es una empresa colombiana, con capital   cien por ciento colombiano, que contribuye con el emprendimiento nacional, con un equipo humano de trabajo comprometido; dedicada a la comercialización de bienes inmuebles, ejecución de proyectos propios y de terceros de construcción, con altos estándares de calidad, generando rentabilidad a los socios, contratantes e inversionistas.",
        },
        {
          id: 2,
          title: "Visión",
          image:"https://res.cloudinary.com/ddegh9xqy/image/upload/v1641541408/cheerful-business-people-job-is-done-group-office-workers-happy-hit-their-own-records-being-successful_jla4rn.jpg",
          text:
            "Posicionarse en el sector para el año 2024, destacarse por el cumplimiento a sus clientes, innovación y cuidado de los recursos naturales; ser la preferida por los colombianos al momento de pensar en inversión de bienes inmuebles y contratación en la ejecución de proyectos.",
        },
      ],
    };
  },

  methods:{
    toggleModalS(title, text){
      this.statusModal = !this.statusModal
      this.currentTitle = title
      this.currentText = text
    }
  },


  mounted() {
    const Swiper = window.Swiper;

    new Swiper(".quienesSomos", {
      spaceBetween: 30,
      centeredSlides: true,
      loop: true,
      autoplay: {
        delay: 2500,
        disableOnInteraction: false,
      },
      pagination: {
        el: ".swiper-pagination",
        clickable: true,
      },
      navigation: {
        nextEl: ".swiper-button-next",
        prevEl: ".swiper-button-prev",
      },
    });
  },

  computed: {
    menu() {
      if (this.modal) {
        return "modal-mision";
      }
      return "d-none";
    },
  },
};
</script>
<style scoped>

.ventana {
  top: 0;
  left: 0;
  width: 100%;
  height:100%;
  position: fixed;
  background: rgba(0, 0, 0, 0.432);
  z-index: 1000;
  display: flex;
  justify-content: center;
  align-items: center;
}

.ventana label{
  padding: 0;
  margin-bottom: 1px !important;
}

.tarjetica{
  padding: 25px;
  border-radius: 25px;
  background: white;
  width: 85%;
  height: max-content;
}


.quienesSomos-container {
  width: 100%;
  height: max-content;
}

.quienesSomos {
  max-width: 450px;
  min-width: 300px;
  height: max-content;
}

.quienesSomos .swiper-wrapper .swiper-slide {
  width: 100%;
  height: max-content;
  display: flex;
  text-align: center;
  font-size: 18px;
  background: #fff;
}

.quienesSomos .col {
  padding: 0 25px;
}

.quienesSomos h2 {
  font-size: 25px;
  margin-top: 15px;
  font-weight: 700;
}

.con {
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 3;
  display: -webkit-box;
  font-size: 14px;
  overflow: hidden;
  text-align: left;
}

.sin{
    font-size: 14px;
    text-align: left;
}

.quienesSomos span {
  font-size: 14px;
  color: #94c11e;
  font-weight: 500;
}

.img-quienes {
  width: 100%;
  border-radius: 20px;
}

.label-quienes {
  cursor: pointer;
}

.modal-mision {
  width: 100vw;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  position: fixed;
  top: 0;
  left: 0;
  background: rgba(0, 0, 0, 0.5);
  transition: all 500ms ease;
  opacity: 1;
  z-index: 1000;
}

.modal-mision .contenedor-mision {
  width: 600px;
  height: 400px;
  padding: 20px;
  margin: auto;
  border-radius: 20px;
  background: #fff;
  box-shadow: 1px 7px 25px rgba(0, 0, 0, 0.6);
  transition: all 500ms ease;
  position: relative;
  transform: translateY(-30%);
}

.modal-mision .contenido-mision {
  width: 100%;
}

.modal-mision .contenido-mision h1 {
  font-weight: 700;
  font-size: 25px;
  margin-bottom: 20px;
}

.modal-mision .contenido-mision p {
  font-size: 18px;
}

/* #modal-mision:checked ~ .modal-mision .contenedor-mision{
	transform: translateY(0%);
} */

@media (max-width: 768px) {
  .contenedor-mision {
    width: 95%;
    height: 95%;
  }
}
</style>