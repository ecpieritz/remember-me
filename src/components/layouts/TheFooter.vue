<template>
  <footer>
    <h3>{{message}}</h3>

    <div class="socials">
      <a href="https://www.linkedin.com/in/ecpieritz/" target="_blank" rel="noopener noreferrer">
        <img id="linkedin" src="https://cdn.jsdelivr.net/npm/simple-icons@3.13.0/icons/linkedin.svg" alt="Linkedin">
      </a>

      <a href="https://www.instagram.com/ecpieritz/" target="_blank" rel="noopener noreferrer">
        <img id="instagram" src="https://cdn.jsdelivr.net/npm/simple-icons@3.13.0/icons/instagram.svg" alt="Instagram">
      </a>
      
      <a href="https://github.com/ecpieritz" target="_blank" rel="noopener noreferrer">
        <img id="instagram" src="https://cdn.jsdelivr.net/npm/simple-icons@3.13.0/icons/github.svg" alt="Instagram">
      </a>
    </div>
  </footer>
</template>

<script>
export default {
  props:['message'],
  data(){
    return{
      
    }
  }
};
</script>

<style scoped>
  footer{
    width: 100%;
    height: 4rem;
    background-color: #4d7cb3;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    position: fixed;
    bottom: 0;
    width: 100%;
  }

  footer h3{
    color: #000;
    margin-left: 2rem;
  }

  footer .socials{
    margin: auto 0;
    display: flex;
    flex-direction: row;
    width: 100px;
    justify-content: space-between;
    margin-right: 2rem;
  }

  footer .socials #linkedin, .socials #instagram, .socials #github{
  width: 25px;
}
</style>