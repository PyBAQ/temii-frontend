<template>
  <nav>
    <div class="header">
      <div class="header__logo">Temii</div>
      <SearchInput />
    </div>
    <div class="subheader">
      <ul class="subheader__list">
        <li class="subheader__item subheader__item--active">Inicio</li>
        <li class="subheader__item">Agendados</li>
        <li class="subheader__item">Finalizadas</li>
      </ul>
      <ul class="subheader__social">
        <li>
          <i class="fab fa-instagram"></i>
        </li>
        <li>
          <i class="fab fa-twitter-square"></i>
        </li>
        <li>
          <i class="fab fa-facebook-square"></i>
        </li>
        <li>
          <i class="fab fa-meetup"></i>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
import SearchInput from './SearchInput';

export default {
  name: 'Header',
  components: {
    SearchInput,
  }
}
</script>

<style>
/* header */

.header {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  min-height: 80px;
  padding: 10px 0;
  border-bottom: 1px solid #e5e5e5;
  box-shadow: 0px 1px 1px rgba(0, 0, 0, 0.2);
  margin: 0px;
}

.header__logo {
  font-family: 'Pacifico';
  font-size: 48px;
  color: #00a7e1;
  margin-left: 16px;
  display: inline-block;
}

.icon {
  position: relative;
  top: 50%;
  left: 30px;
  height: 18px;
  color: #00a7e1;
  margin-top: -9px;
  font-size: 20px;
}

/* Subheader */

.subheader {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 38px;
  flex-wrap: wrap;
  border-bottom: 1px solid #e5e5e5;
  margin: 0px;
}

.subheader__list {
  display: flex;
}

.subheader__item {
  padding: 10px 14px 0px 17px;
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

.subheader__social {
  display: flex;
  margin-right: 30px;
}

.subheader__social > li {
  list-style-type: none;
  font-size: 25px;
  color: #00a7e1;
  padding: 5px;
}
</style>
