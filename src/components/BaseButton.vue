<template>
  <button :class="type" :disabled="disabled">
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: 'BaseButton',
  props: {
    type: {
      type: String
    },
    disabled: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style scoped>
button {
  padding: 10px 20px;
  border: 1px solid #ddd;
  color: #333;
  background-color: #fff;
  border-radius: 4px;
  font-family: 'Raleway';
  font-size: 14px;
  cursor: pointer;
}
button[disabled] {
  cursor: not-allowed;
}
button.danger {
  background-color: #ff4949;
  color: #fff;
}
button.success {
  background-color: #13ce66;
  color: #fff;
}
button.info {
  background-color: #00a7e1;
  border-color: #00a7e1;
  color: #fff;
}
</style>
