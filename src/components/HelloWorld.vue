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
}

h2 {
 width: 100%;
 text-align: left;
 font-size: 28px;
 font-weight: 200;
 margin-bottom: 10px;;
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
  /* border: 1px solid black; */
  text-align: left;
  width: 700px;
  margin-left: 100px;
  padding: 0;
}

h4{
 color: #acacac;
 font-size: 16px;
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
</style>
