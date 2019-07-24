<template>
  <div>
    <div class="charlaDetailBox">
      <div class="charlaDetailImg">
        <div class="charlaDetailImg__box">
          <img :src="testData[$route.params.id].imgUrl" width="115" height="115" alt />
        </div>
      </div>
      <div class="charlaDetailMeta">
        <div class="charlaDetailMeta__title">{{ testData[$route.params.id].titulo }}</div>
        <div
          class="charlaDetailMeta__author"
        >{{ testData[$route.params.id].usuario }} -{{ testData[$route.params.id].fecha_publicacion }}</div>
        <div class="charlaDetailMeta__tags">
          <div class="tag">python</div>
          <div class="tag">linux</div>
        </div>
      </div>
    </div>
    <div
      class="charlaDetailContent"
    >Muchas de las herramientas que se usan para pruebas de penetración en diferentes entornos están hechas con python. La idea es tomar alguna función pequeña de estas herramientas y recrearla con python.</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      testData: [
        {
          titulo: 'Pentesting con Python',
          fecha_publicacion: '27/03/2019',
          usuario: 'Rafael Villareal',
          votos: '20',
          imgUrl: 'https://imgur.com/veyASfn.png',
          upvoted: false,
          tags: ['python', 'linux']
        },
        {
          titulo: 'Big Data y Cloud Computing',
          fecha_publicacion: '27/03/2019',
          usuario: 'Rafael Villareal',
          votos: '20',
          imgUrl: 'https://imgur.com/o96FbDB.png',
          upvoted: false,
          tags: ['python', 'big-data']
        },
        {
          titulo: 'Docker-py',
          fecha_publicacion: '27/03/2019',
          usuario: 'Rafael Villareal',
          votos: '20',
          imgUrl: 'https://imgur.com/819GxJm.png',
          upvoted: false,
          tags: ['python', 'docker']
        },
        {
          titulo: 'Pasarela de Pagos',
          fecha_publicacion: '27/03/2019',
          usuario: 'Rafael Villareal',
          votos: '20',
          imgUrl: 'https://imgur.com/u9iSLfM.png',
          upvoted: false,
          tags: ['python']
        },
        {
          titulo: 'Como usar GraphQL con Django y Flask',
          fecha_publicacion: '27/03/2019',
          usuario: 'Rafael Villareal',
          votos: '20',
          imgUrl: 'https://imgur.com/40lBxyW.png',
          upvoted: false,
          tags: ['python', 'flask', 'django']
        }
      ]
    }
  }
}
</script>

<style>
.charlaDetailBox {
  margin: 5px;
  box-sizing: border-box;
  border-radius: 10px;
  width: 850px;
  height: 140px;
  display: flex;
}

.charlaDetailContent {
  margin: 5px 5px 5px 140px;
  box-sizing: border-box;
  border-radius: 10px;
  width: 595px;
  height: 140px;
  display: flex;
  font-size: 18px;
  letter-spacing: 0.05em;
  line-height: 22px;
}

.charlaDetailImg {
  width: 14%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.charlaDetailImg__box {
  /* border-radius: 10px; */
  /* border: 0.5px solid #00a7e1; */
  height: 100px;
  width: 100px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.charlaDetailMeta {
  margin-top: 5px;
  margin-left: 15px;
}

.charlaDetailMeta__title {
  font-size: 36px;
}

.charlaDetailMeta__author {
  font-size: 18px;
  color: #4d646d;
}

.charlaDetailMeta__tags {
  display: flex;
  flex-direction: row;
}

.charlaDetailMeta__tags > .tag {
  margin-left: 5px;
}

.tag {
  background: #c4c4c4;
  box-sizing: border-box;
  border-radius: 4px;
  width: 70px;
  height: 20px;
  text-align: center;
  font-size: 14px;
}
</style>
