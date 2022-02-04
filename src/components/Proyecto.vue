<template >
  <div class="fondo pt-5 pb-5 pb-lg-0" id="la-reserva">
    <div class="container proyecto-container pt-lg-5" >

      <div class="info-container row pt-lg-5 flex-column flex-lg-row ">
          <div class="col-xl-4 col-lg-5 col-auto container-img">
            <img src="https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503144/33_v1kezy.jpg" alt="" class="imagen">
          </div>
          <div class="col-lg-5 col-12 d-flex flex-column p-3 text-center text-lg-start">
            <h2 class="titulo">{{textos[0].titulo}}</h2>
            <p class=" texto">{{textos[0].parrafo}}</p>
            <button type="button" class="btn galeria " @click="toggleGalery">Ver galería</button>
          </div>
      </div>

      <div class="video-container row justify-content-end flex-column flex-lg-row">
          <div class="col-lg-5 col-auto align-items-lg-end align-items-center d-flex flex-column p-3 text-lg-end text-center order-2 order-lg-1">
            <h2 class="titulo">{{textos[1].titulo}}</h2>
            <p class=" texto">{{textos[1].parrafo}}</p>
            <div class="v">
              <button type="button" class="btn galeria " @click="toggleVideo">Ver video</button>
            </div>
            
          </div>
          <div class="col-xl-4  col-lg-5 col-auto  container-img order-1 order-lg-2">
            <img src="https://res.cloudinary.com/ddegh9xqy/image/upload/v1641503128/57_ssfknb.jpg" alt="" class="imagen">
          </div>
      </div>
    </div>
    <div class="galery" v-if="galery">
      <Servicios :toggle="galery" @toggleClose="toggleClose"/>
    </div>
    <div class="galery" v-if="video" @click="toggleVideo">
      <ModalVideo />
    </div>
  </div>
</template>
<script>
import Servicios from '@/components/Servicios.vue'
import ModalVideo from '@/components/ModalVideo.vue'
export default {
  name: 'Proyecto',
  components:{
    Servicios,
    ModalVideo
  },
  data() {
    return {
      galery:false,
      video:false,
      fondo:"",
      textos:[
        {
          id:0,
          titulo:"Nuestro proyecto",
          parrafo:"Inalfez sas tiene el gusto de presentarle a Urbanización La Reserva, ubicada en la zona urbana de Cumaral - Meta y a tan solo tres (3) cuadras del parque central. Consta de 19.5 hectáreas, se compone de 812 lotes distribuidos en 33 manzanas para que construya la casa de sus sueños; con amplias zonas verdes de paisajismo, arborizaciøn y calles amplias conformadas con sus sardineles."
        },
        {id:1,
          titulo:"Urbanización la Reserva",
          parrafo:"Los lotes cuentan con gran variedad de medidas y valores. La urbanización está dividida en dos (2) zonas: El área comercial y el área residencial todos diseñados para 2 pisos más altillo con terreno acto para 3 pisos. Los lotes se entregan con escrituras públicas e individuales y disponibilidad de servicios públicos (agua, alcantarillado y energía, urbanismo completamente terminado para el 2024."
        },
      ]
    }
  },

  methods:{
    toggleGalery(){
      this.galery = !this.galery
    },
    toggleVideo(){
      this.video = !this.video
    },
    toggleClose(status){
      this.galery = status
    }
  }
}
</script>
<style scoped>



.galery{
   width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  position: fixed;
  background: rgba(0, 0, 0, 0.671);
  z-index: 1000;
  top: 0;
  left: 0;
}

  .fondo {
  width: 100%;
  height: auto;
  background: #0d6efd;
}

.info-container{
  padding-left:100px;
}

.video-container{
  padding-right: 100px;
  position: relative;
  top: -100px;
}

.container-img{
  padding: 30px 55px;
}

.imagen{
  height: 450px;
  width: 100%;
  object-fit: cover;
  border-radius: 25px;
  position: relative;
  top: -170px;
  border: 5px solid white;
  box-shadow:  20px 20px 60px #0000001c,
             -20px -20px 60px #0000001c;
}

.galeria{
  background: #70C217;
  color:white ;
  font-size: 14px;
  font-weight: 500;
  padding: 10px 30px;
  width: inherit;
  border-radius: 50px;
   box-shadow: -10px 12px 23px -11px rgba(57, 57, 57, 0.67);
  -webkit-box-shadow: -10px 12px 23px -11px rgba(57, 57, 57, 0.67);
  -moz-box-shadow: -10px 12px 23px -11px rgba(57, 57, 57, 0.67);
}

.titulo{
  color: white;
  font-weight: 600;
}

.texto{
  color: white;
  font-size: 14px;
  font-weight: 300;
}

.proyecto-container {
  height: 100%;
  display: flex;
  flex-direction: column;
  margin-bottom: -200px !important;
}

@media (max-width:1400px) {
  .info-container{
    padding-left: 0;
  }

  .video-container{
    padding-right: 0;
  }

  .container-img{
    padding: 30px;
  }
}

@media (max-width:992px) {
  .imagen{
  top: 0px;
}
.video-container{
  top: 0px;
}

.proyecto-container {
  margin-bottom: 0 !important;
}

.v{
  width: 100%;
}
}

</style>