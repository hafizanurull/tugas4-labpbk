<template>
  <div>
    <p>Hello</p>
    <child-component @data-emitted="displayData"></child-component>
    <p>{{ receivedData }}</p>
    <slot></slot>
  </div>
</template>

<script>
import ChildComponent from './ChildComponent.vue'

export default {
  name: 'ParentComponent',
  components: {
    ChildComponent
  },
  data() {
    return {
      receivedData: ''
    }
  },
  methods: {
    displayData(data) {
      this.receivedData = data
    }
  }
}
</script>

<style scoped>
p {
  color: #34495e;
  font-size: 18px;
}
</style>
