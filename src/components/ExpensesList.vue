<script lang="ts" setup>
import type { IExpense } from "~/interfaces/expenses.interface";

defineProps<{
    expensesList: Array<IExpense>;
}>();
</script>

<template>
    <div class="space-y-4">
        <ExpensesCard
            v-for="expense in expensesList"
            :key="expense.id"
            :expense="expense"
        />
    </div>
</template>

<style lang="scss" scoped></style>
