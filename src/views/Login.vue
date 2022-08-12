<template>
  <v-container style="min-width: 100%; height: 100%; padding: 0; font-family: 'circular';">
    <v-row no-gutters>
      <v-col sm="12" md="6" lg="6" class="first-col">
      </v-col>
      <v-col sm="12" md="6" lg="6" style="background-color:#e3f2fa">
        <v-row align="center" no-gutters style="height:100vh; text-align: center;">
          <v-col sm="12" md="12" lg="12">
            <img class="logo-image" width="250" :src="logo" />
            <h1 class="greating" style="color: #e31238; font-size: 50px;">Bienvenu sur Vino</h1>
            <v-container class="form-container">
              <h4>Veuillez vous connecter pour voir nos catalogues.</h4>
              <v-text-field class="input-text" placeholder="Nom d'utilisateur" prepend-inner-icon="mdi-account"
                variant="underlined"></v-text-field>
              <v-text-field class="input-text" placeholder="Mot de passe" prepend-inner-icon="mdi-lock"
                variant="underlined" type="password">
              </v-text-field>
              <v-btn class="btn-login" size="large" :rounded="0" color="#e31238" variant="tonal" @click="login()">
                Se connecter
              </v-btn>
            </v-container>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>


<script lang='ts'>
import router from '@/router'
import { defineComponent } from 'vue'


export default defineComponent({
  name: 'Login',

  data() {
    return {
      logo: require("../assets/images/raisin.png")
    }
  },
  methods: {
    login() {
      router.push({ path: '/home' })
    }
  }

})
</script>


<style lang="scss" scoped>
@font-face {
  font-family: 'circular';
  src: local('circular'), url(../assets/fonts/CircularStdBold/CircularStdBold.woff) format('Woff');
}

.btn-login {
  box-shadow: none;
  color: white;
  margin-top: 5%
}

.first-col {
  background-image: url(../assets/images/vino.jpg);
  background-repeat: no-repeat;
  background-size: cover;
  background-position: top;
  height: 100vh;
  padding: 0 10% 0 10%;
}

.form-container {
  padding: 0 25% 0 25%;
  margin-top: 3%;
}


@media screen and (max-width: 600px) {
  .first-col {
    display: none;
  }
}

@media screen and (max-width: 435px) {
  .logo-image {
    width: 150px;
  }

  .greating {
    font-size: 30px !important;
  }

  .form-container {
    padding: 0 10% 0 10%;
  }
}
</style>