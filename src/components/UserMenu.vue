<template>
  <div class="user-container">
    <BaseButton @click.native="showLogin = true">Iniciar Sesion</BaseButton>
    <BaseButton @click.native="showRegister = true" type="info">Registrate</BaseButton>
    <modal :show="showLogin" @close="showLogin = false">
      <!--
        you can use custom content here to overwrite
        default content
      -->
      <h3 slot="header">INICIAR SESION</h3>
      <div slot="body">
        <form ref="loginForm">
          <div class="form-control">
            <label for="loginEmail">email</label>
            <BaseInput :type="'email'" v-model="userLogin.email" id="loginEmail"/>
          </div>
          <div class="form-control">
            <label for="loginPassword">password</label>
            <BaseInput :type="'password'" v-model="userLogin.password" id="loginPassword"/>
          </div>
        </form>
      </div>
      <div slot="footer">
        <BaseButton @click.native="login()" type="info">Ingresar</BaseButton>
      </div>
    </modal>
    <modal :show="showRegister" @close="showRegister = false">
      <h3 slot="header">REGISTRATE</h3>
      <div slot="body">
        <form ref="registerForm">
          <div class="form-control">
            <label for="registerFirstName">nombre</label>
            <BaseInput v-model="userRegister.firstname" id="registerFirstName"/>
          </div>
          <div class="form-control">
            <label for="registerLastName">apellido</label>
            <BaseInput v-model="userRegister.lastname" id="registerLastName"/>
          </div>
          <div class="form-control">
            <label for="registerEmail">email</label>
            <BaseInput :type="'email'" v-model="userRegister.email" id="registerEmail"/>
          </div>
          <div class="form-control">
            <label for="registerPassword">password</label>
            <BaseInput :type="'password'" v-model="userRegister.password" id="registerPassword"/>
          </div>
        </form>
      </div>
      <div slot="footer">
        <BaseButton @click.native="register()" type="info">Registrar</BaseButton>
      </div>
    </modal>
  </div>
</template>

<script>
import BaseButton from './BaseButton.vue'
import BaseInput from './BaseInput.vue'
import modal from './BaseModal.vue'
export default {
  name: 'UserMenu',
  components: {
    BaseButton,
    BaseInput,
    modal
  },
  data() {
    return {
      showLogin: false,
      showRegister: false,
      userLogin: {
        email: '',
        password: ''
      },
      userRegister: {
        email: '',
        password: '',
        firstname: '',
        lastname: ''
      }
    }
  },
  methods: {
    login() {
      this.showLogin = false
      console.log(this.userLogin)
      this.$refs.loginForm.reset()
    },
    register() {
      this.showRegister = false
      console.log(this.userRegister)
      this.$refs.registerForm.reset()
    }
  }
}
</script>

<style >
.user-container {
  display: flex;
  align-content: space-between;
  justify-content: center;
  margin-top: 24px;
  min-width: 290px;
}

.user-container > button {
  margin: 10px;
}

.form-control {
  margin-bottom: 15px;
}

@media (min-width: 767px) {
  .user-container {
    margin-top: 0;
  }
}
</style>
