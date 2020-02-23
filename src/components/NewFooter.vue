<template>
    <div class="root-footer">
        <div class="footer-1">
            <div class="legal-cont">
            &copy;Powered by  
            </div>
            <div class="img-cont">
            <a href="#"><img src="../assets/SVGLogo.svg" alt="SoftwareBuild Logo" height="50px"></a>
            </div>
        </div>
        <div class="footer-2">
            <router-link to="/">Home</router-link>
            <router-link to="/about">About</router-link>
            <router-link to="/portfolio">Portfolio</router-link>
            <router-link to="/contact">Contact</router-link>
        </div>
  </div>
</template>

<script>
export default {
  name: "NewFooter"
};
</script>

<style scoped>

.root-footer{
    display: flex;
    flex-flow:column;
    width: 100%;
}

.footer-1{
  width: 100%;
  height: 60px;
  padding-top: 10px;
  display: flex;
  flex-direction: row;
  justify-content: center;
  z-index: 100;
  background-color: #f2f2f2;
}
.legal-cont{
    padding-top: 15px;
}

.img-cont{
  width: 80px;
}
.footer-2 a{
  padding: 0 10px 0 10px;
  color: #151515;
  text-decoration: none;
}

.footer-2{
  text-align: center;
  height: 35px;
  width: 100%;
  padding-left: 8px;
  padding-top: 15px;
  z-index: 100;
  background-color: #f2f2f2;
}


@media (min-width: 320px) and (max-width: 1024px) {
  .img-cont{
  width: 80px;
}
  
}

</style>