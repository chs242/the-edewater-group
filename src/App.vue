<template>
  <div id="app">
    <div id="nav">
      <div class="logo-wrapper"><img src="../public/assets/edgewater_logo.jpg" alt=""></div>
      <router-link to="/" class="mobile">Home</router-link> 
      <router-link to="/about" class="mobile">About</router-link>
      <router-link to="/portfolio" class="mobile">Portfolio</router-link>
      <router-link to="/contact" class="mobile">Contact</router-link>
      <a href="#" class="for-mobile" @click="navbarOpen = !navbarOpen">Menu</a>
    </div>
    <div id="mySidenav" :class="{open: navbarOpen}" class="sidenav" @click="navbarOpen = !navbarOpen">
      <a href="javascript:void(0)" class="closebtn" @click.stop="navbarOpen = !navbarOpen">&times;</a>
      <router-link to="/" class="mobile" >Home</router-link> 
      <router-link to="/about" class="mobile" >About</router-link>
      <router-link to="/portfolio" class="mobile" >Portfolio</router-link>
      <router-link to="/contact" class="mobile" >Contact</router-link>
    </div>
    <router-view />
  </div>
</template>

<script>
export default {
  data() {
    return {
      navbarOpen: false,
    }
  },
  methods:{
    toggleSidebar () { if (this.$sidebar.showSidebar) { this.$sidebar.displaySidebar(false) } }
  }
}
</script>
<style>

#app {
  font-family: 'Playfair Display', serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  position: absolute;
  top: 0;
  left: 0;
  width: 20%;
  height: 100%;
  display: flex;
  flex-direction: column;
  background-color: background; -moz-linear-gradient:(80deg, rgba(24,115,204,1) 0%, rgba(28,120,218,1) 10%, rgba(255,255,255,1) 61%, rgba(255,255,255,1) 100%); /* ff3.6+ */
background: -webkit-gradient(linear, left top, left bottom, color-stop(0%, rgba(255,255,255,1)), color-stop(39%, rgba(255,255,255,1)), color-stop(90%, rgba(28,120,218,1)), color-stop(100%, rgba(24,115,204,1))); /* safari4+,chrome */
background: -webkit-linear-gradient(80deg, rgba(24,115,204,1) 0%, rgba(28,120,218,1) 10%, rgba(255,255,255,1) 61%, rgba(255,255,255,1) 100%); /* safari5.1+,chrome10+ */
background: -o-linear-gradient(80deg, rgba(24,115,204,1) 0%, rgba(28,120,218,1) 10%, rgba(255,255,255,1) 61%, rgba(255,255,255,1) 100%); /* opera 11.10+ */
background: -ms-linear-gradient(80deg, rgba(24,115,204,1) 0%, rgba(28,120,218,1) 10%, rgba(255,255,255,1) 61%, rgba(255,255,255,1) 100%); /* ie10+ */
background: linear-gradient(10deg, rgba(24,115,204,1) 0%, rgba(28,120,218,1) 10%, rgba(255,255,255,1) 61%, rgba(255,255,255,1) 100%); /* w3c */
filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#ffffff', endColorstr='#1873CC',GradientType=0 ); /* ie6-9 */
}


#nav a {
  font-weight: bold;
  color: #fff;
  margin-left: 40%;
  font-weight: bold;
  text-align: center;
  /* position: relative; */
  text-decoration: none;
  /* z-index: 1; */
  font-weight: bold;
  transition: 0.3s ease;
  border-radius: 25px;
  padding: 20px 50px 0px 50px;
  margin-right: 10px;
}

#nav a:hover{
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #2c3e50;
}

.for-mobile{
  display: none;
}

.logo-wrapper{
  height: 50%;
  width: 100%;
  padding-top: 30%;
}

img{
  width: 86%;
}

.sidenav{
  display: none;
}

