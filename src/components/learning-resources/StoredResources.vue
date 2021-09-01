<template>
  <div class="stored-resources">
    <LearningResources v-for="res in storedResources" :key="res.id"
      :title="res.title" :description="res.description" :link="res.link" />
  </div>
</template>

<script>
import LearningResources from './LearningResource.vue'
export default {
  components: {
    LearningResources
  },
  data(){
    return{
      storedResources: [
        {id:'vue-doc', 
        title: 'Vue Documentation', 
        description: 'Site with official Vue.js documentation',
        link: 'https://vuejs.org/v2/guide/'},
        {id:'bootstrap-vue-doc', 
        title: 'Bootstrap-Vue Documentation', 
        description: 'Site with official Bootstrap Vue documentation',
        link: 'https://bootstrap-vue.org/'},
        {id:'vuetify-doc', 
        title: 'Vuetify Documentation', 
        description: 'Site with official Vuetify documentation',
        link: 'https://vuetifyjs.com/en/getting-started/installation/'}
      ]
    }
  }
}
</script>

<style>

</style>