<template>
  <div class="register">
    <a href="#" :class="{ select: select }" @click="phone">手机注册</a>
    <a href="#" :class="{ select: !select }" @click="email">邮箱注册</a>
  </div>
</template>

<script>
export default {
  data() {
    return {
      select: true,
    };
  },
  methods: {
    phone() {
      this.select = true;
      this.$parent.comName = "Phone";
    },
    email() {
      this.select = false;
      this.$parent.comName = "Email";
    },
  },
};
</script>

<style>
.register {
  display: flex;
  justify-content: space-evenly;
  margin-top: 15px;
  margin-bottom: 10px;
  font-size: 30px;
}
.register a {
  text-decoration: none;
  color: black;
}
.select {
  border-bottom: 3px solid skyblue;
  color: skyblue !important;
}
</style>
