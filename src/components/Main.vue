<template>
  <div class="container">
      <div class="d-flex flex-wrap mt-3" id="prova">
     <!-- <div v-for="(disco, index) in array_dischi " :key="index"      >  -->
    <Copertina v-for="(disco, index) in array_dischi " :key="index"  :info="disco"/>
    </div>
  </div>
  <!-- </div> -->
           
         
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
            array_dischi:[],
            array_generi_singoli:[],
            prova: ''
        }
    },
    mounted() {
        this.get_disk();
        

    },
    methods:{
        get_vettore_generi(){
            for (let i = 0; i< this.array_dischi.length; i++){
                if (!this.array_generi_singoli.includes(this.array_dischi[i].genre)){
                    this.array_generi_singoli.push(this.array_dischi[i].genre)
                }
            }
        },

        get_disk(){
            axios.get(this.url_dishi).then(res =>{
                this.array_dischi=res.data.response;
                this.get_vettore_generi(); 
            }
            
            );
            

           
            
        }
       
    }

}
</script>

<style  scoped lang="scss">
@import '~bootstrap/scss/bootstrap';
#prova{
    width: 80%;
    margin: 0 auto; 
}

</style>