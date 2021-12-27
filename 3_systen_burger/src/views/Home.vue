<template>
<Banner />
  <div class="main-container">
    <h1>Escolha sua camisa:</h1>
    <Camisaform />
  </div>
</template>

<script>
import Banner from '../components/Banner.vue'
import Camisaform from '../components/Camisaform.vue'
export default {
  name:"Home",
  components: {
  Banner,
  Camisaform
}
}



</script>
