<template>
  <h1>Meu nome é: {{ nome }}</h1>
</template>

<script>
  export default ({
    name: 'LifeCycle',
    data() {
      return {
          nome: 'Shirley Alice'
      }
    },
    created() {
      setTimeout(() => {
            this.nome = 'Matheus'
      }, 2000)
    },
    mounted() {
      setTimeout(() => {
            this.nome = 'Pedro'
      }, 1000)
    }    
  })
</script>
