<template>
  <div>hover compteur</div>
  <div>
    <h1 @mouseover="incrementCount">hovered {{count}} times </h1>
  </div>
</template>

<script>

// import CounterMixin from '../mixins/counter' 
import useCounter from '@/composables/useCounter'

export default {
  name: 'HoverCounter',
  // mixins: [CounterMixin] 
  setup(){
  
    const {count, incrementCount} = useCounter()
    
    return {
      count,
      incrementCount
    }
  } 
}
</script>

<style>

</style>