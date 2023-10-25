<template lang="">
    <h1 :class="titleClass">Make a red</h1>
</template>
<script>
import { ref } from 'vue';
export default {
    name: "AttributeBinding",
    setup(){
        const titleClass = ref('title')
        return {
            titleClass
        }
    }
}
</script>
<style>
    .title {
        color: red;
    }
</style>


