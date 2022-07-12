<template >
  <div>app compo</div>
  <button  @click="showPopup=true">afficher popup</button>
  <PopupCompo v-if="showPopup" @cacher="showPopup = false"/>
</template>

<script>

import PopupCompo from './components/Popup.vue'

export default {
  name: 'App',
  components: {PopupCompo},
  data(){
    return {
      showPopup: false
    }    
  },
  methods: {},
  computed: {},
  watch: {}
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
