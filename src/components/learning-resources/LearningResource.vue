<template>
  <div class="learning-resource">
    <ul>
      <li>
        <base-card>
          <header>
            <h3>{{title}}</h3>
            <base-button>Delete</base-button>
          </header>
          <p>{{description}}</p>
          <nav>
            <a :href="link" target="_blank">View Resource</a>
          </nav>
        </base-card>
      </li>
    </ul>
  </div>
</template>

<script>
import BaseButton from '../UI/BaseButton.vue'
export default {
  components: { BaseButton },
  props: ['title', 'description', 'link']
}
</script>

<style>
li {
  margin: auto;
  max-width: 40rem;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

h3 {
  font-size: 1.25rem;
  margin: 0.5rem 0;
  color: #00499c;
}

p {
  margin: 0.5rem 0;
}

a {
  text-decoration: none;
  color: #ce0071;
}

a:hover,
a:active {
  color: #d14190;
}
</style>