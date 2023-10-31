<template>
    <div>
        <div>Todo is: {{ todoId }}</div>
        <button @click="increaseTodo">Fetch next Todo</button>
        <div v-if="!todoData">Loading...</div>
        <div v-else>{{ todoData }}</div>
    </div>
</template>

<script>
import { ref, watch } from 'vue'
export default {
    setup () {
        const todoId = ref(1)
        const todoData = ref(null)
        const increaseTodo = ()=>{
            todoId.value++;
        }

        const fetchData = async ()=>{
            todoData.value = null
            const res = await fetch(`https://jsonplaceholder.typicode.com/todos/${todoId.value}`
            )
            todoData.value = await res.json();
        }   
        watch(todoId, ()=>{
            fetchData()
        },{ immediate: true } )
        return {
            todoId,
            todoData,
            increaseTodo,
            fetchData,
        }
    }
}
</script>

<style lang="scss" scoped>

</style>