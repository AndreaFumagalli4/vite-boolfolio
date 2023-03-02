<script>
import AppMain from './components/AppMain.vue';

export default{
  name: 'App',

  components:{
    AppMain,
  },
  
  data() {
    return {
      
    }
  },
}
</script>

<template>
  <!-- Header -->
  <main>
    <AppMain />
  </main>
</template>

<style lang="scss">
@use '../node_modules/bootstrap' as *;
@use './styles/general.scss' as *;
@use './styles/partials/variables' as *;

</style>
