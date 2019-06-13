<template>
  <div class="blog">
    <input type="text" v-model="newItem"/>
    <div class="singleBlog" v-for="item in newItems" :key="item.id">
      <router-link :to="'/todetail/'+item.id"><h1>{{item.title}}</h1></router-link>
      <p>{{item.body}}</p>
    </div>
  </div>
</template>

<script>

export default {
  name: 'blog',
  data() {
    return {
      items: [],
      newItem: ''
    }
  },
  created() {
    this.getData()
  },
  methods: {
    getData() {
      this.$axios.get("/posts").then(response => {
        this.items = response.data.splice(0,5)
      })
    }
  },
  computed: {
    newItems() {
      return this.items.filter((item)=> {
        return item.title.match(this.newItem)
      })
    }
  },
  components: {
    
  }
}
</script>

<style lang="less" scope>
  .singleBlog {
    border: 1px solid #333;
    margin: 20px;
    p {
      text-align: left;
      padding: 10px 20px;
    }
  }
</style>

