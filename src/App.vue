<template>
  <div id="app">
    <div id="nav">
      <div class="logo-wrapper"><img src="../public/assets/SmallLogo.png" alt=""></div>
      <router-link to="/" class="mobile">Home</router-link> 
      <router-link to="/about" class="mobile">About</router-link>
      <router-link to="/portfolio" class="mobile">Portfolio</router-link>
      <router-link to="/contact" class="mobile">Contact</router-link>
      <a href="#" class="for-mobile" @click="openNav">Menu</a>
    </div>
    <div id="mySidenav" class="sidenav" @click="closeNav">
      <a href="javascript:void(0)" class="closebtn" @click="closeNav">&times;</a>
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
  methods:{
    openNav: function() {
      document.getElementById("mySidenav").style.width = "80%";
    },
    closeNav: function() {
      document.getElementById("mySidenav").style.width = "0";
    },
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
 
}


#nav a {
  font-weight: bold;
  color: #2c3e50;
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
  color: #42b983;
}

#nav a.router-link-exact-active {
  color: #42b983;
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
  background-color: rgb(255, 255, 255);
  opacity: 0.5;
  position: absolute;
  top: 0%;
  width: 100vw;
  height: 70px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  z-index: 100;
 
}
.for-mobile{
  color: black;
  font-family: 'Josefin Sans', sans-serif;
  font-size: 1.5em;
  display: inline;
  padding: 0;
  padding-top: 20px;
  margin-right: 50px;
  max-width: content;
}

.mobile {
  display: none;
}

#nav a:hover{
  color: #42b983;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

.logo-wrapper{
  height: 80%;
  width: 10%;
  padding: 0px 0;
  padding-top: 10px;
  margin-left: 7%;
}

img{
  width: 100%;
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
  background-color: #111;
  overflow-x: hidden;
  transition: 0.5s;
  padding-top: 60px;
  font-family: 'Josefin Sans', sans-serif;
}

.sidenav a {
  padding: 20px 8px 10px 32px;
  text-decoration: none;
  font-size: 32px;
  color: #818181;
  display: block;
  transition: 0.3s;
}

.sidenav a:hover {
  color: #f1f1f1;
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
    width: 13%;
    padding-top: 20px;
  }
  
}
</style>
