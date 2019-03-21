<template>
  <div id="app" class="bg-indigo-dark p-6">
    <div id="appe" class="max-w-md shadow-lg p-6 rounded-lg m-auto bg-white justify-center items-center">
    <div class="flex flex-row flex-wrap p-4 bg-white mb-6 border-b justify-between items-center">
      <div class="icon">
        <i class="fas text-indigo fa-angle-left"></i>
      </div>
      <h2 class="text-lg inline-flex tracking-loose text-indigo-dark"><Fieldset>FRIDAY</Fieldset>, <p class="text-indigo opacity-75 ml-3">22th march</p></h2>
      <div class="icon">
        <i class="fas text-indigo fa-angle-right"></i>
      </div>
    </div>
    <Todos v-bind:todos="todos" v-on:del-todo="deleteTodo" />
    <AddTodo v-on:add-todo="addTodo"/>
  </div>
  </div>
</template>

<script>
import Todos from './components/Todos_index.vue'
import AddTodo from './components/AddTodo.vue'

export default {
  name: 'app',
  components: {
    Todos,
    AddTodo
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
  methods: {
    deleteTodo (id){
      this.todos = this.todos.filter(todo => todo.id != id)
    },
    addTodo (newTodo) {
      this.todos = [...this.todos, newTodo]
    }
  }
}
</script>

<style>
@import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.8.0/css/all.css');
@import url('https://cdn.jsdelivr.net/npm/pretty-checkbox@3.0/dist/pretty-checkbox.min.css');
  @import url('https://cdnjs.cloudflare.com/ajax/libs/animate.css/3.7.0/animate.css');
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
