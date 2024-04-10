<template>
  <div>{{ props.sendProps1 }}</div>
  <div>{{ props.sendProps2 }}</div>
  <div>{{ props.sendProps3.id }}</div>
  <div>{{ props.sendProps3.name }}</div>
</template>

<script setup lang="ts">
import { toRef } from "vue";

interface Obj {
  id: number;
  name: string;
}
interface Props {
  sendProps1: String;
  sendProps2: Number;
  sendProps3: Obj;
}

// defineProps는 import 할 필요 없음
const props = defineProps<Props>();
// const { sendProps1, sendProps2, sendProps3 } = toRef(props);
</script>

<style lang="scss" scoped></style>
