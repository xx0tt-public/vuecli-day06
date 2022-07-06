<template>
  <div>
    <p>选择所在地区(实名认证主体所在地)</p>
    <input type="radio" />中国大陆 <input type="radio" />中国香港
    <p>手机号码</p>
    <div>
      <input type="text" placeholder="输入手机号码" :value="num" />
      <slot name="mobiles" :row="num"></slot>
    </div>
    <br />
    <input type="text" placeholder="验证码" />
    <p>登录密码</p>
    <input type="password" placeholder="请输入密码" /><br />
    <input type="password" placeholder="再次输入密码" />
    <p>邀请码(选填)</p>
    <input type="text" placeholder="输入客户经理邀请码" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      num: 123456,
    };
  },
};
</script>

<style>
.mobile {
  font-size: 30px;
  margin-right: 30px;
}
.email {
  font-size: 30px;
}
</style>
