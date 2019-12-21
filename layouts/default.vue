<template>
  <v-card class="overflow-hidden">
    <v-app
      fixed
      color="#fff"
      prominent
    >
    <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
      right
    >
      <v-list
        nav
        dense
      >
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item>
            <v-list-item-title>
              <v-layout>
                <v-flex xs5>
                  <v-avatar size="80">
                    <img
                      src="@/assets/resume_image.jpg"
                      alt="Ismail"
                    >
                  </v-avatar>
                </v-flex>
                <v-flex xs7 class="mt-3">
                  <span class="body-1 font-weight-black">
                    Ismail Hossain
                  </span>
                  <br>
                  <v-btn class="my-2" small rounded color="primary">
                    tap to chat
                  </v-btn>
                </v-flex>
              </v-layout>
            </v-list-item-title>
          </v-list-item>
        </v-list-item-group>

        <v-subheader>
         View Interviews
        </v-subheader>

        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item>
             <v-list-tile-avatar>
              <v-icon left color="primary">
                mdi-text-to-speech-off
              </v-icon> 
            </v-list-tile-avatar>

            <v-list-item-title>
              <v-btn class=" text-capitalize" small block outlined rounded color="primary">
                 Audio & Text
              </v-btn>
            </v-list-item-title>
          </v-list-item>
          <v-list-item>
             <v-list-tile-avatar>
              <v-icon left color="primary">
                mdi-youtube-tv
              </v-icon>
            </v-list-tile-avatar>

            <v-list-item-title>
              <v-btn class=" text-capitalize" small block outlined rounded color="primary">
                 Video
              </v-btn>
            </v-list-item-title>
          </v-list-item>
        </v-list-item-group>

        <v-divider ></v-divider>

        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item>
            <v-list-item-title>
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
            </v-list-item-title>
          </v-list-item>
          <v-divider ></v-divider>
          <v-list-item>
            <v-list-item-title>
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
            </v-list-item-title>
          </v-list-item>
        </v-list-item-group>
        <v-divider ></v-divider>
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item>
            <v-list-item-title>
              <v-btn class="my-2" rounded block color="primary">
                <span class="text-capitalize">Hire Me</span>
              </v-btn>
            </v-list-item-title>
          </v-list-item>
        </v-list-item-group>
        <v-divider ></v-divider>
      </v-list>
    </v-navigation-drawer>

    <div style="background-color: white">
      <v-container grid-list-xs class="hidden-xs-and-down">
        <v-layout row wrap>
          <v-flex lg1 xs3>
            <v-avatar size="90">
              <img
                src="@/assets/resume_image.jpg"
                alt="Ismail"
              >
            </v-avatar>
            <v-btn class="my-2 hidden-sm-and-down" small rounded color="primary">
              tap to chat
            </v-btn>
          </v-flex>

          <v-flex lg2 xs7 class="mt-3">
            <div class="ml-2">
              <h3>
                Ismail Hossain
              </h3>
              <h6 class="overline font-weight-black">
                Software Engineer
              </h6>
              <h6 class="caption">
                Laravel & Vue.js Developer
              </h6>
           
            </div>
          </v-flex>
          <v-app-bar-nav-icon class="hidden-sm-and-up" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
          <v-flex lg9 class="hidden-sm-and-down mt-2">
            <v-card-title class="mt-2 pt-0 ">
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
        <nuxt />
      </v-container>
    </div>
    </v-app>
  </v-card>
</template>

<script>
import SkillSet from '@/components/Skills'
export default {
  components:{
    SkillSet
  },
  data () {
    return {
      tab: '',
      tabLists: [
        { id: 1, name: 'Portfolio', link: '/portfolio' },
        { id: 2, name: 'Works', link: '/works' },
        { id: 3, name: 'Education', link: '/education' }
      ],
      drawer: false,
      group: null,
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

</style>
