<script setup lang="ts">
const footerLinks = [
  {
    title: 'Продукт',
    links: ['Возможности', 'Цены', 'Обновления', 'Дорожная карта'],
  },
  {
    title: 'Компания',
    links: ['О нас', 'Блог', 'Карьера', 'Контакты'],
  },
  {
    title: 'Правовая информация',
    links: ['Политика конфиденциальности', 'Условия использования', 'Политика Cookie'],
  },
]
</script>

<template>
  <footer class="flex flex-col gap-8 md:gap-12 w-full px-5 md:px-[120px] py-10 md:py-[60px] bg-text-primary">
    <!-- Top Row -->
    <div class="flex flex-col md:flex-row md:justify-between gap-8 w-full">
      <!-- Brand -->
      <div class="flex flex-col gap-3 md:w-[300px]">
        <span
          class="text-white text-[22px] md:text-[24px] font-bold"
          style="font-family: 'DM Sans', sans-serif"
        >HabitBoost</span>
        <p class="text-white/50 text-[13px] md:text-[14px] leading-[1.6]" style="max-width: 280px">
          Формируйте полезные привычки, меняйте свою жизнь. Один маленький шаг за раз.
        </p>
      </div>

      <!-- Links: 3-column grid on mobile, flex row on desktop -->
      <div class="grid grid-cols-3 md:flex md:flex-row gap-6 md:gap-16">
        <div
          v-for="col in footerLinks"
          :key="col.title"
          class="flex flex-col gap-3 md:gap-4"
        >
          <span
            class="text-white text-[13px] md:text-[14px] font-semibold"
            style="font-family: 'DM Sans', sans-serif"
          >{{ col.title }}</span>
          <a
            v-for="link in col.links"
            :key="link"
            href="#"
            class="text-white/50 text-[12px] md:text-[14px] hover:text-white/80 transition-colors leading-[1.4]"
          >{{ link }}</a>
        </div>
      </div>
    </div>

    <!-- Divider -->
    <div class="w-full h-px bg-white/[0.08]"></div>

    <!-- Bottom Row -->
    <div class="flex flex-col md:flex-row md:justify-between items-center gap-4 w-full">
      <span class="text-white/[0.38] text-[12px] md:text-[13px] text-center md:text-left">© 2026 HabitBoost. Все права защищены.</span>
      <div class="flex gap-5 items-center">
        <!-- Twitter -->
        <a href="#" class="text-white/[0.38] hover:text-white/70 transition-colors">
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="M22 4s-.7 2.1-2 3.4c1.6 10-9.4 17.3-18 11.6 2.2.1 4.4-.6 6-2C3 15.5.5 9.6 3 5c2.2 2.6 5.6 4.1 9 4-.9-4.2 4-6.6 7-3.8 1.1 0 3-1.2 3-1.2z"/>
          </svg>
        </a>
        <!-- Instagram -->
        <a href="#" class="text-white/[0.38] hover:text-white/70 transition-colors">
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <rect width="20" height="20" x="2" y="2" rx="5" ry="5"/><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/><line x1="17.5" y1="6.5" x2="17.51" y2="6.5"/>
          </svg>
        </a>
        <!-- GitHub -->
        <a href="#" class="text-white/[0.38] hover:text-white/70 transition-colors">
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="M15 22v-4a4.8 4.8 0 0 0-1-3.2c3 0 6-2 6-5.5.08-1.25-.27-2.48-1-3.5.28-1.15.28-2.35 0-3.5 0 0-1 0-3 1.5-2.64-.5-5.36-.5-8 0C6 2 5 2 5 2c-.3 1.15-.3 2.35 0 3.5A5.403 5.403 0 0 0 4 9c0 3.5 3 5.5 6 5.5-.39.49-.68 1.05-.85 1.65S8.93 17.38 9 18v4"/>
            <path d="M9 18c-4.51 2-5-2-7-2"/>
          </svg>
        </a>
        <!-- LinkedIn -->
        <a href="#" class="text-white/[0.38] hover:text-white/70 transition-colors">
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect width="4" height="12" x="2" y="9"/><circle cx="4" cy="4" r="2"/>
          </svg>
        </a>
      </div>
    </div>
  </footer>
</template>
