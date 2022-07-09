<template >
  <h2>computed total - {{ total }} </h2>
  <h2>Method total - {{ getTotal() }} </h2>
  <button @click="items.push({id: 4, title: 'essai', price: 1500})" >ajouter</button>
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      firstName: 'bruce',
      lastName: 'wayne',
      items: [
        {
          id: 1,
          title: 'tv',
          price: 200
        },
        {
          id: 2,
          title: 'phone',
          price: 3500
        },
        {
          id: 3,
          title: 'laptop',
          price: 400
        },
    ]
    }    
  },
  methods: {
    getTotal(){
      return this.items.reduce((total, curr) => (total = total + curr.price), 0) 
    }
  },
  computed: {
    total(){
      return this.items.reduce((total, curr) => (total = total + curr.price), 0) 
    }
  }
}
</script>

<style>

#app {

  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}


</style>
