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
  height: 38px;
  display: flex;
  width: 100%;
  max-width: 700px;
  min-width: 200px;
  height: 40px;
}

.input-field {
  text-indent: 40px;
  border: 0.75px solid #a0bec8;
  background: #f8f8f8;
  border-radius: 4px;
  width: 100%;
  max-width: 800px;
  min-width: 200px;
  outline: none;
  font-family: 'Raleway';
  font-size: 14px;
}

.input-field:hover,
.input-field:focus {
  background: white;
  border: 0.75px solid rgb(0, 121, 211);
}

</style>
