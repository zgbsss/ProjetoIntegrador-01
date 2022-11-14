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
      <RouterLink to="/cadastro">Já tem uma conta?</RouterLink>
    </div>
  </main>
</template>
