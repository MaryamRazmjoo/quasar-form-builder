<template>
  <div>
    hi {{ name }} from CustomComponent with value: {{ value }}
    <button @click="addValue">+</button>
  </div>
</template>

<script>
import { inputMixin } from '../index'
export default {
  name: 'CustomComponent',
  mixins: [inputMixin],
  props: {
    value: {
      default: null
    },
    name: {
      type: String,
      default: 'ali'
    }
  },
  methods: {
    addValue () {
      this.inputData++
      this.change(this.inputData)
    }
  }
}
</script>

<style scoped>

</style>
