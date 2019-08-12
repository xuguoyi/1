<template>
  <div class="Down">
    <el-dialog title="Hold Lot" :visible.sync="visible">
      <div slot="footer" class="dialog-footer">
        <el-button @click="visible = false">取 消</el-button>
        <el-button type="primary" @click="visible = false">确 定</el-button>
      </div> 
    </el-dialog>
  </div>
</template>

<script>
export default {
  data() {
    return {
      visible: false
    }
  },
  methods: {
    open() {
      this.visible = true;
    }
  }
}
</script>

<style lang="less" scoped>
  .Down {
    .el-select {
      width: 100%;
    }
  }
  
</style>
