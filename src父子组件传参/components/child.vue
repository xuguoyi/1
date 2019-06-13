<template>
  <div>
    <form @submit="formSubmit">
      <input type="text" v-model="age">
      <input type="submit" value="计算" @click="emitAge">
    </form>
  </div>
</template>

<script>
export default {
  name: 'Child',
  data() {
    return {
      age: ''
    }
  },
  methods: {
    formSubmit(e) {
      e.preventDefault();
    },
    emitAge() {
      this.$emit("emitAge",+this.age+20);
    }
  }
}
</script>

<style scoped>
</style>
