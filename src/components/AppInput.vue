<script>
import axios from 'axios';
export default {
    props: {
        apiMounted: Object,
    },

    data() {

        return {
            upInput:"",
            downInput:"",
            upSelect:"",
            downSelect:"",

        }

    },
    computed: {
        getValue(from, to, amount,result) {
            axios.get(`https://api.frankfurter.app/latest?base=${from}&symbols=${to}&`)
                .then((response) => {
                    const convertedAmount = (amount * response.data.rates[to]).toFixed(2);
                    result = convertedAmount;
                });
        }

    },

    methods: {

    },

    mounted() {
        console.log("input");
        console.log(this.apiMounted);
    }

}


</script>

<template>
    <div class="appInput">
        <input @keyup="getValue(upSelect,downSelect,upInput,downInput)" type="number" name="" id="">
        <select name="currency" v-model="upSelect" id="upCurrency">
            <option v-for="currency in apiMounted" value="">{{ currency }}</option>
        </select>
    </div>
    <div class="appInput">
        <input type="number" name="" id="">
        <select v-model="downSelect" name="currency" id="downCurrency">
            <option v-for="currency in apiMounted" value="">{{ currency }}</option>
        </select>
    </div>


</template>

<style scoped></style>
