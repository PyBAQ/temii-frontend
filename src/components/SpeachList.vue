<template>
  <div class="container">
      <SingleSpeachCard v-for="speach in speaches" :key="speach.id" :speach="speach" />
  </div>
</template>

<script>
import SingleSpeachCard from './SingleSpeachCard.vue'

export default {
  name: 'SpeachList',
  components: {
    SingleSpeachCard
  },
  data() {
    return {
      upvoted: false,
      speaches: [
        {
          id: 1,
          titulo: 'Pentesting con Python',
          fecha_publicacion: '27/03/2019',
          usuario: 'Rafael Villareal',
          votos: '20',
          imgUrl: 'https://imgur.com/veyASfn.png',
          upvoted: false
        },
        {
          id: 2,
          titulo: 'Big Data y Cloud Computing',
          fecha_publicacion: '27/03/2019',
          usuario: 'Rafael Villareal',
          votos: '20',
          imgUrl: 'https://imgur.com/o96FbDB.png',
          upvoted: false
        },
        {
          id: 3,
          titulo: 'Docker-py',
          fecha_publicacion: '27/03/2019',
          usuario: 'Rafael Villareal',
          votos: '20',
          imgUrl: 'https://imgur.com/819GxJm.png',
          upvoted: false
        },
        {
          id: 4,
          titulo: 'Pasarela de Pagos',
          fecha_publicacion: '27/03/2019',
          usuario: 'Rafael Villareal',
          votos: '20',
          imgUrl: 'https://imgur.com/u9iSLfM.png',
          upvoted: false
        },
        {
          id: 5,
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

<style scoped>
.container {
  grid-row: 2 / span 1;
  display: flex;
  flex-direction: column;
  width: 100%
}
</style>
