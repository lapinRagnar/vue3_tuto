<template>
  <div>hover compteur</div>
  <div>
    <h1 @mouseover="incrementCount">hovered {{count}} times </h1>
  </div>
</template>

<script>

import CounterMixin from '../mixins/counter' 

export default {
  name: 'HoverCounter',
  mixins: [CounterMixin] 
}
</script>

<style>

</style>