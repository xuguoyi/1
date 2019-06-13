<template>
  <div class="writeBlog">
    <form action="">
      标题：<input type="text" name="" id="" v-model="add.title"><br/>
      内容：<textarea name="" id="" cols="30" rows="10" v-model="add.body"></textarea><br/>
      <button type="button" @click="submit">提交</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      add: {
        title: '',
        body: ''
      }
    }
  },
  methods: {
    submit() {
      this.$axios.post("http://jsonplaceholder.typicode.com/posts/",this.add).then(response => {
        
      })
    }
  }
}
</script>


<style scoped>

</style>

