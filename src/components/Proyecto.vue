<template >
  <div class="fondo pt-5" id="la-reserva">
    <div class="container proyecto-container pt-5" >
      <div class="info-container row pt-5 flex-column flex-lg-row">
          <div class="col-xl-4 col-5 container-img">
            <img src="https://res.cloudinary.com/ddegh9xqy/image/upload/v1634895053/WhatsApp_Image_2021-06-08_at_9.35.07_AM_7_toutii.jpg" alt="" class="imagen">
          </div>
          <div class="col-5 d-flex flex-column p-3 text-start">
            <h2 class="titulo">{{textos[0].titulo}}</h2>
            <p class=" texto">{{textos[0].parrafo}}</p>
            <button type="button" class="btn galeria ">Ver galería</button>
          </div>
      </div>

      <div class="video-container row justify-content-end flex-column flex-lg-row">
          <div class="col-5 align-items-end d-flex flex-column p-3 text-end">
            <h2 class="titulo">{{textos[0].titulo}}</h2>
            <p class=" texto">{{textos[0].parrafo}}</p>
            <button type="button" class="btn galeria ">Ver video</button>
          </div>
          <div class="col-xl-4  col-5 container-img">
            <img src="https://res.cloudinary.com/ddegh9xqy/image/upload/v1634895053/WhatsApp_Image_2021-06-08_at_9.35.07_AM_7_toutii.jpg" alt="" class="imagen">
          </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Proyecto',
  data() {
    return {
      fondo:"",
      textos:[
        {
          titulo:"Soy el titulo",
          parrafo:"The holaaaaaaa chunk of Lorem Ipsum used since the 1500s is reproduced below for those interested. Sections 1.10.32 and 1.10.33 from de Finibus Bonorum et Malorum by Cicero are also reproduced in their exact original form, accompanied by English versions from the 1914 translation by H. Rackham."
        },
        {
          titulo:"Soy el titulo2",
          parrafo:"222The standard chunk of Lorem Ipsum used since the 1500s is reproduced below for those interested. Sections 1.10.32 and 1.10.33 from de Finibus Bonorum et Malorum by Cicero are also reproduced in their exact original form, accompanied by English versions from the 1914 translation by H. Rackham."
        },
      ]
    }
  },
}
</script>
<style scoped>
  .fondo {
  width: 100%;
  height: auto;
  background: #0d6efd;
  background-size: cover;
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
  margin-bottom: -200px;
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

@media (max-width:1200px) {
  
}

</style>