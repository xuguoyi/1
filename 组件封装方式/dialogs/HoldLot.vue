<template>
  <div class="HoldLot">
    <el-dialog title="Hold Lot" :visible="visible" @update:visible="change">
      <div slot="footer" class="dialog-footer">
        <el-button @click="change(false)">取 消</el-button>
        <el-button type="primary" @click="change(false)">确 定</el-button>
      </div> 
    </el-dialog>
  </div>
</template>

<script>
export default {
  props: {
    visible: {
      type: Boolean,
      default: false
    }
  },
  data() {
    return {
      
    }
  },
  methods: {
    change(val) {
      this.$emit("update:visible", val)
    }
  }
}
</script>

<style lang="less" scoped>
  .HoldLot {
    
    .el-select {
      width: 100%;
    }
  }
  
</style>
