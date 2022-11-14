<script setup>
import { RouterLink } from "vue-router";
</script>

<template>
  <div class="container">
    <h2>Bem Vindo(a)</h2>
    <input type="text" placeholder="Usuário" />
    <input type="text" placeholder="Email" />
    <input type="text" placeholder="Senha" />
    <button><RouterLink to="/timeline">Criar</RouterLink></button>
    <a href="https://www.youtube.com/watch?v=roughtzsCDI&ab_channel=SMTOWN">Esqueceu a Senha?</a>
    <RouterLink to="/">Crie Uma Conta</RouterLink>
  </div>
</template>
