<template >
  <h4>volume tracker - (0-20)</h4>
  <p>current volume - {{ volume }}</p>
  <p style="background: red; color white;" v-if="isAlarme">le volume est trop haut, baisse le stp...</p>
  <div>
    <button @click="volume += 2">increase</button>
    <button @click="volume -= 2">decrease</button>
  </div>

</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      volume: 0,
      isAlarme: false
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
