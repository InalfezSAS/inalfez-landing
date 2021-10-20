<template >
  <div class="fondo">
    <div class="container proyecto-container" >
      <div class="info-container">
        <div>
          <div class="img"></div>
        </div>
        <div></div>
      </div>

      <div class="video-container">
        <div></div>
        <div></div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Proyecto'
}
</script>
<style scoped>
  .fondo {
  width: 100%;
  height: 780px;
  /* position: absolute; */
  background-image: url("https://res.cloudinary.com/ddegh9xqy/image/upload/v1633466174/fondo_yayuma.svg");
  background-size: cover;
}

.proyecto-container {
  height: 100%;
  display: flex;
  flex-direction: column;
}

.info-container {
  height:50%;
  padding: 20px;
  display: grid;
  grid-template-columns: 1fr 1fr;
}

.img {
  width: 350px;
  height: 90%;
  background-color: brown;
}

.video-container {
  height:50%;
  padding: 20px;
  display: grid;
  grid-template-columns: 1fr 1fr;
}


</style>