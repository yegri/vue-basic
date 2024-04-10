<template>
  <div>
    <!-- 영어로 입력받을 때 -->
    <input type="text" v-model="inputValue1" />

    <!-- 한글을 입력받을 땐 이 방법이 권장됨 -->
    <input
      type="text"
      :value="inputValue2"
      @input="inputValue2 = $event.target.value"
    />
  </div>
  <div>{{ inputValue1 }}</div>
  <div>{{ inputValue2 }}</div>
</template>

<script>
export default {
  data() {
    return {
      inputValue1: "",
      inputValue2: "",
    };
  },
};
</script>

<style lang="scss" scoped></style>
