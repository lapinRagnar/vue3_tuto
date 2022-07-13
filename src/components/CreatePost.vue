<template>
  <h1>Create Post</h1>
  <div>
    <form @submit.prevent="createPost">
      <div>
        <label for="title">title</label>
        <input type="text" id="title" name="title" v-model="formData.title"/>
      </div>
      <div>
        <label for="body">body</label>
        <input type="text" id="body" name="body" v-model="formData.body"/>
      </div>
      <button>create post</button>
    </form>
  </div>
</template>

<script>

import axios from 'axios'

export default {
    name: 'CreatePost',
    data(){
      return {
        formData: {
            userId: '',
            title: '',
            body: ''
        }
      }
    },
    methods: {
      createPost(){
        axios.post('https://jsonplaceholder.typicode.com/posts', this.formData)
          .then(response => console.log(response))
          .catch(error => console.log(error))
      }
    }
}
</script>

<style>

  form{
    display: flex;
    flex-direction: column;
    width: 300px;
    align-items: flex-start;
    justify-content: space-between;
    gap: 20px;
  }

  form div{
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  form div label {
    width: 50px;
    font-size: 20px;
    font-weight: bold;
  }

  form div input{
    border: none;
    border-bottom: 1px solid yellowgreen;
  }


</style>