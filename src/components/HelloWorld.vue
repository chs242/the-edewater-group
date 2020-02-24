<template>
  <div class="hello">
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
      <div class="content"  @click="isActive = !isActive">
          <a>
            <div class="content-overlay" :class="{contentOverlayActive: isActive}"></div>
            <img class="content-image" src="https://images.unsplash.com/photo-1433360405326-e50f909805b3?ixlib=rb-0.3.5&q=80&fm=jpg&crop=entropy&w=1080&fit=max&s=359e8e12304ffa04a38627a157fc3362">
            <div class="content-details fadeIn-top" :class="{contentDetailsActive: isActive}">
              <h3>{{ projectTitle }}</h3>
              <p>{{ projectDescription }}</p>
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
    "projectTitle",
    "projectDescription"
  ],
  data(){
    return{
      isActive: false,
      isActive1: false,
      isActive2: false,
      scroll5: 0
    }
  },
  
 
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
  margin: 10px 0px 10px 0px;
  padding: 0;
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
  height: 100%;
  width: 100%;
  opacity: 0;
  -webkit-transition: all 0.2s ease-in-out 0s;
  -moz-transition: all 0.2s ease-in-out 0s;
  transition: all 0.2s ease-in-out 0s;
}

.content-image{
  width: 100%;
  padding: 0;
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
  -webkit-transition: all 0.1s ease-in-out 0s;
  -moz-transition: all 0.1s ease-in-out 0s;
  transition: all 0.1s ease-in-out 0s;
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
  top: 50%;
}
</style>
