<template>
  <div>
    <Header/>
    <div class="container main-home-container">
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
  max-width: 1024px;
  display: grid;
  grid-template-columns: 1fr;
  margin: 0 auto;
}

@media (min-width: 900px) {
  .main-home-container {
    grid-template-columns: 1fr 1fr 300px;
    grid-gap: 16px;
  }
}
</style>
