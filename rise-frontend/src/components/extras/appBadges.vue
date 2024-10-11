<template>
  <div class="">
    <div class="display_flex mob_justify_center gap">
      <!-- apple -->
      <div class="button_style hover_animation">
        <img
          src="@/assets/icon/applebadge.svg"
          style="width: 100%"
          alt="download from apple store"
          class=""
        />
      </div>
      <!-- google -->
      <div class="button_style hover_animation">
        <img
          src="@/assets/icon/playstoreBadge.svg"
          style="width: 100%"
          alt="download from playstore"
          class=""
        />
      </div>
      <div></div>
    </div>
  </div>
</template>
<script setup></script>
<style setup>
@media (max-width: 640px) {
  .width_style {
    text-align: center !important;
    width: 100% !important;
  }
  .gap {
    gap: 0.5rem !important;
  }
  .mob_justify_center {
    justify-content: center !important;
  }
}
.hover_animation:hover {
  transform: scale(1.05); /* Slightly enlarges the button */
}
.button_style {
  cursor: pointer;
  transition: transform 0.3s ease, background-color 0.3s ease;
}
</style>
