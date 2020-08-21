<template>
  <div class="login">
    <div class="row">
      <div class="col-md-8">
        
      </div>
      <div class="col-md-4">
        <LoginComponente></LoginComponente>
      </div>
    </div>
  </div>
</template>

<script>
import LoginComponente from "@/components/LoginComponente.vue";
export default {
  name: "Home",
  components: {
    LoginComponente,
  },
};
</script>

<style scoped>
.login {
  background: linear-gradient(to bottom, #090909, #2d2d2d);
}
</style>
