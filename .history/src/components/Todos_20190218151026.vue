<template>
  <div>
    <div v-for="todo in todos" :key="todo.id">
      <TodoItem :todo="todo" :del-todo="$emit('del-todo', todo.id)" :update-array="$emit('update-array', todo)"/>
    </div>
  </div>
</template>

<script>
import TodoItem from './TodoItem.vue';

export default {
  components: {
    TodoItem
  },
  name: 'Todos',
  props: ['todos']
}
</script>

<style scoped>

</style>
