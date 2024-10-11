<template>
  <div>
    <div class="grid grid_margin">
      <div class="relative">
        <!-- grid 1 -->
        <div class="display_flex justify_content_center second_order">
          <img
            src="@/assets/images/Phonesav.svg"
            class="img_width"
            alt="phone"
          />
        </div>
        <div
          class="display_flex justify_content_center second_order Buildcard_position"
        >
          <img
            src="@/assets/images/Buildcard.svg"
            class="buildimg_width bounce"
            alt="phone"
          />
        </div>
      </div>
      <!-- grid 2 -->
      <div class="width_style first_order">
        <div>
          <div class="spacing fs-400">
            <span class="">The Rise App </span>
          </div>
          <div class="TG_font fs-570 mob_title_size">
            <span>Save for your <span class="c_Indigo">future</span></span>
          </div>
          <div class="spacing fs-400">
            <span class=""
              >With Rise, you achieve your financial goals faster. Save for
              school, your home, vacations, your children’s future and more.
            </span>
          </div>
          <div>
            <button
              class="bg_teal c_white button_style hover_animation"
              aria-label="button to Start Saving"
            >
              <span>Start Saving</span>
            </button>
          </div>
        </div>
      </div>
    </div>
    <!-- how we are regulated -->
    <div class="gradient-background diplay_flex justify_content_center">
      <div class="title_style">
        <div class="TG_font fs-570 mob_title_size">
          <span>How we are Regulated</span>
        </div>
        <div class="spacing fs-400">
          <span
            >Rise is registered and regulated both in the US and in Nigeria. Our
            team is made up of US registered investment advisers, our Nigerian
            users are covered by our SEC licensed trustees, ARM Trustees and all
            our assets are held with regulated third parties, in all relevant
            jurisdictions</span
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script setup></script>

<style scoped>
.title_style {
  text-align: center;
  width: 50%;
  margin: 0 auto;
  background: radial-gradient(circle at 50% 50%, #ffffff, transparent 150%);
  padding: 5rem 0rem;
}
.gradient-background {
  background: radial-gradient(circle at 20% 20%, #fff4f0, transparent 60%),
    radial-gradient(circle at 80% 30%, #f8deef, transparent 60%),
    radial-gradient(circle at 30% 70%, #e5ddf9, transparent 60%),
    radial-gradient(circle at 70% 80%, #daf5f5, transparent 60%);

  width: 100%;
  /* padding: 1rem 0rem; */
}
@keyframes bounce {
  0%,
  20%,
  50%,
  80%,
  100% {
    transform: translateY(0);
  }
  40% {
    transform: translateY(-30px);
  }
  60% {
    transform: translateY(-15px);
  }
}

.bounce {
  animation: bounce 7s infinite;
}
.Buildcard_position {
  position: absolute;
  top: 0;
  bottom: 0;
}
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

@media (min-width: 768px) {
  .img_width {
    width: 80%;
    /* height: 90%; */
  }
  .buildimg_width {
    width: 80%;
    /* height: 90%; */
  }
  .grid_margin {
    margin: 5rem 0rem !important;
  }
}
@media (min-width: 1024px) {
  .img_width {
    width: 55%;
    /* height: 90%; */
  }
  .buildimg_width {
    width: 60%;
    /* height: 90%; */
  }
}
@media (max-width: 768px) {
  .title_style {
    text-align: center;
    width: 100%;
    background: radial-gradient(circle at 50% 50%, #ffffff, transparent 150%);
    padding: 5rem 1rem;
  }
  /* mobile title */
  .mob_title_size {
    font-size: 1.2rem !important;
  }
  .fs-400 {
    font-size: 1rem !important;
  }
  .grid_margin {
    display: none;
  }
}
</style>
