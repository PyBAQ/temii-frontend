<template>
  <div class="header__search">
    <i class="fa fa-search icon"></i>
    <input class="input-field" type="text" placeholder="Buscar charlas en Temii" name="usrnm">
  </div>
</template>

<script>
export default {
  name: 'SearchInput'
}
</script>


<style>
.header__search {
  margin: auto;
  margin-left: 74px;
  height: 38px;
  display: -ms-flexbox;
  display: flex;
  width: 100%;
  height: 40px;
}
</style>
