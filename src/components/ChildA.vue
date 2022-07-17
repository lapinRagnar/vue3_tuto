<template>
  <div>child A</div>
  <child-b/>
</template>

<script>

import ChildB from './ChildB.vue'

export default {
  name: 'ChildA',
  components: { ChildB }

}
</script>

<style>

</style>