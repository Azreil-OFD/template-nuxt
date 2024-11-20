<script setup>
import { ref } from 'vue'

const login = ref('')
const password = ref('')

function handleLogin() {
  console.log('Логин:', login.value)
  console.log('Пароль:', password.value)
}
</script>

<template>
    <div class="main-block flex flex-row grow h-screen bg-white text-black">
        <div class="left-block flex relative basis-2/4 h-screen">
            
            <div class="logo-block absolute top-10 left-0 w-full flex flex-col items-center text-[40px] z-10">
                <div class="flex flex-row justify-center items-center bg-black text-white px-5 py-4 rounded-3xl space-x-3 font-semibold">
                    <h1 class="Hanta">Ханта</h1>
                    <h1 class="Ton bg-orange-400 text-black rounded-2xl px-1.5">Тон</h1>
                </div>
            </div>


            <div class="enter-column flex flex-col items-center justify-center h-full w-full pt-24 text-[40px]">
                <div class="enter-group flex flex-col items-center w-full -mt-20 space-y-7">
                    <h2 class="enter-h2 font-bold">Вход</h2>
                    <input 
                        type="text" 
                        v-model="login" 
                        class="login-input bg-white text-black border-2 border-gray-400 rounded-xl pl-2.5 text-[35px] w-[45%]" 
                        placeholder="Логин"
                    >
                    <input 
                        type="text" 
                        v-model="password" 
                        class="password-input bg-white text-black border-2 border-gray-400 rounded-xl pl-2.5 text-[35px] w-[45%]" 
                        placeholder="Пароль"
                    >
                    
                    <button 
                        class="enter-button bg-black text-white px-20 py-2 rounded-xl font-semibold" 
                        @click="handleLogin">
                        Вход
                    </button>
                </div>
            </div>
        </div>

        
        <div class="right-block basis-3/4 h-screen">
            <img src="/public/img/gibun-(sozoshu)-Anime-Art-artist-Frieren-8676730.png" alt="" class="backgroung-img grow h-screen">
        </div>
    </div>
</template>