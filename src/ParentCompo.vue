<template>
  <div>parent</div>
  <button @click="showChild=!showChild">toggle child</button>
  <child-compo v-if="showChild"></child-compo>
</template>

<script>

import ChildCompo from './components/ChildCompo.vue'

export default {
  name: 'ParentCompo',
  components: {ChildCompo},
  data () {
    return {
        showChild: true
    }
  },
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