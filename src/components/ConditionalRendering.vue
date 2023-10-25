<template>
    <div>
        <button @click="toggle">Toggle</button>
        <div v-if="awesome">Vue is awesome</div>
        <div v-else>Oh No!</div>
    </div>
</template>

<script>
import { ref } from 'vue';
export default {
    
    setup () {
        const awesome = ref(true)

        function toggle(){
            awesome.value = ! awesome.value;
        }

        return {
            awesome,
            toggle
        }
    }
}
</script>

<style lang="scss" scoped>

</style>