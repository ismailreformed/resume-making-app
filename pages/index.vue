<template>
 <div>

 </div>
</template>

<script>

export default {
   beforeRouteEnter(to, from, next) {
    if (to.path == '/') {
      //next('/settings/general-settings')
        next(vm => {
          next('/works')   
      })
    }
  },
}
</script>
