<template>
  <div>
    
  </div>
</template>
<script>
export default {
  name: 'themeTwo.vue',
  layout: 'themeTwoLayout',
  beforeRouteEnter(to, from, next) {
    if (to.path == '/theme-two') {
        next(vm => {
          next('/theme-two/works')   
      })
    }
  },
}
</script>