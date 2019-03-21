<template>
  <div>
    <form @submit="addTodo">
     <div class="mb-5 mt-8 pb-3 border-b focus:border-black">
        <input type="text" v-model="title" name="title" id="title" placeholder="Add todo" class="outline-none text-indigo-dark focus:font-bold">
      <input v-model="time" type="text" name="time" id="time" placeholder="Intended time" class="outline-none text-indigo-dark focus:font-bold"/>
     </div>
      <!-- <div class="bg-indigo-dark text-white max-w-sm"> -->
      <input type="submit" value="Add New " class="bg-indigo-dark text-white px-6 py-2 text-center">
      <!-- <i class="far fa-arrow-alt-circle-right"></i> -->
      <!-- </div> -->
    </form>
  </div>
</template>

<script>
import uuid from 'uuid'

export default {
  name: 'AddTodo',
  data() {
    return {
      title: '',
      time: ''
    }
  },
  methods: {
    addTodo (e){
      e.preventDefault()
      const newTodo = {
        id: uuid.v4(),
        title: this.title,
        time: this.time,
        completed: false
      }
      this.$emit('add-todo', newTodo)
    }
  }
}
</script>