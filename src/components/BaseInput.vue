<template>
  <input :type="type" :value="value" @input="$emit('input', $event.target.value)">
</template>

<script>
export default {
  name: 'BaseInput',
  props: {
    value: String,
    type: {
      type: String,
      default: 'text'
    }
  }
}
</script>
<style scoped>
input[type='text'],
input[type='password'],
input[type='email'] {
  height: 38px;
  width: 500px;
  font-size: 14px;
  display: block;
  padding: 6px 10px; /* The 6px vertically centers text on FF, ignored by Webkit */
  background-color: #fff;
  border: 1px solid #d1d1d1;
  border-radius: 4px;
  box-shadow: none;
  box-sizing: border-box;
  font-family: 'Raleway';
  outline: none;
}
</style>
