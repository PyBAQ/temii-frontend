<template>
  <textarea :value="value" @input="$emit('input', $event.target.value)"></textarea>
</template>

<script>
export default {
  name: 'BaseTextarea',
  props: ['value']
}
</script>

<style scoped>
textarea {
  height: 38px;
  width: 500px;
  outline: none;
  font-family: 'Raleway';
  font-size: 14px;
  padding: 6px 10px; /* The 6px vertically centers text on FF, ignored by Webkit */
  background-color: #fff;
  border: 1px solid #d1d1d1;
  border-radius: 4px;
  box-shadow: none;
  box-sizing: border-box;
  min-height: 65px;
  padding-top: 6px;
  padding-bottom: 6px;
}
</style>
