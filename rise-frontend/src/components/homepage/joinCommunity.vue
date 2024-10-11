<template>
  <div>
    <div class="grid grid_margin">
      <!-- grid 1 -->
      <div class="width_style first_order">
        <div>
          <div class="TG_font fs-570 mob_title_size">
            <span>Join The Rise Community</span>
          </div>
          <div class="spacing fs-400">
            <span>If you want to go far, go together.</span>
            <span class="display_none_mobile"
              >Our Telegram community surrounds you with others who can help you
              along your financial journey with tips, support, advice and
              learning. It's completely free and open to new and seasoned
              investors.</span
            >
          </div>
          <div>
            <button
              class="bg_teal2 button_style hover_animation"
              aria-label="Join rise community"
            >
              <span>Join our Community</span>
            </button>
          </div>
        </div>
      </div>
      <!-- grid 2 -->
      <div class="display_flex justify_content_center second_order">
        <img
          src="/join.svg"
          class="img_width"
          alt="image that shows various various people in the community"
        />
      </div>
    </div>
  </div>
</template>

<script setup></script>

<style scoped>
.width_style {
  display: grid !important;
  width: 90% !important;
  height: 35vh;
  align-self: center;
  margin: 0rem auto;
}
.spacing {
  padding: 1rem 0rem 1.5rem 0rem !important;
}

.grid_margin {
  margin-top: 8rem !important;
}

.button_style {
  padding: 1rem 1.3rem !important;
  border-radius: 0.4rem;

  cursor: pointer;
  transition: transform 0.3s ease, background-color 0.3s ease;
}
.hover_animation:hover {
  transform: scale(1.05); /* Slightly enlarges the button */
  background-color: #006666; /* Darker teal on hover */
}

.img_width {
  width: 80%;
  height: 90%;
}
@media (min-width: 640px) {
  .grid_margin {
    margin-top: 4rem !important;
  }
}
@media (max-width: 640px) {
  .grid_margin {
    margin-top: 4rem !important;
  }
  .first_order {
    order: 2 !important;
  }

  /* Second order grid item */
  .second_order {
    order: 1 !important;
  }
  /* mobile title */
  .mob_title_size {
    font-size: 1.2rem !important;
  }
  .fs-400 {
    font-size: 1rem !important;
  }
  .width_style {
    width: 100% !important;
    height: auto;
    margin: 2rem 0rem;
  }
  .display_none_mobile {
    display: none;
  }
  .spacing {
    padding: 1rem 0rem !important;
  }
  .img_width {
    width: 0% !important;
  }
}
</style>
