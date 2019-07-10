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
      <img :src="speach.imgUrl" width="115" height="115" alt>
    </div>
    <div class="speachMeta">
      <div class="speachMeta__title">{{ speach.titulo }}</div>
      <div class="speachMeta__author">{{ speach.usuario }} - {{ speach.fecha_publicacion}}</div>
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
  padding: 10px;
  box-sizing: border-box;
  border-radius: 10px;
  box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
  width: 100%;
  max-width: 850px;
  height: 140px;
  display: grid;
  grid-template-columns: 120px 1fr 40px;
  grid-column-gap: 5px;
  grid-template-areas: 
    "image meta meta"
    "image meta meta"
    "image votes votes";
  transition: 300ms ease;
}

.speachBox:hover {
  box-shadow: 8px 8px 25px 5px rgba(0,0,0,0.25);
  cursor: pointer;
}

.speachIcon {
  display: flex;
  flex-direction: row-reverse;
  align-items: flex-end;
  justify-content: space-between;
  grid-area: votes;
}

.speachIcon i {
  font-size: 24px;
}

.speachIcon__votes {
  color: #a0bec8;
  font-size: 14px;
}

.speachImg {
  display: flex;
  justify-content: center;
  align-items: center;
  grid-area: image;
}

.speachImg img {
  flex-shrink: 0;
}

.speachMeta {
  grid-area: meta;
}

.speachMeta__title {
  font-size: 18px;
  font-weight: 900;
  color: #00a7e1;
  text-transform: uppercase;
  line-height: 1.2;
}

.speachMeta__author {
  font-size: 14px;
  color: #4d646d;
}

.fa-heart {
  color: #00a7e1;
}

@media screen and (min-width: 900px) {
  .speachMeta__title {
    font-size: 20px;
  }

  .speachMeta__author {
    font-size: 16px;
  }

  .speachIcon i {
    font-size: 28px;
  }

  .speachIcon__votes {
    font-size: 14px;
  }
}
</style>