@media (min-width: 320px) and (max-width: 1024px) {
  #nav {
  background-color: background; -moz-linear-gradient:(240deg, rgba(24,115,204,1) 0%, rgba(28,120,218,1) 10%, rgba(255,255,255,1) 61%, rgba(255,255,255,1) 100%); /* ff3.6+ */
                    background: -webkit-gradient(linear, left bottom, right top, color-stop(0%, rgba(255,255,255,1)), color-stop(39%, rgba(255,255,255,1)), color-stop(90%, rgba(28,120,218,1)), color-stop(100%, rgba(24,115,204,1))); /* safari4+,chrome */
                    background: -webkit-linear-gradient(240deg, rgba(24,115,204,1) 0%, rgba(28,120,218,1) 10%, rgba(255,255,255,1) 61%, rgba(255,255,255,1) 100%); /* safari5.1+,chrome10+ */
                    background: -o-linear-gradient(240deg, rgba(24,115,204,1) 0%, rgba(28,120,218,1) 10%, rgba(255,255,255,1) 61%, rgba(255,255,255,1) 100%); /* opera 11.10+ */
                    background: -ms-linear-gradient(240deg, rgba(24,115,204,1) 0%, rgba(28,120,218,1) 10%, rgba(255,255,255,1) 61%, rgba(255,255,255,1) 100%); /* ie10+ */
                    background: linear-gradient(210deg, rgba(24,115,204,1) 0%, rgba(28,120,218,1) 10%, rgba(255,255,255,1) 61%, rgba(255,255,255,1) 100%); /* w3c */
                    filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#1873CC', endColorstr='#ffffff',GradientType=0 ); /* ie6-9 */;
  position: absolute;
  top: 0%;
  width: 100vw;
  height: 70px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  z-index: 100;
}

#nav a{
  margin-left: 30%;
}
.for-mobile{
  font-family: 'Josefin Sans', sans-serif;
  font-size: 1.5em;
  display: inline;
  padding: 0;
  padding-top: 20px;
  max-width: content;
}

.mobile {
  display: none;
}

#nav a:hover{
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #2c3e50;
}

.logo-wrapper{
  width: 100%;
  padding-top: 20px;
  margin-right: 30%;
}

img{
  width: 150px;
}



/* sidenav  */
.sidenav{
  display: inline;
}
}

.sidenav {
  height: 100%;
  width: 0;
  position: fixed;
  z-index: 1000;
  top: 0;
  right: 0;
  overflow-x: hidden;
  transition: 0.5s;
  padding-top: 60px;
  font-family: 'Josefin Sans', sans-serif;
  background-color: background; -moz-linear-gradient:(260deg, rgba(24,115,204,1) 0%, rgba(28,120,218,1) 6%, rgba(255,255,255,1) 87%, rgba(255,255,255,1) 100%); /* ff3.6+ */
                    background: -webkit-gradient(linear, left top, left bottom, color-stop(0%, rgba(24,115,204,1)), color-stop(6%, rgba(28,120,218,1)), color-stop(87%, rgba(255,255,255,1)), color-stop(100%, rgba(255,255,255,1))); /* safari4+,chrome */
                    background: -webkit-linear-gradient(260deg, rgba(24,115,204,1) 0%, rgba(28,120,218,1) 6%, rgba(255,255,255,1) 87%, rgba(255,255,255,1) 100%); /* safari5.1+,chrome10+ */
                    background: -o-linear-gradient(260deg, rgba(24,115,204,1) 0%, rgba(28,120,218,1) 6%, rgba(255,255,255,1) 87%, rgba(255,255,255,1) 100%); /* opera 11.10+ */
                    background: -ms-linear-gradient(260deg, rgba(24,115,204,1) 0%, rgba(28,120,218,1) 6%, rgba(255,255,255,1) 87%, rgba(255,255,255,1) 100%); /* ie10+ */
                    background: linear-gradient(190deg, rgba(24,115,204,1) 0%, rgba(28,120,218,1) 6%, rgba(255,255,255,1) 87%, rgba(255,255,255,1) 100%); /* w3c */
                    filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#1873CC', endColorstr='#ffffff',GradientType=0 ); /* ie6-9 */
}

.open {
  width: 80% !important;
}

.sidenav a {
  padding: 20px 8px 10px 32px;
  text-decoration: none;
  font-size: 32px;
  color: #fff;
  display: block;
  transition: 0.3s;
}

.sidenav a:hover {
  color: #2c3e50;
}

.sidenav .closebtn {
  position: absolute;
  top: 0;
  right: 25px;
  font-size: 36px;
  margin-left: 50px;
}

@media (min-width: 320px) and (max-width: 580px) {
  /* Device = Most of the Smartphones Mobiles (Portrait)*/
  .logo-wrapper{
    padding-top: 20px;
    width: 100%;
    margin-right: 0px;
  }
}
</style>
