<script lang="ts" setup>
import type { IExpense } from "~/interfaces/expenses.interface";

const expensesList = ref<IExpense[]>([]);

function handleSubmitExpensesForm(expensesFormState: IExpense) {
    const newExpense = { ...expensesFormState };

    expensesList.value.push(newExpense);
}
</script>

<template>
    <div class="space-y-4">
        <ExpensesForm @submit="handleSubmitExpensesForm" />

        <ExpensesList :expenses-list="expensesList" />
    </div>
</template>
