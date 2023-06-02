<script setup lang="ts" generic="T extends string">
import {defineEmits, defineModel, defineProps, watch, watchEffect} from 'vue';

const {item, listItem} = defineProps<{ item: T; listItem: T[] }>()
const emit = defineEmits<{ increment: [...rest: any[]] }>()
const modelValue = defineModel<number>({default: 0})

watchEffect(() => {
  console.log(listItem) // show
})

watch(item, () => {
  console.log(listItem) // not show
})

</script>
<template>
  <div>{{ item }}</div>
  <div>{{ listItem }}</div>
  <div>
    <button @click="emit('increment')">Increment</button>
    <button @click="modelValue++">Increment Counter Model</button>
    <p>Counter Model: {{ modelValue }}</p>
  </div>
</template>

<style scoped></style>
