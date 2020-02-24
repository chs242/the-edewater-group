<template>
  <div class="root-contact">
      <IMG />
      <ContactForm2 />
      <NewFooter />
    </div>
</template>

<script>


import IMG from "@/components/IMG.vue";
import ContactForm2 from "@/components/ContactForm2.vue";
import NewFooter from "@/components/NewFooter.vue";

export default {
  name: "Contact",
  components: {
    IMG,
    ContactForm2,
    NewFooter
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

  @media (min-width: 320px) and (max-width: 1024px) {
    .root-contact{
      width: 100%;
    }
  }
</style>