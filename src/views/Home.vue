<template>
  <div class="home">
    <div class="title-wrapper">
      <div class="title-cont">
        <h1>The sky is the limit</h1>
        <h6>London based real estate developers</h6>
      </div>
    </div>
    <div class="image-cont">
      <img class="bg-img" src="../assets/london-night.jpg" alt="">
    </div>
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
    position: absolute;
    top: 0;
    right: 0;
    max-height: 100%;
    width: 80%;
    overflow-y: scroll;
    overflow-x: hidden;
    
  }

  .title-wrapper{
    position: absolute;
    top: 0;
    right: 0;
    height: 100%;
    width: 100%;
    z-index: 2;
  }

  .title-cont{
    width: 80%;
     margin: 300px auto;
    font-size: 62px;
    font-weight: 100;
    color: white;
    letter-spacing: 3px;
    font-family: 'Josefin Sans', sans-serif;
  }


  .image-cont{
    height: 100%;
    width: 100%;
  }

  .bg-img{
    filter:  saturate(60%);
    width: 100%;
    height: 100%;
  }

@media (min-width: 320px) and (max-width: 1024px) {
  .home{
    position: absolute;
    top: 0px;
    right: 0;
    height: 100%;
    width: 100vw;
    overflow-y: scroll;
    overflow-x: hidden;
    
  }

  .title-wrapper{
    position: absolute;
    top: 0;
    right: 0;
    height: 100%;
    width: 100%;
    z-index: 2;
  }

  .title-cont{
    width: 80%;
    margin: 300px auto;
    font-size: 62px;
    font-weight: 100;
    color: white;
    letter-spacing: 3px;
    font-family: 'Josefin Sans', sans-serif;
  }


  .image-cont{
    height: 120%;
    width: 100%;
  }

  .bg-img{
    filter:  saturate(60%);
    height: 100%;
    transform: scale(1.5);
    width: 100vw;
    min-width: 773px;
  }

}

@media (min-width: 320px) and (max-width: 580px) {
  /* Device = Most of the Smartphones Mobiles (Portrait)*/
 .bg-img{
    filter:  saturate(60%);
    height: 90%;
    transform: scale(2);
    width: 100vw;
  }
}
</style>
