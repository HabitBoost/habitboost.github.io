<script setup lang="ts"></script>

<template>
  <section
    class="flex flex-col md:flex-row items-center w-full gap-10 md:gap-[60px] px-5 md:px-20 pt-12 md:pt-20 pb-10 md:pb-[60px]"
    style="background: linear-gradient(180deg, #7C3AED 0%, #A78BFA 60%, #EDE9FE 100%)"
  >
    <!-- Left Column -->
    <div class="flex flex-col items-center md:items-start gap-6 md:gap-8 flex-1 w-full">
      <!-- Badge -->
      <div class="inline-flex self-center md:self-start bg-white/[0.19] rounded-full px-4 py-[6px]">
        <span class="text-white text-[13px] font-semibold">Приложение #1 для трекинга привычек</span>
      </div>

      <!-- Headline -->
      <h1
        class="text-white text-[32px] md:text-[48px] font-extrabold leading-[1.1] text-center md:text-left"
        style="font-family: 'DM Sans', sans-serif"
      >
        Формируйте полезные привычки день за днём
      </h1>

      <!-- Subline -->
      <p class="text-white/80 text-[15px] md:text-[18px] leading-[1.5] font-normal text-center md:text-left">
        Отслеживайте ежедневные привычки, сохраняйте мотивацию с помощью серий и меняйте свою жизнь благодаря мощной аналитике. Присоединяйтесь к миллионам.
      </p>

      <!-- Buttons -->
      <div class="flex flex-col md:flex-row gap-3 md:gap-4 w-full md:w-auto">
        <a
          href="#download"
          class="flex items-center justify-center gap-[10px] bg-white rounded-[14px] md:rounded-full px-7 py-[14px] hover:bg-white/90 transition-colors w-full md:w-auto"
        >
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="#7C3AED" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="M12 20.94c1.5 0 2.75 1.06 4 1.06 3 0 6-8 6-12.22A4.91 4.91 0 0 0 17 5c-2.22 0-4 1.44-5 2-1-.56-2.78-2-5-2a4.9 4.9 0 0 0-5 4.78C2 14 5 22 8 22c1.25 0 2.5-1.06 4-1.06z"/>
            <path d="M10 2c0 2.5-2 4-2 4"/>
          </svg>
          <span class="text-primary text-[15px] font-semibold">App Store</span>
        </a>
        <a
          href="#download"
          class="flex items-center justify-center gap-[10px] bg-white/[0.125] border border-white/[0.375] rounded-[14px] md:rounded-full px-7 py-[14px] hover:bg-white/20 transition-colors w-full md:w-auto"
        >
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <polygon points="5 3 19 12 5 21 5 3"/>
          </svg>
          <span class="text-white text-[15px] font-semibold">Google Play</span>
        </a>
      </div>

      <!-- Trust Row -->
      <div class="flex items-center gap-2 md:gap-6">
        <div class="flex items-center gap-1">
          <svg v-for="i in 5" :key="i" xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="#FBBF24" stroke="#FBBF24" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"/>
          </svg>
        </div>
        <span class="text-white/80 text-[13px] font-medium">4.9 — 10,000+ пользователей</span>
      </div>
    </div>

    <!-- Phone Mockup (desktop only) -->
    <div
      class="hidden md:flex w-[320px] h-[560px] rounded-[32px] flex-shrink-0 overflow-hidden"
      style="box-shadow: 0 20px 60px rgba(0,0,0,0.15)"
    >
      <img
        src="/images/generated-1773760604232.png"
        alt="HabitBoost app screenshot"
        class="w-full h-full object-cover"
      />
    </div>
  </section>
</template>
