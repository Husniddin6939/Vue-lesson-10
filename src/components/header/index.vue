<template>
    <header class="bg-slate-600">
        <div class="container mx-auto">
      <nav class="flex items-center justify-between p-4">
        <a href="/">Logo.Vue</a>
        <ul class="flex">
            <li class="p-2" v-for="el in navigation">
                <a :href="el.path">{{ el.title }}</a>
            </li>
        </ul>
        <button @click="increment" class="px-3 py-1 bg-green-500 text-white">Increment</button>
      </nav>
        </div>
    </header>
</template>

<script setup lang="ts">
import {navigation} from "@constants";
import { useCounterStore } from "@store";

const {increment}=useCounterStore();
</script>

<style scoped>

</style>