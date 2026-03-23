<script setup lang="ts">
const features = [
  { color: '#FF6B6B', title: 'Трекер привычек', desc: 'Отслеживайте ежедневные привычки и отмечайте выполненные задачи одним нажатием' },
  { color: '#6366F1', title: 'Аналитика прогресса', desc: 'Наглядные графики и статистика покажут ваш путь к успеху' },
  { color: '#22C55E', title: 'Умные напоминания', desc: 'Настройте персональные уведомления, чтобы не пропустить ни одной привычки' },
  { color: '#FBBF24', title: 'Дневник рефлексии', desc: 'Записывайте мысли и отслеживайте своё эмоциональное состояние каждый день' },
  { color: '#FF6B6B', title: 'SOS поддержка', desc: 'Дыхательные упражнения и мотивационные цитаты в трудные моменты' },
  { color: '#6366F1', title: 'Достижения и бейджи', desc: 'Система геймификации с наградами за регулярность и достижение целей' },
]
</script>

<template>
  <section id="features" class="flex flex-col items-center gap-8 md:gap-16 w-full px-5 md:px-20 py-12 md:py-20 bg-bg-card">
    <!-- Header -->
    <div class="flex flex-col items-center gap-3 w-full">
      <h2
        class="text-[28px] md:text-[36px] font-bold text-text-primary text-center"
        style="font-family: 'Bricolage Grotesque', sans-serif"
      >
        Всё для ваших привычек
      </h2>
      <p class="text-text-secondary text-base md:text-lg text-center leading-[1.5]" style="max-width: 600px">
        Инструменты, которые помогут вам стать лучшей версией себя
      </p>
    </div>

    <!-- Grid -->
    <div class="flex flex-col gap-4 md:gap-6 w-full">
      <!-- Row 1 -->
      <div class="flex flex-col md:flex-row gap-4 md:gap-6 w-full">
        <div
          v-for="feature in features.slice(0, 3)"
          :key="feature.title"
          class="flex flex-col gap-3 md:gap-4 flex-1 p-6 md:p-8 rounded-2xl md:rounded-[20px] bg-white"
        >
          <div
            class="w-10 md:w-14 h-10 md:h-14 rounded-full flex-shrink-0"
            :style="{ backgroundColor: feature.color }"
          ></div>
          <h3 class="text-base md:text-lg font-bold text-text-primary">{{ feature.title }}</h3>
          <p class="text-text-secondary text-[13px] md:text-sm leading-[1.5]">{{ feature.desc }}</p>
        </div>
      </div>
      <!-- Row 2 -->
      <div class="flex flex-col md:flex-row gap-4 md:gap-6 w-full">
        <div
          v-for="feature in features.slice(3)"
          :key="feature.title"
          class="flex flex-col gap-3 md:gap-4 flex-1 p-6 md:p-8 rounded-2xl md:rounded-[20px] bg-white"
        >
          <div
            class="w-10 md:w-14 h-10 md:h-14 rounded-full flex-shrink-0"
            :style="{ backgroundColor: feature.color }"
          ></div>
          <h3 class="text-base md:text-lg font-bold text-text-primary">{{ feature.title }}</h3>
          <p class="text-text-secondary text-[13px] md:text-sm leading-[1.5]">{{ feature.desc }}</p>
        </div>
      </div>
    </div>
  </section>
</template>
