<template>
  <div class="root-contact-form">
    <div class="contact-wrapper">
        <div class="about-title-wrapper">
          <div class="inner-wrapper">
            <h3>Contact</h3>
            <p><i>Please be in touch</i></p>
          </div>
        </div>
        <div class="about-text-wrapper">
          <div id="contact-form" class="contact-form">
            <div class="separator"></div>
            <div v-if="isSending" class="loading">Sending...</div>
              <form class="form" name="contact" method="POST" data-netlify="true" data-netlify-honeypot="bot-field">
                <!-- Hidden input to check for bots -->
                <input type="hidden" name="form-name" value="contact" />

                <input required name="name" v-model='formData.name' placeholder="Name" type="text" autocomplete="off">
                <input required name="email" v-model="formData.email" placeholder="E-mail" type="email" autocomplete="off">
                <textarea name="message" v-model="formData.message" rows="4" placeholder="Message"></textarea>
                <button class="button" type="submit">Send</button>
              </form>
            </div>
          </div>
        </div>
    </div>
</template>

<script>
export default {
  name:"ContactForm",
  data(){
    return{
    formData: {
        name: '',
        email: '',
        message: '',
    },
    isSending: false
    }
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
        .then((res) =>
          console.log(res),
          alert(
            "Thank you!\rWe have successfully recieved your form submission!"
          )
        )
        .catch(error => alert(error));
    }
  }

}
</script>

<style scoped>
  .contact-wrapper{
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
    width: 80%;
    margin: 0 auto;
  }

  .inner-text-wrapper{
    margin-left: 20px;
    width: 80%;
    font-size: 1.5rem;
  }

    .contact-form {
    font-family: 16px;
    margin: 50px 0;
    margin-bottom: 50px;
    max-width: 600px;
    width: 100%;
    }

    .contact-form .separator {
    border-bottom: solid 1px #ccc;
    margin-bottom: 15px;
    }

    .contact-form .form {
    display: flex;
    flex-direction: column;
    font-size: 16px;
    }

    .contact-form_title {
    color: #333;
    text-align: left;
    font-size: 28px;
    }

    .contact-form input[type="email"],
    .contact-form input[type="text"],
    .contact-form textarea {
    border: solid 1px #e8e8e8;
    font-family: 'Josefin Sans', sans-serif;
    padding: 10px 7px;
    margin-bottom: 15px;
    outline: none;
    }

    .contact-form textarea {
    resize: none;
    }

    .contact-form .button {
    width: 150px;
    background: #acacac;
    border: solid 1px #acacac;
    color: white;
    cursor: pointer;
    padding: 10px 50px;
    text-align: center;
    text-transform: uppercase;
    }

    .contact-form .button:hover {
    background: #ea532a;
    border: solid 1px #ea532a;
    }

    .contact-form input[type="email"],
    .contact-form input[type="text"],
    .contact-form textarea,
    .contact-form .button {
    font-size: 1rem;
    border-radius: 3px
    }

  @media (min-width: 320px) and (max-width: 1024px) {
    .contact-wrapper{
      width: 80%;
      flex-direction: column;
      margin-bottom: 0px;
    }

    .about-title-wrapper, .about-text-wrapper{
      width: 100%;
      margin: 0 10%;
    }

    .inner-wrapper{
      margin-bottom: 10px;
      margin-left: 0px;
    }
    
  h3:after{
    content:'';
    display:block;
    border:0.5px solid #ffc000;
    position: absolute;
    margin-left: 8%;
    margin-top: 5px;
    width: 100px;
    left: 0px;
    z-index: 3;
  }
}

</style>