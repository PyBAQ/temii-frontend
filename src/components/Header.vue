<template>
  <nav>
    <div class="header">
      <div class="header__logo">Temii</div>
      <SearchInput />
    </div>
    <div class="subheader">
      <Menu />
      <SocialMenu />
    </div>
  </nav>
</template>

<script>
import SearchInput from './SearchInput';
import Menu from './Menu';
import SocialMenu from './SocialMenu';

export default {
  name: 'Header',
  components: {
    SearchInput,
    Menu,
    SocialMenu,
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
  padding-bottom: 24px;
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
  flex-direction: column;
  margin: 0px;
}

@media (min-width: 767px) {
  .subheader {
    flex-direction: row;
    border-bottom: 1px solid #e5e5e5;
  }
}
</style>
