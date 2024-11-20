<template>
    <div class="p-4">
        <h1>About Page</h1>
        <p>This is the about page.</p>
        <h2>Redirect home page: {{ click }}</h2>

        <NuxtLink to="/">
            <button
                @click="click++"
                class="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-700"
            >
                Home
            </button>
        </NuxtLink>
    </div>
</template>

<script setup lang="ts">

const click = useLocalStorage("about-click", 0)
</script>
