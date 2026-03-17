<script setup lang="ts"></script>

<template>
  <section
    id="download"
    class="flex flex-col items-center gap-6 md:gap-8 w-full px-5 md:px-[120px] py-12 md:py-20"
    style="background: linear-gradient(180deg, #7C3AED 0%, #5B21B6 100%)"
  >
    <!-- Badge -->
    <div class="bg-white/[0.125] rounded-full px-4 py-2">
      <span class="text-white/80 text-[12px] md:text-[13px] font-semibold">Скоро в доступе</span>
    </div>

    <!-- Title -->
    <h2
      class="text-white text-[28px] md:text-[44px] font-bold text-center tracking-tight"
      style="font-family: 'DM Sans', sans-serif; letter-spacing: -0.5px; max-width: 700px"
    >
      Начните формировать полезные привычки уже сегодня
    </h2>

    <!-- Subtitle -->
    <p
      class="text-white/80 text-[15px] md:text-[18px] leading-[1.6] text-center"
      style="max-width: 600px"
    >
      Скачайте HabitBoost и присоединяйтесь к 50 000+ людей, которые меняют свою жизнь шаг за шагом. Бесплатный старт.
    </p>

    <!-- Buttons -->
    <div class="flex flex-col md:flex-row gap-3 md:gap-4 pt-2 w-full md:w-auto">
      <!-- App Store -->
      <a
        href="#"
        class="flex items-center justify-center gap-3 bg-white px-7 py-[14px] rounded-xl hover:bg-white/90 transition-colors w-full md:w-auto"
      >
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#7C3AED" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <path d="M12 20.94c1.5 0 2.75 1.06 4 1.06 3 0 6-8 6-12.22A4.91 4.91 0 0 0 17 5c-2.22 0-4 1.44-5 2-1-.56-2.78-2-5-2a4.9 4.9 0 0 0-5 4.78C2 14 5 22 8 22c1.25 0 2.5-1.06 4-1.06z"/>
          <path d="M10 2c0 2.5-2 4-2 4"/>
        </svg>
        <div class="flex flex-col gap-0.5">
          <span class="text-text-secondary text-[11px]">Загрузите в</span>
          <span class="text-text-primary text-[18px] font-bold" style="font-family: 'DM Sans', sans-serif">App Store</span>
        </div>
      </a>

      <!-- Google Play -->
      <a
        href="#"
        class="flex items-center justify-center gap-3 bg-white px-7 py-[14px] rounded-xl hover:bg-white/90 transition-colors w-full md:w-auto"
      >
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#7C3AED" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <polygon points="5 3 19 12 5 21 5 3"/>
        </svg>
        <div class="flex flex-col gap-0.5">
          <span class="text-text-secondary text-[11px]">Доступно в</span>
          <span class="text-text-primary text-[18px] font-bold" style="font-family: 'DM Sans', sans-serif">Google Play</span>
        </div>
      </a>
    </div>

    <!-- Trust note -->
    <p class="text-white/60 text-[12px] md:text-[14px] text-center">
      Бесплатное скачивание · Без банковской карты · Отмена в любой момент
    </p>
  </section>
</template>
