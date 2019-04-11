<template>
  <ul class="subheader__list">
    <li class="subheader__item subheader__item--active">Inicio</li>
    <li class="subheader__item">Agendados</li>
    <li class="subheader__item">Finalizadas</li>
  </ul>
</template>

<script>
export default {
  name: 'Menu',
}
</script>

<style>
.subheader__list {
  width: 100%;
  height: 100%;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}

.subheader__item {
  padding: 10px;
  padding-bottom: 0;
  text-align: center;
  box-sizing: border-box;
  list-style-type: none;
  font-size: 14px;
  color: #4d646d;
}

.subheader__item--active {
  border-bottom: 2px solid #00a7e1;
  box-shadow: 0px 2px 0px rgba(0, 0, 0, 0.25);
  color: #000000;
}
</style>

