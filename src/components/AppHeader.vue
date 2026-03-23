<script setup lang="ts">
import { ref } from 'vue'

const mobileMenuOpen = ref(false)
</script>

<template>
  <header class="sticky top-0 z-50 flex items-center justify-between w-full h-16 md:h-20 px-5 md:px-20 bg-white border-b border-border">
    <!-- Logo -->
    <div class="flex items-center gap-2">
      <img src="/leafIcon.png" alt="HabitBoost" class="w-7 h-7 md:w-8 md:h-8 rounded-full" />
      <span class="text-lg md:text-[22px] font-bold text-text-primary" style="font-family: 'Bricolage Grotesque', sans-serif">HabitBoost</span>
    </div>

    <!-- Nav (desktop) -->
    <nav class="hidden md:flex items-center gap-8">
      <a href="#features" class="text-[15px] font-medium text-text-secondary hover:text-text-primary transition-colors">Возможности</a>
      <a href="#how-it-works" class="text-[15px] font-medium text-text-secondary hover:text-text-primary transition-colors">Как это работает</a>
      <a href="#testimonials" class="text-[15px] font-medium text-text-secondary hover:text-text-primary transition-colors">Отзывы</a>
      <a href="#stats" class="text-[15px] font-medium text-text-secondary hover:text-text-primary transition-colors">Цены</a>
    </nav>

    <!-- CTA Button (desktop) -->
    <a
      href="#download"
      class="hidden md:flex items-center gap-2 bg-accent-coral text-white text-[15px] font-semibold px-6 py-3 rounded-full hover:opacity-90 transition-opacity"
    >
      Скачать приложение
    </a>

    <!-- Hamburger (mobile) -->
    <button
      class="md:hidden p-1"
      @click="mobileMenuOpen = !mobileMenuOpen"
      aria-label="Меню"
    >
      <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#1A1A1A" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <line x1="4" y1="6" x2="20" y2="6"/><line x1="4" y1="12" x2="20" y2="12"/><line x1="4" y1="18" x2="20" y2="18"/>
      </svg>
    </button>

    <!-- Mobile Menu -->
    <div
      v-if="mobileMenuOpen"
      class="absolute top-full left-0 right-0 bg-white border-b border-border flex flex-col px-5 py-4 gap-4 z-50 md:hidden"
    >
      <a href="#features" class="text-[15px] font-medium text-text-secondary" @click="mobileMenuOpen = false">Возможности</a>
      <a href="#how-it-works" class="text-[15px] font-medium text-text-secondary" @click="mobileMenuOpen = false">Как это работает</a>
      <a href="#testimonials" class="text-[15px] font-medium text-text-secondary" @click="mobileMenuOpen = false">Отзывы</a>
      <a
        href="#download"
        class="flex items-center justify-center bg-accent-coral text-white text-[15px] font-semibold px-6 py-3 rounded-full"
        @click="mobileMenuOpen = false"
      >Скачать приложение</a>
    </div>
  </header>
</template>
