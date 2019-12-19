<template>
  <v-card class="overflow-hidden">
    <v-app
      fixed
      color="#FBFBFB"
      prominent
      fade-img-on-scroll
    >
      <v-container>
        <v-layout>
          <v-flex lg1>
            <v-avatar class="ml-4" size="80">
              <img
                src="https://cdn.vuetifyjs.com/images/john.jpg"
                alt="John"
              >
            </v-avatar>
            <v-btn class="ma-2" small rounded color="primary">
              tap to chat
            </v-btn>
          </v-flex>
          <v-flex lg2 class="mt-3 ml-2">
            <h3>
              Jesam Smith
            </h3>
            <h6 class="caption">
              Professional UI/UX
            </h6>
            <h6 class="overline">
              Designer
            </h6>
          </v-flex>
          <v-flex lg9>
            <v-card-title class="mt-2 pt-0">
              <div
                class="ma-2"
              >
                <div class="text-center body-1">
                  View interviews:
                </div>
              </div>
              <v-spacer />
              <v-btn class="ma-2 text-capitalize" small outlined rounded color="primary">
                <v-icon left>
                  mdi-text-to-speech-off
                </v-icon>  Audio & Text
              </v-btn>
              <v-spacer />
              <v-btn class="ma-2 text-capitalize" small rounded outlined color="primary">
                <v-icon left>
                  mdi-youtube-tv
                </v-icon> Video
              </v-btn>
              <v-spacer />

              <div
                class="ma-2"
              >
                <div class="text-center body-2 font-weight-bold">
                  $15
                </div>
                <div class="text-center body-2 font-weight-bold">
                  Hourly Rate
                </div>
              </div>
              <v-spacer />
              <div
                class="ma-2"
              >
                <div class="text-center body-2 font-weight-bold">
                  10 hours
                </div>
                <div class="text-center body-2 font-weight-bold">
                  Weekly Availabilty
                </div>
              </div>
              <v-spacer />
              <v-btn rounded color="primary">
                <span class="text-capitalize">Hire Me</span>
              </v-btn>
            </v-card-title>
          </v-flex>
        </v-layout>
      </v-container>
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
        <nuxt />
      </v-container>
      </div>
    </v-app>
  </v-card>
</template>

<script>
export default {
  data () {
    return {
      tab: '',
      tabLists: [
        { id: 1, name: 'Portfolio', link: '/portfolio' },
        { id: 2, name: 'Works', link: '/works' },
        { id: 3, name: 'Education', link: '/education' }
      ]
    }
  }
}
</script>

<style lang="stylus">
.v-tab--active{
  background-color: #5D82ED;
  border-radius: 25px;
  width: 80%
}
.width350{
  width: 300px;
}

</style>
