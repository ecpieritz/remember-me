<template>
  <div class="learning-resource">
    <ul>
      <li>
        <div>
          <header>
            <h3>{{title}}</h3>
            <button>Delete</button>
          </header>
        </div>
        <p>{{description}}</p>
        <nav>
          <a :href="link" target="_blank">View Resource</a>
        </nav>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: ['title', 'description', 'link']
}
</script>

<style>

</style>