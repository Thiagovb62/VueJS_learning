<template>
  <div>
    <P v-if="esta_trabalhando">Etou trabalhando no momento</P>
    <p v-else>Estou em busca de novas oportunidades</p>
    <p>utilizo essas tecnologias no meu dia dia</p>
    <ul>
      <li>javascript</li>
      <li>Nodejs</li>
      <li>React</li>
    </ul>
    <p v-show="mostra_emails">Mande Uma mensagem para :{{ email }}</p>
    <p>
      Para acessa meu portfolio
      <a v-bind:href="github">Clique aqui</a>
    </p>
    <Picture />
  </div>
</template>
<script lang="ts">
import Picture from "./Picture.vue";
export default {
  name: "Info",
  components: {
    Picture,
  },
  data() {
    return {
      esta_trabalhando: false,
      mostra_emails: true,
      email: "info@gmail.com",
      github: "https://github.com/Thiagovb62",
    };
  },
};
</script>