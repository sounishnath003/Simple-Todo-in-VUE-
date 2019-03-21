<template>
  <div class="p-6 border-indigo rounded">
    <h2 class="text-indigo-darker  tracking-loose mb-4 ">Todays</h2>
    <div class="flex flex-col justify-center items-center">
      <div class="div inline-flex flex-wrap" v-bind:key="todo.id" v-for="todo in todos">
        <TodoItem v-bind:todo="todo" />
      </div>
    </div>
  </div>
</template>


<script>
import TodoItem from './Todo_item.vue'

export default {
  name: 'Todos',
  components: {
    TodoItem,
  },
  props: ['todos'],
}
</script>


/*

    <div class="m-3  inline-flex flex-row">
          <h3 class="text-indigo-dark justify-start text-center"> {{todo.title}} </h3>
          <p class="ml-10 text-sm justify-end text-indigo-dark text-center"> {{todo.time}} </p>
        </div>

*/