<template>
<div>
  <h2>Essa é a descrição do: {{ nome }}</h2>
  <Info  :email="email" />
  <Form />
</div>
</template>

<script>
  import Info from './Info.vue'
  import Form from './Form.vue'

  export default {
    name: 'Person',
    components: {
      Info,
      Form
    },
    data() {
      return {
        nome: 'Alice',
        email: "shirley@gmail.com"
      }
    }
  }
</script>
