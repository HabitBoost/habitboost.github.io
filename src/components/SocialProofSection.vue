<script setup lang="ts">
const stats = [
  { num: '50K+', label: 'Активных пользователей' },
  { num: '1M+', label: 'Привычек отслежено' },
  { num: '4.8★', label: 'Рейтинг App Store' },
  { num: '92%', label: 'Успешность' },
]

const testimonials = [
  {
    stars: 5,
    quote: 'HabitBoost полностью изменил мой утренний распорядок. Отслеживание серий мотивирует меня каждый день!',
    avatarColor: '#7C3AED',
    name: 'Anna K.',
    role: 'Использует HabitBoost 6 месяцев',
  },
  {
    stars: 5,
    quote: 'Я перепробовала десятки приложений для привычек, но именно это прижилось. Напоминания умные, а интерфейс красивый.',
    avatarColor: '#8B5CF6',
    name: 'Michael T.',
    role: 'Серия 21 день и не останавливается',
  },
  {
    stars: 5,
    quote: 'Бейджи достижений затягивают! Вся моя семья теперь соревнуется, кто соберёт самую длинную серию.',
    avatarColor: '#5B21B6',
    name: 'Sarah L.',
    role: 'Сбросила 10 кг благодаря полезным привычкам',
  },
]
</script>

<template>
  <section id="testimonials" class="flex flex-col items-center gap-10 md:gap-16 w-full px-5 md:px-[120px] py-12 md:py-20 bg-white">
    <!-- Section Title -->
    <div class="flex flex-col items-center gap-3 text-center">
      <h2
        class="text-[26px] md:text-[40px] font-bold text-text-primary tracking-tight"
        style="font-family: 'DM Sans', sans-serif; letter-spacing: -0.5px"
      >
        Что говорят наши пользователи
      </h2>
      <p class="text-text-secondary text-[14px] md:text-[18px] text-center">
        Присоединяйтесь к тысячам людей, изменивших свой распорядок дня
      </p>
    </div>

    <!-- Stats: 2x2 grid on mobile, row on desktop -->
    <div class="grid grid-cols-2 md:flex md:flex-row gap-3 md:gap-8 w-full">
      <div
        v-for="stat in stats"
        :key="stat.label"
        class="flex flex-col items-center gap-1 md:gap-2 flex-1 px-4 md:px-6 py-5 md:py-8 rounded-2xl bg-white border border-border"
      >
        <span
          class="text-[32px] md:text-[48px] font-bold text-primary tracking-tight"
          style="font-family: 'DM Sans', sans-serif; letter-spacing: -1px"
        >{{ stat.num }}</span>
        <span class="text-[13px] md:text-[16px] font-medium text-text-secondary text-center">{{ stat.label }}</span>
      </div>
    </div>

    <!-- Testimonials -->
    <div class="flex flex-col md:flex-row gap-4 md:gap-6 w-full">
      <div
        v-for="t in testimonials"
        :key="t.name"
        class="flex flex-col gap-4 md:gap-5 flex-1 p-6 md:p-8 rounded-2xl bg-primary-bg border border-[#E8E0F5]"
      >
        <span class="text-primary text-[18px] md:text-[20px]">★★★★★</span>
        <p class="text-text-primary text-[14px] md:text-[16px] leading-[1.6] w-full">{{ t.quote }}</p>
        <div class="flex items-center gap-3">
          <div
            class="w-11 h-11 rounded-full flex-shrink-0"
            :style="{ backgroundColor: t.avatarColor }"
          ></div>
          <div class="flex flex-col gap-0.5">
            <span
              class="text-[15px] font-semibold text-text-primary"
              style="font-family: 'DM Sans', sans-serif"
            >{{ t.name }}</span>
            <span class="text-[13px] text-text-muted">{{ t.role }}</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
