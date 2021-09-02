<template>
  <button :type="type" :class="mode">
    <slot></slot>
  </button>
</template>

<script>
export default {
  props:['type', 'mode']
}
</script>

<style scoped>
  button {
    padding: 0.75rem 1.5rem;
    font-family: inherit;
    background-color: #ce0071;
    border: 1px solid #ce0071;
    border-radius: 8px;
    color: white;
    cursor: pointer;
  }

  button:hover,
  button:active {
    background-color: #d14190;
    border-color: #d14190;
  }

  .flat {
    background-color: transparent;
    color: #ce0071;
    border: none;
  }

  .flat:hover,
  .flat:active {
    background-color: #e065a9;
    color: #fff;
  }
</style>