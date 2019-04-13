<template>
  <div class="charlasContainer">
    <div class="charlaBox" v-for="(charla, index) in charlas" :key="index">
      <div class="charlaIcon">
        <i
          v-if="charla.upvoted"
          @click="charla.upvoted = !charla.upvoted"
          class="fas fa-heart fa-2x"
        ></i>
        <i v-else @click="charla.upvoted = !charla.upvoted" class="far fa-heart fa-2x"></i>
        <div class="charlaIcon__votes">{{ charla.votos }} votos</div>
      </div>
      <div class="charlaImg">
        <div class="charlaImg__box">
          <img :src="charla.imgUrl" width="115" height="115" alt>
        </div>
      </div>
      <div class="charlaMeta">
        <div class="charlaMeta__title">{{ charla.titulo }}</div>
        <div class="charlaMeta__author">{{ charla.usuario }} - {{ charla.fecha_publicacion}}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Charlas',
  data() {
    return {
      upvoted: false,
      charlas: [
        {
          titulo: 'Pentesting con Python',
          fecha_publicacion: '27/03/2019',
          usuario: 'Rafael Villareal',
          votos: '20',
          imgUrl: 'https://imgur.com/veyASfn.png',
          upvoted: false
        },
        {
          titulo: 'Big Data y Cloud Computing',
          fecha_publicacion: '27/03/2019',
          usuario: 'Rafael Villareal',
          votos: '20',
          imgUrl: 'https://imgur.com/o96FbDB.png',
          upvoted: false
        },
        {
          titulo: 'Docker-py',
          fecha_publicacion: '27/03/2019',
          usuario: 'Rafael Villareal',
          votos: '20',
          imgUrl: 'https://imgur.com/819GxJm.png',
          upvoted: false
        },
        {
          titulo: 'Pasarela de Pagos',
          fecha_publicacion: '27/03/2019',
          usuario: 'Rafael Villareal',
          votos: '20',
          imgUrl: 'https://imgur.com/u9iSLfM.png',
          upvoted: false
        },
        {
          titulo: 'Como usar GraphQL con Django y Flask',
          fecha_publicacion: '27/03/2019',
          usuario: 'Rafael Villareal',
          votos: '20',
          imgUrl: 'https://imgur.com/40lBxyW.png',
          upvoted: false
        }
      ]
    }
  },
  methods: {
    upvote() {
      this.upvoted = !this.upvoted
    }
  }
}
</script>

<style>
.charlasContainer {
  display: flex;
  flex-direction: column;
}

.charlaBox {
  margin: 5px;
  box-sizing: border-box;
  border-radius: 10px;
  width: 850px;
  height: 140px;
  display: flex;
}

.charlaBox:hover {
  border: 0.5px solid #00a7e1;
  cursor: pointer;
}

.charlaIcon {
  width: 12%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.charlaIcon__votes {
  color: #a0bec8;
}

.charlaImg {
  width: 14%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.charlaImg__box {
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
