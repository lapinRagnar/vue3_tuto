<template>
  <div>child C</div>
  <h3>options api - provide et inject</h3>
  <div>on a recupé la donnée name du parent component - name = {{userName}} </div>
  <h3>composition api - provide et inject</h3>
  <div>injection donnée parent lointain - username = {{childUserName}} </div>

</template>

<script>

import {inject} from 'vue'

export default {
  name: 'ChildC',
  inject: ['userName'],
  setup(){
    const childUserName = inject('c_userName', 'default username')
    return {
        childUserName
    }
  }
}
</script>

<style>

</style>