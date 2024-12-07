<template>
    <Header/>
    <Main>
    <div>
        <h2>{{ user.name }}</h2>
        <h3>{{ age }}</h3>
        <button @click="inctrementAge">0</button>
    </div>
    </Main>
    <Footer/>
</template>

<script setup lang="ts">
import { reactive, ref, toRefs } from 'vue';
import { Header, Main, Footer } from './components';
import type { Iuser } from './types';

const num=ref<number>(1);
const str=ref<string>("hello");


console.log(num);
console.log(str);

const user= reactive<Iuser>({
    name:"Khusi",
    age:20,
    email:"namesurename@.com",
    address:{
        street:"fdtbdfvd",
        city:"drgdbv",
        state:"grdrvd",
        zip:"dvfvfdvdfv"
    }
});

const {name, age, email, address}=toRefs<Iuser>(user);

const inctrementAge =():void=> {
    age.value=age.value+1
}



</script>

<style scoped>

</style>