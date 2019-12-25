<template>
  <v-card class="overflow-hidden">
    <v-app
      fixed
      color="#fff"
      prominent
    >
    <div>
      <v-container>
        <nuxt />
      </v-container>
    </div>
    <!-- <Footer /> -->
    </v-app>
  </v-card>
</template>

<script>
import Footer from '@/components/Footer'
export default {
  name: 'default',
  components:{
    Footer
  },
  data () {
    return {
    }
  },
}
</script>

<style scoped>
.v-tab--active{
  background-color: #5D82ED;
  border-radius: 25px;
  width: 100px;;
}
.width350{
  max-width: 300px;
}

</style>
