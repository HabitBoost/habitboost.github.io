<script setup lang="ts">
const steps = [
  {
    num: '01',
    numColor: '#FF6B6B',
    title: 'Выберите привычки',
    desc: 'Выберите из каталога готовых привычек или создайте свои собственные по категориям',
    image: '/images/sqeZQ.png',
  },
  {
    num: '02',
    numColor: '#22C55E',
    title: 'Отмечайте прогресс',
    desc: 'Ежедневно отмечайте выполненные привычки и наблюдайте за своей серией',
    image: '/images/EegEJ.png',
  },
  {
    num: '03',
    numColor: '#6366F1',
    title: 'Достигайте целей',
    desc: 'Анализируйте статистику, получайте награды и становитесь лучше каждый день',
    image: '/images/EFnvg.png',
  },
]
</script>

<template>
  <section id="how-it-works" class="flex flex-col items-center gap-8 md:gap-16 w-full px-5 md:px-20 py-12 md:py-20 bg-white">
    <!-- Header -->
    <div class="flex flex-col items-center gap-3 w-full">
      <h2
        class="text-[28px] md:text-[36px] font-bold text-text-primary text-center"
        style="font-family: 'Bricolage Grotesque', sans-serif"
      >
        Как это работает
      </h2>
      <p class="text-text-secondary text-base md:text-lg text-center">
        Три простых шага к лучшей жизни
      </p>
    </div>

    <!-- Steps -->
    <div class="flex flex-col md:flex-row gap-6 md:gap-8 w-full">
      <div
        v-for="step in steps"
        :key="step.num"
        class="flex flex-col items-center gap-4 md:gap-5 flex-1 p-7 md:p-10 rounded-2xl md:rounded-[20px] bg-bg-card"
      >
        <span
          class="text-[48px] md:text-[64px] font-extrabold opacity-20"
          :style="{ color: step.numColor, fontFamily: 'Bricolage Grotesque, sans-serif' }"
        >{{ step.num }}</span>

        <h3 class="text-lg md:text-xl font-bold text-text-primary text-center">{{ step.title }}</h3>
        <p class="text-text-secondary text-[13px] md:text-sm leading-[1.5] text-center w-full">{{ step.desc }}</p>

        <div class="w-full h-[140px] md:h-[160px] rounded-xl md:rounded-2xl overflow-hidden bg-border">
          <img
            :src="step.image"
            :alt="step.title"
            class="w-full h-full object-cover"
          />
        </div>
      </div>
    </div>
  </section>
</template>
