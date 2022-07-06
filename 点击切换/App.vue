<template>
  <div>
    <span class="mobile" @click="comName = 'mobile'">手机注册</span>
    <span class="email" @click="comName = 'email'">邮箱注册</span>
    <div>
      <!-- 点击切换，数据还保存 -->
      <keep-alive>
        <component :is="comName"></component>
        <mobile>
          <template v-slot:mobiles="scope">
            <input type="text" placeholder="输入手机号码" :value="scope.row" />
            <!-- {{ scope.row }} -->
          </template>
        </mobile>
        <email>
          <template v-slot:emails="scope">
            {{ scope.row }}
          </template>
        </email>
      </keep-alive>
    </div>
  </div>
</template>

<script>
import mobile from './components/mobile.vue';
import email from './components/email.vue';
export default {
  components: {
    mobile,
    email,
  },
  data() {
    return {
      comName: 'email',
    };
  },
};
</script>

<style></style>
