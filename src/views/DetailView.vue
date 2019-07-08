<template>
  <div>
    <Header/>
    <div class="container">
      <div class="detail-container">
        <CharlasDetail />
        <CommentSection />
      </div>
      <Sidebar/>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Header from '@/components/Header.vue'
import CommentSection from '@/components/CommentSection.vue'
import CharlasDetail from '@/components/CharlasDetail.vue'
import Sidebar from '@/components/Sidebar.vue'

export default {
  name: 'home',
  components: {
    CommentSection,
    CharlasDetail,
    Sidebar,
    Header
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
