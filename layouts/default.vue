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
                <div class="text-center body-2">
                  $15
                </div>
                <div class="text-center body-2">
                  Hourly Rate
                </div>
              </div>
              <v-spacer />
              <div
                class="ma-2"
              >
                <div class="text-center body-2">
                  10 hours
                </div>
                <div class="text-center body-2">
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
          <v-card>
            <v-tabs
              v-model="tab"
              background-color="deep-purple accent-4"
              centered
              dark
            >
              <v-tabs-slider />

              <v-tab v-for="item in tabLists" :key="item.id" :to="item.link">
                {{ item.name }}
              </v-tab>
            </v-tabs>
          </v-card>
        </template>
      </div>
    </v-app>

    <!-- <v-sheet
      id="scrolling-techniques-4"
      class="overflow-y-auto"
      max-height="600"
    >
      <v-container style="height: 1000px;" />
    </v-sheet> -->
  </v-card>
</template>

<script>
export default {
  data () {
    return {
      tab: '',
      tabLists: [
        { id: 1, name: 'Education', link: '/' },
        { id: 2, name: 'Website', link: '/' },
        { id: 3, name: 'Skills', link: '/' }
      ]
    }
  }
}
</script>
