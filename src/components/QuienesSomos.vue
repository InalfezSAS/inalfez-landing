<template >
    <div class="container w-full quienes d-none d-lg-block" id="quienes-somos">
      <div class="d-flex justify-content-between">
          <div class=" card-container" style="width: 350px" v-for=" card in cardInfo" :key="card.id" @click="toggleModal(card.title, card.text)">
            <div class="row row-cols-1">
              <div class="col">
                <img
                  :src="card.image"
                  alt=""
                  class="img-quienes"
                />
              </div>
              <div class="col text-start">
                <h2>{{card.title}}</h2>
                <p class="con">
                  {{card.text}}
                </p>
                <span>Ver más...</span>
              </div>
            </div>
          </div>
      </div>
      <div class="ventana" v-if="statusModal">
        <div class="tarjetica">
          <header class="d-flex justify-content-end">
        <label for="modal-mision" class="btn btn-primary-outline" @click="toggleModal"
          >X</label
        >
      </header>
          <h2 class="mt-0 mb-4">{{currentTitle}}</h2>
          <p class="sin">{{currentText}}</p>
        </div>
      </div>
    </div>
</template>
<script>
export default {
  name: 'QuienesSomos',
  data(){
    return {
      currentTitle: "",
      currentText: "",
      statusModal: false,
      cardInfo: [
        {id: 0,
          title: "Quienes somos",
          // image: require("../assets/hola.jpg"),
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1632465595/WhatsApp_Image_2021-08-20_at_11.04.56_AM_1_fwacmf.jpg",
          text:"Nuestra empresa INVERSIONES ALFÉREZ FERNÁNDEZ S.A.S (Inalfez s.a.s), es una empresa legalmente constituida identificada con número NIT 901228858-0. el cual abrió sus ofertas al mercado el 26 de octubre 2018, es una empresa dedicada a la compra y venta de inmuebles, ejecución de proyectos propios y de terceros de vivienda, urbanismos y toda clase de ejecución de obras civiles, la cual comenzó la operación de un nuevo proyecto a finales de noviembre del 2020, ofreciendo al mercado su nuevo proyecto llamado URBANIZACIÓN LA RESERVA, ubicada en la zona urbana de Cumaral - Meta."
        },
        {id: 1,
          title: "Mision",
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641541408/business-team-planning-marketing-strategy_ocrn2g.jpg",
          text:"INVERSIONES ALFEREZ Y FERNANDEZ S.A.S, es una empresa colombiana, con capital   cien por ciento colombiano, que contribuye con el emprendimiento nacional, con un equipo humano de trabajo comprometido; dedicada a la comercialización de bienes inmuebles, ejecución de proyectos propios y de terceros de construcción, con altos estándares de calidad, generando rentabilidad a los socios, contratantes e inversionistas."
        },
        {id: 1,
          title: "Visión",
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1641541408/cheerful-business-people-job-is-done-group-office-workers-happy-hit-their-own-records-being-successful_jla4rn.jpg",
          text:"Posicionarse en el sector para el año 2024, destacarse por el cumplimiento a sus clientes, innovación y cuidado de los recursos naturales; ser la preferida por los colombianos al momento de pensar en inversión de bienes inmuebles y contratación en la ejecución de proyectos."
        },
      ]
    }
  },
  methods:{

    toggleModal(title, text){
      this.statusModal = !this.statusModal
      this.currentTitle = title
      this.currentText = text
    }

  }
}
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
  width: 60%;
  height: max-content;
}

  .quienes {
    margin-bottom: 80px;
}

.quienes .col {
    padding: 0 25px;
}

.quienes h2 {
  margin-top: 15px;
    font-weight: 700;
    font-size: 25px;
}

.img-quienes {
    width: 100%;
    border-radius: 20px;
}

.con{
    -webkit-box-orient: vertical;
    -webkit-line-clamp: 3;
    display: -webkit-box;
    font-size: 14px;
    overflow: hidden;
    text-align: left;
}

.quienes span {
    font-size: 14px;
    color: #94C11E;
    font-weight: 500;
}

.label-quienes {
  cursor: pointer;
}

.sin{
    font-size: 14px;
    text-align: left;
}

@media (max-width: 1200px) {
  .card-container {
    width: 300px !important;
  }
}
</style>