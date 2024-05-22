<template>
  <div>
    <button @click="sendData">Home</button>
  </div>
</template>

<script>
export default {
  name: 'GrandChildComponent',
  methods: {
    sendData() {
      this.$emit('data-emitted', 'Hello from My Company!')
    }
  }
}
</script>

<style scoped>
button {
  background-color: palevioletred;
  color: burlywood;
  border: none;
  padding: 10px 20px;
  cursor: pointer;
  margin: 10px;
}
</style>
