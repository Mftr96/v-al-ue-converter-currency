<script>
import axios from 'axios';
import AppInput from './components/AppInput.vue';
export default {
    components:{
        AppInput,
    },

data() {

    return {
        apiMounted:{},
        

    }

},

methods: {
 ciao(){
    console.log("ciao");
 },
 
},

created() {
    axios.get("https://api.frankfurter.app/currencies")
    .then((response) =>{
        //Stampo in console  i risultati
        console.log(response.data);
        //salvo la ricerca in una variabile 
        this.apiMounted=response.data;
    });

}

}



</script>

<template>
    <AppInput :apiMounted="apiMounted"/>
</template>

<style scoped>

</style>
