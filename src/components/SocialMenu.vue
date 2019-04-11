<template>
  <ul class="subheader__social">
    <li>
      <a href="https://www.instagram.com/pybaq/" target="_blank">
        <i class="fab fa-instagram"></i>
      </a>
    </li>
    <li>
      <a href="http://twitter.com/pybaq" target="_blank">
        <i class="fab fa-twitter-square"></i>
      </a>
    </li>
    <li>
      <a href="https://www.facebook.com/pybaq/" target="_blank">
        <i class="fab fa-facebook-square"></i>
      </a>
    </li>
    <li>
      <a href="https://www.meetup.com/pythonbaq/" target="_blank">
        <i class="fab fa-meetup"></i>
      </a>
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
  margin-top: 8px;
}

.subheader__social > li {
  list-style-type: none;
  font-size: 32px;
  color: #00a7e1;
  padding: 8px;
}

.subheader__social > li a {
  color: inherit;
  text-decoration: none;
}
</style>
