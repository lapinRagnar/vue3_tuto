<template>
  <h1>option api </h1>
  <div>
    <input type="text" placeholder="name" v-model="name">
  </div>

  <h1>watch</h1>


</template>

<script>

export default {
  name: 'WatchCompo',
  data(){
    return{
        name: ''
    }
  },
  watch:{
    name(newValue, oldValue){
        console.log('oldValue', oldValue);
        console.log('newValue', newValue);
    }
  }

}
</script>

<style>

</style>