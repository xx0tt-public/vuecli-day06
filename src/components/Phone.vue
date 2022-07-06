<template>
  <div class="main">
    <p>选择所在地区(实名认证主体所在地)</p>
    <input type="radio" name="area" value="1" id="DL" />
    <label for="DL">中国大陆</label>
    <input type="radio" name="area" value="0" id="HK" />
    <label for="HK">中国香港</label>

    <p>手机号码</p>
    <span>+86 </span>
    <input type="text" placeholder="输入手机号" /><br />
    <input type="text" placeholder="输入验证码" />
    <button class="btn">发送验证码</button>
    <p>登陆密码</p>
    <input type="password" placeholder="输入登陆密码" /><br />
    <input type="password" placeholder="再次输入登陆密码" />
    <p>邀请码（选填）</p>
    <input type="text" placeholder="输入客户经理邀请码" />
  </div>
</template>

<script>
export default {}
</script>

<style lang="less" scoped>
main {
  padding: 10px;
  input[type='radio'] {
    margin-left: 10px;
  }
  input {
    margin: 10px 0;
    vertical-align: middle;
  }
  button {
    margin-left: 10px;
  }
  p {
    transform: translateY(20px);
  }
}
.btn {
  margin-left: 10px;
  margin-top: 10px;
  widows: 100px;
  height: 25px;
  background-color: rgb(51, 51, 240);
  line-height: 25px;
  color: aliceblue;
}
</style>
