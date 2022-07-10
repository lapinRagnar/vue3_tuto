<template >
  <GreetCompo name="clarc" heroName="batman" ></GreetCompo>
  <GreetCompo name="lady gaga"  heroName="superman" ></GreetCompo>
  <GreetCompo name="diana" heroName="catwoman" ></GreetCompo>
  <GreetCompo :name="name"  :heroName="prenom" ></GreetCompo>
  <hr>
  <ArticleCompo id="mon-super-id" :likes="2" :isPublished="false"></ArticleCompo>
</template>

<script>
import GreetCompo from './components/Greet.vue'
import ArticleCompo from './components/Article.vue'

export default {
  name: 'App',
  components: { GreetCompo, ArticleCompo },
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
