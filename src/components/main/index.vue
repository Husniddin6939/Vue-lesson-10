<template>
    <div>
        <slot/> 
        <h1>{{ count }}</h1>
    </div>
</template>

<script setup lang="ts">
import { storeToRefs } from 'pinia';
import { useCounterStore } from '@store';

const counterStore=useCounterStore();
const {count}=storeToRefs(counterStore)
</script>

<style scoped>

</style>