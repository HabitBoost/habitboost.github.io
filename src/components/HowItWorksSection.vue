<script setup lang="ts">
const steps = [
  {
    num: '1',
    iconBg: '#7C3AED',
    iconPath: 'M12 22a10 10 0 1 1 0-20 10 10 0 0 1 0 20zm0-7l-3-3 1.41-1.41L12 12.17l4.59-4.58L18 9l-6 6z',
    title: 'Поставьте цели',
    desc: 'Выберите из шаблонов или создайте свои привычки. Настройте частоту, напоминания и цели под ваш образ жизни.',
    numColor: '#A78BFA',
  },
  {
    num: '2',
    iconBg: '#10B981',
    iconPath: 'M22 11.08V12a10 10 0 1 1-5.93-9.14M22 4L12 14.01l-3-3',
    title: 'Отмечайте ежедневно',
    desc: 'Отмечайте привычки одним нажатием. Собирайте серии, зарабатывайте бейджи и наблюдайте за прогрессом.',
    numColor: '#A78BFA',
  },
  {
    num: '3',
    iconBg: '#8B5CF6',
    iconPath: 'M23 6l-9.5 9.5-5-5L1 18M17 6h6v6',
    title: 'Смотрите результаты',
    desc: 'Откройте мощную аналитику с визуализацией. Отслеживайте прогресс, находите закономерности и празднуйте рост.',
    numColor: '#A78BFA',
  },
]
</script>

<template>
  <section id="how-it-works" class="flex flex-col items-center gap-8 md:gap-12 w-full px-5 md:px-20 py-10 md:py-20 bg-primary-bg">
    <!-- Header -->
    <div class="flex flex-col items-center gap-4 w-full">
      <div class="bg-white rounded-full px-4 py-[6px]">
        <span class="text-primary text-[13px] font-semibold">Как это работает</span>
      </div>
      <h2
        class="text-[26px] md:text-[36px] font-bold text-text-primary text-center leading-[1.2]"
        style="font-family: 'DM Sans', sans-serif"
      >
        Как работает HabitBoost
      </h2>
      <p
        class="text-text-secondary text-[14px] md:text-[17px] leading-[1.5] text-center"
        style="max-width: 550px"
      >
        Три простых шага, чтобы изменить свой распорядок дня и сформировать привычки, которые останутся.
      </p>
    </div>

    <!-- Steps -->
    <div class="flex flex-col md:flex-row gap-4 md:gap-8 w-full">
      <div
        v-for="step in steps"
        :key="step.num"
        class="flex flex-col items-center gap-4 md:gap-5 flex-1 p-8 md:p-10 rounded-[20px] bg-white border border-border"
      >
        <span
          class="text-[32px] md:text-[40px] font-extrabold"
          :style="{ color: step.numColor, fontFamily: '\'DM Sans\', sans-serif' }"
        >{{ step.num }}</span>

        <div
          class="w-14 h-14 md:w-16 md:h-16 flex items-center justify-center rounded-2xl flex-shrink-0"
          :style="{ backgroundColor: step.iconBg }"
        >
          <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path :d="step.iconPath" />
          </svg>
        </div>

        <h3
          class="text-[17px] md:text-[20px] font-bold text-text-primary text-center"
          style="font-family: 'DM Sans', sans-serif"
        >{{ step.title }}</h3>
        <p class="text-text-secondary text-[14px] leading-[1.5] text-center w-full">{{ step.desc }}</p>
      </div>
    </div>
  </section>
</template>
