<template>
  <div>
    <div v-for="title in todoTitles" :key="title">
      <todo :title="title" />
    </div>
    <button @click="addTodo(inputTitle)">ぼたんです</button>
    <input v-model="inputTitle" placeholder="edit me">
  </div>
</template>

<script>
import Todo from '~/components/Todo.vue'

export default {
  data () {
    return {
      todoTitles: [],
      inputTitle: ''
    }
  },
  components: {
    Todo
  },
  methods: {
    addTodo (title) {
      this.todoTitles = this.todoTitles.concat([title])
    }
  }
}
</script>

<style>
</style>
