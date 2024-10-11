<template>
  <div>
    <!-- header -->
    <div class="text_style" style="padding: 1.5rem 0rem">
      <div class="TG_font fs-570 mob_title_size">
        <span>Asset Classes</span>
      </div>
      <div class="fs-400">
        <span>It’s your money, choose where you invest it</span>
      </div>
    </div>
    <div class="grid-asset">
      <div
        v-for="(item, index) in AssetData"
        :key="index"
        class="text_style relative card_style bg_white"
      >
        <!-- icon -->
        <div
          class="card_icon_design relative"
          :class="{
            bg_lightOrange: item.title === 'Stocks',
            bg_lightIndigo: item.title === 'Real Estate',
            bg_lightTeal: item.title === 'Fixed Income',
          }"
        >
          <div class="icon_position">
            <div class="icon_radius">
              <img
                :src="`/${item.icon}`"
                :alt="`icon that represents ${item.title}`"
              />
            </div>
          </div>
        </div>

        <!-- content -->
        <div style="padding: 3.5rem 1rem">
          <div style="font-size: 1.2rem" class="TG_font">
            <span>{{ item.title }}</span>
          </div>
          <div class="fs-250">
            <span>{{ item.text }}</span>
          </div>
          <!-- Historical returns and risk level -->
          <div style="padding: 1rem 0rem 3rem 0rem">
            <div class="fs-250">
              <span class="c_lightgrey">Historical returns:</span>
              <span> {{ item.Historical_returns }}</span>
            </div>
            <div class="fs-250">
              <span class="c_lightgrey">Risk Level:</span>
              <span> {{ item.Risk_Level }}</span>
            </div>
          </div>
          <!-- footnote -->
          <div class="TG_font c_teal card_footnote_position">
            <div
              :aria-label="`Learn how ${item.title} works`"
              class="display_flex justify_card_footnote"
            >
              <div>
                <span>Learn how {{ item.title }} works</span>
                <span style="padding: 0rem 1rem"
                  ><img src="@/assets/icon/right-arrow.svg" alt="arrow icon"
                /></span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import AssetData from "@/json/assets.json";
</script>

<style scoped>
.text_style {
  text-align: center !important;
}
.card_footnote_position {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
}
.justify_card_footnote {
  justify-content: center;
}

.card_style {
  border: 0.5px solid rgb(225, 225, 225);
  border-radius: 1rem !important;
}

@media (max-width: 640px) {
  /* mobile title */
  .mob_title_size {
    font-size: 1.2rem !important;
  }
  .fs-400 {
    font-size: 1rem !important;
  }
  .card_style {
    margin: 0.8rem 0rem;
  }
}
.card_icon_design {
  border-radius: 1rem 1rem 0 0 !important;
  height: 120px;
}
.icon_position {
  position: absolute;
  bottom: -3.2rem;
  left: 0rem;
  right: 0;
}
.icon_radius {
  background-color: white !important;
  z-index: 99999;
  padding: 1rem !important;
  display: inline-block;
  border-radius: 100%;
}
</style>
