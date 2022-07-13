<template >
  <div>app compo - http api request</div>
  <CreatePost/>
  <PostList/>

</template>

<script>


import PostList from './components/PostList.vue'
import CreatePost from './components/CreatePost.vue'

export default {
  name: 'App',
  components: { PostList, CreatePost },
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
