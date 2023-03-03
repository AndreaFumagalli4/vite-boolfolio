<script>
import AppHeader from './components/AppHeader.vue';

export default{
  name: 'App',

  components:{
    AppHeader,
  },
  
  data() {
    return {
      
    }
  },
}
</script>

<template>
  <header>
    <AppHeader />
  </header>
  <router-view></router-view>
</template>

<style lang="scss">
@use '../node_modules/bootstrap' as *;
@use './styles/general.scss' as *;
@use './styles/partials/variables' as *;

</style>
