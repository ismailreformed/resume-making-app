<template>
  <div>
    
  </div>
</template>
<script>
export default {
  beforeRouteEnter(to, from, next) {
    if (to.path == '/theme-two') {
        next(vm => {
          next('/theme-two/works')   
      })
    }
  },
}
</script>