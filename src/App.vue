<template>
  <div id="app">
    <TheHeader title="RememberMe"></TheHeader>
    <TheResources></TheResources>

    <TheFooter message="Developed with 💙 by Emilyn C. Pieritz" />
  </div>
</template>

<script>
import TheHeader from './components/layouts/TheHeader.vue';
import TheResources from './components/learning-resources/TheResoucers.vue';
import TheFooter from './components/layouts/TheFooter.vue'

export default {
  components: {TheHeader, TheResources, TheFooter}
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