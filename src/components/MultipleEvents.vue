<template>
<div>
    <button @click="primeiro($event), segundo($event), terceiro($event)">Ativar múltiplos eventos</button>
    <p>{{ multiplos_eventos }}</p>
</div>
</template>

<script>
  export default {
    name: 'MultipleEvents',
    data() {
      return {
        multiplos_eventos: ""
      }
    },
    methods: {
      primeiro(e) {
        this.multiplos_eventos = "Primeiro evento!"
      },
      segundo(e) {
        setTimeout(() => this.multiplos_eventos = "Segundo evento!", 500)
      },
      terceiro(e) {
        setTimeout(() => this.multiplos_eventos = "", 1500)
      }
    }
  }
</script>