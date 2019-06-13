<template>
  <div id="app">
    <h3>计算年龄</h3>
    <Child @emitAge="getAge"/>
    <Count :count="reCount"/>
  </div>
</template>

<script>
import Child from './components/child'
import Count from './components/count'

export default {
  name: 'app',
  data() {
    return {
      reCount: ''
    }
  },
  methods: {
    getAge(data) {
      this.reCount = data
    }
  },
  components: {
    Child,
    Count
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
