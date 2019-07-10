<template>
  <div>
    <div class="reactionHeader">
      <ul class="reactionHeader__list">
        <li class="reactionHeader__item"><i class="fa fa-heart fa-2x"></i><span class="reactionHeader__itemText">me gusta</span></li>
        <li class="reactionHeader__item"><i class="far fa-comment-alt fa-2x"></i><span class="reactionHeader__itemText">comentar</span></li>
        <li class="reactionHeader__item"><i class="far fa-share-square fa-2x"></i><span class="reactionHeader__itemText">compartir</span></li>
      </ul>
    </div>
    <div class="userReactions">
      <div>
        <i class="fa fa-heart fa-2x"></i>
        <span class="userReactions__list">Tu, Helena, Tomy y otras 48 personas más</span>
      </div>
    </div>
    <div class="commentFeed">
      <div class="comment" v-for="(user, index) in users" :key="index">
        <div class="comment__img">
          <img :src="user.imgURL" alt="user">
        </div>
        <div class="comment__meta">
          <div class="comment__usr">{{ user.name }}</div>
          <div class="comment__time">{{ user.time }}</div>
          <div class="comment__content">{{ user.content }}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CommentSection',
  data () {
    return {
      users: [
        {
          name: 'Tony Pham',
          time: '3 horas atrás',
          content: 'Es una buena iniciativa, espero escuchar mas de ella.',
          imgURL: 'https://i.imgur.com/M2lnNjI.png'
        },
        {
          name: 'Leah Amber',
          time: '3 horas atrás',
          content: 'Pienso lo mismo, es una buena charla.',
          imgURL: 'https://i.imgur.com/M2lnNjI.png'
        },
        {
          name: 'Helena Hernandez',
          time: '3 horas atrás',
          content: 'No lo se Rick...',
          imgURL: 'https://i.imgur.com/M2lnNjI.png'
        }
      ]
    }
  }
}
</script>


<style>
  .reactionHeader {
    border-top: 1.3px solid #E9E9E9;
    border-bottom: 1.3px solid #E9E9E9;
    width: 755px;
    height: 50px;
  }

  .reactionHeader__list {
    width: 400px;
    height: 50px;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    justify-items: center;
    align-items: center;
  }

  .reactionHeader__item {
    text-align: center;
    box-sizing: border-box;
    list-style-type: none;
    font-size: 12px;
    color: #4d646d;
  }

  .reactionHeader__itemText {
    margin-left: 5px;
    font-size: 14px;
  }

  .userReactions {
    margin: 10px 0px 0px 25px;
    font-size: 10px;
  }

  .userReactions__list {
    font-size: 12px;
    margin-left:5px;
  }

  .commentFeed {
    margin: 30px 0px 0px 20px;
  }

  .comment {
    display: flex;
    flex-direction: row;
    margin-bottom: 20px;
  }

  .comment__meta {
    display: flex;
    flex-direction: column;
    margin-left: 10px;
  }

  .comment__usr {
    font-weight: 500;
    font-size: 18px;
    line-height: 24px;
  }

  .comment__time {
    font-size: 15px;
    line-height: 24px;
    color: rgba(0, 0, 0, 0.38);
  }

  .comment__content {
    font-size: 15px;
    line-height: 24px;
    color: rgba(0, 0, 0, 0.54);
  }

  .comment__img {
    height: 50px;
    width: 50px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

</style>
