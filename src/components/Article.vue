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
    title: String,
    likes: Number,
    isPublished: Boolean
  }
}
</script>

<style>

</style>