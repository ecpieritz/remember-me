<template>
  <div id="app">
    <TheHeader title="RememberMe" />
    <StoredResources />
  </div>
</template>

<script>
import StoredResources from './components/learning-resources/StoredResources.vue'
import TheHeader from './components/layouts/TheHeader.vue'
export default {
  components: {
    StoredResources, TheHeader
  },
  data(){
    return{
      
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

* {
  box-sizing: border-box;
}

html {
  font-family: 'Roboto', sans-serif;
  background-color: #01152c;
}

body {
  margin: 0;
}
</style>