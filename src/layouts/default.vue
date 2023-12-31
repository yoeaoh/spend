<template>
    <div class="w-full h-screen flex">
        <Sidebar />

        <div class="h-full w-full p-2 bg-stone-200 dark:bg-slate-900">
            <slot />
        </div>
    </div>
</template>
