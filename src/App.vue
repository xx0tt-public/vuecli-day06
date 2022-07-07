<template>
  <div>
    <MyHeader title="归属地" background="orange" color="purple" />
    <div class="box">
      <MyGoods v-for="item in list" :key="item.id" :obj="item" />
    </div>
    <MyFooter />
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MyGoods from './components/MyGoods.vue'
import MyFooter from './components/MyFooter.vue'
export default {
  data() {
    return {
      list: [],
    }
  },
  components: {
    MyHeader,
    MyGoods,
    MyFooter,
  },
  created() {
    this.$axios({
      url: '/api/cart',
    }).then((res) => {
      this.list = res.data.list
    })
  },
}
</script>

<style scoped>
.box {
  margin-top: 45px;
  margin-bottom: 45px;
}
</style>
