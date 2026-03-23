<script setup lang="ts">
const stats = [
  { num: '50,000+', label: 'Активных пользователей', color: '#FF6B6B' },
  { num: '2.5M+', label: 'Привычек выполнено', color: '#22C55E' },
  { num: '92%', label: 'Пользователей остаются после 30 дней', color: '#6366F1' },
  { num: '4.8★', label: 'Средняя оценка в App Store', color: '#D97706' },
]

const testimonials = [
  {
    quote: 'HabitBoost полностью изменил мой подход к утренней рутине. За 3 месяца я выработал 5 новых привычек, которые теперь выполняю автоматически. Трекер стриков невероятно мотивирует!',
    avatar: '/images/generated-1774262765377.png',
    name: 'Дмитрий Козлов',
    role: 'Предприниматель',
  },
  {
    quote: 'Функция SOS — это находка! В моменты стресса дыхательные упражнения реально помогают. А дневник рефлексии помог мне лучше понять свои паттерны поведения. Рекомендую всем!',
    avatar: '/images/generated-1774262787426.png',
    name: 'Анна Петрова',
    role: 'Дизайнер',
  },
  {
    quote: 'Пользуюсь уже полгода. Система достижений и бейджей делает процесс формирования привычек настоящей игрой. Мой лучший стрик — 89 дней! Приложение стало частью моей жизни.',
    avatar: '/images/generated-1774262805369.png',
    name: 'Максим Волков',
    role: 'Спортсмен',
  },
]
</script>

<template>
  <!-- Stats Section -->
  <section id="stats" class="flex flex-col items-center gap-8 md:gap-12 w-full px-5 md:px-20 py-12 md:py-20" style="background: linear-gradient(180deg, #FFF5F5 0%, #FFFFFF 100%)">
    <div class="flex flex-col items-center gap-3 w-full">
      <div class="bg-[#FEF2F2] rounded-[20px] px-4 py-[6px]">
        <span class="text-accent-coral text-[13px] font-semibold">Наше сообщество</span>
      </div>
      <h2
        class="text-[28px] md:text-[44px] font-bold text-text-primary text-center"
        style="font-family: 'Bricolage Grotesque', sans-serif"
      >
        Цифры говорят сами за себя
      </h2>
      <p class="text-text-secondary text-sm md:text-lg text-center leading-[1.5]" style="max-width: 600px">
        Присоединяйтесь к сообществу людей, которые меняют свою жизнь каждый день
      </p>
    </div>

    <!-- Stats Grid -->
    <div class="grid grid-cols-2 md:flex md:flex-row gap-4 md:gap-8 w-full">
      <div
        v-for="stat in stats"
        :key="stat.label"
        class="flex flex-col items-center gap-1 md:gap-2 flex-1 px-4 md:px-6 py-6 md:py-10 rounded-[20px] md:rounded-3xl bg-white border border-border-subtle"
      >
        <span
          class="text-[32px] md:text-[48px] font-extrabold tracking-tight"
          :style="{ color: stat.color, fontFamily: 'Bricolage Grotesque, sans-serif' }"
        >{{ stat.num }}</span>
        <span class="text-[12px] md:text-base font-medium text-text-secondary text-center">{{ stat.label }}</span>
      </div>
    </div>
  </section>

  <!-- Testimonials Section -->
  <section id="testimonials" class="flex flex-col items-center gap-8 md:gap-12 w-full px-5 md:px-20 py-12 md:py-20 bg-bg-card">
    <div class="flex flex-col items-center gap-3 w-full">
      <div class="bg-[#F0FDF4] rounded-[20px] px-4 py-[6px]">
        <span class="text-accent-green text-[13px] font-semibold">Отзывы</span>
      </div>
      <h2
        class="text-[28px] md:text-[44px] font-bold text-text-primary text-center"
        style="font-family: 'Bricolage Grotesque', sans-serif"
      >
        Что говорят наши пользователи
      </h2>
      <p class="text-text-secondary text-sm md:text-lg text-center">
        Реальные истории людей, которые изменили свои привычки
      </p>
    </div>

    <!-- Testimonial Cards -->
    <div class="flex flex-col md:flex-row gap-4 md:gap-6 w-full">
      <div
        v-for="t in testimonials"
        :key="t.name"
        class="flex flex-col gap-4 md:gap-5 flex-1 p-6 md:p-8 rounded-[20px] md:rounded-3xl bg-white"
      >
        <span class="text-accent-yellow text-lg md:text-xl font-bold">★★★★★</span>
        <p class="text-text-primary text-sm md:text-base leading-[1.6]">{{ t.quote }}</p>
        <div class="flex items-center gap-3">
          <img
            :src="t.avatar"
            :alt="t.name"
            class="w-10 md:w-12 h-10 md:h-12 rounded-full object-cover flex-shrink-0"
          />
          <div class="flex flex-col gap-0.5">
            <span class="text-[15px] font-semibold text-text-primary">{{ t.name }}</span>
            <span class="text-[13px] text-text-secondary">{{ t.role }}</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
