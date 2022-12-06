<script setup>
import { RouterLink } from "vue-router";
</script>

<template>
  <main>
    <h1>Inscreva-se para ver desenhos!</h1>
    <div class="container">
      <h2>Bem Vindo(a)</h2>
      <input type="text" placeholder="Usuário" />
      <input type="text" placeholder="Email" />
      <input type="text" placeholder="Senha" />
      <button><RouterLink to="/timeline">Criar</RouterLink></button>
      <RouterLink to="/login">Já tem uma conta?</RouterLink>
    </div>
  </main>
</template>
<style scoped>
body {
  background-color: aquamarine;
}
.container {
  background-color: antiquewhite;
  border-radius: 10px;
  padding: 60px 10px;
  margin-left: 700px;
}
.container input {
  display: flex;
  height: 60px;
  width: 400px;
  border-radius: 10px;
  border-width: 0px;
  box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 12px;  margin: 10px;
}
</style>
