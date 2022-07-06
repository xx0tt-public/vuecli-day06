<template>
  <div>
    <MyHeader title="我的购物车"></MyHeader>
    <div class="main">
      <MyGoods v-for="item in list" :key="item.id" :item="item"></MyGoods>
    </div>
    <MyFooter :list="list"></MyFooter>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader'
import MyGoods from './components/MyGoods'
import MyFooter from './components/MyFooter'
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
    }).then((res) => (this.list = res.data.list))
  },
}
</script>

<style scoped>
.main {
  margin: 45px 0;
}
</style>
