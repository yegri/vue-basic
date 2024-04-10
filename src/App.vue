<template>
  <div>
    <ChildComponent
      :sendProps1="title"
      :sendProps2="createdAt"
      :sendProps3="obj"
    />
  </div>
</template>

<script setup lang="ts">
import { reactive, ref } from "vue";
import ChildComponent from "./components/ChildComponent.vue";

interface Obj {
  id: number;
  name: string;
}

const title = ref<string>("부모컴포넌트에서 선언된 데이터입니다.");
const createdAt = ref<number>(2024);
const obj = reactive<Obj>({
  id: 2024,
  name: "John",
});
</script>

<style lang="scss" scoped></style>
