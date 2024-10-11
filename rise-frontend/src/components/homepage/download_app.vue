<template>
  <div>
    <div class="grid grid_margin bg_lightTeal card_style">
      <!-- grid 1 -->
      <div class="width_style">
        <div>
          <div class="spacing fs-40 c_teal">
            <span>Download The Rise App.</span>
          </div>
          <div class="TG_font fs-570 mob_title_size">
            <span>Join our 1 users investing and setting long term goals!</span>
          </div>
          <div class="spacing fs-40 c_grey">
            <span>Dollar investments that help you grow.</span>
          </div>
          <!-- app store badges -->
          <div class="">
            <AppBadges />
          </div>
        </div>
      </div>
      <!-- grid 2 -->
      <div class="display_flex justify_content_center mobile_phone_sapcing">
        <img
          src="@/assets/images/Phone2.svg"
          class="img_width"
          alt="mobile phone that shows the app interface"
        />
      </div>
    </div>
  </div>
</template>

<script setup>
import AppBadges from "@/components/extras/appBadges.vue";
</script>

<style scoped>
.width_style {
  width: 100% !important;
  margin: 2rem !important;
  height: auto;
}
.spacing {
  padding: 1rem 0rem 1.5rem 0rem !important;
}

.grid_margin {
  margin-top: 2rem !important;
}
.gap {
  gap: 1rem !important;
}

/* @media (min-width: 768px) { */
.img_width {
  /* width: 100%; */
  height: auto;
  object-fit: contain !important;
  object-position: top;
}
.card_style {
  height: auto;
  padding: 1rem 1rem 0 1rem;
  border-radius: 2.5rem !important;
  box-shadow: 0 4px 6px -1px rgba(141, 141, 141, 0.1),
    0 2px 4px -1px rgba(118, 118, 118, 0.06);
}
/* } */
@media (max-width: 768px) {
  .grid_margin {
    margin-top: 1rem !important;
  }
  .img_width {
    width: 100%;
    height: auto;
    object-fit: cover !important;
    object-position: top;
    /* overflow: hidden !important; */
  }
  .card_style {
    height: 500px;
    padding: 1rem 1rem 0 1rem;
    border-radius: 2.5rem !important;
    box-shadow: 0 4px 6px -1px rgba(141, 141, 141, 0.1),
      0 2px 4px -1px rgba(118, 118, 118, 0.06);
  }

  .mob_display_flex {
    display: flex !important;
    /* align-items: center !important; */
  }
  /* mobile title */
  .mob_title_size {
    font-size: 1.2rem !important;
  }
  .fs-400 {
    font-size: 1rem !important;
  }
  .width_style {
    display: block !important;
    width: 100% !important;
    margin: unset !important;
    height: unset;
  }
  .spacing {
    padding: 0.8rem !important;
  }

  .mobile_phone_sapcing {
    padding: 1rem 0 0 0 !important;
    overflow: hidden !important;
  }
}
</style>
