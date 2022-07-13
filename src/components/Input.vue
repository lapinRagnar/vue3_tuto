<template>
  <input 
    type="text" 
    :value="modelValue"
    @input="$emit('update:modelValue', $event.target.value)"  
  >
</template>

<script>
export default {
  name: 'InputCompo',
  props: {
    modelValue: String
  }
}
</script>

<style>
  input{
    border:0;
    border-bottom:1px solid #555;  
    background:transparent;
    width:100%;
    padding:8px 0 5px 0;
    font-size:16px;
    color:rgb(143, 24, 24);
  }
  input:focus{
    border:none;	
    outline:none;
    border-bottom:1px solid #e74c3c;	
  }
</style>