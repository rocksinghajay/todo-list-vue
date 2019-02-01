<template>
  <div class="todo-container">
    <h1>{{ msg }}</h1>
    <div>
      <input v-model="message" placeholder="Add Todo">
      <p>Message is: {{ message }}</p>
      <button v-on:click="addTodo">Add</button>
    </div>
      <ul>
      <li v-for="(item, index) in todos">
        Messsage {{item}}
      </li>
    </ul>

  </div>
</template>

<script>
export default {
  name: 'Todo',
  props: {
    msg: String
  },
  data () {
    return {
      message: '',
      todos:[]
    }
  },
  methods: {
    addTodo() {
      this.todos.push(this.message)
      console.log(this.todos, 'dkdkk')
    },
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
