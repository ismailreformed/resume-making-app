<template>
  <div>
    
  </div>
</template>
<script>
export default {
  beforeRouteEnter(to, from, next) {
    if (to.path == '/theme-one') {
        next(vm => {
          next('/theme-one/works')   
      })
    }
  },
}
</script>