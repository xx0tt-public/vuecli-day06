<template>
  <div>
    <MyTable>
      <template v-slot:idcast="scope">
        {{ scope.row.id }}
      </template>
      <template v-slot:title="scope">
        {{ scope.row.name }}
      </template>
      <template v-slot:age="scope">
        {{ scope.row.age }}
      </template>
      <template v-slot:img="scope">
        <img
          v-if="scope.row.type === 1"
          :src="scope.row.headImgUrl"
          alt=""
          width="100px"
        />
        <a v-else-if="scope.row.type === 0" :href="scope.row.headImgUrl">{{
          scope.row.headImgUrl
        }}</a>
        <p v-else>{{ scope.row.headImgUrl }}</p>
      </template>
    </MyTable>
  </div>
</template>

<script>
import MyTable from './components/MyTable.vue';
export default {
  components: {
    MyTable,
  },
};
</script>

<style></style>
