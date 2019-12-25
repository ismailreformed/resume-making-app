<template>
  <div>
      <SlickCarousel />
  </div>
</template>

<script>
import SlickCarousel from '@/components/SlickCarousel'
export default {
  name: 'themeOne.vue',
  layout: 'themeOneLayout',
  components: {
    SlickCarousel
  }
}
</script>