<template>
  <div>
    <div style="margin-top: 8rem; margin-bottom: 3rem">
      <div class="grid-footer">
        <div class="display_flex justify_center">
          <div>
            <div>
              <img src="@/assets/icon/black_Logo.svg" alt="rise logo" />
            </div>
            <div
              class="hover_animation"
              v-for="(item, index) in FooterData.first"
              :key="index"
              style="padding: 0.9rem 0"
            >
              <span
                :aria-label="`visit our ${item.name} page`"
                class="nav_buttons"
                >{{ item.name }}</span
              >
            </div>
          </div>
        </div>
        <!-- explore -->
        <div class="display_flex justify_center">
          <div class="">
            <div class="TG_font">
              <span>Explore</span>
            </div>
            <div
              class="hover_animation"
              v-for="(item, index) in FooterData.Explore"
              :key="index"
              style="padding: 0.9rem 0"
            >
              <div
                :aria-label="`visit our ${item.name} page`"
                class="display_flex"
              >
                <div>
                  <span class="nav_buttons">{{ item.name }}</span>
                </div>
                <div>
                  <img
                    src="@/assets/icon/slant_arrow.svg"
                    alt="slant arrow icon"
                  />
                </div>
              </div>
            </div>
          </div>
        </div>
        <!-- products -->
        <div class="display_flex justify_center">
          <div class="">
            <div class="TG_font">
              <span>Products</span>
            </div>
            <div
              class="hover_animation"
              v-for="(item, index) in FooterData.Products"
              :key="index"
              style="padding: 0.9rem 0"
            >
              <span
                :aria-label="`Explore our ${item.name}`"
                class="nav_buttons"
                >{{ item.name }}</span
              >
            </div>
          </div>
        </div>
        <!-- contact us -->
        <div class="display_flex justify_center">
          <div class="">
            <div class="TG_font">
              <span>Contact Us</span>
            </div>
            <div
              class="hover_animation"
              v-for="(item, index) in FooterData.Contact_Us"
              :key="index"
              style="padding: 0.9rem 0"
            >
              <div
                :aria-label="`contact us with ${item.name} `"
                class="display_flex nav_buttons"
              >
                <div>
                  <span class="">{{ item.name }}</span>
                </div>
                <div>
                  <img
                    src="@/assets/icon/slant_arrow.svg"
                    alt="slant arrow icon"
                  />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import FooterData from "@/json/footer.json";
</script>

<style scoped>
.justify_center {
  justify-content: center;
}

.nav_buttons {
  /* font-weight: 900; */
  transition: 0.3s ease;
  cursor: pointer;
}

.hover_animation:hover .nav_buttons {
  color: #07969e;
  font-weight: 700 !important;
  cursor: pointer;
}
</style>
