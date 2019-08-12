<template>
  <div>
    <el-dialog title="Hold Lot" :visible="value" @update:visible="change">
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
    value: {
      type: Boolean,
      default: false
    }
  },
  data() {
    return {
      
    }
  },
  change(val) {
    this.$emit("input", val)
  }
  
}
</script>

<style>

</style>
