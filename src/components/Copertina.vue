<template>
  <div id="cop" class="d-flex flex-column   align-items-center mb-2  p-1 m-1 prov1a">
      <img :src="info.poster" alt="">
      <div  >{{info.title}}</div>
      <div class="mb-3">{{info.author}}</div>
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
    .prov1a{
    background-color: darkolivegreen;
}
#cop{
    width: calc(20% - 15px);
    height: 250px;
}
</style>