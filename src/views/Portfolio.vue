<template>
  <div class="root-portfolio">
      <IMG />
    <!-- <div class="image-cont">
      <img class="bg-img" src="../assets/SVGLogo.svg" alt="">
    </div> -->
    <HelloWorld title="developments of 10 units+"></HelloWorld>
    <HelloWorld title="developments of 15 units+"></HelloWorld>
    <HelloWorld title="profitable developments of 50 units+"></HelloWorld>
    <NewFooter />
  </div>
</template>

<script>


import IMG from "@/components/IMG.vue";
import HelloWorld from "@/components/HelloWorld.vue";
import NewFooter from "@/components/NewFooter.vue";

export default {
  name: "Portfolio",
  components: {
    IMG,
    HelloWorld,
    NewFooter
  }
};
</script>

<style scoped>
  .root-portfolio{
    position: absolute;
    top: 0;
    right: 0;
    height: 100%;
    width: 80%;
    overflow-y: scroll;
    overflow-x: hidden;
    
  }
  @media (min-width: 320px) and (max-width: 1024px) {
    .root-portfolio{
      width: 100%;
    }
  }
</style>