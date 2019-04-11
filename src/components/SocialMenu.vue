<template>
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
</template>

<script>
export default {
  name: 'SocialMenu',
}
</script>

<style>
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
