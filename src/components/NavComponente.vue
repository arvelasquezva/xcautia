<template>
  <b-navbar type="dark" class="navbarxcautia">
    <b-navbar-brand class="xcautiabrand" href="/">XCAUTIA</b-navbar-brand>

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto">
        <div v-if="!loggedIn">
          <b-button href="/login" variant="light" class="loginButton ml-3">
            Inicia sesión</b-button
          >
          <b-button href="/signUp" variant="light" class="registerButton ml-3">
            Regístrate</b-button
          >
        </div>
        <div v-else>
          <router-link :to="{name: 'Profile', params:{id: user.role}}">
                <b-button class="perfilButton mr-3" variant="light">Perfil {{user.user}}</b-button>
            </router-link> 
          <b-button class="logoutButton" @click="logout" href="/login" variant="light"> Cierra Sesión</b-button>
        </div>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<script>
export default {
  name: "NavComponente"
};
</script>

<style scoped>
.navbarxcautia { 
  font-family: 'Alata', sans-serif;
  border-style: none;
  background: black;
  position: fixed;
  width: 100%;
  top: 0;
  color: white;
  z-index: 1071;
}
.xcautiabrand {
}
</style>
