<template>
    <div>
        Child Emit Component
    </div>
</template>

<script>
import { onMounted } from 'vue';
export default {
    emits:["responseEmit"],
    setup (props, { emit }) {
        // created(()=>{
        //     emit("responseEmit", "Get message from emit child component successfully...!")
        //     emit('response', 'hello from child')
        // }) 
      
        onMounted(()=>{
            emit("responseEmit", "Get message from emit child component successfully...!")
        })
        return {}
    }
}
</script>

<style lang="scss" scoped>

</style>