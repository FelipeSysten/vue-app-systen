<template>
    <div>
          <p> {{ email }}</p>
          <p v-if="esta_trabalhando">Estou trabalhando no momento</p>
          <p v-else>Estou em busca de novas oportunidades</p>
    <p>Utilizo as seguintes tecnologias para back-end:</p>
    <ul>
        <li v-for="(technology, index) in backend_tecnologies" v-bind:key="index">{{ technology }}</li>
    </ul>
    <p>Utilizo as seguintes tecnologias para o front-end:</p>
    <ul>
      <li v-for="technology in frontend_technologies" :key="technology.id">{{ technology.language }}</li>
    </ul>
    <div>
      <button @click="showEmail">Mostrar e-mail</button>
    </div>
    <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
    <p>Para acessar meu portfolio basta <a v-bind:href="meu_link" target="_blank">clicar aqui</a></p>
    <p v-if="1 > 2">testando</p>
    <Picture />
    </div>
</template>

<script>

import Picture from './Picture.vue'

export default {
  name: 'Info',
  components: {
    Picture
  },
  props: {
    email: String
  },
  data(){
    return {
      esta_trabalhando: false,
      mostrar_email: false,
      meu_link: 'http://google.com',
      backend_tecnologies: ['PHP', 'JavaScript', 'Python'],
      frontend_technologies: [
        {id: 1, language: 'HTML'},
        {id: 2, language: 'CSS'},
        {id: 3, language: 'Vue'}
      ]
    }
  },
  methods: {
    showEmail() {
      this.mostrar_email = !this.mostrar_email
    }
  }

}
</script>