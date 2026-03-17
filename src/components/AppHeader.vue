<script setup lang="ts">
import { ref } from 'vue'

const mobileMenuOpen = ref(false)
</script>

<template>
  <header class="relative flex items-center w-full px-4 md:px-20 py-4 bg-white border-b border-[#E5E7EB]">
    <!-- Logo -->
    <span class="text-[22px] font-bold text-primary font-heading">HabitBoost</span>

    <!-- Nav (desktop) -->
    <nav class="hidden md:flex items-center justify-center gap-8 flex-1">
      <a href="#features" class="text-[15px] font-medium text-text-secondary hover:text-primary transition-colors">Возможности</a>
      <a href="#how-it-works" class="text-[15px] font-medium text-text-secondary hover:text-primary transition-colors">Как это работает</a>
      <a href="#testimonials" class="text-[15px] font-medium text-text-secondary hover:text-primary transition-colors">Отзывы</a>
    </nav>

    <!-- CTA Button (desktop) -->
    <a
      href="#download"
      class="hidden md:flex items-center gap-2 bg-primary text-white text-[14px] font-semibold px-6 py-[10px] rounded-lg hover:bg-primary-dark transition-colors"
    >
      <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"/><polyline points="7 10 12 15 17 10"/><line x1="12" y1="15" x2="12" y2="3"/>
      </svg>
      Скачать
    </a>

    <!-- Hamburger (mobile) -->
    <button
      class="ml-auto md:hidden p-1"
      @click="mobileMenuOpen = !mobileMenuOpen"
      aria-label="Меню"
    >
      <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#1F2937" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <line x1="3" y1="6" x2="21" y2="6"/><line x1="3" y1="12" x2="21" y2="12"/><line x1="3" y1="18" x2="21" y2="18"/>
      </svg>
    </button>

    <!-- Mobile Menu -->
    <div
      v-if="mobileMenuOpen"
      class="absolute top-full left-0 right-0 bg-white border-b border-[#E5E7EB] flex flex-col px-4 py-4 gap-4 z-50 md:hidden"
    >
      <a href="#features" class="text-[15px] font-medium text-text-secondary hover:text-primary transition-colors" @click="mobileMenuOpen = false">Возможности</a>
      <a href="#how-it-works" class="text-[15px] font-medium text-text-secondary hover:text-primary transition-colors" @click="mobileMenuOpen = false">Как это работает</a>
      <a href="#testimonials" class="text-[15px] font-medium text-text-secondary hover:text-primary transition-colors" @click="mobileMenuOpen = false">Отзывы</a>
      <a
        href="#download"
        class="flex items-center justify-center gap-2 bg-primary text-white text-[14px] font-semibold px-6 py-[10px] rounded-lg hover:bg-primary-dark transition-colors"
        @click="mobileMenuOpen = false"
      >Скачать</a>
    </div>
  </header>
</template>
