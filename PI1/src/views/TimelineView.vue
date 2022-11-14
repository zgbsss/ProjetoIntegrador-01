<script>
import { RouterLink } from "vue-router";
export default {
  data() {
    return {
      posts: [
        { arroba: "template 1", coment: "Lorem ipsum dolor sit amet" },
        { arroba: "template 2", coment: "Lorem ipsum dolor sit amet" },
        { arroba: "template 3", coment: "Lorem ipsum dolor sit amet" },
        { arroba: "template 4", coment: "Lorem ipsum dolor sit amet" },
      ],
      novopost: "",
    };
  },
  methods: {
    enviar() {
      if (this.novopost !== ""){
        const novoarroba = "seu arroba";
        this.posts.push({
          arroba: novoarroba,
          coment: this.novopost,
        });
        this.novopost = " ";
      }},
    ocultar(coment) {
      const indice = this.posts.indexOf(coment);
      this.posts.splice(indice, 1);
    },
  },
};
</script>

<template>
  <h1>Seu Nome</h1>
  <h2>Seu arroba</h2>
  <p>Seguidores: 0 Seguindo: 0</p>
  <RouterLink to="/">Logout</RouterLink>
  <br>
  <input type="text" v-model="novopost" placeholder="Como está a sua arte?" />
  <button @click="enviar">Enviar</button>
  <table>
    <tbody>
      <tr v-for="post in posts" :key="post.arroba">
        <td>{{ post.arroba }}</td>
        <td>{{ post.coment }}</td>
        <td><Button @click="ocultar">Ocultar</Button></td>
      </tr>
    </tbody>
  </table>
</template>

<style>
table {
  width: 100%;
  margin: 2% auto;
  border-collapse: collapse;
}

table tr th {
  border: 1px solid;
  padding: 10px;
  font-weight: bold;
}

table tr td {
  border: 1px solid #ccc;
  padding: 10px;
}
</style>
