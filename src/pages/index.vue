<script lang="ts" setup>
import { useGlobalStore } from "~/store/global.store";

const globalStore = useGlobalStore();
const { count } = storeToRefs(globalStore);
const { incrementCount } = globalStore;
</script>

<template>
    <div>
        <div>hi there!</div>
        <div>count is {{ count }}</div>
        <UButton @click="incrementCount">increment</UButton>
    </div>
</template>
