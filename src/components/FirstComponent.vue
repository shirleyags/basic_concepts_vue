<template>
  <h1>Olá, Vue!</h1>
  <p>Meu nome é {{ nome }} e trabalho como {{ profissão }}</p>
  <MultipleEvents />
  <Reuse/>
  <br>
  <Reuse/>
</template>

<script>
  import MultipleEvents from './MultipleEvents.vue'
  import Reuse from './Reuse.vue'

  export default {
    name: 'FirstComponent',
    components: {
      MultipleEvents,
      Reuse
    },
    data() {
      return {
        nome: "Shirley Alice",
        profissão: "Deva"
      }
    }
  }
</script>
