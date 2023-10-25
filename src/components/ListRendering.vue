<template>
    <div>
        <div class="add-todo flex">
            <input type="text" class="add-todo-input" v-model="newTodo">
            <button class="add-todo-btn" @click="addTodo">Add Button</button>
        </div>
        <ul>
            <li v-for="(item, index) in todoList" :key="index">{{ item }}<button class="border close-btn" @click="removeTodo(index)">X</button></li> 
        </ul>
    </div>
       
</template>

<script>
import { ref } from 'vue'
export default {
    setup () {
        const newTodo = ref(null);
        const todoList = ref([
            'Learn JavaScript', 'Learn VueJS'
        ]);

        function addTodo(){

            todoList.value.push(newTodo.value);
        }
        function removeTodo(idx){
            todoList.value = todoList.value.filter((item, index)=>{
                return index !== idx;
            })
        }
        return {
            todoList,
            addTodo,
            removeTodo,
            newTodo
        }
    }
}
</script>

<style lang="scss" scoped>

</style>