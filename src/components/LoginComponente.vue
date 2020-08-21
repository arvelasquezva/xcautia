<template>
  <div class="body">
    <div class="login">
      <b-form @submit.prevent="loginUsuario">
        <b-form-group id="input-group-1" label="User ID:" label-for="input-1">
          <b-form-input
            id="input-1"
            v-model="user"
            required
            placeholder="Ingresa tu User ID"
          ></b-form-input>
        </b-form-group>

        <b-form-group
          id="input-group-2"
          label="Tu contraseña:"
          label-for="input-2"
        >
          <b-form-input
            id="input-2"
            v-model="password"
            required
            placeholder="Ingresa una contraseña"
            type="password"
          ></b-form-input>
        </b-form-group>

        <b-button block pill type="submit" class="button-ingresar"> Ingresa a XCautia</b-button>
        <b-button href="/signUp" block pill class="button-register"> Crea un Usuario </b-button>
      </b-form>
    
    </div>
    <b-modal ok-only v-model="show" size="sm">
      <p class="my-4">El Usuario o Contraseña son incorrectos</p>
    </b-modal>
    
  </div>
</template>

<script>
export default {
  name: "LoginComponente",
  data() {
    return {
      user: "",
      password: "",
      show: false,
    };
  },
};
</script>

<style scoped>
.body {
  margin: 0;
  height: 100vh;
  display: grid;
  place-items: center;
  overflow: hidden;
}
.login {
  display: flex;
  padding: 30px;
  border: 1px solid #eef6e1;
  border-radius: 5px;
  background-color: white;
}
.button-ingresar{
    background: black;
}
.button-register{
    background: black;
}

</style>
