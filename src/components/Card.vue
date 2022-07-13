<template>
  <div class="card">
    <div id="card-header">
      <slot name="header"></slot>
    </div>

    <div id="card-content">
      <slot></slot>
    </div>

    <div id="card-footer">
      <slot name="footer"></slot>
    </div>
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