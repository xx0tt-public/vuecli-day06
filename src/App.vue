<template>
  <div id="box">
    <div class="hander">
      <span class="phone" :class="{ count: isClick == 'left' }" @click="leftFn"
        >手机注册</span
      >
      <span
        class="email"
        :class="{ count: isClick == 'right' }"
        @click="rightFn"
        >邮箱注册</span
      >
    </div>
    <keep-alive>
      <component :is="componentId"></component>
    </keep-alive>
  </div>
</template>

<script>
import Phone from './components/Phone.vue'
import Email from './components/Email.vue'
export default {
  data() {
    return {
      isClick: 'left',
      componentId: 'Phone',
    }
  },
  components: {
    Email,
    Phone,
  },
  methods: {
    leftFn() {
      this.componentId = 'Phone'
      this.isClick = 'left'
    },
    rightFn() {
      this.componentId = 'Email'
      this.isClick = 'right'
    },
  },
}
</script>

<style scoped>
#box {
  padding: 40px;
}
.hander {
  /* background-color: orange; */
  display: flex;
  justify-content: center;
  margin: 0 auto;
  font-size: 24px;
  margin-top: 10px;
}
.phone {
  margin-right: 40px;
}
.count {
  color: blue;
  border-bottom: 2px solid blue;
}
</style>
