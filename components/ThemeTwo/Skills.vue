<template>
  <div>
    <v-card flat>
      <v-tabs
        v-model="tab"
        class="text-center mt-1"
        background-color="#FBFBFB"
        height="60"
        centered
        hide-slider
        align-with-title
        next-icon="mdi-arrow-right-bold-box-outline"
        prev-icon="mdi-arrow-left-bold-box-outline"
        show-arrows
 
      >        
        <v-tab href="#programming">
           Programming
        </v-tab>
        <v-tab class="mx-1"  href="#framework">
            Framework & Database
        </v-tab>
        <v-tab class="mx-1"  href="#design-skills">
            Design Skills
        </v-tab>
        <v-tab  href="#software">
           Software
        </v-tab>
      </v-tabs>

      <v-expand-transition>
        <v-tabs-items v-model="tab" class="py-2">
          <v-tab-item   class="fade-in" value="design-skills">
            <DesignSkills />
          </v-tab-item>
          <v-tab-item  class="fade-in" value="framework">
            <Framework />
          </v-tab-item>
          <v-tab-item  class="fade-in" value="programming">
            <Programming />
          </v-tab-item>
          <v-tab-item  class="fade-in" value="software">
            <Software />
          </v-tab-item>
        </v-tabs-items>
      </v-expand-transition>
    </v-card>
  </div>
</template>

<script>
import DesignSkills from '@/components/ThemeTwo/Skills/DesignSkills'
import Framework from '@/components/ThemeTwo/Skills/Framework'
import Programming from '@/components/ThemeTwo/Skills/Programming'
import Software from '@/components/ThemeTwo/Skills/Software'

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
    background-color: #EEF6FF;
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
  background-color: white;
  border-radius: 25px;
  width: 130px;
}
.fade-in {
	opacity: 1;
	animation-name: fadeInOpacity;
	animation-iteration-count: 1;
	animation-timing-function: ease-in;
	animation-duration: 1s;
}

@keyframes fadeInOpacity {
	0% {
		opacity: 0;
	}
	100% {
		opacity: 1;
	}
}
</style>