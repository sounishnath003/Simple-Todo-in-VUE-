<template>
  <div>
    <div class="m-3  inline-flex flex-row" v-bind:class="{'line-through opacity-75 rubberBand':todo.completed}">
        <h3 class="text-indigo-dark justify-start text-center"> {{todo.title}} </h3>
        <p class="ml-10 text-sm justify-end text-indigo-dark text-center"> {{todo.time}} </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TodoItem',
  props: ['todo'],
}
</script>

<style>
  @import url('https://cdnjs.cloudflare.com/ajax/libs/animate.css/3.7.0/animate.css');
</style>
