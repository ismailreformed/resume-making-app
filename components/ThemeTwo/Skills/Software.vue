<template>
  <div class="py-5" style="display: flex;
  justify-content: center;">
    <ul class="pa-0">
        <li class="listDesign ma-1" v-for="item in skillPercentages" :key="item.id">
          <span style="color: #0A56E9;" >{{ item.title }}</span>
          <br >
          <div class="leftSideTag" >
            <v-progress-linear :value="item.percentage"></v-progress-linear>
          </div>
          <div class="rightSideTag">
            {{ item.percentage }}
          </div>
        </li>
    </ul>
  </div>
</template>
<script>
export default {
  data(){
    return{
      skillPercentages:[
        {id: 1, title: 'Ps', percentage: '85%' },
        {id: 2, title: 'Xd', percentage: '65%' },
        {id: 3, title: 'Ai', percentage: '95%' },
        {id: 4, title: 'In', percentage: '75%' },
        {id: 5, title: 'Ae', percentage: '45%' },
      ]
    }
  }
}
</script>
<style scoped>

ul {
  list-style-type: none;
}

li{
  display: inline-block;
  text-align: start !important;
}

li div{
  display: inline-flex;
}
.listDesign{
  width:150px;
}
.leftSideTag{
  width:65%;
}
.rightSideTag{
  width:28%;
  color: #0A56E9
}

</style>