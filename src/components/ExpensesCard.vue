<script lang="ts" setup>
import { type IExpense } from "~/interfaces/expenses.interface";

defineProps<{
    expense: IExpense;
}>();
</script>

<template>
    <UCard>
        <template #header>{{ expense.category }}</template>

        <template #default>
            <div>{{ expense.id }}</div>
            <div>{{ expense.sum }}</div>
            <div>{{ expense.date }}</div>
        </template>

        <template #footer>{{ expense.description }}</template>
    </UCard>
</template>

<style lang="scss" scoped></style>
