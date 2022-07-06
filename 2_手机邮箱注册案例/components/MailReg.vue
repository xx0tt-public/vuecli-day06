<template>
  <main>
    <p>选择所在地区(实名认证主体所在地)</p>
    <input type="radio" name="area" value="1" id="DL" />
    <label for="DL">中国大陆</label>
    <input type="radio" name="area" value="0" id="HK" />
    <label for="HK">中国香港</label>
    <MailRegIpt>
      <template>
        <p>邮箱号码</p>
        <span>@qq.com</span>
        <input type="text" placeholder="输入邮箱号" /><br />
        <input type="text" placeholder="输入验证码" />
      </template>
    </MailRegIpt>
    <p>登陆密码</p>
    <input type="password" placeholder="输入登陆密码" /><br />
    <input type="password" placeholder="再次输入登陆密码" />
    <p>邀请码（选填）</p>
    <input type="text" placeholder="输入客户经理邀请码" />
  </main>
</template>

<script>
import MailRegIpt from './MailRegIpt.vue'
export default {
  components: { MailRegIpt },
}
</script>

<style lang="less">
main {
  padding: 10px;
  input[type='radio'] {
    margin-left: 10px;
  }
  input {
    margin: 10px 0;
  }
  button {
    margin-left: 10px;
  }
  p {
    transform: translateY(20px);
  }
}
</style>
