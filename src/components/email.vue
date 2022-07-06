<template>
  <div>
    <p>邮箱地址</p>
    <input type="text" placeholder="请输入邮箱" :value="emailNum" />
    <slot name="emails" :row="emailNum"></slot>
    <br />
    <input type="text" placeholder="验证码" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      emailNum: '112233445566@qq.com',
    };
  },
};
</script>

<style></style>
