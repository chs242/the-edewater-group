<template>
  <div class="root-about">
    <IMG />
    <div class="about-wrapper">
      <div class="about-title-wrapper">
        <div class="inner-wrapper">
          <h3>About Us</h3>
          <p><i>Our experience, ethos and values</i></p>
        </div>
      </div>
      <div class="about-text-wrapper">
        <div class="inner-wrapper inner-text-wrapper">
          <p>This is where your text starts. You can click here and start typing. Odit aut fugit sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt neque porro quisquam est qui dolorem ipsum quia dolor sit amet consectetur<br><br>adipisci velit sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem ut enim ad minima veniam quis nostrum exercitationem ullam corporis suscipit laboriosam nisi ut aliquid ex ea commodi consequatur quis autem.Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium<br><br>doloremque laudantium totam rem aperiam eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt neque porro quisquam est qui dolorem ipsum quia dolor sit amet consectetur adipisci velit sed quia non numquam eius modi tempora.</p>
        </div>
      </div>
    </div>
    <NewFooter />
  </div>
</template>

<script>
import IMG from "@/components/IMG.vue"
import NewFooter from "@/components/NewFooter.vue"
export default {
  name: "About",
  components:{
    IMG,
    NewFooter
  }
}
</script>
<style scoped>
  .root-about{
    position: absolute;
    top: 0;
    right: 0;
    height: 100%;
    width: 80%;
    overflow-y: scroll;
    overflow-x: hidden;
  }

  .about-wrapper{
    display: flex;
    width: 100%;
    margin-bottom: 50px;
  }

  .about-title-wrapper{
    width: 30%;
  }

  .inner-wrapper{
    margin-top: 50px;
    width: 50%;
    margin-left: 70px;
    text-align: left;
  }

  h3{
    margin: 0 0 10px 0;
  }

  h3:after{
    content:'';
    display:block;
    border:0.5px solid #ffc000;
    position: absolute;
    margin-left: 70px;
    margin-top: 5px;
    width: 100px;
    left: 0;
    z-index: 3;
}

  p{
    margin: 0;
    font-family: 'Josefin Sans', sans-serif;
  }

  .about-text-wrapper{
    width: 100%;
  }

  .inner-text-wrapper{
    margin-left: 20px;
    width: 80%;
    font-size: 1.5rem;
  }

@media (min-width: 320px) and (max-width: 1024px) {
  .root-about{
    width: 100%;
  }
  .about-wrapper{
    display: flex;
    flex-direction: column;
    margin-left: 10%;
  }

  .inner-wrapper{
    margin-top: 50px;
    width: 80%;
    margin-left: 0px;
  }

  
}
@media (min-width: 320px) and (max-width: 1024px) {
  h3:after{
    margin-left: 10%;
  }
}
</style>