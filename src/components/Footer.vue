<script setup></script>

<template>
  <svg viewBox="0 0 500 60" class="wave">
    <path
      d="M 0 30 C 150 100 280 0 500 20 L 500 0 L 0 0"
      fill="rgb(78, 79, 235)"
    ></path>
  </svg>
  <footer class="footer">
    <div class="container">footer</div>
  </footer>
</template>

<style scoped>
@import url("../assets/main.css");

.footer {
  background: var(--primary);
}
.wave {
  position: relative;
  top: 5px;
  transform: scale(-1, -1);
}
</style>
