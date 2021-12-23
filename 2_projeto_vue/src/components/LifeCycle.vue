<template>
    <h1>Meu nome é: {{ nome }}</h1>
</template>

<script>

export default {
  name: 'LifeCycle',
  data() {
      return {
          nome: 'Ainda nao sei'
      }
  },
   created() {
       setTimeout(() =>{
    this.nome = 'Felipe'
       }, 1000);
     
    },

    mounted() {
            setTimeout(() =>{
    this.nome = 'Phelipe'
       }, 2000);
       
    }
}
</script>
