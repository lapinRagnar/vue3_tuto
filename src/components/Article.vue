<template>
  <h2>Article compo</h2>
  <h4>{{ title}}</h4>
  <p>nombre de like - {{ likes }}</p>
  <p>published : {{isPublished ? 'yes' : 'no'}}</p>
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
  }
}
</script>

<style>

</style>