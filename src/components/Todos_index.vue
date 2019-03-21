<template>
  <div>
    <h2 class="text-indigo-dark tracking-loose">Todays</h2>
    <div class="flex flex-col">
      <div class="div inline-flex flex-wrap" v-bind:key="todo.id" v-for="todo in todos">
        <h3> {{todo.title}} </h3>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  name: 'Todos',
  props: ['todos'],
}
</script>