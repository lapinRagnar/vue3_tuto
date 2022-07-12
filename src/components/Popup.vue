<template>
  <h1>c'est le popup</h1>
  <button @click="$emits('cacher')">cacher</button>

</template>

<script>
export default {
  name: 'PopupCompo',
  emits: ['cacher']

}
</script>

<style>

</style>