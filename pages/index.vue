<template>
  <v-container grid-list-md>
    <v-layout wrap>
      <v-flex v-for="item in themes" :key="item.id" xs4>
        <v-card
        >
          <v-list-item>
            <!-- <v-list-item-avatar color="grey"></v-list-item-avatar> -->
            <v-list-item-content>
              <v-list-item-title class="headline text-xs-center">{{ item.name }}</v-list-item-title>
              <!-- <v-list-item-subtitle>by Kurt Wagner</v-list-item-subtitle> -->
            </v-list-item-content>
          </v-list-item>

          <v-img
            src="https://cdn.vuetifyjs.com/images/cards/mountain.jpg"
            height="194"
          ></v-img>
<!-- 
          <v-card-text>
            Visit ten places on our planet that are undergoing the biggest changes today.
          </v-card-text> -->

          <v-card-actions color="text-xs-center primary">
            <!-- <v-btn
              text
              color="deep-purple accent-4"
            >
              Read
            </v-btn>
            <v-btn
              text
              color="deep-purple accent-4"
            >
              Bookmark
            </v-btn>
            <v-spacer></v-spacer> -->
            <v-btn :to="item.to" icon color="deep-purple accent-4">
              <v-icon>mdi-eye</v-icon> 
              Preview
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>

export default {
  name: "default",
  layout: "default",
  data(){
    return {
      themes: [
        {id: 1, name: 'Theme One', to: '/theme-one'},
        {id: 2, name: 'Theme Two', to: '/theme-two'},
      ]
    }
  }
}
</script>
