<template>
  <div class="base-card">
    <slot></slot>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
  .base-card{
    border-radius: 12px;
    box-shadow: 0 2px 8px rgba(253, 254, 255, 0.6);
    background-color: #b1ceec;
    padding: 1rem;
    margin: 2rem auto;
    max-width: 40rem;
  }
</style>