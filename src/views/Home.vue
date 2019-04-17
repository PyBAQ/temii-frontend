<template>
  <div>
    <Header/>
    <div class="container">
      <SpeachList/>
      <Sidebar/>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import SpeachList from '@/components/SpeachList.vue'
import Header from '@/components/Header.vue'
import Sidebar from '@/components/Sidebar.vue'

export default {
  name: 'home',
  components: {
    SpeachList,
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
  width: calc(100% - 32px);
  max-width: 1200px;
  margin: 15px auto;
  display: grid;
  grid-template-columns: 1fr;
}

@media (min-width: 1200px) {
  .container {
    flex-direction: row;
  }
}
</style>
