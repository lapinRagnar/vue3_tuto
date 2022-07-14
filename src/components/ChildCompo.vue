<template>
  <div>Child</div>
</template>

<script>


export default {
  name: 'ChildCompo',
  beforeCreate(){
    console.log('child beforeCreate');
  },
  created(){
    console.log('child created');
  },
  beforeMount(){
    console.log('child beforeMount');
  },
  mounted(){
    console.log('child mounted');
  },
  beforeUpdate(){
    console.log('child beforeUpdate');
  },
  updated(){
    console.log('child updated');
  },
  beforeUnmount(){
    console.log('child beforeUnmount');
  },
  unmounted(){
    console.log('child unmounted');
  }
}
</script>

<style>

</style>