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
                <p>
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
          <p>{{currentText}}</p>
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
          text:"Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum."
        },
        {id: 1,
          title: "Mision",
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1632465595/WhatsApp_Image_2021-08-20_at_11.04.56_AM_1_fwacmf.jpg",
          text:"hermano"
        },
        {id: 1,
          title: "vision",
          image: "https://res.cloudinary.com/ddegh9xqy/image/upload/v1632465595/WhatsApp_Image_2021-08-20_at_11.04.56_AM_1_fwacmf.jpg",
          text:"tio"
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

.quienes p {
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

@media (max-width: 1200px) {
  .card-container {
    width: 300px !important;
  }
}
</style>