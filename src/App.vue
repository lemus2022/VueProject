<template>
  <SecondaryComponent />
  <MainComponent  />
  
</template>

<script>
import MainComponent from './components/MainComponent.vue'
import SecondaryComponent from './components/SecondaryComponent.vue';

export default {
  name: 'App',
  components: {
    MainComponent,
    SecondaryComponent
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
