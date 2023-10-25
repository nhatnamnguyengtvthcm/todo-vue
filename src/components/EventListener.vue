<template lang="">
    <div>
        <button @click="increment">Increase</button>
        <div>Count is: {{count}}</div>
    </div>
</template>
<script>
import { ref } from 'vue';
export default {
    name: "EventListener",
    setup() {
        const count = ref(0);
        function increment() {
            this.count++;
        
        }
        return {
            count,
            increment
        };
    },
}
</script>
<style></style>