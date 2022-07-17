<template>
  <div>child B</div>
  <ChildC />
</template>

<script>

import ChildC from './ChildC.vue'

export default {
  name: 'ChildB',
  components: { ChildC}
}
</script>

<style>

</style>