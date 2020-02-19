<template>
    <div class="root-footer">
        <div class="footer">
            <div class="footer-site-links">
            <div class="footer-site-links-container">
                <p>Site-Links |</p>
                <router-link to="/">Home</router-link>
                <router-link to="/about">About</router-link>
                <router-link to="/portfolio">Portfolio</router-link>
                <router-link to="/contact">Contact</router-link>
            </div>
            </div>
            <div class="footer-legal">
            &copy;Copywrite. Built and maintained by SoftwareBuild LTD 2020 - 2021 | All Rights Reserved 
            </div>
        </div>
        <div class="footer-image">
            <a href="#"><img src="../assets/SVGLogo.svg" height="85"></a>
        </div>
  </div>
</template>

<script>
export default {
  name: "Footer"
};
</script>

<style scoped>

.root-footer{
    display: flex;
    width: 100%;
    height: 100px;
    background-color: #f2f2f2;
}

.footer{
  width: 100%;
  height: 100px;
  
  display: flex;
  flex-direction: column;
  z-index: 100;
}

.footer-site-links{
  height: 70%;
  /* border: 1px solid black; */
}
p{
  width: 100px;
}
.footer-site-links-container {
  display: flex;
  justify-content: left;
  width: 100%;
  padding-top: 30px
}
.footer-site-links-container a{
  padding: 0 30px 0 0;
  color: #151515;
}

.footer-legal{
  text-align: left;
  height: 30%;
  width: 100%;
  padding-left: 8px;
  /* border: 1px solid black; */

}

p{
  margin: 0px;
}

.footer-image{
    width: 30%;
    /* background-color: #f2f2f2; */
    
}

img{
    padding-top: 10px;
}

@media (min-width: 320px) and (max-width: 1024px) {
  .root-footer{
    position: absolute;
    left: 0;
    z-index: 100;
    flex-direction: row-reverse;
    height: 150px;
  }
  .footer-image{
    z-index: 100;
    background-color: #f2f2f2;
  }

  .footer{
    background-color: #f2f2f2;
    height: 150px;
  }
  
}

</style>