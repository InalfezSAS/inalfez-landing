<template >
    <div class="quienesSomos-container container w-full d-flex mb-5 d-lg-none">
      <div class="swiper quienesSomos p-0">
        <div class="swiper-wrapper">
          <div class="swiper-slide">
            <div class="" style="">
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
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Impedit provident corporis delectus perspiciatis,
                    voluptatibus doloribus cum accusamus earum. Eum rerum,
                    maxime labore ipsa quibusdam vel quaerat odio perferendis in
                    ea.
                  </p>
                  <span>Ver más...</span>
                </div>
              </div>
            </div>
          </div>
          <div class="swiper-slide">
            <div class="">
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
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Impedit provident corporis delectus perspiciatis,
                    voluptatibus doloribus cum accusamus earum. Eum rerum,
                    maxime labore ipsa quibusdam vel quaerat odio perferendis in
                    ea.
                  </p>
                  <span>Ver más...</span>
                </div>
              </div>
            </div>
          </div>
          <div class="swiper-slide">
            <div class="">
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
                    Impedit provident corporis delectus perspiciatis,
                    voluptatibus doloribus cum accusamus earum. Eum rerum,
                    maxime labore ipsa quibusdam vel quaerat odio perferendis in
                    ea.
                  </p>
                  <span>Ver más...</span>
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
  name: "Equipo",
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

</style>