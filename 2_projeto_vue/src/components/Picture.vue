<template>
<div >
  <img width="500" :src="avatar" :alt="descricao">
<MudarImagem @mudar-imagem="trocarImagem" />

</div>

  
 </template>

 <script>

import MudarImagem from './MudarImagem.vue'

 export default {
     name: 'Picture',
     components: {
         MudarImagem
     },
     data() {
         return {
             avatar: "/img/avatar.png",
             descricao: "Felipe Systen"
         }
     },

     methods: {
         trocarImagem(){
            this.avatar = "/img/avatar2.png"
         }
     }


 }
 </script>

 <style scoped>

 
 </style>