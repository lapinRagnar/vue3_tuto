<template>
  <div>
    <h2>Article compo</h2>
    <h4 v-bind="$attrs" >{{ title}}</h4>
    <p>nombre de like - {{ likes }}</p>
    <p>published : {{isPublished ? 'yes' : 'no'}}</p>
  </div>
</template>

<script>
export default {
  name: 'ArticleCompo',
  props: {
    title: {
        type: String,
        required: true,
        default: 'ceci est le titre par defaut'
    },
    likes: Number,
    isPublished: Boolean
  },
  inheritAttrs: false
}
</script>

<style>

</style>