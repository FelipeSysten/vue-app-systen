<template>
    <div>
          <p v-if="esta_trabalhando">Estou trabalhando no momento</p>
          <p v-else>Estou em busca de novas oportunidades</p>
    <p>Utilizo as seguintes tecnologias</p>
    <ul>
        <li>JavaScript</li>
        <li>PHP</li>
        <li>Python</li>
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
  data(){
    return {
      esta_trabalhando: false,
      mostrar_email: false,
      email: 'systen3@gmail.com',
      meu_link: 'http://google.com'
    }
  },
  methods: {
    showEmail() {
      this.mostrar_email = !this.mostrar_email
    }
  }

}
</script>