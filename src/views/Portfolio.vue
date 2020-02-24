<template>
  <div class="root-portfolio" @scroll.native="isActive2 = !isActive2">
      <IMG />
      <div class="portfolio-inner">
  
        <PortfolioTitle title="developments of 10 units+" />
        <div class="hello-world-cont">
        <HelloWorld projectTitle="Your Title" projectDescription="Your description goes here" />
        <HelloWorld projectTitle="Your Title" projectDescription="Your description goes here" />
        </div>
        <PortfolioTitle title="profitable developments of 50 units+"/>
        <div class="hello-world-cont">
        <HelloWorld projectTitle="Your Title" projectDescription="Your description goes here" />
        <HelloWorld projectTitle="Your Title" projectDescription="Your description goes here" />
        <HelloWorld projectTitle="Your Title" projectDescription="Your description goes here" />
        </div>
        <PortfolioTitle title="developments of 15 units+"/>
        <div class="hello-world-cont">
        <HelloWorld projectTitle="Your Title" projectDescription="Your description goes here" />
        <HelloWorld projectTitle="Your Title" projectDescription="Your description goes here" />
        <HelloWorld projectTitle="Your Title" projectDescription="Your description goes here" />
        <HelloWorld projectTitle="Your Title" projectDescription="Your description goes here" />
        </div>
      </div>
    <NewFooter />
  </div>
</template>

<script>


import IMG from "@/components/IMG.vue";
import PortfolioTitle from "@/components/PortfolioTitle.vue";
import HelloWorld from "@/components/HelloWorld.vue";
import NewFooter from "@/components/NewFooter.vue";

export default {
  name: "Portfolio",
  components: {
    IMG,
    PortfolioTitle,
    HelloWorld,
    NewFooter
  },
  // data(){
  //   return{
  //     scroll5: false
  //   }
  // },
  // methods: {
  //    handleScroll() {
  //     this.scroll5 = window.scrollY;
  //     let scrolled = this.scroll5 + 50;
  //     if(this.scroll5 == scrolled){
  //       return this.scroll5 = true;
  //     }
  //     console.log(this.scroll5)
  //   }
  // },
  // mounted() {
  //   window.addEventListener("scroll", this.handleScroll);
  // },
  // destroyed() {
  //   window.removeEventListener("scroll", this.handleScroll);
  // }
};
</script>

<style scoped>
  .root-portfolio{
    position: absolute;
    height: 100%;
    top: 0;
    right: 0;
    width: 80%;
    overflow-y: scroll;
    overflow-x: hidden;
  }
  .portfolio-inner{
    display: flex;
    flex-flow: column;
    overflow-y:scroll;
    overflow-x: hidden;
    
  }
  @media (min-width: 320px) and (max-width: 1024px) {
    .root-portfolio{
      width: 100%;
    }
  }
</style>