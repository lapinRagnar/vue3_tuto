<template>
  <h1>life cycle avec - composition api</h1>
</template>

<script>


import {
  onBeforeMount,
  onMounted,
  onBeforeUpdate,
  onBeforeUnmount,
  onUnmounted,
  onUpdated
} from 'vue'

export default {
  name: 'LifecycleComposition',
  setup(){

    onBeforeMount(()=>{
      console.log('lifecycle c onBeforeMount');
    })

    onMounted(()=>{
      console.log('lifecycle c onMounted');
    })

    onBeforeUpdate(()=>{
      console.log('lifecycle c onBeforeUpdate');
    })

    onUpdated(()=>{
        console.log(('lifecycle c onUpdated'));
    })

    onBeforeUnmount(()=>{
      console.log('lifecycle c onBeforeUnmount');
    })

    onUnmounted(()=>{
        console.log('lifecycle c onUnmounted');
    })

  }


}

</script>

<style>

</style>