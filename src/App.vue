<template>
  <div id="app" class="max-w-sm shadow-lg p-6 m-auto justify-center items-center">
    <div class="flex flex-row flex-wrap p-4 bg-white mb-6 border-b justify-between items-center">
      <div class="icon">
        <i class="fas text-indigo fa-angle-left"></i>
      </div>
      <h2 class="text-lg inline-flex tracking-loose text-indigo-dark">THRUSDAY, <p class="text-indigo opacity-75 ml-3">21th march</p></h2>
      <div class="icon">
        <i class="fas text-indigo fa-angle-right"></i>
      </div>
    </div>

    <Todos v-bind:todos="todos"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Todos from './components/Todos_index.vue'
import TodoItem from './components/Todo_item.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    Todos,
    TodoItem
  },
  data() {
    return {
      todos: [
        {
          id: 1,
          title: 'Morning Run',
          time: '7:30 am',
          completed: false
        },
        {
          id: 2,
          title: 'Meeting',
          time: '12:30 pm',
          completed: true
        },
        {
          id: 3,
          title: 'Launch with Mike',
          time: '02:30 pm',
          completed: false
        }
      ],
    }
  },
}
</script>

<style>
@import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.8.0/css/all.css');
@import './mainly.css';

*{
  font-family: product sans;
}

#app {
  /*font-family: 'Avenir', Helvetica, Arial, sans-serif;*/
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
