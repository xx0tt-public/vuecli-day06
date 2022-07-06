<template>
  <div>
    <Row>
      <template v-slot:name="scope">
        {{ scope.row.name }}
      </template>
      <template v-slot:age="scope">
        {{ scope.row.age }}
      </template>
      <template v-slot:headImgUrl="scope">
        <a v-if="scope.row.type == 0" :href="scope.row.headImgUrl">跳转</a>
        <img v-if="scope.row.type == 1" :src="scope.row.headImgUrl" alt="" />
        <span v-if="scope.row.type == 2">{{ scope.row.headImgUrl }}</span>
      </template>
    </Row>
  </div>
</template>

<script>
import Row from "./components/Row.vue";
export default {
  components: {
    Row,
  },
};
</script>

<style></style>
