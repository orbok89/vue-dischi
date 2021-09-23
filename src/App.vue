<template>
  <div id="app">
    
    <Header @filtro="prova_filtro" />
    <Main />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main
  },
  methods:{
    prova_filtro(){
      console.log( 'ciao')
    }
  }
}
</script>

<style lang="scss">

</style>
