<script setup lang="ts">
import type { ChildComponentType } from '@/types'

const { message = '', title } = defineProps<ChildComponentType & { title?: string }>()
</script>

<template>
  <div>{{ title }}</div>
  <div>{{ message }}</div>
</template>

<style lang="scss" scoped></style>
