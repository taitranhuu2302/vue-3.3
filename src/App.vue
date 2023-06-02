<script setup lang="ts">
import {ref} from 'vue';
import ChildComponent from './components/ChildComponent.vue';
import GenericComponent from './components/GenericComponent.vue';
import AlertComponent from "@/components/AlertComponent.vue";

const listItem = ref<string[]>(["qwe", "asd"])
const counter = ref<number>(0)
const counterModel = ref<number>(0)

const increment = () => counter.value++

</script>

<template>
  <ChildComponent message="Hello" title="Tran Huu Tai"/>
  <p>Counter: {{ counter }}</p>
  <GenericComponent item="TEXT" :listItem="listItem" @increment="increment" v-model="counterModel"/>
  <AlertComponent></AlertComponent>
</template>

<style scoped></style>
