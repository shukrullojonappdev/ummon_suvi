<script setup></script>

<template>
  <main class="main">
    <div class="container">
      <div class="column">
        <div class="row">
          <img src="../assets/water-filter.png" alt="" />
          <p>Zamonaviy filter</p>
        </div>
        <div class="row">
          <img src="../assets/minerals.png" alt="" />
          <p>Minerallarga boy</p>
        </div>
        <div class="row">
          <img src="../assets/healthcare.png" alt="" />
          <p>Sog'lik uchun foydali</p>
        </div>
        <div class="row">
          <img src="../assets/save-money.png" alt="" />
          <p>Arzon narx</p>
        </div>
      </div>
    </div>
  </main>
</template>

<style scoped>
@import url("../assets/main.css");
.row {
  display: flex;
  padding: 20px 0px;
  align-items: center;
}

.main {
  margin: 40px 0;
  font-size: 1.5rem;
  font-weight: 600;
}

img {
  position: relative;
  width: 50px;
  margin-right: 10px;
}

img:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-image: linear-gradient(to bottom, var(--primary) var(--secondary));
  z-index: 1;
}

.container {
  display: flex;
  justify-content: center;
  align-items: center;
}

@media (max-width: 430px) {
  .row {
    flex-direction: column;
    text-align: center;
    font-size: 1.3rem;
  }

  img {
    width: 40px;
    margin-bottom: 10px;
  }
}
</style>
