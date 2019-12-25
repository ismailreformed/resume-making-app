<template>
  <v-card class="overflow-hidden">
    <v-app
      fixed
      color="#fff"
      prominent
    >

    <div style="background-color: white">
      <v-container grid-list-xs class="my-0 pt-0 pb-0">
        <v-layout  class="mt-4" row wrap>
          <v-flex lg1 xs3>
            <img
            width="100"
            height="100"
              src="@/assets/resume_image.jpg"
              alt="Ismail"
            >
          </v-flex>

          <v-flex lg4 xs7 class="ml-3">
            <div class="ml-2" >
              <h3 style="color: #0A56E9">
                Ismail Hossain
              </h3>
              <h6 style="color: #2E81F4" class="caption">
                Laravel & Vue.js Developer
              </h6>
              <v-avatar size="40" v-for="item in listIcon" :key="item.id" class="listDesign my-2 mr-2">
                <v-icon color="#0A56E9"> {{ item.icon }}</v-icon>
              </v-avatar>
            </div>
          </v-flex>
          <v-flex xs1 class="hidden-sm-and-up pa-0 mt-5">
            <v-icon color="#0A56E9">
              mdi-text-to-speech-off
            </v-icon> 
            <br>
            <v-icon color="#0A56E9" class="mt-3">
              mdi-youtube-tv
            </v-icon>
          </v-flex>
          <v-spacer></v-spacer>
          <v-flex lg6 xs12>
            <v-card-title class="my-0 py-0 hidden-sm-and-down">
              <div
                class="ma-2"
              >
                <h3 class="text-center font-weight-bold body-1"  style="color: #0A56E9">
                  View interviews :
                </h3>
              </div>
              <v-btn class="ma-2" color="#EEF6FF" style="box-shadow: none">
                <v-icon left color="#0A56E9">
                  mdi-text-to-speech-off
                </v-icon> 
                <span style="color: #0A56E9">Audio & Text </span> 
              </v-btn>
              <v-btn class="ma-2 " color="#EEF6FF" style="box-shadow: none">
                <v-icon color="#0A56E9" left>
                  mdi-youtube-tv
                </v-icon> 
                <span style="color: #0A56E9">Video </span>      
              </v-btn>
              </v-card-title>
              <v-card-title class="ma-0 pb-1 pt-1 px-0">
                <div
                  class="ma-2"
                >
                  <div class="text-center body-2">
                    <span style="font-size: x-large; color: #0A56E9">15$</span> 
                    <br class="hidden-sm-and-up">
                    <span style="color: #2E81F4"> Hourly Rate</span>
                  </div>
                </div>
                <div
                  class="ma-2"
                >
                  <div class="text-center body-2">
                    <span style="font-size: x-large; color: #0A56E9">10hr</span>
                    <br class="hidden-sm-and-up">
                    <span style="color: #2E81F4"> Weekly Availabilty</span>
                  </div>
                </div>
                <v-btn style="box-shadow: none" color="primary">
                  <span class="text-capitalize">Hire Me</span>
                </v-btn>
              </v-card-title>
          </v-flex>
        </v-layout>
      </v-container>
    </div>
  
    <div>
      <template>
        <v-card flat>
          <v-tabs
            background-color="blue accent-4"
            centered
            hide-slider
            dark
          >
            <v-tab v-for="item in tabLists" :key="item.id" :to="item.link" class="text-capitalize">
              {{ item.name }}
            </v-tab>
          </v-tabs>
        </v-card>
      </template>
      <v-container>
        <SkillSet />
        <v-divider class="py-1"></v-divider>
        <nuxt />
      </v-container>
    </div>
    <Footer />
    </v-app>
  </v-card>
</template>

<script>
import SkillSet from '@/components/ThemeTwo/Skills'
import Footer from '@/components/Footer'
export default {
  name: 'themeTwoLayout',
  components:{
    SkillSet,
    Footer
  },
  data () {
    return {
      tab: '',
      tabLists: [
        { id: 1, name: 'Portfolio', link: '/theme-two/portfolio' },
        { id: 2, name: 'Works', link: '/theme-two/works' },
        { id: 3, name: 'Education', link: '/theme-two/education' }
      ],
      drawer: false,
      group: null,
      listIcon:[
        { id: 'a', icon: 'mdi-message-text'},
        { id: 'b', icon: 'mdi-behance'},
        { id: 'c', icon: 'mdi-web'},
        { id: 'd', icon: 'mdi-instagram'},
      ]
    }
  },
   watch: {
      group () {
        this.drawer = false
      },
    },
}
</script>

<style scoped>
.v-tab--active{
  background-color: #5D82ED;
  border-radius: 25px;
  width: 100px;;
}
.width350{
  max-width: 300px;
}

ul {
  list-style-type: none;
}

li{
  display: inline-block
}


.listDesign{
  height: 40px;
  width: 40px;
  border: 2px solid #0A56E9;
  background-color: #EEF6FF
}
</style>
