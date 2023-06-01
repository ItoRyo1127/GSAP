<script lang="ts" setup>
import { gsap } from "gsap";
import { onMounted } from "vue";

onMounted(() => {
  gsap
    .timeline({ repeat: -1, repeatDelay: 0.5 })
    .set("h1", { textContent: "Show Motion" })
    .from(".rect1", {
      y: -32,
      opacity: 0,
      duration: 0.5,
      rotate: 360,
      scale: 1.5,
    })
    .from(".rect2", { x: 32, y: 32, opacity: 0, duration: 0.5, scale: 1.5 })
    .from(".rect3", { y: -32, opacity: 0, duration: 0.5, rotate: 360 })
    .from(".rect4", { x: 32, y: 32, opacity: 0, duration: 0.5, scale: 1.5 })
    .from(".rect5", { y: -32, opacity: 0, duration: 0.5, rotate: 360 })
    .from(".rect6", { x: 32, y: 32, opacity: 0, duration: 0.5, scale: 1.5 })
    .set("h1", { textContent: "Hide Motion" }, "+=1") // 1秒待機
    .to(
      ".rect1",
      { y: -32, opacity: 0.5, duration: 0.5, rotate: 360, scale: 100 },
      "+=0.5"
    )
    .to(
      ".rect2",
      { x: 32, y: 32, opacity: 0.5, duration: 0.5, scale: 100 },
      "-=0.4"
    )
    .to(".rect3", { y: -32, opacity: 0.5, duration: 0.5, rotate: 360 }, "-=0.4")
    .to(
      ".rect4",
      { x: 32, y: 32, opacity: 0.5, duration: 0.5, scale: 100 },
      "-=0.4"
    )
    .to(".rect5", { y: -32, opacity: 0.5, duration: 0.5, rotate: 360 }, "-=0.4")
    .to(
      ".rect6",
      { x: 32, y: 32, opacity: 0.5, duration: 0.5, scale: 100 },
      "-=0.4"
    );
});
</script>

<template>
  <div class="container">
    <div class="rect rect1">こ</div>
    <div class="rect rect2">う</div>
    <div class="rect rect3">さ</div>
    <div class="rect rect4">か</div>
    <div class="rect rect5">さ</div>
    <div class="rect rect6">ん</div>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  gap: 32px;
}
.rect {
  font-size: 100px;
  color: #000;
  display: block;
}
</style>
