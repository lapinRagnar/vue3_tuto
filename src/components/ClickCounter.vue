<template>
  <div>click compteur</div>
  <div>
    <button @click="incrementCount">clicked {{count}} times </button>
  </div>
</template>

<script>

import CounterMixin from '../mixins/counter'

export default {
  name: 'ClickCounter',
  mixins: [CounterMixin], 
}
</script>

<style>

</style>