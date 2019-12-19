<template>
  <div>
    <v-card color="#FBFBFB" flat>
      <v-card-actions class="text-xs-center">
        <div  v-for="item in skillSets" :key="item.id" >
          <v-chip :to="item.to" x-large outlined class="px-5">
            <div class="text-center">
              {{ item.title }}
            </div>
          </v-chip>
          <v-spacer></v-spacer>
        </div>
      </v-card-actions>
      <nuxt-child />
    </v-card>
  </div>
</template>
<script>
export default {
  data(){
    return {
      skillSets: [
        { id: 1, to: '/skills/programming', title: 'Programming Language'},
        { id: 2, to: '/skills/framework', title: 'Framwork/Database'},
        { id: 3, to: '/skills/design-skills', title: 'Design Skill'},
        { id: 4, to: '/skills/software', title: 'Software'},
      ]
    }
  }
}
</script>
<style scoped>
</style>