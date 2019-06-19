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
    <modal :show="showModal" @close="showModal = false">
      <!--
        you can use custom content here to overwrite
        default content
      -->
      <h3 slot="header">POSTULAR UN TEMA</h3>
      <div slot="body">
        <form ref="myForm">
          <div class="form-control">
            <label for="titulo">Titulo</label>
            <BaseInput v-model="tema.titulo" id="titulo"/>
          </div>
          <div class="form-control">
            <label for="descripcion">Descripcion</label>
            <BaseTextarea v-model="tema.descripcion" id="descripcion"/>
          </div>
          <div class="form-control">
            <label for="requisitos">Requisitos</label>
            <BaseTextarea v-model="tema.requisitos" id="requisitos"/>
          </div>
        </form>
      </div>
      <div slot="footer">
        <!-- <button type="submit">Submit</button> -->
        <BaseButton @click.native="postular()" type="info">Postular</BaseButton>
      </div>
    </modal>
  </div>
</template>

<script>
import BaseButton from './BaseButton.vue'
import BaseInput from './BaseInput.vue'
import BaseTextarea from './BaseTextarea.vue'
import modal from './BaseModal.vue'
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
    postular() {
      this.showModal = false
      console.log(this.tema)
      this.$refs.myForm.reset()
    }
  }
}
</script>

<style>
.sidebar {
  display: flex;
  flex-direction: column;
  align-items: center;
  box-sizing: border-box;
  width: 100%;
  margin: 0 auto;
  padding: 15px;
  border: 1px solid #a0bec8;
  border-radius: 10px;
}

.sidebar-content {
  font-family: Raleway;
  font-style: normal;
  font-weight: normal;
  font-size: 18px;
  line-height: 22px;
  letter-spacing: 0.05em;
  margin-bottom: 15px;
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
