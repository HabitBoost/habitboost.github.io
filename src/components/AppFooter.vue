<script setup lang="ts">
const footerLinks = [
  {
    title: 'Продукт',
    links: ['Возможности', 'Цены', 'Обновления', 'Бета-тест'],
  },
  {
    title: 'Компания',
    links: ['О нас', 'Блог', 'Карьера', 'Контакты'],
  },
  {
    title: 'Поддержка',
    links: ['Помощь', 'FAQ', 'Обратная связь', 'Сообщество'],
  },
  {
    title: 'Юридическая информация',
    links: ['Политика конфиденциальности', 'Условия использования', 'Cookie'],
  },
]
</script>

<template>
  <footer class="flex flex-col gap-8 md:gap-12 w-full px-5 md:px-20 py-10 md:py-12 bg-[#1A1A1A]">
    <!-- Top Row -->
    <div class="flex flex-col md:flex-row md:justify-between gap-8 w-full">
      <!-- Brand -->
      <div class="flex flex-col gap-4 md:w-[300px]">
        <div class="flex items-center gap-2">
          <img src="/leafIcon.png" alt="HabitBoost" class="w-7 h-7 rounded-full" />
          <span class="text-white text-[22px] font-bold" style="font-family: 'Bricolage Grotesque', sans-serif">HabitBoost</span>
        </div>
        <p class="text-white/60 text-[13px] md:text-sm leading-[1.6]">
          Создавай привычки, которые меняют жизнь. Трекер привычек с дневником, аналитикой и системой достижений.
        </p>
        <!-- Social Icons -->
        <div class="flex gap-3">
          <a href="https://github.com/habitboost" class="w-9 h-9 flex items-center justify-center rounded-full bg-white/[0.08] hover:bg-white/[0.15] transition-colors">
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="rgba(255,255,255,0.6)" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
              <path d="M15 22v-4a4.8 4.8 0 0 0-1-3.2c3 0 6-2 6-5.5.08-1.25-.27-2.48-1-3.5.28-1.15.28-2.35 0-3.5 0 0-1 0-3 1.5-2.64-.5-5.36-.5-8 0C6 2 5 2 5 2c-.3 1.15-.3 2.35 0 3.5A5.403 5.403 0 0 0 4 9c0 3.5 3 5.5 6 5.5-.39.49-.68 1.05-.85 1.65S8.93 17.38 9 18v4"/>
              <path d="M9 18c-4.51 2-5-2-7-2"/>
            </svg>
          </a>
        </div>
      </div>

      <!-- Link Columns: 2x2 on mobile, row on desktop -->
      <div class="grid grid-cols-2 md:flex md:flex-row gap-6 md:gap-12">
        <div
          v-for="col in footerLinks"
          :key="col.title"
          class="flex flex-col gap-3 md:gap-4"
        >
          <span class="text-white text-sm font-semibold">{{ col.title }}</span>
          <a
            v-for="link in col.links"
            :key="link"
            href="#"
            class="text-white/50 text-sm hover:text-white/80 transition-colors"
          >{{ link }}</a>
        </div>
      </div>
    </div>

    <!-- Divider -->
    <div class="w-full h-px bg-white/[0.08]"></div>

    <!-- Bottom Row -->
    <div class="flex flex-col md:flex-row md:justify-between items-center gap-3 w-full">
      <span class="text-white/[0.38] text-xs md:text-[13px]">© 2026 HabitBoost. Все права защищены.</span>
      <div class="flex items-center gap-1.5">
        <svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="rgba(255,255,255,0.38)" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <circle cx="12" cy="12" r="10"/><path d="M2 12h20M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/>
        </svg>
        <span class="text-white/[0.38] text-xs">Русский</span>
      </div>
    </div>
  </footer>
</template>
