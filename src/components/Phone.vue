<template>
  <div>
    <p>选择所在地区(实名认证主体所在地)</p>
    <input type="radio" name="china" id="china" checked />
    <label for="china">中国大陆</label>
    <input type="radio" name="china" id="taiwan" />
    <label for="taiwan">中国台湾</label>
    <p>手机号码</p>

    <slot>
      <input type="text" class="text" placeholder="请输入手机号码" />
    </slot>
    <br />
    <input type="text" class="text" placeholder="请输入验证码" />
    <br />
    <input type="text" class="text" placeholder="登录密码" />
    <br />
    <input type="text" class="text" placeholder="再次确认密码" />
    <br />
    <input type="text" class="text" placeholder="邀请码" />
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.text {
  width: 250px;
  height: 40px;
  margin: 20px 0 0 20px;
}
</style>
