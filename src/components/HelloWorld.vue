<template>
  <div class="hello">
    <div class="head-wrapper">    
      <h2>{{ title }}</h2>
    </div>
    <div class="sub-head-wrapper">
      <h4>This is where your text starts. You can click here and start typing. Et dolore magnam aliquam quaerat voluptatem ut enim ad minima veniam quis nostrum exercitationem ullam corporis.</h4>
    </div>
    <ul>
      <li>
        <img class="bg-img" src="../assets/SVGLogo.svg" alt="">
        <p>name of development</p>
      </li>
      <li>
        <img class="bg-img" src="../assets/SVGLogo.svg" alt="">
        <p>name of development</p>
      </li>
      <li>
        <img class="bg-img" src="../assets/SVGLogo.svg" alt="">
        <p>name of development</p>
      </li>
      <li>
        <img class="bg-img" src="../assets/SVGLogo.svg" alt="">
        <p>name of development</p>
      </li>
      <li>
        <img class="bg-img" src="../assets/SVGLogo.svg" alt="">
        <p>name of development</p>
      </li>
    </ul>
    
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props:[
    "title"
  ]
 
};
</script>


<style scoped>

.head-wrapper{
  margin-left: 100px;
  width: 100%;
 text-align: left;
 font-weight: 200;
}

.head-wrapper:after{
    content:'';
    display:block;
    border:0.5px solid #ffc000;
    position: absolute;
    /* top: 0px; */
    margin-left: 100px;
    width: 100px;
    left: 0;
    z-index: 3;
}

.sub-head-wrapper{
  text-align: left;
  width: 700px;
  margin-left: 100px;
  padding: 0;
  color: #acacac;
 font-size: 16px;
 
}

h4{
 font-weight: 200;
}

ul {
  list-style-type: none;
  margin-left: 100px;
  padding: 0;
  display: flex;
  flex-flow: row wrap;
  justify-content: left;
}

img{
  width: 100%;
}

li {
  height: 250px;
  width: 250px;
  background-color: azure;
  margin: 20px 40px 20px 0px;
}
a {
  color: #42b983;
}

@media (min-width: 500px) and (max-width: 520px) {
    .hello{
      margin-top: 70px;
    }
}
@media (min-width: 580px) and (max-width: 610px) {
    .hello{
      margin-top: 50px;
    }
}
@media (min-width: 320px) and (max-width: 1024px) {
    .head-wrapper{
      margin: 0;
    }

    .sub-head-wrapper{
      width: 100%;
      margin: 0;
    }
    h2, h4{
      margin: 0;
      padding: 10px 20px;
      text-align: center;
    }

    .head-wrapper:after{
      margin-left: 45%;
    }

    ul{
      justify-content: center;
      margin: 0;
    }

    li{
      width: 80%;
      height: 65vw;
      margin: 20px 0;
    }
    
}
@media (min-width: 950px) and (max-width: 1024px) {
    .head-wrapper:after{
      margin-left: 45%;
    }
}
@media (min-width: 750px) and (max-width: 950px) {
    .head-wrapper:after{
      margin-left: 40%;
    }
}
@media (min-width: 550px) and (max-width: 750px) {
    .head-wrapper:after{
      margin-left: 40%;
    }
}
@media (min-width: 320px) and (max-width: 550px) {
    .head-wrapper:after{
      margin-left: 38%;
    }
}
</style>
