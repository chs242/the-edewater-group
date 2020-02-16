<template>
  <div class="root-contact">
      <IMG />
      <ContactForm></ContactForm>
      <Footer></Footer>
    </div>
</template>

<script>


import IMG from "@/components/IMG.vue";
import ContactForm from "@/components/ContactForm.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: "Contact",
  components: {
    ContactForm,
    IMG,
    Footer
  }
};
</script>

<style scoped>
  .root-contact{
    position: absolute;
    top: 0;
    right: 0;
    height: 100%;
    width: 80%;
    overflow-y: scroll;
    overflow-x: hidden;
    
  }
</style>