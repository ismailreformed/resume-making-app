<template>
  <div>
    <v-card
      style="box-shadow: none; border: 1px solid #0A56E9"
      color="#FFFFFF"
    >
      <v-container grid-list-lg class="pa-5">
        <h1 style="color: #0A56E9;" class="font-weigh-bold">Education</h1>
        <v-layout v-for="item in educationExperinceLists" :key="item.id" row wrap>
          <v-flex xs12 lg12>
            <div class="title font-weight-black" >
              <div class="dot"></div> <span style="color:#0A56E9">{{ item.institute }}</span>
            </div>
            <div class="ml-2">
              <p class="ml-3">
                <span class="body-2" style="color:#0A56E9">{{item.title }} || </span>
               <span class="caption" style="color: black">{{ item.since }}</span> 
              </p>
              <p class=" ml-3 body-2" style="color: #2E81F4">
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
        {id: 1, institute: 'IIUC', title: '(CSE) Bachelor Degree of Computer Science', since: 'May 2018 - Present', text: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quos dicta delectus et ratione, minus excepturi esse officia, quaerat quod, numquam optio quibusdam velit est accusantium voluptate necessitatibus? Excepturi exercitationem beatae nesciunt est velit illo tempore quo assumenda? Aliquid, maiores ad. Corporis velit sint nulla illum voluptates reiciendis. Quisquam, deserunt explicabo!'},
        {id: 2, institute: 'Oxford University', title: '(MBA) Master of Business Administration', since: 'May 2018 - Present', text: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quos dicta delectus et ratione, minus excepturi esse officia, quaerat quod, numquam optio quibusdam velit est accusantium voluptate necessitatibus? Excepturi exercitationem beatae nesciunt est velit illo tempore quo assumenda? Aliquid, maiores ad. Corporis velit sint nulla illum voluptates reiciendis. Quisquam, deserunt explicabo!'},
      ]
    }
  }
}
</script>

<style >
.dot{
  height: 15px;
  width: 15px;
  background-color: #0A56E9;
  border-radius: 50%;
  display: inline-block;
  padding: 5px;
}
</style>