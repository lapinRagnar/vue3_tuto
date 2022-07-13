<template >
  <div>app compo</div>
  <PostList/>

</template>

<script>


import PostList from './components/PostList.vue'

export default {
  name: 'App',
  components: { PostList },
  data(){
    return {}    
  },
  methods: {},
  computed: {},
  watch: {}
}
</script>

<style scoped>

  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
  }

</style>
