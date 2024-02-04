<script lang="ts" setup>
import type { FormSubmitEvent } from "@nuxt/ui/dist/runtime/types";
import { z } from "zod";

import type { IExpense } from "~/interfaces/expenses.interface";

const emit = defineEmits<{
    submit: [value: IExpense];
}>();

const schema = z.object({
    sum: z.number().min(1),
    date: z.string().min(1),
    category: z.string().min(1),
    description: z.string().min(1),
});

const state = reactive({
    sum: 0,
    date: "",
    category: "",
    description: "",
});

function generateId() {
    return Date.now().toString();
}

function handleSubmit(event: FormSubmitEvent<IExpense>) {
    emit("submit", { id: generateId(), ...event.data });
}
</script>

<template>
    <UForm
        :schema="schema"
        :state="state"
        class="space-y-2 bg-gray-100 dark:bg-gray-800 p-6 rounded-lg"
        @submit="handleSubmit"
    >
        <UFormGroup label="Сумма" name="sum" eager-validation>
            <UInput v-model.number="state.sum" placeholder="Сумма расхода" />
        </UFormGroup>

        <UFormGroup label="Дата" name="date" eager-validation>
            <UInput v-model="state.date" placeholder="Дата" />
        </UFormGroup>

        <UFormGroup label="Категория" name="category" eager-validation>
            <UInput v-model="state.category" placeholder="Категория" />
        </UFormGroup>

        <UFormGroup label="Описание" name="description" eager-validation>
            <UInput
                v-model="state.description"
                placeholder="Дополнительное описание"
            />
        </UFormGroup>

        <UButton type="submit">Добавить</UButton>
    </UForm>
</template>
