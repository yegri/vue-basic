<template>
  <div>
    {{ count }}
  </div>
  <h1>Vue.js 라이프사이클 테스트</h1>
</template>

<script>
export default {
  data() {
    return {
      count: 0,
    };
  },
  beforeCreate() {
    console.log("lifeCycle is beforeCreate", this.count);
  },
  created() {
    console.log("lifeCycle is created", this.count);
  },
  beforeMount() {
    console.log("lifeCycle is beforeMount", document.querySelector("h1"));
  },
  mounted() {
    console.log("lifeCycle is mounted", document.querySelector("h1"));
  },
};
</script>

<style lang="scss" scoped></style>
