<template>
  <base-card>
    <base-button
      @click="setSelectedTab('stored-resources')"
      :mode="storedResButtonMode"
    >Stored Resources</base-button>
    <base-button @click="setSelectedTab('add-resources')" :mode="addResButtonMode">Add Resource</base-button>
  </base-card>
  <keep-alive>
    <component :is="selectedTab"></component>
  </keep-alive>
</template>

<script>
import StoredResources from './StoredResources.vue';
import AddResources from './AddResources.vue';

export default {
  components: {
    StoredResources,
    AddResources,
  },
  data() {
    return {
      selectedTab: 'stored-resources',
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
      ],
    };
  },
  provide() {
    return {
      resources: this.storedResources,
      addResource: this.addResource
    };
  },
  computed: {
    storedResButtonMode() {
      return this.selectedTab === 'stored-resources' ? null : 'flat';
    },
    addResButtonMode() {
      return this.selectedTab === 'add-resource' ? null : 'flat';
    },
  },
  methods: {
    setSelectedTab(tab) {
      this.selectedTab = tab;
    },
    addResource(title, description, url){
      const newResource = {
        id: new Date().toISOString(),
        title: title,
        description: description,
        link: url
      }
      this.storedResources.unshift(newResource)
      this.selectedTab = 'stored-resources'

    }
  },
};
</script>

<style>

</style>