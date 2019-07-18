<template>
  <ul class="subheader__list">
    <li class="subheader__item subheader__item--active">Inicio</li>
    <li class="subheader__item">Agendados</li>
    <li class="subheader__item">Finalizadas</li>
  </ul>
</template>

<script>
export default {
  name: 'Menu'
}
</script>

<style>
.subheader__list {
  width: 100%;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  box-shadow: 0 0 3px rgba(0, 0, 0, 0.25);
}
.subheader__item {
  padding: 13px;
  text-align: center;
  box-sizing: border-box;
  list-style-type: none;
  font-size: 14px;
  color: #4d646d;
}
.subheader__item--active {
  border-bottom: 2px solid #00a7e1;
  /* box-shadow: 0px 2px 0px rgba(0, 0, 0, 0.25); */
  color: #000000;
}
@media (min-width: 767px) {
  .subheader__list {
    width: 400px;
    box-shadow: none;
  }
}
</style>
