<template>
  <h2>templateRef avec - option api</h2>
  <input type="text" placeholder="tapez texte" ref="inputRef">
  
  
</template>

<script>


export default {
  name: 'TemplateRefere',
  mounted(){
    this.$refs.inputRef.focus()
  }
}
</script>

<style>

</style>