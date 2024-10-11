<template>
  <div>
    <!-- Navaigation bar component -->
    <div class="sticky-element"><Navbar /></div>
    <div class="container">
      <!-- hero section -->
      <div>
        <Hero />
      </div>
      <!-- info section -->
      <div>
        <Info />
      </div>
      <!-- Asset section -->
      <div>
        <Asset />
      </div>
      <!-- Savings Community -->
      <div>
        <Savings />
      </div>
      <!-- Join Community -->
      <div>
        <Join />
      </div>
      <!-- Download App -->
      <div>
        <Download />
      </div>
      <!-- Footer section -->
      <div>
        <Footer />
      </div>
    </div>
  </div>
</template>

<script setup>
import Navbar from "../components/navigation/navbar.vue";
import Hero from "../components/homepage/hero.vue";
import Info from "../components/homepage/info.vue";
import Asset from "../components/homepage/asset_classes.vue";
import Footer from "../components/homepage/footer.vue";
import Download from "../components/homepage/download_app.vue";
import Join from "../components/homepage/joinCommunity.vue";
import Savings from "../components/homepage/saving.vue";
</script>

<style scoped>
.sticky-element {
  position: sticky; /* Sticky positioning */
  top: 0; /* Sticks to the top of the viewport */
  z-index: 50; /* Higher stacking context */
  background-color: white; /* Background color white */
}
</style>
