<template>
    <div class="relative">
        <!-- Шапка с кнопкой вызова слайдера 888 -->
        <div class="flex justify-end border-b-2 ">
            <div @click="toggleSidebar" class="block border-l-2 p-3 hover:bg-gray-50  active:bg-gray-100 transition">
                <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24"><path fill="#888888" d="M9.367 2.25h5.266c1.092 0 1.958 0 2.655.057c.714.058 1.317.18 1.869.46a4.75 4.75 0 0 1 2.075 2.077c.281.55.403 1.154.461 1.868c.057.697.057 1.563.057 2.655v5.266c0 1.092 0 1.958-.057 2.655c-.058.714-.18 1.317-.46 1.869a4.75 4.75 0 0 1-2.076 2.075c-.552.281-1.155.403-1.869.461c-.697.057-1.563.057-2.655.057H9.367c-1.092 0-1.958 0-2.655-.057c-.714-.058-1.317-.18-1.868-.46a4.75 4.75 0 0 1-2.076-2.076c-.281-.552-.403-1.155-.461-1.869c-.057-.697-.057-1.563-.057-2.655V9.367c0-1.092 0-1.958.057-2.655c.058-.714.18-1.317.46-1.868a4.75 4.75 0 0 1 2.077-2.076c.55-.281 1.154-.403 1.868-.461c.697-.057 1.563-.057 2.655-.057m6.383 1.503v16.494a20 20 0 0 0 1.416-.049c.62-.05 1.005-.147 1.31-.302a3.25 3.25 0 0 0 1.42-1.42c.155-.305.251-.69.302-1.31c.051-.63.052-1.434.052-2.566V9.4c0-1.132 0-1.937-.052-2.566c-.05-.62-.147-1.005-.302-1.31a3.25 3.25 0 0 0-1.42-1.42c-.305-.155-.69-.251-1.31-.302a20 20 0 0 0-1.416-.05"/></svg>
            </div>
        </div>

        <div @click="toggleSidebar" v-if="isOpen" class="fixed inset-0 bg-black bg-opacity-50 transition-opacity "></div>

        <!-- Слайдер -->
        <div :class="{'translate-x-0': isOpen, '-translate-x-full': !isOpen}" class=" h-screen transition-transform duration-500 fixed top-0 ">
            <div class=" block h-full w-80 border bg-gray-50 p-3">
            <!-- Блок всего слайдера bg-gray-200 -->
                <div class="flex flex-col w-full h-screen">
                    <!-- слайдер хедер bg-gray-300 -->
                    <div class=" h-20 mb-2 gap-1 p-3 flex ">
                        <div class="  p-1">
                            <div class="p-4 bg-gray-900 h-full w-full rounded-xl flex items-center justify-center">
                                <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24"><path fill="#ffffff" d="M4 5h16V3H4zm16 4H4V7h16zM9 13h6v-2h6v9a1 1 0 0 1-1 1H4a1 1 0 0 1-1-1v-9h6z"/></svg>
                            </div>
                        </div>
                        <div class=" w-full flex-col flex items-start justify-center">
                            <h1 class=" text-xm text-gray-600 font-semibold">Семён Богданов</h1>
                            <span class=" text-xs text-gray-600">Личный кабинет</span>
                        </div>
                    </div>
                    <!-- слайдер боди bg-gray-300-->
                    <div class=" flex-1 min-h-96 mb-2 p-3">
                    <label for="" class="inline-block mb-3 text-sm text-gray-400 px-4">Разделы</label>
                        <ul class=" block flex-col mb-2">

                            <li class="flex-row mb-2 hover:bg-gray-200 h-14 rounded-lg flex justify-between items-center px-4">
                            <p class="text-gray-600">Личный профиль</p>
                            <svg class="" xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"><path fill="#888888" d="M12.172 12L9.343 9.173l1.415-1.414L15 12l-4.242 4.242l-1.415-1.414z"/></svg>
                            </li>

                            <li class="flex-row mb-2 hover:bg-gray-200 h-14 rounded-lg flex justify-between items-center px-4">
                            <p class="text-gray-600">Видеозаписи</p>
                            <svg class="" xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"><path fill="#888888" d="M12.172 12L9.343 9.173l1.415-1.414L15 12l-4.242 4.242l-1.415-1.414z"/></svg>
                            </li>

                            <li class="flex-row mb-2 hover:bg-gray-200 h-14 rounded-lg flex justify-between items-center px-4">
                            <p class="text-gray-600">Вебинары</p>
                            <svg class="" xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"><path fill="#888888" d="M12.172 12L9.343 9.173l1.415-1.414L15 12l-4.242 4.242l-1.415-1.414z"/></svg>
                            </li>
                        </ul>

                        <label for="" class="inline-block mb-3 text-sm text-gray-400 px-4 mt-6">Разделы</label>
                            <ul class=" block flex-col mb-2">

                                <li class="flex-row mb-2 hover:bg-gray-200 h-14 rounded-lg flex justify-between items-center px-4">
                                <p class="text-gray-600">Личный профиль</p>
                                <svg class="" xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"><path fill="#888888" d="M12.172 12L9.343 9.173l1.415-1.414L15 12l-4.242 4.242l-1.415-1.414z"/></svg>
                                </li>

                                <li class="flex-row mb-2 hover:bg-gray-200 h-14 rounded-lg flex justify-between items-center px-4">
                                <p class="text-gray-600">Видеозаписи</p>
                                <svg class="" xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"><path fill="#888888" d="M12.172 12L9.343 9.173l1.415-1.414L15 12l-4.242 4.242l-1.415-1.414z"/></svg>
                                </li>

                                <li class="flex-row mb-2 hover:bg-gray-200 h-14 rounded-lg flex justify-between items-center px-4">
                                <p class="text-gray-600">Вебинары</p>
                                <svg class="" xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24"><path fill="#888888" d="M12.172 12L9.343 9.173l1.415-1.414L15 12l-4.242 4.242l-1.415-1.414z"/></svg>
                                </li>
                            </ul>

                    </div>
                    <!-- слайдер футер bg-gray-300-->
                    <div class="h-20">
                    </div>
                </div>
            </div>
        </div>

    </div>
</template>

<script setup>
import { ref } from 'vue'

const isOpen = ref(false)

const toggleSidebar = () => {
  isOpen.value = !isOpen.value
}
</script>
