<template>
  <h2>Bonjour {{ name }} a.k.a {{ heroName}}</h2>
</template>

<script>
export default {
  name: 'GreetCompo',
  props: ['name', 'heroName']
}
</script>

<style>

</style>