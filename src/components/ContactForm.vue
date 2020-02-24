
<template>
  <form name="contact" data-netlify="true" data-netlify-honeypot="bot-field">
    <input type="hidden" name="form-name" value="contact" />
    <p hidden>
      <label>
        Don’t fill this out:
        <input name="bot-field" />
      </label>
    </p>
    <div class="sender-info">
      <div>
        <!-- <label for="name" class="label" >Your name</label> -->
        <input type="text" name="name" v-model="formData.name" placeholder="Name" />
      </div>
      <div>
        <!-- <label for="email">Your email</label> -->
        <input type="email" name="email" v-model="formData.email" placeholder="E-Mail" />
      </div>
    </div>

    <div class="message-wrapper">
      <!-- <label for="message">Message</label> -->
      <textarea name="message" v-model="formData.message" placeholder="Message"></textarea>
      <ui-button @click="handleSubmit" icon="send" :cta="true">Send</ui-button>
    </div>
  </form>
</template>

<script>
// import UiButton from "~/components/UI/UiButton";

export default {
  // components: { UiButton },
  data() {
    return {
      formData: {}
    };
  },
  methods: {
    encode(data) {
      return Object.keys(data)
        .map(
          key => encodeURIComponent(key) + "=" + encodeURIComponent(data[key])
        )
        .join("&");
    },
    handleSubmit() {
      fetch("/", {
        method: "POST",
        headers: { "Content-Type": "application/x-www-form-urlencoded" },
        body: this.encode({
          "form-name": "contact",
          ...this.formData
        })
      })
        .then(() =>
          alert(
            "Thank you!\rWe have successfully recieved your form submission!"
          )
        )
        .catch(error => alert(error));
    }
  }
};
</script>

<style scoped>
form {
  margin: 12px auto 44px;
  width: 80%;
  max-width: 800px;
}
input,
textarea {
  width: 100%;
}

  button {
    position: absolute;
    bottom: 15px;
    right: 15px;
  }

textarea {
  margin-top: 6px;
  height: 220px;
}
.sender-info {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(185px, 1fr));
  grid-gap: 6px;
}
</style>