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
  height: 40px;
}
.input-field {
  display: inline-flex;
  width: 100%;
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
@media (min-width: 767px) {
  .header__search {
    margin-left: 24px;
    width: 100%;
    max-width: 700px;
  }
}

@media (min-width: 1200px) {
  .header__search {
    margin-left: 0;
  }
}
</style>
