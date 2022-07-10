<template >
  <h4>volume tracker - (0-20)</h4>
  <p>current volume - {{ volume }}</p>
  <p style="background: red; color white;" v-if="isAlarme">le volume est trop haut, baisse le stp...</p>
  <div>
    <button @click="volume += 2">increase</button>
    <button @click="volume -= 2">decrease</button>
  </div>

  <!--Immediate and Deep Watchers-->
  <input type="text" v-model="movie">
  <input type="text" v-model="movieInfo.title">
  <input type="text" v-model="movieInfo.actor">
  <div>
    <button @click="movieList.push('wonder woman')">ajouter movie</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      volume: 0,
      isAlarme: false,
      movie: 'batman',
      movieInfo: {
        title: '',
        actor: ''
      },
      movieList: ['rambo', 'vandamme']
    }    
  },
  methods: {},
  computed: {},
  watch: {
    volume(newValue, oldValue){
      if (newValue> oldValue && newValue === 16) {
        this.isAlarme = true
      }else {
        this.isAlarme = false
      }
    },
    movie: {
      handler(newValue){
      console.log(`app de l'api = ${newValue} `);
      },
      immediate: true
    },
    movieInfo: {
      handler(newValue){
        console.log(`app avec = ${newValue.title} ## ${newValue.actor} `);
      },
      deep: true
    },
    movieList: {
      handler(newValue){
        console.log(`liste movie mise à jour ${newValue} `)
      },
      deep: true
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
