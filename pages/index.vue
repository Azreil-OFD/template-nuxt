<template>
    <div class="p-4">
        <Toast />
        <h1>Welcome to my Nuxt 3 app!</h1>
        <h2>Redirect about page: {{ click }} </h2>
        <NuxtLink to="/about">
            <button @click="click++" class="bg-blue-500 text-white py-2 p-2 rounded hover:bg-blue-600">
                About
            </button>
        </NuxtLink>
        <Button @click="show" label="Contrast" severity="contrast" />
    </div>
</template>

<script setup lang="ts">
const toast = useToast();
const show = () => {
    toast.add({ severity: 'info', summary: 'Info', detail: 'HHFDHSFDKHSLKH', life: 3000 });
};

const click = useLocalStorage("index-click", 0)
</script>
