<template>
<div>
  <base-card>
    <base-button @click="setSelesctedTab('stored-resources')">Stored Resources</base-button>
    <base-button @click="setSelesctedTab('add-resource')">Add Resources</base-button>
  </base-card>
  <component :is="selectedTab"></component>
</div>
</template>

<script>
import StoredResources from './StoredResources.vue'
import AddResource from './AddResource.vue'

export default {
  components: {StoredResources, AddResource},
  data(){
    return{
      selectedTab: 'stored-resources'
    }
  },
  methods: {
    setSelectedTab(tab){
      this.selectedTab = tab
    }
  }
}
</script>

<style>

</style>