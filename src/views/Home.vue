<template>
  <div class="home">   
    <div class="image-cont">
      <div class="title-cont">
        <h1>The sky is the limit</h1>
        <h6>London based real estate developers</h6>
      <img class="bg-img" src="../assets/london-night.jpg" alt="">
      </div>
    </div>
    <div class="push"></div>
    <NewFooter></NewFooter>
  </div>
</template>

<script>
import NewFooter from "@/components/NewFooter.vue";
export default {
  name: "Home",
  components: {
    NewFooter
  }
};
</script>

<style scoped>
  .home{
    /* background-color: #f2f2f2; */
    position: absolute;
    top: 0;
    right: 0;
    height: 100%;
    width: 80%;
    overflow-y: scroll;
    overflow-x: hidden;
    
  }
    .image-cont{
    height: 100%;
    width: 100%;
    overflow-y: hidden;
    overflow-x: hidden;
    margin-bottom: -10px;
  }

  h1, h6{
    z-index: 300;
    margin: 0;
    margin-top: 10%;
  }


  img{
    position: fixed;
    top: 0;
    right: 0;
    object-fit: cover;
    z-index: -200;
    filter:  saturate(60%);
    transform: scale(1.5);
    width: 100%;
    min-width: 773px;
    height: 100%;
    
  }

  .title-cont{
    width: 100%;
    overflow: hidden;
    margin: 0 auto;
    font-size: 62px;
    font-weight: 100;
    color: #fff;
    letter-spacing: 3px;
    font-family: 'Josefin Sans', sans-serif;
  }

  .push{
    width: 100%;
    margin-bottom: 10px;
  }


@media (min-width: 320px) and (max-width: 1024px) {
  .home{
    width: 100%;
    height: 100vh;
    min-height: 1280px;
  }

  img{
    position: fixed;
    top: 0;
    left: 0;
    object-fit: cover;
  }

   h1, h6{
    margin-top: 30%;
  }
}

@media (min-width: 320px) and (max-width: 1024px) {
  .home{
    max-height: 850;
  }
}
</style>
