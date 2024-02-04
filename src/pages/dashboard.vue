<script lang="ts" setup></script>

<template>
    <div class="dashboard">
        <div class="dashboard__column">
            <UCard>
                <template #header>asd</template>

                <template #default>asd</template>

                <template #footer>asd</template>
            </UCard>
        </div>

        <div class="dashboard__column">
            <UCard>
                <template #header>asd</template>

                <template #default>asd</template>

                <template #footer>asd</template>
            </UCard>
        </div>

        <div class="dashboard__column">
            <UCard>
                <template #header>asd</template>

                <template #default>asd</template>

                <template #footer>asd</template>
            </UCard>
        </div>

        <div class="dashboard__column">
            <UCard>
                <template #header> asd </template>

                <template #default>asd</template>

                <template #footer> asd </template>
            </UCard>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.dashboard {
    @apply grid grid-cols-4;

    &__column {
        @apply p-2;
    }
}
</style>
