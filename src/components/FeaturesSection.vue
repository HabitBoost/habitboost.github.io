<script setup lang="ts">
const features = [
  {
    icon: 'bell',
    title: 'Умные напоминания',
    desc: 'Никогда не пропустите привычку благодаря умным уведомлениям, которые подстраиваются под ваш график.',
  },
  {
    icon: 'flame',
    title: 'Отслеживание серий',
    desc: 'Поддерживайте мотивацию с помощью визуальных счётчиков серий, которые отмечают вашу стабильность.',
  },
  {
    icon: 'trending-up',
    title: 'Ежедневная аналитика',
    desc: 'Получайте персонализированную аналитику и полезные инсайты для улучшения ваших привычек.',
  },
  {
    icon: 'layout-template',
    title: 'Шаблоны привычек',
    desc: 'Начните быстро с готовыми шаблонами для фитнеса, осознанности, продуктивности и многого другого.',
  },
  {
    icon: 'calendar',
    title: 'Календарь прогресса',
    desc: 'Визуализируйте свой путь с помощью красивого календаря, показывающего ежедневный прогресс.',
  },
  {
    icon: 'trophy',
    title: 'Бейджи достижений',
    desc: 'Зарабатывайте бейджи и награды за достижение целей, поддерживая интерес и радость от побед.',
  },
]

const iconPaths: Record<string, string> = {
  'bell': 'M18 8A6 6 0 0 0 6 8c0 7-3 9-3 9h18s-3-2-3-9M13.73 21a2 2 0 0 1-3.46 0',
  'flame': 'M8.5 14.5A2.5 2.5 0 0 0 11 12c0-1.38-.5-2-1-3-1.072-2.143-.224-4.054 2-6 .5 2.5 2 4.9 4 6.5 2 1.6 3 3.5 3 5.5a7 7 0 1 1-14 0c0-1.153.433-2.294 1-3a2.5 2.5 0 0 0 2.5 2.5z',
  'trending-up': 'M23 6l-9.5 9.5-5-5L1 18M17 6h6v6',
  'layout-template': 'M3 9h18v10a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V9zM3 9V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2v4M13 9v12M3 14h10',
  'calendar': 'M8 2v4M16 2v4M3 10h18M5 4h14a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V6a2 2 0 0 1 2-2z',
  'trophy': 'M6 9H4.5a2.5 2.5 0 0 1 0-5H6M18 9h1.5a2.5 2.5 0 0 0 0-5H18M4 22h16M10 14.66V17c0 .55-.47.98-.97 1.21C7.85 18.75 7 20.24 7 22M14 14.66V17c0 .55.47.98.97 1.21C16.15 18.75 17 20.24 17 22M18 2H6v7a6 6 0 0 0 12 0V2z',
}
</script>

<template>
  <section id="features" class="flex flex-col items-center gap-8 md:gap-12 w-full px-5 md:px-20 py-10 md:py-20 bg-white">
    <!-- Header -->
    <div class="flex flex-col items-center gap-4 w-full">
      <div class="bg-primary-bg rounded-full px-4 py-[6px]">
        <span class="text-primary text-[13px] font-semibold">Возможности</span>
      </div>
      <h2
        class="text-[26px] md:text-[36px] font-bold text-text-primary text-center leading-[1.2] md:leading-[1.15]"
        style="font-family: 'DM Sans', sans-serif; max-width: 700px"
      >
        Всё, что нужно для формирования устойчивых привычек
      </h2>
      <p class="text-text-secondary text-[14px] md:text-[17px] leading-[1.5] text-center" style="max-width: 600px">
        Мощные инструменты для создания, отслеживания и поддержания полезных привычек каждый день.
      </p>
    </div>

    <!-- Grid -->
    <div class="flex flex-col gap-4 md:gap-6 w-full">
      <!-- Row 1 -->
      <div class="flex flex-col md:flex-row gap-4 md:gap-6 w-full">
        <div
          v-for="feature in features.slice(0, 3)"
          :key="feature.title"
          class="flex flex-col gap-3 md:gap-4 flex-1 p-6 md:p-8 rounded-2xl bg-bg border border-border"
        >
          <div class="w-12 h-12 flex items-center justify-center rounded-xl bg-primary-bg flex-shrink-0">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" :stroke="'#7C3AED'" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
              <path :d="iconPaths[feature.icon]" />
            </svg>
          </div>
          <h3 class="text-[17px] md:text-[18px] font-bold text-text-primary" style="font-family: 'DM Sans', sans-serif">{{ feature.title }}</h3>
          <p class="text-text-secondary text-[14px] leading-[1.5]">{{ feature.desc }}</p>
        </div>
      </div>
      <!-- Row 2 -->
      <div class="flex flex-col md:flex-row gap-4 md:gap-6 w-full">
        <div
          v-for="feature in features.slice(3)"
          :key="feature.title"
          class="flex flex-col gap-3 md:gap-4 flex-1 p-6 md:p-8 rounded-2xl bg-bg border border-border"
        >
          <div class="w-12 h-12 flex items-center justify-center rounded-xl bg-primary-bg flex-shrink-0">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" :stroke="'#7C3AED'" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
              <path :d="iconPaths[feature.icon]" />
            </svg>
          </div>
          <h3 class="text-[17px] md:text-[18px] font-bold text-text-primary" style="font-family: 'DM Sans', sans-serif">{{ feature.title }}</h3>
          <p class="text-text-secondary text-[14px] leading-[1.5]">{{ feature.desc }}</p>
        </div>
      </div>
    </div>
  </section>
</template>
