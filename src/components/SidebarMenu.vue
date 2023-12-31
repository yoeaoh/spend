<script setup>
const links = [
    {
        label: "Обзор",
        icon: "ph:grid-four-bold",
    },
    {
        label: "Расходы",
        icon: "ph:trend-down-bold",
    },
    {
        label: "Категории",
        icon: "ph:list-bold",
    },
    {
        label: "Доходы",
        icon: "ph:trend-up-bold",
    },
];
</script>

<template>
    <UVerticalNavigation
        :links="links"
        :ui="{
            base: 'dark:hover:before:bg-white/10 hover:before:bg-black/10',
            padding: 'p-2',
            // active: 'text-blue-500 dark:text-blue-400 font-semibold',
            // inactive: 'text-red-700 hover:text-red-900 dark:text-red-400 dark:hover:text-red-300',
        }"
    >
        <template #icon="{ link }">
            <Icon :name="link.icon" class="text-xl shrink-0" />
        </template>

        <template #default="{ link }">
            <span class="text-lg">{{ link.label }}</span>
        </template>
    </UVerticalNavigation>
</template>
