<script lang="ts" setup>
import { gsap } from "gsap";
import { onMounted } from "vue";

onMounted(() => {
  gsap.defaults({
    repeat: -1, // 無限に繰り返し
    repeatDelay: 5, // 繰り返し時に0.5秒の待機,
    ease: "power4.inOut",
  });

  gsap.to(".example-x .rect", {
    x: 40,
    duration: 2,
  });

  gsap.to(".example-y .rect", {
    y: 40,
    delay: 1,
    duration: 2,
  });

  gsap.to(".example-rotate .rect", {
    rotate: 360,
    delay: 2,
    duration: 2,
  });

  gsap.to(".example-scale .rect", {
    scale: 0.5,
    delay: 3,
    duration: 2,
  });

  gsap.to(".example-skewX .rect", {
    skewX: 30,
    delay: 4,
    duration: 2,
  });

  gsap.to(".example-complex .rect", {
    x: 100,
    rotate: 360,
    scale: 0.5,
    delay: 5,
    duration: 2,
  });

  gsap.to(".example-origin .rect", {
    rotate: 360,
    transformOrigin: "bottom right",
    delay: 6,
    duration: 2,
  });
});
</script>

<template>
  <div class="wrap">
    <div class="container">
      <div class="example-x">
        <h1>x</h1>
        <div class="rect"></div>
      </div>

      <div class="example-y">
        <h1>y</h1>
        <div class="rect"></div>
      </div>

      <div class="example-rotate">
        <h1>rotate</h1>
        <div class="rect"></div>
      </div>

      <div class="example-scale">
        <h1>scale</h1>
        <div class="rect"></div>
      </div>

      <div class="example-skewX">
        <h1>skewX</h1>
        <div class="rect"></div>
      </div>

      <div class="example-complex">
        <h1>x & scale & rotate</h1>
        <div class="rect"></div>
      </div>

      <div class="example-origin">
        <h1>transformOrigin</h1>
        <div class="rect"></div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(128px, 1fr));
  gap: 32px 16px;
  margin: 32px;
}

.rect {
  width: 10vw;
  height: 10vw;
  display: block;
  background: #000;
  position: relative;
}

.wrap {
  display: flex;
  flex-direction: column;
}
.nav {
  display: block;
}
</style>
