<template>
  <div v-for=" (name, i) in names" :key="i">
    Bonjour # 
    <slot :firstName="name.firstName" :lastName="name.lastName"></slot>
  </div>
</template>

<script>
export default {
  name: 'NameList',
  data() {
    return { 
      names: [
        {
            firstName: 'lapin',
            lastName: 'Lance',
        },
        {
            firstName: 'bitro',
            lastName: 'robert',
        },
        {
            firstName: 'france',
            lastName: 'gall',
        },
      ],
    }
  }
}
</script>

<style>

</style>