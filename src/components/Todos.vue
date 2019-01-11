<template>
    <div>
        <div :key="todo.id" v-for="todo in todos">
            <TodoItem
                :todo="todo"
                @del-todo="$emit('del-todo', todo.id)"
            />
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
        },
        methods: {

        }
    }
</script>

<style scoped>

</style>