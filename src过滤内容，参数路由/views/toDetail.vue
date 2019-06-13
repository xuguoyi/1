<template>
  <div>
    <h3>{{blog.title}}</h3>
    <p>{{blog.body}}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      id: this.$route.params.id,
      blog: {}
    }
  },
  created() {
    this.$axios.get("/posts/"+ this.id).then(response => {
      this.blog = response.data
    })
  }
}
</script>

<style>

</style>
