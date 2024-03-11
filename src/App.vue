<template>
  <Header />
  <FirstComponent />
  <LifeCycle />
  <Person />
</template>

<script>
  import Header from './components/Header.vue'
  import FirstComponent from "./components/FirstComponent.vue"
  import LifeCycle from "./components/LifeCycle.vue"
  import Person from './components/Person.vue'
  
  export default({
    name: 'App',
    components: {
      FirstComponent,
      LifeCycle,
      Person,
      Header
    }
  })
</script>

<!-- Exemplo de CSS Global -->
<style>
  body {
    background-color: #333;
    color: #FFF;
  }
  a {
    color: #FF0000;
  }
  .teste {
    background-color: #000000;
  }
</style>
