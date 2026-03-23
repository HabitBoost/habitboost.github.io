<script setup lang="ts"></script>

<template>
  <section class="flex flex-col md:flex-row items-center w-full gap-8 md:gap-16 px-5 md:px-20 py-10 md:py-14 bg-white min-h-[calc(100vh-64px)] md:min-h-[calc(100vh-80px)] justify-center">
    <!-- Left Column -->
    <div class="flex flex-col items-center md:items-start gap-8 flex-1 w-full">
      <h1
        class="text-[32px] md:text-[48px] font-extrabold leading-[1.15] text-center md:text-left text-text-primary"
        style="font-family: 'Bricolage Grotesque', sans-serif"
      >
        Создавай привычки, которые меняют жизнь
      </h1>

      <p class="text-text-secondary text-base md:text-lg leading-[1.5] text-center md:text-left">
        HabitBoost — ваш персональный помощник для формирования полезных привычек. Отслеживайте прогресс, получайте мотивацию и достигайте целей каждый день.
      </p>

      <!-- Buttons -->
      <div class="flex flex-col md:flex-row gap-3 md:gap-4 w-full md:w-auto">
        <a
          href="#download"
          class="flex items-center justify-center gap-[10px] bg-text-primary text-white rounded-full px-7 py-[14px] hover:opacity-90 transition-opacity w-full md:w-auto"
        >
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="M12 20.94c1.5 0 2.75 1.06 4 1.06 3 0 6-8 6-12.22A4.91 4.91 0 0 0 17 5c-2.22 0-4 1.44-5 2-1-.56-2.78-2-5-2a4.9 4.9 0 0 0-5 4.78C2 14 5 22 8 22c1.25 0 2.5-1.06 4-1.06z"/>
            <path d="M10 2c0 2.5-2 4-2 4"/>
          </svg>
          <span class="text-[15px] font-semibold">App Store</span>
        </a>
        <a
          href="#download"
          class="flex items-center justify-center gap-[10px] bg-text-primary text-white rounded-full px-7 py-[14px] hover:opacity-90 transition-opacity w-full md:w-auto"
        >
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <polygon points="5 3 19 12 5 21 5 3"/>
          </svg>
          <span class="text-[15px] font-semibold">Google Play</span>
        </a>
      </div>

      <span class="text-text-tertiary text-sm font-medium text-center md:text-left">
        50,000+ пользователей уже с нами
      </span>
    </div>

    <!-- Phone Mockup — hidden in initial viewport on mobile, visible on desktop fully fitting screen -->
    <div class="hidden md:flex items-center justify-center rounded-[44px] bg-bg-card border-2 border-border p-5 flex-shrink-0 relative" style="height: calc(100vh - 80px - 112px); aspect-ratio: 380/780;">
      <img
        src="/images/REkoD.png"
        alt="HabitBoost app"
        class="w-full h-full object-cover rounded-[28px]"
      />
      <div class="absolute top-7 left-1/2 -translate-x-1/2 w-[120px] h-8 bg-text-primary rounded-2xl"></div>
    </div>
  </section>

  <!-- Phone Mockup for mobile — separate block below hero, appears on scroll -->
  <div class="flex md:hidden items-center justify-center px-5 pb-10 bg-white">
    <div class="flex items-center justify-center w-[280px] h-[560px] rounded-[36px] bg-bg-card border-2 border-border p-4 relative">
      <img
        src="/images/REkoD.png"
        alt="HabitBoost app"
        class="w-full h-full object-cover rounded-[22px]"
      />
      <div class="absolute top-6 left-1/2 -translate-x-1/2 w-[90px] h-[26px] bg-text-primary rounded-xl"></div>
    </div>
  </div>
</template>
