<template>
  <div>
    <div class="content">
      <h1 class="title">
          Coffee plans
      </h1>

      <h2 class="subtitle">
          we travel the world
      </h2>


      <items/>
    </div>
  </div>
</template>

<script>
import Items from '@/components/Items'

export default {
  name: 'Home',
  components: {
    Items
  },
  data () {
    return { 
      model: {
        id: null,
        name: null
      }
    }
  },
}
</script>

<style>
body {
    height: 100vh;
    -webkit-font-smoothing: auto;
    -moz-osx-font-smoothing: auto;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    font-family: Roboto, sans-serif;
    background-color: #ccdcdc;
    /* background-image: url("./assets/coffee.jpg"); */
    background-repeat: no-repeat;
    background-position: 100% 100%;
    text-align: center;
}
</style>
