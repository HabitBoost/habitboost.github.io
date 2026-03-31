<script setup lang="ts"></script>

<template>
  <section
    id="download"
    class="flex flex-col items-center gap-6 md:gap-8 w-full px-5 md:px-20 py-12 md:py-20 bg-accent-coral"
  >
    <span class="text-4xl md:text-5xl">🚀</span>

    <h2
      class="text-white text-[28px] md:text-[48px] font-bold text-center"
      style="font-family: 'Bricolage Grotesque', sans-serif; max-width: 800px"
    >
      Начните менять свою жизнь сегодня
    </h2>

    <p
      class="text-white/[0.87] text-sm md:text-lg text-center leading-[1.5]"
      style="max-width: 650px"
    >
      Скачайте HabitBoost бесплатно и присоединяйтесь к пользователям, которые уже формируют полезные привычки
    </p>

    <!-- Buttons -->
    <div class="flex flex-col md:flex-row gap-3 md:gap-4 w-full md:w-auto">
      <a href="#" class="hover:opacity-85 transition-opacity w-full md:w-auto flex justify-center">
        <img src="/images/badge-appstore.png" alt="Download on the App Store" class="h-[54px]" />
      </a>
      <a href="#" class="hover:opacity-85 transition-opacity w-full md:w-auto flex justify-center">
        <img src="/images/badge-googleplay.png" alt="Get it on Google Play" class="h-[54px]" />
      </a>
    </div>

    <!-- Trust -->
    <div class="flex items-center gap-2">
      <svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="rgba(255,255,255,0.67)" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <path d="M20 13c0 5-3.5 7.5-7.66 8.95a1 1 0 0 1-.67-.01C7.5 20.5 4 18 4 13V6a1 1 0 0 1 1-1c2 0 4.5-1.2 6.24-2.72a1.17 1.17 0 0 1 1.52 0C14.51 3.81 17 5 19 5a1 1 0 0 1 1 1z"/>
        <path d="m9 12 2 2 4-4"/>
      </svg>
      <span class="text-white/[0.67] text-xs md:text-sm">Бесплатно · Без рекламы · Безопасно</span>
    </div>
  </section>
</template>
