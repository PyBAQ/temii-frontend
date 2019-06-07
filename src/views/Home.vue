<template>
  <div>
    <Header/>
    <div class="container">
      <Charlas/>
      <Sidebar/>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Charlas from '@/components/Charlas.vue'
import Header from '@/components/Header.vue'
import Sidebar from '@/components/Sidebar.vue'

export default {
  name: 'home',
  components: {
    Charlas,
    Header,
    Sidebar
  }
}
</script>

<style>
/* remove default margin */
body {
  margin: 0px;
  line-height: 1.6;
  font-weight: 400;
  font-family: 'Raleway';
}

ul {
  margin: 0;
  padding: 0;
}

.container {
  margin: 15px 150px 15px 150px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
</style>
