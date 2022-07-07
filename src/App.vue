<template>
  <h2 v-bind:class="status">souligner ce text</h2>
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      status: 'success'
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.souligner{
  text-decoration: underline;
}

</style>
