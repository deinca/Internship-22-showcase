<template>
  <div>
    <header class="mb-5">
      <div class="img-container-header">
        <b-img-lazy src="~/assets/images/hero.jpg"></b-img-lazy>
        <h1 class="text-center header-title">Contact</h1>
      </div>
    </header>

    <b-container class="mb-5">
      <b-row>
        <b-col cols="4" align-self="stretch">
          <div class="img-container-ava mb-4">
            <b-img src="~/assets/images/Avatar-formeel-valtech.png"> </b-img>
          </div>
          <b-card-group>
            <h5>Deiver Zamora Cortez</h5>
            <p>
              Hey daar ✌, je kan altijd in contact komen met mij door het
              formulier hiernaast in te vullen! Of je kan mij altijd een
              vriendschapsverzoek sturen op de onderstaande socialmedia
              platformen.
            </p>
          </b-card-group>

          <h5 class="mb-4">Sociaal media</h5>

          <b-row class="text-center">
            <a
              href="https://www.linkedin.com/in/deiver-zamora-cortez-378405110"
            >
              <b-col>
                <b-img
                  class="mb-3"
                  v-bind="mainProps"
                  rounded
                  width="50"
                  alt="Circle image"
                  src="~/assets/icons/linkedin-brands.svg"
                ></b-img>
                <h5>LinkedIn</h5>
              </b-col>
            </a>
            <a href="https://github.com/deinca">
              <b-col>
                <b-img
                  class="mb-3"
                  v-bind="mainProps"
                  rounded
                  width="55"
                  alt="Circle image"
                  src="~/assets/icons/github-brands.svg"
                ></b-img>
                <h5>Github</h5>
              </b-col>
            </a>
          </b-row>
        </b-col>

        <b-col cols="8">
          <h2>Contact Formulier</h2>
          <div class="container">
            <form @submit.prevent="sendEmail">
              <label>Naam</label>
              <input
                v-model="name"
                type="text"
                name="name"
                placeholder="Vul jouw naam in bijv.: Jan Velden"
              />
              <label>Email</label>
              <input
                v-model="email"
                type="email"
                name="email"
                placeholder="Vul jouw Email in bijv.: j.velden@gmail.com "
              />
              <label>Bericht</label>
              <textarea
                v-model="message"
                name="message"
                cols="30"
                rows="5"
                placeholder="Hallo Deiver, Met dit bericht..."
              >
              </textarea>

              <b-button
                pill
                type="submit"
                variant="primary"
                value="Send"
                class="p-3 w-25 button-blue"
                >Verzenden</b-button
              >
            </form>
          </div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import emailjs from 'emailjs-com'
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
export default {
  name: 'Page1',
  components: FontAwesomeIcon,
  data() {
    return {
      name: '',
      email: '',
      message: '',
    }
  },
  methods: {
    sendEmail(e) {
      try {
        emailjs.sendForm(
          'service_zldq1lq',
          'template_l0i8qw2',
          e.target,
          'user_5s9ml9oSgDkedAwVWxFth',
          {
            name: this.name,
            email: this.email,
            message: this.meessage,
          }
        )
        // console.log('it works!!!')
      } catch (error) {
        // console.log({ error })
      }
      // Reset form field
      this.name = ''
      this.email = ''
      this.message = ''
    },
  },
}
</script>
<style lang="scss" scoped>
a {
  color: $color-black;
  text-decoration: none;
}
a:hover {
  color: $color-cerulean;
  text-decoration: none;
}
header img {
  width: 100%;
  display: flex;
  object-fit: cover;
  object-position: bottom;
}
div .img-container-ava img {
  width: 80%;
}
.img-container-ava {
  overflow: hidden;
  width: 100%;
  display: flex;
  justify-content: center;
}
.img-container-header {
  height: 12rem;
  overflow: hidden;
  width: inherit;
  display: flex;
  justify-content: center;
}
.header-title {
  position: absolute;
  align-self: center;
  color: $color-white;
}

// form //

label {
  float: left;
}

input[type='text'],
[type='email'],
textarea {
  width: 100%;
  padding: 12px;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
  margin-top: 6px;
  margin-bottom: 16px;
  resize: vertical;
}

input[type='submit'] {
  background-color: #4caf50;
  color: white;
  padding: 12px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

input[type='submit']:hover {
  background-color: #45a049;
}
.button-blue {
  background-color: $color-midnight-blue;
  border: none;
}
.button-blue:hover {
  background-color: $color-cerulean;
}
</style>
