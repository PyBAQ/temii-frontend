<template>
  <div class="sidebar">
    <div class="sidebar-title">Temii</div>
    <div class="sidebar-content">
      Temii es una aplicación para ayudar a la comunidad de Python Barranquilla a generar temas para su meetup.
      <br>
      <br>Registrate y vota tu tema favorito. O si te gustaria un tema diferente postula tu tema aqui:
    </div>
    <BaseButton type="info" id="show-modal" @click.native="showModal = true">Postular Tema</BaseButton>
    <!-- use the modal component, pass in the prop -->
    <!-- <modal v-if="showModal" @keydown.esc="showModal = false"> -->
    <modal :show="showModal" @close="showModal = false">
      <!--
        you can use custom content here to overwrite
        default content
      -->
      <h3 slot="header">POSTULAR UN TEMA</h3>
      <div slot="body">
        <form @submit.prevent="formSubmit()" ref="myForm">
          <div>
            <label for="titulo">Titulo</label>
            <BaseInput v-model="tema.titulo" id="titulo"/>
          </div>
          <div>
            <label for="descripcion">Descripcion</label>
            <BaseTextarea v-model="tema.descripcion" id="descripcion"/>
          </div>
          <div>
            <label for="requisitos">Requisitos</label>
            <BaseTextarea v-model="tema.requisitos" id="requisitos"/>
          </div>
        </form>
      </div>
      <div slot="footer">
        <!-- <button type="submit">Submit</button> -->
        <BaseButton @click.native="test()" type="info">Postular</BaseButton>
      </div>
    </modal>
  </div>
</template>

<script>
import BaseButton from './BaseButton.vue'
import BaseInput from './BaseInput.vue'
import BaseTextarea from './BaseTextarea.vue'
import modal from './PostularTema.vue'
export default {
  name: 'Sidebar',
  components: {
    BaseButton,
    BaseInput,
    BaseTextarea,
    modal
  },
  data() {
    return {
      showModal: false,
      tema: {
        titulo: '',
        descripcion: '',
        requisitos: ''
      }
    }
  },
  methods: {
    test() {
      this.showModal = false
      console.log(this.tema)
      this.$refs.myForm.reset()
    }
  }
}
</script>

<style>
.sidebar {
  /* display: inline-flex;
  width: calc(100% - 72.75px); */
  display: flex;
  flex-direction: column;
  align-items: center;
  box-sizing: border-box;
  height: 427px;
  width: 271px;
  border: 1px solid #a0bec8;
  border-radius: 10px;
  margin-left: 15px;
}

.sidebar-content {
  margin: 0px 25px 18px 30px;
  font-family: Raleway;
  font-style: normal;
  font-weight: normal;
  font-size: 18px;
  line-height: 22px;
  letter-spacing: 0.05em;
}

.sidebar-title {
  font-family: 'Pacifico';
  font-size: 48px;
  color: #00a7e1;
  display: inline-block;
}

form {
  margin-bottom: 2.5rem;
}
</style>
