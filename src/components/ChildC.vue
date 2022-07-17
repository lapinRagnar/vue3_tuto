<template>
  <div>child C</div>
  <h3>options api - provide et inject</h3>
  <div>on a recupé la donnée name du parent component - name = {{userName}} </div> <hr>

  <h3>composition api - provide et inject</h3>
  <div>injection donnée parent lointain - username = {{childUserName}} </div> <hr>
  
  <h3>composition api - provide et inject - avec ref reactive toRefs</h3>
  <p>child component c count = {{childCount}}</p>
  <p>child component c hero = {{firstName}} et {{lastName}}</p>
  <button @click="incrementCount">incrementcount from child c</button>

</template>

<script>

import {inject, toRefs} from 'vue'

export default {
  name: 'ChildC',
  inject: ['userName'],
  setup(){
    const childUserName = inject('c_userName', 'default username')
    const childCount = inject('c_count', 0)
    const childHero = inject('c_hero', {})
    const incrementCount = inject('incrementCount')

    return {
        childUserName,
        childCount,
        ...toRefs(childHero),
        incrementCount,
    }
  }
}
</script>

<style>

</style>