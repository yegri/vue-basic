<template>
  <button @click="changeMessage">{{ message }}</button>
</template>

<script>
export default {
  data() {
    return {
      message: "안녕하세요. Vue.js Watch 기능 테스트 오리지널 문구",
    };
  },

  // message라는 변수가 바뀌는 것을 지켜보고 있다가 changeMessage()를 통해 바뀌게 되면 alert창을 띄워줌
  // 데이터 뿐만 아니라 computed로 계산된 형태의 데이터도 watch로 감지할 수 있음
  // 보통 게시판에서 한 컬럼을 선택하였을 때, 고유한 id 값이 바뀜을 감지하고
  // 이때, 그 id 값에 따른 상세 데이터를 호출할 때 주로 사용함
  watch: {
    message() {
      window.alert("message 변수에 담긴 데이터가 변경되었습니다.");
    },
    id() {
      // 해당 상세데이터를 조회하는 api 호출
    },
  },

  methods: {
    changeMessage() {
      console.log("함수 호출");
      this.message = "변경된 message 데이터입니다.";
    },
  },
};
</script>

<style lang="scss" scoped></style>
