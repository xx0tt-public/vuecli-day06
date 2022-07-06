<template>
  <div>
    <Handler />
    <keep-alive>
      <component :is="comName"></component>
    </keep-alive>
  </div>
</template>

<script>
import Phone from "./components/Phone.vue";
import Email from "./components/Email.vue";
import Handler from "./components/Handler.vue";
export default {
  data() {
    return {
      comName: "Phone",
    };
  },
  components: {
    Phone,
    Email,
    Handler,
  },
};
</script>

<style></style>
