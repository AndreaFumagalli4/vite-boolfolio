<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';

export default{
  name: 'App',

  components:{
    AppHeader,
    AppMain,
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
  <main>
    <AppMain />
  </main>
</template>

<style lang="scss">
@use '../node_modules/bootstrap' as *;
@use './styles/general.scss' as *;
@use './styles/partials/variables' as *;

</style>
