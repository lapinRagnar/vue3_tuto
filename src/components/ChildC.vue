<template>
  <div>child C</div>
  <div>on a recupé la donnée name du parent component - name = {{userName}} </div>
</template>

<script>

export default {
  name: 'ChildC',
  inject: ['userName']
}
</script>

<style>

</style>