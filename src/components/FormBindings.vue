<template>
    <div>
        <input type="text" v-on:input="onInput">
        <div> {{ text }}</div>
    </div>
</template>

<script>
import { ref } from 'vue';
export default {
    name: "FormBindings",

    setup () {
        const text = ref("");
        function onInput(e){
            this.text = e.target.value;
        }

        return {
            text,
            onInput
        }
    }
}
</script>

<style lang="scss" scoped>

</style>