<template>
  <div>
    <ul class="text-center">
        <li class="listDesign ma-1" v-for="item in skillPercentages" :key="item.id">
          <div class="leftSideTag" >{{ item.title }}</div>
          <div class="white--text rightSideTag">{{ item.percentage }}</div>
        </li>
    </ul>
  </div>
</template>
<script>
export default {
  data(){
    return{
      skillPercentages:[
        {id: 1, title: 'PHP', percentage: '85%' },
        {id: 2, title: 'js', percentage: '65%' },
        {id: 3, title: 'HTML', percentage: '95%' },
        {id: 4, title: 'CSS', percentage: '75%' },
        {id: 5, title: 'C++', percentage: '45%' },
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
  display: inline-block
}

li div{
  display: inline-flex;
  align-items: center;
  justify-content: center;
  height: 100%;
}
.listDesign{
  height:35px;
  width:100px;
  border-radius:25px;
  border-left: 1px solid #313450;
  border-top:  1px solid #313450;
  border-bottom:  1px solid #313450
}
.leftSideTag{
  width:48%;
}
.rightSideTag{
  width:47%;
  background-color: #313450;
  border-top-right-radius: 25px;
  border-bottom-right-radius: 25px;
}
</style>