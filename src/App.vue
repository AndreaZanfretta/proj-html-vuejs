<template>
  <div id="app">

    <app-header />


    <app-main />

    <app-footer />

  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';


export default {
  name: 'App',
  components: {
    AppHeader,
    AppMain,
    AppFooter
  },
  data(){
    return{

    }
  }
}
</script>

<style lang="scss">
@import "./styles/generals";
#app {

}
</style>
