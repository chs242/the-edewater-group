<template>    
    <div class="hello">
        <div class="head-wrapper">    
        <h2>{{ title }}</h2>
        </div>
        <div class="sub-head-wrapper">
        <h4>This is where your text starts. You can click here and start typing. Et dolore magnam aliquam quaerat voluptatem ut enim ad minima veniam quis nostrum exercitationem ullam corporis.</h4>
        </div>
    </div>
</template>

<script>
export default {
  name: "PortfolioTitle",
  props:[
    "title"
  ],
}
</script>

<style scoped>

    .hello{
        margin: 20px;
        min-width: 700px;
    }
    .head-wrapper{
      /* margin-left: 100px; */
      width: 100%;
      text-align: left;
      font-weight: 200;
    }

.head-wrapper:after{
    content:'';
    display:block;
    border:0.5px solid #ffc000;
    position: absolute;
    margin-left: 3%;
    width: 100px;
    left: 0;
    z-index: 3;
}

.sub-head-wrapper{
  text-align: left;
  width: 750px;
  padding: 0;
  color: #acacac;
 font-size: 16px;
 
}

  h2{
      margin-bottom: 2px;
  }
  h4{
      width: 100%;
      margin-left: 20px;
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
      margin-left: 20px;
    }

    .sub-head-wrapper{
      width: 750px;
      margin: 0;
      padding: 0;
    }

    .head-wrapper:after{
      margin-left: 45%;
    }
    
}
@media (min-width: 950px) and (max-width: 1024px) {
    .head-wrapper:after{
      margin-left: 45%;
    }
}
@media (min-width: 750px) and (max-width: 950px) {
    .head-wrapper:after{
      margin-left: 5%;
    }
}
@media (min-width: 550px) and (max-width: 750px) {
    .head-wrapper:after{
      margin-left: 7%;
    }
}
@media (min-width: 320px) and (max-width: 550px) {
    .hello{
        margin-left: 5px;
    }
    .head-wrapper:after{
      margin-left: 38%;
    }
    h2, h4{
        max-width: 45%;
    }
    .sub-head-wrapper{
        width: 90%;
    }
} 
</style>