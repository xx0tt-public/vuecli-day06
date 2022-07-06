<template>
  <div class="my-counter">
    <button
      type="button"
      class="btn btn-light"
      @click="sum.goods_count--"
      :disabled="sum.goods_count <= 1"
    >
      -
    </button>
    <input type="number" class="form-control inp" v-model="sum.goods_count" />
    <button type="button" class="btn btn-light" @click="sum.goods_count++">
      +
    </button>
  </div>
</template>

<script>
export default {
  props: ["sum"],
  watch: {
    sum: {
      deep: true,
      handler() {
        this.sum.goods_count = this.sum.goods_count * 1;
        if (this.sum.goods_count < 1) {
          this.sum.goods_count = 1;
        }
      },
    },
  },
};
</script>

<style lang="less" scoped>
.my-counter {
  display: flex;
  .inp {
    width: 45px;
    text-align: center;
    margin: 0 10px;
  }
  .btn,
  .inp {
    transform: scale(0.9);
  }
}
</style>
