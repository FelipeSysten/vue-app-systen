<template>
<div>
    <h2>Essaé a descrição da pessoa: {{ nome }} </h2>
    <Info :email="email" />
    <Form />

    </div>
</template>

<script>
import Info from './Info.vue'
import Form from './Form.vue'

export default {
  name: 'Pessoa',
  components: {
      Info,
      Form
  },
  data(){
      return{
        nome : 'Felipe',
        email: 'systen3@gmail.com'
      }
  }
}
</script>