<template>
  <div class="">
    <div class="display_flex mob_justify_center gap">
      <!-- apple -->
      <div>
        <img
          src="@/assets/icon/applebadge.svg"
          style="width: 100%"
          alt="download from apple store"
        />
      </div>
      <!-- google -->
      <div>
        <img
          src="@/assets/icon/playstoreBadge.svg"
          style="width: 100%"
          alt="download from playstore"
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
</style>
