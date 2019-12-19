<template>
  <div>
    <v-card flat>
      <v-tabs
        v-model="tab"
        centered
        class="text-center"
        background-color="#FBFBFB"
        height="70"
        hide-slider
      >        
        <v-tab href="#programming">
           Programming
        </v-tab>
        <v-tab class="mx-3"  href="#framework">
            Framework
        </v-tab>
        <v-tab class="mx-3"  href="#design-skills">
            Design Skills
        </v-tab>
        <v-tab  href="#software">
           Software
        </v-tab>
      </v-tabs>

      <v-tabs-items v-model="tab" class="pt-5">
        <v-tab-item value="design-skills">
          <DesignSkills />
        </v-tab-item>
        <v-tab-item value="framework">
          <Framework />
        </v-tab-item>
        <v-tab-item value="programming">
          <Programming />
        </v-tab-item>
        <v-tab-item value="software">
          <Software />
        </v-tab-item>
      </v-tabs-items>
    </v-card>
  </div>
</template>

<script>
import DesignSkills from '@/components/Skills/DesignSkills'
import Framework from '@/components/Skills/Framework'
import Programming from '@/components/Skills/Programming'
import Software from '@/components/Skills/Software'

export default {
  components:{
    DesignSkills,
    Framework,
    Programming,
    Software
  },
  data(){
    return {
      tab: 'programming',
      skillSets: [
        { id: 1, to: 'programming', title: 'Programming Language'},
        { id: 2, to: 'framework', title: 'Framwork/Database'},
        { id: 3, to: 'design-skills', title: 'Design Skill'},
        { id: 4, to: 'software', title: 'Software'},
      ]
    }
  },

}
</script>
<style scoped>
.theme--light.v-tabs-items {
    background-color: #FBFBFB;
}
.v-item-group.theme--light.v-slide-group.v-tabs-bar{
height: 70px;;
}
.v-tab{
  background-color: white;
  border-radius: 25px;
  width: 20%;
}
.v-tab--active{
  background-color: blanchedalmond;
  border-radius: 25px;
  width: 20%;
}
</style>