<template>
<div >
  <img width="500" :src="avatar" :alt="descricao">


</div>

  
 </template>

 <script>
 export default {
     name: 'Picture',
     data() {
         return {
             avatar: "/img/avatar.png",
             descricao: "Felipe Systen"
         }
     }


 }
 </script>

 <style scoped>

 
 </style>