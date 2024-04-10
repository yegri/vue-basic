<template>
  <h1>{{ text }}</h1>
  <h1>changeText 함수 호출 값: {{ changeText() }}</h1>
  <h1>changeText 함수 호출 값: {{ changeText() }}</h1>
  <h1>changeText 함수 호출 값: {{ changeText() }}</h1>

  <h2>{{ computedText }}</h2>
  <h2>{{ computedText }}</h2>
  <h2>{{ computedText }}</h2>
</template>

<script>
export default {
  data() {
    return {
      text: "Computed 테스트 데이터 문구입니다.",
    };
  },
  // methods 부분에 선언된 함수와 동일한 로직일 때,
  // 캐싱 기능이 없는 methods는 호출될 때마다 console 값이 출력 됨
  // 반면에, computed는 캐싱 기능이 있기 때문에 methods와 어떤 차이점이 있는지 주의 깊게 살펴보는 것이 포인트
  computed: {
    computedText() {
      console.log("Computed 기능을 생성하였습니다.");
      return this.text.split("").reverse().join("");
    },
  },
  methods: {
    changeText() {
      console.log("함수 호출");
      console.log(this.text);

      return this.text.split("").reverse().join("");
    },
  },
};
</script>

<style lang="scss" scoped></style>
