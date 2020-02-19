<template>
    <div class="image-cont">
      <img class="bg-img" src="../assets/london.jpg" alt="Image">
    </div>
</template>

<script>
export default {
    name: "IMG"
}
</script>

<style scoped>
  
  .image-cont{
    z-index: 100;
    min-height: 350px;
    width: 100%;
  }

  img{
    height: 100%;
    width: 100%;
  }

  .bg-img{
    filter: opacity(60%);
  }

  @media (min-width: 320px) and (max-width: 1024px) {
    .image-cont{
      min-height: 350px;
    }

    img{
      
      /* transform: scale(2); */
    }
  }  

  @media (min-width: 730px) and (max-width: 930px) {
    .image-cont{
      min-height: 450px;
    }
     img{
      transform: scale(2);
    }
  }
  @media (min-width: 610px) and (max-width: 730px) {
    .image-cont{
      min-height: 400px;
    }
     img{
      transform: scale(2);
    }
  }
  @media (min-width: 520px) and (max-width: 610px) {
    .image-cont{
      min-height: 380px;
    }
     img{
      transform: scale(3);
    }
  }
  @media (min-width: 320px) and (max-width: 520px) {
    .image-cont{
      min-height: 400px;
    }
     img{
      transform: scale(4);
    }
  }
</style>