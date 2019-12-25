<template>
  <div>
    <v-card
      class="mx-auto"
      flat
      color="#FBFBFB"
    >
      <v-container grid-list-lg>
        <v-layout v-for="item in educationExperinceLists" :key="item.id" row wrap>
          <v-flex xs12 lg6>
            <div class="borderLeft">
              <p class="headline font-weight-black text--primary  ml-3 width350">
                {{ item.title }}
              </p>
            </div>
            <div class="ml-5">
              <p class="caption">{{ item.since }}</p>
              <p class="body-2 text--primary">
                {{ item.text }}
              </p>
            </div>
          </v-flex>
        </v-layout>
      </v-container>
    </v-card>
  </div>
</template>

<script>
export default {
  name: 'themeTwo.vue',
  layout: 'themeTwoLayout',
  data(){
    return {
      educationExperinceLists: [
        {id: 1, title: '(CSE) Bachelor Degree of Computer Science', since: 'May 2018 - Present', text: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quos dicta delectus et ratione, minus excepturi esse officia, quaerat quod, numquam optio quibusdam velit est accusantium voluptate necessitatibus? Excepturi exercitationem beatae nesciunt est velit illo tempore quo assumenda? Aliquid, maiores ad. Corporis velit sint nulla illum voluptates reiciendis. Quisquam, deserunt explicabo!'},
        {id: 2, title: '(MBA) Master of Business Administration', since: 'May 2018 - Present', text: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quos dicta delectus et ratione, minus excepturi esse officia, quaerat quod, numquam optio quibusdam velit est accusantium voluptate necessitatibus? Excepturi exercitationem beatae nesciunt est velit illo tempore quo assumenda? Aliquid, maiores ad. Corporis velit sint nulla illum voluptates reiciendis. Quisquam, deserunt explicabo!'},
      ]
    }
  }
}
</script>

<style >
.borderLeft{
  border-left: 5px solid;
  border-left-color: blue;
  }
</style>