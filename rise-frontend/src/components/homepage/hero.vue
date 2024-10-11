<template>
  <div class="hero-section">
    <div class="grid grid_margin">
      <!-- grid 1 -->
      <div class="width_style">
        <div>
          <div class="TG_font c_teal">
            <span class="hero_intro_font"
              >Dollar investments that help you grow</span
            >
          </div>
          <div class="spacing fs-400">
            <span
              >We put your money in high quality assets that help you build
              wealth and achieve your financial goals.</span
            >
          </div>
          <!-- app store badges -->
          <div class="">
            <AppBadges />
          </div>
        </div>
      </div>
      <!-- grid 2 -->
      <div class="second_order display_flex justify_content_evenly">
        <!-- phone image -->
        <img src="/Phone.svg" class="img_width" alt="phone image" />
      </div>
    </div>
    <!-- Scatter Circles -->
    <Balls />
    <!-- partners -->
    <div class="display_flex justify_content_center">
      <!-- <div> -->
      <img
        src="/partners.svg"
        alt="supported by ,Arm trustees , western union , techstars , Ventures Platform"
        class="partners_image_size"
      />
      <!-- </div> -->
    </div>
  </div>
</template>

<script setup>
// app badge component
import AppBadges from "@/components/extras/appBadges.vue";
import Balls from "@/components/extras/balls.vue";
</script>

<style scoped>
.width_style {
  display: grid !important;
  width: 100% !important;
  height: 50vh;
  align-self: center;
}
.spacing {
  padding: 1rem 0rem 1.5rem 0rem !important;
}
.first_order {
  order: 2;
}

/* Second order grid item */
.second_order {
  order: 1 !important;
}
.grid_margin {
  margin-top: 2rem !important;
}
.gap {
  gap: 1rem !important;
}
.img_width {
  width: 45%;
  /* height: 90%; */
  object-fit: cover;
}
/* partners_image_size */

.hero-section {
  position: relative;
  overflow: hidden;
}

@media (min-width: 992px) {
  .hero_intro_font {
    font-size: 3.5rem !important;
  }
}
@media (min-width: 640px) {
  .hero_intro_font {
    font-size: 2.8rem !important;
  }
}
@media (max-width: 568px) {
  .partners_image_size {
    width: 100%;
    object-fit: contain !important;
  }
}
@media (max-width: 768px) {
  .img_width {
    width: 45%;
    padding: 2rem 0rem;
    object-fit: cover;
    /* height: auto; */
  }
  .mob_justify_center {
    justify-content: center !important;
  }
  .mob_display_flex {
    display: flex !important;
    /* align-items: center !important; */
  }
  .width_style {
    height: auto;
    width: 100% !important;
  }
  .hero_intro_font {
    font-size: 1.8rem;
  }
  .fs-400 {
    font-size: 1rem !important;
  }
}
</style>
