<template>
  <v-card class="overflow-hidden">
    <v-app-bar
      fixed=""
      color="#FBFBFB"
      prominent
      fade-img-on-scroll
    >
      <v-container>
        <v-layout>
          <v-flex lg1>
            <v-avatar size="80">
              <img
                src="https://cdn.vuetifyjs.com/images/john.jpg"
                alt="John"
              >
            </v-avatar>
          </v-flex>
          <v-flex lg2 style="margin-top: 10px;">
            <h3>
              Jesam Smith
            </h3>
            <h6 class="caption font-weight-thin">
              Professional UI/UX
            </h6>
            <h6 class="overline font-weight-thin">
              Designer
            </h6>
          </v-flex>
          <v-flex lg9>
            <v-card-title>
              <v-chip
                class="ma-2"
                color="#fff"
              >
                View interviews:
              </v-chip>
              <v-spacer />

              <v-chip
                class="ma-2"
                color="indigo darken-3"
                outlined
              >
                <v-icon left color="blue">
                  mdi-text-to-speech-off
                </v-icon>
                Audio & Text
              </v-chip>
              <v-spacer />

              <v-chip
                class="ma-2"
                color="indigo darken-3"
                outlined
              >
                <v-icon left>
                  mdi-youtube-tv
                </v-icon>
                Video
              </v-chip>
              <v-spacer />

              <div
                class="ma-2 text-xs-center"
              >
                <p>$15</p>
                <p>Hourly Rate</p>
              </div>
              <v-spacer />
              <div
                class="ma-2 text-xs-center"
              >
                <p>10 hours</p>
                <p>Weekly Availabilty</p>
              </div>
              <v-spacer />
              <v-btn rounded color="error">
                Hire Me
              </v-btn>
            </v-card-title>
          </v-flex>
        </v-layout>
      </v-container>

      <template v-slot:extension>
        <v-tabs
          class="blue"
          align-with-title
          background-color="#4771EA"
        >
          <v-tab>Tab 1</v-tab>
          <v-tab>Tab 2</v-tab>
          <v-tab>Tab 3</v-tab>
        </v-tabs>
      </template>
    </v-app-bar>
    <!-- <v-sheet
      id="scrolling-techniques-4"
      class="overflow-y-auto"
      max-height="600"
    >
      <v-container style="height: 1000px;" />
    </v-sheet> -->
  </v-card>
</template>
