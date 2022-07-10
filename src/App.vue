<template >
  <GreetCompo name="clarc" heroName="batman" ></GreetCompo>
  <GreetCompo name="lady gaga"  heroName="superman" ></GreetCompo>
  <GreetCompo name="diana" heroName="catwoman" ></GreetCompo>
  <GreetCompo :name="name"  :heroName="prenom" ></GreetCompo>
</template>

<script>
import GreetCompo from './components/Greet.vue'
export default {
  name: 'App',
  components: { GreetCompo },
  data(){
    return {
      name: 'lapin',
      prenom: 'ragnar'
    }    
  },
  methods: {},
  computed: {},
  watch: {
   
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
