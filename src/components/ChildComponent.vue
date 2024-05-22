<template>
  <div>
    <p>Welcome!</p>
    <grand-child-component @data-emitted="receiveData"></grand-child-component>
  </div>
</template>

<script>
import GrandChildComponent from './GrandChildComponent.vue'

export default {
  name: 'ChildComponent',
  components: {
    GrandChildComponent
  },
  methods: {
    receiveData(data) {
      this.$emit('data-emitted', data)
    }
  }
}
</script>

<style scoped>
p {
  color: #2c3e50;
  font-weight: bold;
}
</style>
