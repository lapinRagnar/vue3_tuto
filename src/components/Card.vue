<template>
  <div class="card">
    <p>je suis dans card </p>
    <slot>Default content</slot> 
  </div>
</template>

<script>
export default {
  name: 'CardCompo',
  props: ['content']
}
</script>

<style>
  .card{
    width: 60%;
    height: 80%;
    max-height: 300px;
    padding: auto;
    text-align: center;
    background: #242625;
    color: white;
    border-radius: 10px;
    box-shadow: 25px 25px 50px #1b1c1b, -25px -25px 50px 
  }
</style>