<template>
  <div>
    <header>
      <nav class="nav">
        <a href="/">TOP</a>
        <a href="/sample1">sample1</a>
      </nav>
    </header>
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
nav a {
  margin: 0 30px;
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
