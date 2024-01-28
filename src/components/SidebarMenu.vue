<script setup>
const links = [
    {
        label: "Обзор",
        icon: "ph:grid-four-bold",
        to: "dashboard",
    },
    {
        label: "Расходы",
        icon: "ph:trend-down-bold",
        to: "expenses",
    },
    {
        label: "Категории",
        icon: "ph:list-bold",
        to: "categories",
    },
    {
        label: "Доходы",
        icon: "ph:trend-up-bold",
        to: "incomes",
    },
];
</script>

<template>
    <UVerticalNavigation :links="links" />
</template>
