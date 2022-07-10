<template>
  <div>Component E</div>
  <ComponentF></ComponentF>
</template>

<script>
import ComponentF from './ComponentF.vue'

export default {
  name: 'ComponentE',
  components: { ComponentF}
}
</script>

<style>

</style>