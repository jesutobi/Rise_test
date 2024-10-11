<template>
  <div>
    <div class="bg_white">
      <div class="container">
        <div class="nav_display nav_spacing">
          <!-- logo -->
          <div aria-label="click to visit home page">
            <img src="../../assets/icon/logo.svg" alt="rise logo" />
          </div>
          <!-- nav buttons -->
          <div class="nav_display TG_reg_font nav_buttons_display">
            <div
              v-for="(items, index) in NavButtons"
              :key="index"
              class="nav_display navbuttons_spacing c_teal"
            >
              <div
                :class="{ active_button: $route.path === items.link }"
                class="hover_animation"
              >
                <div class="display_flex">
                  <div>
                    <span class="nav_buttons">{{ items.text }}</span>
                  </div>
                  <div v-if="items.text === 'Products'">
                    <img src="@/assets/icon/down-arrow.svg" alt="" />
                  </div>
                </div>
                <!-- dot -->
                <div class="display_flex justify_content_center">
                  <img
                    src="@/assets/icon/Ellipse.svg"
                    alt="dot displayed on hover of buttons"
                    class="dot"
                  />
                </div>
              </div>
            </div>
          </div>
          <!-- menu -->
          <div
            aria-label="click to open mobile menu"
            @click="open_menu"
            class="menu_button_display"
          >
            <img src="@/assets/icon/menu.svg" alt="" />
          </div>
        </div>
      </div>
      <!-- mobile menu -->
      <div
        v-if="mobile_menu"
        class="bg_white mobile_menu_position"
        style="padding: 1rem 2rem"
      >
        <div style="padding: 2rem 0rem" class="close_flex">
          <!-- logo -->
          <div aria-label="click to visit home page">
            <img src="../../assets/icon/logo.svg" alt="rise logo" />
          </div>
          <div aria-label="click to close mobile menu" @click="close_menu">
            <img src="@/assets/icon/cancel.svg" alt=" cancel icon " />
          </div>
        </div>
        <div
          style="padding: 1rem 0rem"
          v-for="(items, index) in NavButtons"
          :key="index"
          class="c_teal"
        >
          <div
            :class="{ active_button: $route.path === items.link }"
            class="hover_animation display_flex"
          >
            <div
              :aria-label="`click to go visit ${items.text} page`"
              class="display_flex"
            >
              <div>
                <span class="nav_buttons">{{ items.text }}</span>
              </div>
              <div v-if="items.text === 'Products'">
                <img
                  src="@/assets/icon/down-arrow.svg"
                  alt="down arrow for products button"
                />
              </div>
            </div>
            <!-- dot -->
            <div class=" " style="padding: 0rem 0.8rem">
              <img
                src="@/assets/icon/Ellipse.svg"
                alt="dot displayed on hover of buttons"
                class="dot"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import NavButtons from "@/json/navButtons.json";
import { ref } from "vue";
import { useRouter } from "vue-router";

const router = useRouter();
const mobile_menu = ref(false);

const open_menu = () => {
  mobile_menu.value = true;
};
const close_menu = () => {
  mobile_menu.value = false;
};
</script>

<style scoped>
.mobile_menu_position {
  position: fixed !important;
  width: 100%;
  height: 100%;
  z-index: 999;
  top: 0rem;
  padding: 1rem 0rem;
}
/* display products icon */
.display_products_arrow {
  display: block !important;
}
.nav_display {
  display: flex !important;
  justify-content: space-between;
  align-items: center;
}
.nav_spacing {
  padding: 2rem 0rem;
}
.navbuttons_spacing {
  padding: 0rem 1rem;
}

.dot {
  opacity: 0;
  transition: opacity 0.3s ease;
}
.nav_buttons {
  /* font-weight: 900; */
  transition: 0.3s ease;
  cursor: pointer;
}

.hover_animation:hover .dot {
  opacity: 1; /* Show dot on hover */
  cursor: pointer;
}
.hover_animation:hover .nav_buttons {
  font-weight: 700 !important;
  cursor: pointer;
}
.active_button .dot {
  font-weight: 700 !important;
  opacity: 1;
}
@media (min-width: 992px) {
  .menu_button_display {
    display: none !important;
  }
}
@media (max-width: 992px) {
  .nav_buttons_display {
    display: none !important;
  }
  .close_flex {
    display: flex !important;
    justify-content: space-between;
  }
}
</style>
