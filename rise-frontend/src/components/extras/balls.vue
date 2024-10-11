<template>
  <div>
    <div
      class="circle circle1"
      aria-label="ball of circle bouncing in the hero section"
    ></div>
    <div
      class="circle circle2"
      aria-label="ball of circle bouncing in the hero section"
    ></div>
    <div
      class="circle circle3"
      aria-label="ball of circle bouncing in the hero section"
    ></div>
    <div
      class="circle circle4"
      aria-label="ball of circle bouncing in the hero section"
    ></div>
  </div>
</template>

<script setup></script>

<style scoped>
.circle {
  position: absolute;
  border-radius: 50%;
  background-color: #00c4cc; /* Example circle color */
  opacity: 0.2;
  animation: bounce 6s ease-in-out infinite;
}

.circle1 {
  width: 100px;
  height: 100px;
  top: 10%;
  left: 5%;
  animation: bounce1 8s ease-in-out infinite;
}

.circle2 {
  width: 80px;
  height: 80px;
  top: 60%;
  left: 10%;
  animation: bounce2 8s ease-in-out infinite;
}

.circle3 {
  width: 80px;
  height: 80px;
  top: 30%;
  right: 30%;
  animation: bounce3 7s ease-in-out infinite;
}

.circle4 {
  width: 100px;
  height: 100px;
  bottom: 15%;
  right: 5%;
  animation: bounce4 10s ease-in-out infinite;
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

@keyframes bounce2 {
  0%,
  100% {
    transform: translateY(0) translateX(0);
  }
  50% {
    transform: translateY(30px) translateX(-15px);
  }
}
@keyframes bounce3 {
  0%,
  100% {
    transform: translateY(0) translateX(0);
  }
  50% {
    transform: translateY(-25px) translateX(10px);
  }
}

@keyframes bounce4 {
  0%,
  100% {
    transform: translateY(0) translateX(0);
  }
  50% {
    transform: translateY(15px) translateX(-25px);
  }
}
</style>
