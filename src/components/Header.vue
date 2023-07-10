<script setup></script>

<template>
  <header class="header">
    <div class="container">
      <div>
        <img class="logo" src="../assets/logo.png" alt="" />
      </div>
      <div class="row">
        <div class="texts">
          <h1>UMMON</h1>
          <h3>toza ichimlik suvi</h3>
        </div>
        <img class="bottle" src="../assets/water-bottle-500x500.webp" alt="" />
      </div>
    </div>
  </header>
  <svg viewBox="0 0 500 60" class="wave">
    <path
      d="M 0 30 C 150 100 280 0 500 20 L 500 0 L 0 0"
      fill="rgb(26,118,166)"
    ></path>
    <path
      d="M 0 25 C 145 100 275 0 500 20 L 500 0 L 0 0"
      fill="rgb(26,26,26)"
    ></path>
  </svg>
</template>

<style scoped>
@import url("../assets/main.css");
h1 {
  font-size: 90px;
  background: -webkit-linear-gradient(
    var(--primary),
    var(--secondary),
    var(--third)
  );
  -webkit-background-clip: text;
  background-clip: text;
  -webkit-text-fill-color: transparent;
}

h3 {
  font-weight: 400;
  font-size: 1rem;
}

.wave {
  position: relative;
  top: -10px;
}

.texts {
  margin: 0 40px;
}

.header {
  text-align: center;
  padding-top: 40px;
  background: var(--black);
}

.logo {
  margin-bottom: -50px;
}

.row {
  display: flex;
  justify-content: center;
  align-items: center;
}

.bottle {
  width: 450px;
  animation: animWin 3000ms linear infinite;
  z-index: 2;
}

@keyframes animWin {
  from {
    transform: rotate(10deg) translateY(130px);
  }
  50% {
    transform: rotate(10deg) translateY(110px);
  }
  to {
    transform: rotate(10deg) translateY(130px);
  }
}

@keyframes animTable {
  from {
    transform: rotate(10deg) translateY(90px);
  }
  50% {
    transform: rotate(10deg) translateY(75px);
  }
  to {
    transform: rotate(10deg) translateY(90px);
  }
}

@keyframes animLarge {
  from {
    transform: rotate(10deg) translateY(155px);
  }
  50% {
    transform: rotate(10deg) translateY(135px);
  }
  to {
    transform: rotate(10deg) translateY(155px);
  }
}

@media (min-width: 1400px) {
  .bottle {
    animation: animLarge 3000ms linear infinite;
  }
}

@media (max-width: 1150px) {
  .texts {
    margin: 0 20px;
  }

  h1 {
    font-size: 70px;
  }
  .bottle {
    width: 350px;
    animation: animTable 3000ms linear infinite;
  }
}

@media (max-width: 600px) {
  .texts {
    margin: 0;
    margin-bottom: 40px;
  }

  h1 {
    font-size: 50px;
  }
  .logo {
    width: 70px;
    margin-bottom: 20px;
  }
  .row {
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  .bottle {
    /* width: 250px;
    animation: animPhone 3000ms linear infinite; */
    display: none;
  }
}
</style>
