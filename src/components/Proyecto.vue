<template >
  <div>
    <!-- <div class="proyecto d-flex justify-content-center">
            <div class="fondo"></div>
            <div class="proyecto-p1">
                <div class="img-p1">
                </div>
                <div class="info-p1"></div>
            </div>
        </div> -->
  </div>
</template>
<script>
export default {
  name: 'Proyecto'
}
</script>
<style scoped>
  .proyecto .fondo {
  position: absolute;
  background-image: url("https://res.cloudinary.com/ddegh9xqy/image/upload/v1633466174/fondo_yayuma.svg");
  width: 100%;
  max-width: 1920px;
  height: 780px;
  background-size: cover;
  z-index: 0;
}

.proyecto-p1 {
  z-index: 100;
}

.img-p1 {
  height: 100%;
  width: 370px;
  background-image: url("https://res.cloudinary.com/ddegh9xqy/image/upload/v1633467938/foto_1_jvjen2.png");
  background-size: cover;
}
</style>