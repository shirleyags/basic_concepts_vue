<template>
  <div>
    <button @click="$emit('changeImage')">Trocar imagem do perfil</button>
  </div>
</template>

<script>
  export default {
    name: 'ChangeImage',
    emits: ['changeImage']
  }
</script>
