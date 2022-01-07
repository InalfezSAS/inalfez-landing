<template>
    <div >
        <iframe idth="896" height="506" src="https://www.youtube.com/embed/HiKpUgwsvoI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
</template>
<script>
export default {
    components:{}
}
</script>
<style scoped>
    @media screen and (max-width: 1080px) {
  .video{
    width: 560px;
    height: 315px;
  }
}

@media screen and (max-width: 650px) {
  .video{
    width: 460px;
    height: 260px;
  }
}

@media screen and (max-width: 550px) {
  .video{
    width: 360px;
    height: 220px;
  }
}

@media screen and (max-width: 375px) {
  .video{
    width: 300px;
    height: 175px;
  }
}
</style>