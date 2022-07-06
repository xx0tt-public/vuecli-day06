<template>
  <div>
    <MyHeader />
    <div style="margin: 45px 0">
      <MyGoods v-for="item in list" :key="item.id" :item="item" />
    </div>
    <MyFooter />
  </div>
</template>

<script>
import MyFooter from "./components/stopCar/MyFooter.vue";
import MyGoods from "./components/stopCar/MyGoods.vue";
import MyHeader from "./components/stopCar/MyHeader.vue";
export default {
  data() {
    return {
      list: [],
    };
  },
  components: {
    MyFooter,
    MyGoods,
    MyHeader,
  },
  created() {
    this.$axios({
      url: "api/cart",
    }).then((res) => {
      this.list = res.data.list;
    });
  },
};
</script>

<style></style>
