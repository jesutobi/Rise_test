<template>
  <div>
    <div
      v-for="(item, index) in InfoData"
      :key="index"
      class="grid grid_margin"
    >
      <!-- grid 1 -->
      <!-- information text -->
      <div :class="item.content.order" class="width_style mob_first_order">
        <div class="txt_style">
          <div>
            <div class="TG_font">
              <span class="fs-550 mob_title_size">{{
                item.content.title
              }}</span>
            </div>
            <div class="spacing fs-400">
              <span>{{ item.content.text }}</span>
            </div>
            <!-- button -->
            <div
              aria-label="start investing button"
              class="c_teal display_flex hover_animation"
              style="padding: 1rem 0rem; font-size: 0.1rem1"
            >
              <div>
                <span>Start Investing</span>
              </div>
              <div class="arrow_container" style="padding: 0rem 1rem">
                <img
                  src="@/assets/icon/right-arrow.svg"
                  alt=" right arrow icon"
                />
              </div>
            </div>
          </div>
        </div>
      </div>
      <!-- grid 2 -->
      <div
        :class="item.img.order"
        class="mob_second_order display_flex justify_content_center"
      >
        <img :src="`/${item.img.src}`" class="img_width" alt="" />
      </div>
    </div>
  </div>
</template>

<script setup>
import InfoData from "@/json/info.json";
</script>

<style scoped>
.width_style {
  width: 70% !important;
  height: 40vh !important;
  margin: auto auto 0rem auto !important;
}

.txt_style {
  display: flex !important;
  justify-content: center !important;
}

.hover_animation {
  cursor: pointer;
}
.hover_animation:hover .arrow_container {
  transform: translateX(10px);
  transition: transform 0.3s ease;
}

.arrow_container {
  transition: transform 0.3s ease;
}

@media (min-width: 640px) {
  .first_order {
    order: 2;
  }

  /* Second order grid item */
  .second_order {
    order: 1;
  }
}
@media (min-width: 640px) {
  .img_width {
    width: 80%;
    animation: bounce1 8s ease-in-out infinite;
  }
}
@media (max-width: 768px) {
  .mob_first_order {
    order: 2 !important;
  }

  /* Second order grid item */
  .mob_second_order {
    order: 1 !important;
  }
  .img_width {
    width: 100%;
    animation: bounce1 8s ease-in-out infinite;
  }
  .fs-400 {
    font-size: 1rem !important;
  }
  .width_style {
    width: 100% !important;
    height: unset !important;
  }
  .hover_animation {
    justify-content: center;
  }
  /* mobile title */
  .mob_title_size {
    font-size: 1.2rem !important;
  }
}
/* Keyframes for bouncing animation */
@keyframes bounce1 {
  0%,
  100% {
    transform: translateY(0) translateX(0);
  }
  50% {
    transform: translateY(-20px) translateX(20px);
  }
}
</style>
