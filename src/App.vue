<template>
  <div id="app">
    <div id="nav">
      <div class="logo"></div>
      <router-link to="/">Home</router-link> 
      <router-link to="/about">About</router-link>
      <router-link to="/portfolio">Portfolio</router-link>
      <router-link to="/contact">Contact</router-link>
    </div>
    <router-view />
  </div>
</template>

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
  padding: 10px 50px;
  margin-right: 10px;
}

#nav a:hover{
  color: #42b983;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

.logo{
  height: 60%;
  width: 100%;
}
</style>
