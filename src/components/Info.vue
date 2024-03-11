<template>
  <div>

    <!-- <p>{{ compEmail }}</p> -->
    <p v-if="esta_trabalhando">Estou trabalhando no momento</p>
    <p v-else>Estou em busca de novas oportunidades</p>
    <p>Utilizo as seguintes tecnologias backend</p>
    <ul>
      <li v-for="(technologie, index) in backend_technologies" v-bind:key="index"> {{ technologie }}</li>
    </ul>
    <p>Utilizo as seguintes tecnologias front-end</p>
      <ul>
        <li v-for="technologie in frontend_technologies" :key="technologie.id"> {{ technologie.language }}</li>
    </ul>
    <div>
    </div>
      <button @click="showEmail">{{ texto_botao }}</button>
      <p v-show ="mostra_email">Mande uma mensagem para {{ email }}</p>
      <p class="teste">Para meu portifólio<a v-bind:href="meu_link" target="blank">acesse aqui</a></p>
    <Picture />
  </div>
</template>

<script>
  import Picture from './Picture.vue'
  export default {
    name: 'Info',
    components: {
      Picture
    },
    props: {
      //compEmail: String
      email: String
    },
    data() {
      return {
        esta_trabalhando: false,
        mostra_email: false,
        //email: 'shirloka@gmail.com',
        meu_link: 'https://google.com',
        texto_botao: 'Mostrar e-mail',
        backend_technologies: ['Java', 'PHP', 'Python'],
        frontend_technologies:[
          {id: 1, language: 'HTML'},
          {id: 2, language: 'CSS'},
          {id: 3, language: 'Vue'}
        ]
      }
    },
    methods: {
      showEmail() {
        this.mostra_email = !this.mostra_email
        if(!this.mostra_email) {
          this.texto_botao = 'Mostrar e-mail'
        } else {
          this.texto_botao = 'Esconder e-mail'
        }
      }
    }
  }
</script>
