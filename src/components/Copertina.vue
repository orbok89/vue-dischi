<template>
  <div class="col-6 col-md-3 col-lg-1 m-5 p-2 prova">
      <img :src="info.poster" alt="">
      <div>{{info.title}}</div>
      <div>{{info.author}}</div>
      <div>{{info.year}}</div>
  </div>
</template>

<script>
export default {
    name:'Copertina',
    props: ['info']
}
</script>

<style  scoped lang="scss">
@import '~bootstrap/scss/bootstrap';
    img{
        width: 100px;
    }
    .prova{
    background-color: darkolivegreen;
}
</style>