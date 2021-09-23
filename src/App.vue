<template>
  <div id="app">
    
    <Header @filtro="prova_filtro" />
    <Main :items="filtro_genere"/>
    
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
  data(){
    return{
      filtro_genere:''
    }
  },
  methods:{
    prova_filtro(genere){
      this.filtro_genere=genere
    }
  }
}
</script>

<style lang="scss">

</style>
