<script setup></script>

<template>
  <svg viewBox="0 0 500 60" class="wave">
    <path
      d="M 0 30 C 150 100 280 0 500 20 L 500 0 L 0 10"
      fill="rgb(26,118,166)"
    ></path>
    <path
      d="M 0 25 C 145 100 275 0 500 20 L 500 0 L 0 0"
      fill="rgb(26,26,26)"
    ></path>
  </svg>
  <div class="order">
    <div class="container">
      <div class="form-group">
        <form class="form" action="">
          <label for="address">Manzil</label>
          <input id="address" type="text" />
          <label for="phone">Tel raqam</label>
          <input id="phone" type="phone" />
          <label for="count">Soni</label>
          <input id="count" type="number" />
          <button>Buyurtma qilish</button>
        </form>
      </div>
    </div>
  </div>
  <svg viewBox="0 0 500 60">
    <path
      d="M 0 30 C 150 100 280 0 500 20 L 500 0 L 0 0"
      fill="rgb(26,118,166)"
    ></path>
    <path
      d="M 0 25 C 145 100 275 0 500 20 L 500 0 L 0 0"
      fill="rgb(26,26,26)"
    ></path>
  </svg>
  <footer>
    <div class="container footer">
      <div>
        <div class="contact">
          <img src="../assets/phone-call.png" alt="" class="icon" />
          <span>+998934371770</span>
        </div>
        <div class="contact">
          <img src="../assets/telegram.png" alt="" class="icon" />
          <span>@ilhom</span>
        </div>
      </div>
    </div>
  </footer>
</template>

<style scoped>
@import url("../assets/main.css");

.order {
  background: var(--black);
}
.wave {
  position: relative;
  top: 5px;
  transform: scale(-1, -1);
}
.form {
  font-size: 1rem;
  width: 100%;
  display: flex;
  flex-direction: column;
}

.form-group {
  padding: 40px 0;
  max-width: 500px;
  width: 500px;
}

input {
  border-radius: 5px;
  padding: 5px;
  margin: 10px 0;
  outline: none;
}

label {
  margin-top: 5px;
  color: var(--white);
  font-weight: 300;
}

.contact {
  margin-bottom: 10px;
  display: flex;
  align-items: center;
}

input:focus {
  box-shadow: 0px 1px 5px var(--third), 0px 1px 10px var(--secondary),
    0px 1px 15px var(--primary);
}

span {
  font-size: 1rem;
  font-weight: 400;
}

.icon {
  width: 25px;
  margin-right: 5px;
}

button {
  border: 0;
  padding: 5px;
  border-radius: 5px;
  margin-top: 20px;
  background: linear-gradient(
    to bottom,
    var(--primary),
    var(--secondary),
    var(--third)
  );
  font-size: 1rem;
  color: var(--white);
  font-weight: 400;
}

.container {
  display: flex;
  justify-content: center;
}

footer {
  margin: 40px 0;
}
</style>
