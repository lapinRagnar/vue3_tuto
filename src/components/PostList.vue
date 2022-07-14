<template>
  <div>post list compo</div>
  <button @click="getPosts">Load Post</button>
  <h2 v-if="errorMsg">{{errorMsg}}</h2>
  <div v-for="post in posts" :key="post.id">
    <h3>{{post.id}} ## {{post.title}}</h3>
    <p style="boder-bottom: 1px style orange">{{post.body}}</p>
  </div>
</template>

<script>

import axios from 'axios'

export default {
  name: 'PostList',
  created(){
    this.getPosts()
  },
  data(){
    return {
      posts: [],
      errorMsg: ''
    }
  },
  methods: {
    getPosts(){
      axios.get('https://jsonplaceholder.typicode.com/posts')
        .then((response)=>{
            console.log(response.data);
            this.posts = response.data
        })       
        .catch((error)=>{ 
          console.log(error);
          this.errorMsg = "erreur oups les mecs - " + error
        })  
    }
  }
}
</script>

<style>

</style>