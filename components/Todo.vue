<template>
  <div @click="onClick()">
    <span>{{ displayCheckMark }}</span>
    <span>{{ title }}</span>
  </div>
</template>

<script>
export default {
  props: ['title'],
  data () {
    return {
      isChecked: false
    }
  },
  methods: {
    onClick () {
      this.isChecked = !this.isChecked
    }
  },
  computed: {
    displayCheckMark () {
      return this.isChecked ? '✅' : ''
    }
  }
}
</script>

<style>
</style>
