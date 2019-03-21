<template>
  <div>
        <div class="flex flex-row md:flex-no-wrap justify-between">
          <div class="text-grey-darker text-center px-4 py-2 m-2"  v-bind:class="{'line-through opacity-75 rubberBand':todo.completed}">
            <div class="pretty p-switch p-fill p-icon">
                <input type="checkbox" v-on:change="markAsComplete" v-bind:class="{'line-through opacity-75 rubberBand':todo.completed}" />
                  <div class="state p-danger">
                    <i class="fas fa-close"></i>
                      <label><h3 class="text-indigo-dark text-center justify-start text-center">{{todo.title}} </h3></label>
                  </div>
                </div>
          </div>
          <div class="text-grey-darker text-center px-4 py-2 m-2">
            <p class="ml-10 text-sm text-center justify-end text-indigo-dark text-center" v-bind:class="{'line-through opacity-75 rubberBand':todo.completed}"> {{todo.time}} </p>
          </div>
          <div class="inline-flex text-center px-4 py-2 m-2">
            <button class="ml-6 text-center  px-2 py-2  justify-end text-indifo-darker" @click="$emit('del-todo', todo.id)"><i class="far fa-times-circle text-red text-xl bounce"></i></button>
          </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TodoItem',
  props: ['todo'],
  methods: {
    markAsComplete (){
      this.todo.completed = !this.todo.completed
    }
  }
}
</script>

