<template>
  <h1>life cycle avec - options api</h1>
</template>

<script>

export default {
  name: 'LifecycleOptions',
  beforeCreate(){
    console.log('parent beforeCreate');
  },
  created(){
    console.log('parent created');
  },
  beforeMount(){
    console.log('parent beforeMount');
  },
  mounted(){
    console.log('parent mounted');
  },
  beforeUpdate(){
    console.log('parent beforeUpdate');
  },
  updated(){
    console.log('parent updated');
  },
  beforeUnmount(){
    console.log('parent beforeUnmount');
  },
  unmounted(){
    console.log('parent unmounted');
  }
}
</script>

<style>

</style>