<template>
  <div class="OperBtn">
    <el-button 
      type="primary" 
      size="small" 
      @click="openHoldLot()">
      Hold Lot
    </el-button>
    <el-button 
      type="primary" 
      size="small" 
      @click="openSweepingAddition()">
      Sweeping Addition
    </el-button>
    <el-button 
      type="primary" 
      size="small" 
      @click="openDown()">
      Down
    </el-button>
    <HoldLot :visible.sync="holdLot"/>
    <SweepingAddition v-model="sweepingAddition"/>
    <Down :ref="down"/>
  </div>
</template>

<script>
import HoldLot from './dialogs/HoldLot.vue';
import SweepingAddition from './dialogs/SweepingAddition.vue';
import Down from './dialogs/Down.vue';

export default {
  data() {
    return {
      holdLot: false,
      sweepingAddition: false
    }
  },
  methods: {
    openHoldLot() {
      this.holdLot = true;
    },
    openSweepingAddition() {
      this.sweepingAddition = true;
    },
    openHoldLot() {
      this.$refs.down.open();
    }
  },
  components: {
    HoldLot,
    SweepingAddition,
    Down
  }
}
</script>

<style lang="less" scoped>
  
</style>
