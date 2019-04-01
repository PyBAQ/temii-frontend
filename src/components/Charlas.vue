<template>
  <div class="header">
    <div class="header-logo">Temii</div>
  </div>
</template>

<script>
export default {
  name: 'Charlas',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
body {
  padding: 0px;
  margin: 0px;
}

.header {
  margin: 0px;
  height: 80px;
  border-bottom: 1px solid #e5e5e5;
}

.header-logo {
  font-family: 'Pacifico';
  font-size: 48px;
  color: #00a7e1;
  padding-left: 16px;
}
</style>
