<template >
  <div>
    <pre>
      {{ JSON.stringify(formValues, null, 2)}}
    </pre>
  </div>
  <form action="">
    <div>
      <label for="name">name</label>
      <input type="text" id="name" v-model="formValues.name">
    </div>
  </form>
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      formValues: {
        name:''
      }
    }    
  },
  methods: {

  }
}
</script>

<style>

label{
  font-weight: bold;
  display: flex;
  margin-bottom: 5px;
}

input + label {
  font-weight: bold;
  display: inline-flex;
  margin-right: 20px;
}

input[type='text'], 
textarea,
select{
  display: block;
  width: 400px;
  padding: 6px 12px;
  font-size: 14px;
  line-height: 1.42;
  color: #555;
  background-color: #fff;
  background-image: none;
}

#app {

  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}


</style>
