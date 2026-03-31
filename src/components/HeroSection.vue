<script setup lang="ts"></script>

<template>
  <section class="flex flex-col md:flex-row items-center w-full gap-8 md:gap-16 px-5 md:px-20 py-10 md:py-14 bg-white min-h-[calc(100vh-64px)] md:min-h-[calc(100vh-80px)] justify-center">
    <!-- Left Column -->
    <div class="flex flex-col items-center md:items-start gap-8 flex-1 w-full">
      <h1
        class="text-[32px] md:text-[48px] font-extrabold leading-[1.15] text-center md:text-left text-text-primary"
        style="font-family: 'Bricolage Grotesque', sans-serif"
      >
        Создавай привычки, которые меняют жизнь
      </h1>

      <p class="text-text-secondary text-base md:text-lg leading-[1.5] text-center md:text-left">
        HabitBoost — ваш персональный помощник для формирования полезных привычек. Отслеживайте прогресс, получайте мотивацию и достигайте целей каждый день.
      </p>

      <!-- Buttons -->
      <div class="flex flex-col md:flex-row gap-3 md:gap-4 w-full md:w-auto">
        <a href="#download" class="hover:opacity-85 transition-opacity w-full md:w-auto flex justify-center">
          <img src="/images/badge-appstore.png" alt="Download on the App Store" class="h-[50px]" />
        </a>
        <a href="#download" class="hover:opacity-85 transition-opacity w-full md:w-auto flex justify-center">
          <img src="/images/badge-googleplay.png" alt="Get it on Google Play" class="h-[50px]" />
        </a>
      </div>

      <span class="text-text-tertiary text-sm font-medium text-center md:text-left">
        50,000+ пользователей уже с нами
      </span>
    </div>

    <!-- iPhone Mockup — Desktop only, fits within viewport -->
    <div class="iphone-mockup hidden md:block flex-shrink-0" style="margin-bottom: 60px">
      <!-- Frame -->
      <div class="iphone-frame">
        <!-- Side buttons -->
        <div class="iphone-btn-power"></div>
        <div class="iphone-btn-vol iphone-btn-vol--1"></div>
        <div class="iphone-btn-vol iphone-btn-vol--2"></div>
        <div class="iphone-btn-vol iphone-btn-vol--3"></div>
        <!-- Screen -->
        <div class="iphone-screen">
          <!-- Dynamic Island -->
          <div class="iphone-island"></div>
          <!-- App Screenshot -->
          <img
            src="/images/REkoD.png"
            alt="HabitBoost app"
            class="iphone-app-img"
          />
        </div>
      </div>
    </div>
  </section>

  <!-- iPhone Mockup — Mobile only, below fold (appears on scroll) -->
  <div class="flex md:hidden items-center justify-center px-5 pb-12 bg-white">
    <div class="iphone-frame iphone-frame--sm">
      <div class="iphone-btn-power iphone-btn-power--sm"></div>
      <div class="iphone-btn-vol iphone-btn-vol--sm iphone-btn-vol--sm-1"></div>
      <div class="iphone-btn-vol iphone-btn-vol--sm iphone-btn-vol--sm-2"></div>
      <div class="iphone-btn-vol iphone-btn-vol--sm iphone-btn-vol--sm-3"></div>
      <div class="iphone-screen iphone-screen--sm">
        <div class="iphone-island iphone-island--sm"></div>
        <img src="/images/REkoD.png" alt="HabitBoost app" class="iphone-app-img" />
      </div>
    </div>
  </div>
</template>

<style scoped>
/*
 * Proportions based on devices.css (picturepan2/devices.css)
 * Original: 428×868px, scale ≈ 0.64 for desktop, 0.54 for mobile
 */

/* ── Desktop iPhone ── */
.iphone-mockup {
  display: flex;
  align-items: center;
  justify-content: center;
  height: calc(100vh - 160px);
  max-height: 700px;
  min-height: 500px;
}

.iphone-frame {
  position: relative;
  /* 428 × 0.64 = 274, 868 × 0.64 = 556 */
  width: 274px;
  height: 556px;
  background: #010101;
  border-radius: 44px; /* 68 × 0.64 */
  border: 1px solid #1b1721;
  box-shadow:
    inset 0 0 4px 2px #c0b7cd,
    inset 0 0 0 6px #342c3f,
    0 40px 100px rgba(0, 0, 0, 0.4),
    0 12px 32px rgba(0, 0, 0, 0.25);
  padding: 12px; /* 19 × 0.64 ≈ 12 */
}

/* Power button — right side (100px height × 0.64 ≈ 64, top 200 × 0.64 ≈ 128) */
.iphone-btn-power {
  position: absolute;
  right: -2px;
  top: 128px;
  width: 3px;
  height: 64px;
  background: #342c3f;
  border-radius: 0 2px 2px 0;
}

/* Volume buttons — left side (32px × 0.64 ≈ 20, top 115 × 0.64 ≈ 74) */
.iphone-btn-vol {
  position: absolute;
  left: -2px;
  width: 3px;
  background: #342c3f;
  border-radius: 2px 0 0 2px;
}
.iphone-btn-vol--1 { top: 74px;  height: 20px; } /* Silent */
.iphone-btn-vol--2 { top: 108px; height: 28px; } /* Vol+   */
.iphone-btn-vol--3 { top: 148px; height: 28px; } /* Vol-   */

.iphone-screen {
  position: relative;
  width: 100%;
  height: 100%;
  background: #000;
  border-radius: 32px; /* 49 × 0.64 */
  overflow: hidden;
}

/*
 * Dynamic Island — devices.css: 120×35px, top 29px
 * scaled × 0.64: 77×22px, top 19px
 */
.iphone-island {
  position: absolute;
  top: 10px;
  left: 50%;
  transform: translateX(-50%);
  width: 77px;
  height: 22px;
  background: #000;
  border-radius: 12px;
  z-index: 10;
}

.iphone-app-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 32px;
}

/* ── Mobile iPhone (scale ≈ 0.54) ── */
.iphone-frame--sm {
  width: 231px;  /* 428 × 0.54 */
  height: 469px; /* 868 × 0.54 */
  border-radius: 37px;
  padding: 10px;
}

.iphone-btn-power--sm {
  top: 108px; /* 200 × 0.54 */
  height: 54px;
}

.iphone-btn-vol--sm-1 { top: 62px;  height: 17px; }
.iphone-btn-vol--sm-2 { top: 91px;  height: 24px; }
.iphone-btn-vol--sm-3 { top: 125px; height: 24px; }

.iphone-screen--sm {
  border-radius: 27px;
}
.iphone-screen--sm .iphone-app-img {
  border-radius: 27px;
}

/* Dynamic Island mobile: 120×35 × 0.54 = 65×19 */
.iphone-island--sm {
  top: 8px;
  width: 65px;
  height: 19px;
  border-radius: 10px;
}
</style>
