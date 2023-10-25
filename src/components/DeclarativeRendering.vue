


<script setup>
import { reactive, ref } from 'vue'

const counter = reactive({
    count:0
})
const message = ref('hello World!');
// component logic
// declare some reactive state here.
</script>

<template>
    <h1>{{ message }}</h1>
    <p>Count is: {{ counter.count }}</p>
</template>