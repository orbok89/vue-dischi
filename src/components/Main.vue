<template>
  <div>
     <div class="container">
         <div class="row text-center  p-3 m-5 ">
             <Copertina v-for="(disco, index) in array_dischi " :key="index" :info="disco"/>
         </div>
     </div>
  </div>
</template>

<script>
import axios from 'axios';
import Copertina from './Copertina.vue';


export default {
    name:'Main',
    components:{
        Copertina
    },
    data(){
        return{
            url_dishi:'https://flynn.boolean.careers/exercises/api/array/music',
            array_dischi:[]
        }
    },
    created() {
        this.get_disk();

    },
    methods:{
        get_disk(){
            axios.get(this.url_dishi).then(res =>
            this.array_dischi=res.data.response
            )
        }
    }

}
</script>

<style  scoped lang="scss">
@import '~bootstrap/scss/bootstrap';

</style>