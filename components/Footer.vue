<template>
  <v-footer
    dark
    height="auto"
    class="pa-0"
  >
    <v-card
      class="flex"
      flat
      tile
    >
      <v-card-title class="blue">
        <strong class="body-2 font-weight-black">Please, Get connected with me on social networks!</strong>

        <v-spacer></v-spacer>

        <v-btn
          v-for="item in icons"
          :key="item.link"
          class="mx-3"
          :href="item.link"
          dark
          icon
        >
          <v-icon size="24px">{{ item.icon }}</v-icon>
        </v-btn>
      </v-card-title>

      <v-card-actions class="grey darken-3 justify-center">
        &copy;2020— <strong>Ismail Hossain</strong>
      </v-card-actions>
    </v-card>
  </v-footer>
</template>
<script>
  export default {
    data(){
      return{
        icons: [
          {link: '//www.facebook.com/ismailplus', icon: 'fab fa-facebook', color: '#3A559F'},
          {link: '//www.linkedin.com/in/ismailplus', icon: 'fab fa-linkedin', color: '#0077B7'},
          {link: '//www.instagram.com/ismailplus', icon: 'fab fa-instagram', color: '#E3003A'},
          {link: '//www.twitter.com/ismailcrc', icon: 'fab fa-twitter', color: '#1DABDD'},
        ]
      }
    }
  }
</script>