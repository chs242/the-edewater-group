<template>
  <div class="hello">
    <div class="head-wrapper">    
      <h2>{{ title }}</h2>
    </div>
    <div class="sub-head-wrapper">
      <h4>This is where your text starts. You can click here and start typing. Et dolore magnam aliquam quaerat voluptatem ut enim ad minima veniam quis nostrum exercitationem ullam corporis.</h4>
    </div>
    <!--<ul>
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
    </ul> -->

    <div class="container">
      <div class="content">
          <a>
            <div class="content-overlay"></div>
            <img class="content-image" src="https://images.unsplash.com/photo-1433360405326-e50f909805b3?ixlib=rb-0.3.5&q=80&fm=jpg&crop=entropy&w=1080&fit=max&s=359e8e12304ffa04a38627a157fc3362">
            <div class="content-details fadeIn-top">
              <h3>This is a title</h3>
              <p>This is a short description</p>
            </div>
          </a>
        </div>
    </div>
    <div class="container">
      <div class="content">
          <a>
            <div class="content-overlay"></div>
            <img class="content-image" src="https://images.unsplash.com/photo-1433360405326-e50f909805b3?ixlib=rb-0.3.5&q=80&fm=jpg&crop=entropy&w=1080&fit=max&s=359e8e12304ffa04a38627a157fc3362">
            <div class="content-details fadeIn-top">
              <h3>This is a title</h3>
              <p>This is a short description</p>
            </div>
          </a>
        </div>
    </div>
    <div class="container">
      <div class="content"  @click="isActive = !isActive">
          <a>
            <div class="content-overlay" :class="{contentOverlayActive: isActive}"></div>
            <img class="content-image" src="https://images.unsplash.com/photo-1433360405326-e50f909805b3?ixlib=rb-0.3.5&q=80&fm=jpg&crop=entropy&w=1080&fit=max&s=359e8e12304ffa04a38627a157fc3362">
            <div class="content-details fadeIn-top" :class="{contentDetailsActive: isActive}">
              <h3>This is a title</h3>
              <p>This is a short description</p>
            </div>
          </a>
        </div>
    </div>
    
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props:[
    "title"
  ],
  data(){
    return{
      isActive: false
    }
  }
 
};
</script>


<style scoped>



.main-title{
  color: #2d2d2d;
  text-align: center;
  text-transform: capitalize;
  padding: 0.7em 0;
}

.container{
  padding: 1em 0;
  float: left;
  width: 50%;
}
@media screen and (max-width: 640px){
  .container{
    display: block;
    width: 100%;
  }
}

@media screen and (min-width: 900px){
  .container{
    width: 33.33333%;
  }
}

.container .title{
  color: #1a1a1a;
  text-align: center;
  margin-bottom: 10px;
}

.content {
  position: relative;
  width: 90%;
  max-width: 400px;
  margin: auto;
  overflow: hidden;
}

.content .content-overlay {
  background: rgba(0,0,0,0.7);
  position: absolute;
  height: 99%;
  width: 100%;
  left: 0;
  top: 0;
  bottom: 0;
  right: 0;
  opacity: 0;
  -webkit-transition: all 0.4s ease-in-out 0s;
  -moz-transition: all 0.4s ease-in-out 0s;
  transition: all 0.4s ease-in-out 0s;
}

.content-image{
  width: 100%;
}

.content-details {
  position: absolute;
  text-align: center;
  padding-left: 1em;
  padding-right: 1em;
  width: 100%;
  top: 50%;
  left: 50%;
  opacity: 0;
  -webkit-transform: translate(-50%, -50%);
  -moz-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
  -webkit-transition: all 0.3s ease-in-out 0s;
  -moz-transition: all 0.3s ease-in-out 0s;
  transition: all 0.3s ease-in-out 0s;
}

.contentDetailsActive{
   z-index: 1000;
  top: 50%;
  left: 50%;
  opacity: 1 !important;
}

.contentOverlayActive{
  opacity: 1 !important;
}

.content-details h3{
  color: #fff;
  font-weight: 500;
  letter-spacing: 0.15em;
  margin-bottom: 0.5em;
  text-transform: uppercase;
}

.content-details p{
  color: #fff;
  font-size: 0.8em;
}

.fadeIn-top{
  top: 20%;
}

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

/*h4{
 font-weight: 200;
}

p{
  background-color: rgba(1,1,1,.6);
  transition: 2000ms linear;
}

li::focus p{
  display: none;
  transition: 2000ms linear;
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
  cursor: pointer;
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
} */ 
</style>
