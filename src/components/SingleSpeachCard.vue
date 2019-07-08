<template>
  <div class="speachBox">  
    <div class="speachIcon">
      <i
        v-if="speach.upvoted"
        @click="speach.upvoted = !speach.upvoted"
        class="fas fa-heart fa-2x"
      ></i>
      <i v-else @click="speach.upvoted = !speach.upvoted" class="far fa-heart fa-2x"></i>
      <div class="speachIcon__votes">{{ speach.votos }} votos</div>
    </div>
    <div class="speachImg">
      <div class="speachImg__box">
        <img :src="speach.imgUrl" width="115" height="115" alt>
      </div>
    </div>
    <div class="charlaMeta">
      <div class="charlaMeta__title">{{ speach.titulo }}</div>
      <div class="charlaMeta__author">{{ speach.usuario }} - {{ speach.fecha_publicacion}}</div>
    </div>
  </div>
</template>


<script>
export default {
  name: 'SingleSpeachCard',
  props: [
    'speach'
  ]
}
</script>

<style>
.speachBox {
  margin: 5px;
  box-sizing: border-box;
  border-radius: 10px;
  width: 100%;
  max-width: 850px;
  height: 140px;
  display: flex;
}

.charlaBox:hover {
  border: 0.5px solid #00a7e1;
  cursor: pointer;
}

.speachIcon {
  width: 12%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.speachIcon__votes {
  color: #a0bec8;
}

.speachImg {
  width: 14%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.speachImg__box {
  /* border-radius: 10px; */
  /* border: 0.5px solid #00a7e1; */
  height: 100px;
  width: 115px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.charlaMeta {
  margin-top: 34px;
  margin-left: 27px;
}

.charlaMeta__title {
  font-size: 20px;
}

.charlaMeta__author {
  font-size: 14px;
  color: #4d646d;
}

.fa-heart {
  color: #00a7e1;
}
</style>
