<template>
  <div id="App">
    <header>
      <h3 :class="{ current: comName == 'NumReg' }" @click="comName = 'NumReg'">
        手机注册
      </h3>
      <h3
        :class="{ current: comName == 'MailReg' }"
        @click="comName = 'MailReg'"
      >
        邮箱注册
      </h3>
    </header>
    <keep-alive>
      <component :is="comName"></component>
    </keep-alive>
  </div>
</template>

<script>
import NumReg from './components/NumReg.vue'
import MailReg from './components/MailReg.vue'
export default {
  data() {
    return {
      comName: 'NumReg',
    }
  },
  components: { NumReg, MailReg },
}
</script>

<style lang="less" scoped>
#App {
  padding: 20px;
}
header {
  text-align: center;
  display: flex;
  justify-content: space-around;
  h3 {
    float: left;
  }
  .current {
    color: #0c58f0;
    border-bottom: 3px solid #0c58f0;
  }
}
</style>
