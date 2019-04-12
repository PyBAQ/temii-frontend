<template>
  <div class="header__search">
    <div class="icon-container">
      <i class="fa fa-search icon"></i>
    </div>
    <div class="input-field">
      <input type="text" placeholder="Buscar charlas en Temii" name="usrnm">
    </div>
  </div>
</template>

<script>
export default {
  name: 'SearchInput'
}
</script>


<style>
.header__search {
  display: block;
  position: relative;
  height: 38px;
  width: calc(100% - 32px);
  max-width: 700px;
  min-width: 200px;
  height: 40px;
}

.input-field {
  display: inline-flex;
  width: calc(100% - 72.75px);
  height: 38px;
  border: 0.75px solid #a0bec8;
  background: #f8f8f8;
  border-radius: 4px;
  padding-left: 72px;
}

.input-field input {
  border: none;
  background-color: transparent;
  outline: none;
  font-family: 'Raleway';
  font-size: 14px;
  width: 100%;
}

.input-field:hover,
.input-field:focus {
  background: white;
  border: 0.75px solid rgb(0, 121, 211);
}

.icon-container {
  position: absolute;
  height: 38px;
  width: 72px;
  border: 0.75px solid transparent;
  display: flex;
  justify-content: center;
  align-items: center;
}

.icon {
  height: 18px;
  color: #00a7e1;
  font-size: 20px;
}
</style>
