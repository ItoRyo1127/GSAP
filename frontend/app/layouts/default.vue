<template>
  <div>
    <header>animation</header>
    <div class="container">
      <slot />
    </div>
    <footer>footer area</footer>
  </div>
</template>

<style scoped>
header {
  border-bottom-style: solid;
  padding: 1rem;
}
footer {
  margin-top: 2rem;
  background-color: #000;
  padding: 1rem;
  color: #fff;
}
.container {
  margin: 2rem;
}
</style>
