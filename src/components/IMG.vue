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
</style>