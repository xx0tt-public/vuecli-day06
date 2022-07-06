<template>
  <div>
    <table border="1">
      <thead>
        <tr>
          <th>序号</th>
          <th>姓名</th>
          <th>年龄</th>
          <th>头像</th>
        </tr>
      </thead>
      <thead>
        <tr v-for="item in list" :key="item.id">
          <!-- <td>{{ item.id }}</td>
          <td>{{ item.name }}</td>
          <td>{{ item.age }}</td>
          <td>{{ item.headImgUrl }}</td> -->
          <td><slot name="Myid" :row="item"></slot></td>
          <td><slot name="Myname" :row="item">默认名字</slot></td>
          <td><slot name="Myage" :row="item"></slot></td>
          <td><slot name="MyheadImgUrl" :row="item"></slot></td>
        </tr>
      </thead>
    </table>
  </div>
</template>

<script>
export default {
  props: {
    list: {
      type: Array,
      default: [],
    },
  },
}
</script>
