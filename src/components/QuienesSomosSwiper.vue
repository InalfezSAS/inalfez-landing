<template >
    <div class="quienesSomos-container container w-full d-flex mb-5 d-lg-none">
      <div class="swiper quienesSomos p-0">
        <div class="swiper-wrapper">
          <div v-for="item in items" :key="item.id" class="swiper-slide" @click="abrir">
            <div>
              <div>
                  <div class="row row-cols-1">
                    <div class="col">
                      <img
                        src="https://res.cloudinary.com/ddegh9xqy/image/upload/v1632465595/WhatsApp_Image_2021-08-20_at_11.04.56_AM_1_fwacmf.jpg"
                        alt=""
                        class="img-quienes"
                      />
                    </div>
                    <div class="col text-start">
                      <h2>{{item.titulo}}</h2>
                      <p >
                        {{item.parrafo}}
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
    <div :class="menu">
		<div class="contenedor-mision ">
			<header class="d-flex justify-content-end mb-4">
				<label for="modal-mision" class="btn btn-primary-outline" @click="abrir">X</label>
			</header>
			<div class="contenido-mision">
				<h1>Hola</h1>
				<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Illum nesciunt inventore praesentium id maiores quasi aut recusandae quibusdam accusantium quia cum, numquam repellendus labore amet nemo nobis dolor quae voluptatibus?</p>
			</div>
		</div>
	</div>
</template>
<script>



export default {
  name: "Equipo",

  data() {
    return {
      modal:false,
      quienes:"",
      items:[
        {id:0,
        titulo:"¿Quienes somos?",
        parrafo:"Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum."},
       {id:1,
        titulo:"Misión",
        parrafo:"Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum."},
        {id:2,
        titulo:"Visión",
        parrafo:"Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum."}
      ]
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

    methods:{
    abrir(){
      this.modal = !this.modal
      console.log("hola mundo")
    }
  },

    computed: {
         menu() {
            if (this.modal) {
                return "modal-mision"
            }
            return "d-none"
        }
    },
};
</script>
<style scoped>

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
    
    .quienesSomos p {
        -webkit-box-orient: vertical;
        -webkit-line-clamp: 3;
        display: -webkit-box;
        font-size: 14px;
        overflow: hidden;
        text-align: left;
    }
    
    .quienesSomos span {
        font-size: 14px;
        color: #94C11E;
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
	background: rgba(0,0,0,0.5);
	transition: all 500ms ease;
	opacity: 1;
  z-index: 1000;
}

.modal-mision .contenedor-mision{
	width: 600px;
	height: 400px;
	padding: 20px;
	margin: auto;
	border-radius: 20px;
	background: #fff;
	box-shadow: 1px 7px 25px rgba(0,0,0,0.6);
	transition: all 500ms ease;
	position: relative;
	transform: translateY(-30%);
}

.modal-mision .contenido-mision{
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

@media (max-width:768px){
	.contenedor-mision{
		width: 95%;
		height: 95%;
	}
}
</style>