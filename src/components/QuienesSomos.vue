<template >
    <div class="container w-full quienes d-none d-lg-block">
      <div class="d-flex justify-content-between">
        <input type="checkbox" id="modal-quienes">
        <ModalQuienesSomos />
	      <label for="modal-quienes" class="label-quienes">
          <div class=" card-container" style="width: 350px">
            <div class="row row-cols-1">
              <div class="col">
                <img
                  src="https://res.cloudinary.com/ddegh9xqy/image/upload/v1632465595/WhatsApp_Image_2021-08-20_at_11.04.56_AM_1_fwacmf.jpg"
                  alt=""
                  class="img-quienes"
                />
              </div>
              <div class="col text-start">
                <h2>¿Quiénes somos?</h2>
                <p>
                  Lorem ipsum dolor sit amet consectetur adipisicing elit. Impedit
                  provident corporis delectus perspiciatis, voluptatibus doloribus
                  cum accusamus earum. Eum rerum, maxime labore ipsa quibusdam vel
                  quaerat odio perferendis in ea.
                </p>
                <span>Ver más...</span>
              </div>
            </div>
          </div>
        </label>

        <div class=" card-container" style="width: 350px">
          <div class="row row-cols-1">
            <div class="col">
              <img
                src="https://res.cloudinary.com/ddegh9xqy/image/upload/v1632465595/WhatsApp_Image_2021-08-20_at_11.04.56_AM_1_fwacmf.jpg"
                alt=""
                class="img-quienes"
              />
            </div>
            <div class="col text-start">
              <h2>Misión</h2>
              <p>
                Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                Distinctio dolores nesciunt tenetur minima voluptate molestias
                nemo veritatis cupiditate in eos enim sint iusto, optio,
                eligendi facilis maiores quas necessitatibus officiis!
              </p>
              <span>Ver más...</span>
            </div>
          </div>
        </div>

        <div class=" card-container" style="width: 350px">
          <div class="row row-cols-1">
            <div class="col">
              <img
                src="https://res.cloudinary.com/ddegh9xqy/image/upload/v1632465595/WhatsApp_Image_2021-08-20_at_11.04.56_AM_1_fwacmf.jpg"
                alt=""
                class="img-quienes"
              />
            </div>
            <div class="col text-start">
              <h2>Visión</h2>
              <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
                Perspiciatis possimus autem pariatur placeat consectetur! Rem
                saepe earum a mollitia labore, soluta quis! Nihil eum, tempore
                vel natus excepturi labore officiis.
              </p>
              <span>Ver más...</span>
            </div>
          </div>
        </div>
      </div>
    </div>
</template>
<script>

import ModalQuienesSomos from './Modales/ModalQuienesSomos.vue'

export default {
  name: 'QuienesSomos',
  components: {
    ModalQuienesSomos,
  },
}
</script>
<style scoped>
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
    width: 300px;
  }
}
</style>