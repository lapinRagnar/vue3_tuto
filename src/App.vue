<template >
  <h2>computed total - {{ total }} </h2>
  <h2>Method total - {{ getTotal() }} </h2>
  <button @click="items.push({id: 4, title: 'essai', price: 1500})" >ajouter</button>

  <!--Afficher les produits qui a un prix superieur à 200 euro-->
  <h2 style="border-bottom: 1px solid blue;">prix supérieur à 200 euro avec v-for</h2>
  <template v-for="item in items" :key="item.id">
    <h4 v-if="item.price > 200">{{ item.title}} - {{ item.price}}</h4>
  </template>

  <!--Afficher les produits qui a un prix superieur à 200 euro-->
  <h2 style="border-bottom: 1px solid blue;">prix supérieur à 200 euro avec v-for et computed property</h2>
  <h4 v-for="item in expensiveItems" :key="item.id">{{ item.title}} ## {{ item.price}}</h4>

  <!--getter et setter avec computed property-->
  <h2 style="border-bottom: 1px solid blue;">getter et setter avec computed property</h2>
  <h4>computed fullName - {{ fullName }}</h4>
  <button @click="changeFullName">Changer le nom</button>

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
    },
    changeFullName(){
      this.fullName = 'clark kent'
    }
  },
  computed: {
    total(){
      return this.items.reduce((total, curr) => (total = total + curr.price), 0) 
    },
    expensiveItems(){
      return this.items.filter(item => item.price > 200)
    },
    fullName: {
      get(){
        return `${this.firstName} ** ${this.lastName}`
      },
      set(value){
        const names = value.spit(' ')
        this.firstName = names[0]
        this.lastName = names[1]
      }
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
