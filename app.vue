<template>
    <div class="relative">
        <!-- Шапка с кнопкой вызова слайдера -->
        <div class="flex justify-end border-b-2">
            <div @click="toggleBanner" class="block border-l-2 p-3 hover:bg-gray-50 transition">
                <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24"><path fill="#888888" d="M9.367 2.25h5.266c1.092 0 1.958 0 2.655.057c.714.058 1.317.18 1.869.46a4.75 4.75 0 0 1 2.075 2.077c.281.55.403 1.154.461 1.868c.057.697.057 1.563.057 2.655v5.266c0 1.092 0 1.958-.057 2.655c-.058.714-.18 1.317-.46 1.869a4.75 4.75 0 0 1-2.076 2.075c-.552.281-1.155.403-1.869.461c-.697.057-1.563.057-2.655.057H9.367c-1.092 0-1.958 0-2.655-.057c-.714-.058-1.317-.18-1.868-.46a4.75 4.75 0 0 1-2.076-2.076c-.281-.552-.403-1.155-.461-1.869c-.057-.697-.057-1.563-.057-2.655V9.367c0-1.092 0-1.958.057-2.655c.058-.714.18-1.317.46-1.868a4.75 4.75 0 0 1 2.077-2.076c.55-.281 1.154-.403 1.868-.461c.697-.057 1.563-.057 2.655-.057m6.383 1.503v16.494a20 20 0 0 0 1.416-.049c.62-.05 1.005-.147 1.31-.302a3.25 3.25 0 0 0 1.42-1.42c.155-.305.251-.69.302-1.31c.051-.63.052-1.434.052-2.566V9.4c0-1.132 0-1.937-.052-2.566c-.05-.62-.147-1.005-.302-1.31a3.25 3.25 0 0 0-1.42-1.42c-.305-.155-.69-.251-1.31-.302a20 20 0 0 0-1.416-.05"/></svg>
            </div>
        </div>

        <!-- Слайдер -->
        <div v-if="isBannerVisible" class=" banner h-screen ">
            <div  class="block h-full w-80 border absolute top-0 left-0 bg-gray-50 p-3">
                <div class="flex flex-col  bg-gray-200 w-full h-screen">
                    <!-- слайдер хедер -->
                    <div class="flex bg-gray-300 h-20 mb-2 p-2">
                        <div class="bg-gray-700"></div>
                        </div>
                    <!-- слайдер боди -->
                    <div class="bg-gray-300 flex-1 min-h-96 mb-2">
                    </div>
                    <!-- слайдер футер -->
                    <div class="bg-gray-300 h-20">
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
  import { ref } from 'vue'

  export default {
    setup() {
      // Создаем реактивную переменную для видимости баннера
      const isBannerVisible = ref(false)

      // Функция для переключения видимости баннера
      const toggleBanner = () => {
        isBannerVisible.value = !isBannerVisible.value
      }

      // Возвращаем переменную и функцию для использования в шаблоне
      return {
        isBannerVisible,
        toggleBanner
      }
    }
  }
</script>
