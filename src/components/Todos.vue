<template>
    <div>
        <div :key="todo.id" v-for="todo in todos">
            <TodoItem :todo="todo" />
        </div>
    </div>
</template>

<script>
    import TodoItem from './TodoItem';

    export default {
        props: [
            'todos'
        ],
        name: "Todos",
        components: {
            TodoItem
        }
    }
</script>

<style scoped>

</style>