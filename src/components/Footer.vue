<script setup>
import { ref } from "vue";
import emailjs from "@emailjs/browser";

const message = ref({
  address: "",
  phone: "",
  count: "",
});

function sendEmail() {
  emailjs
    .sendForm(
      "service_oszettl",
      "template_5nn0riw",
      "#form",
      "gjrezzH7hbpMfMssB"
    )
    .then(
      (result) => {
        alert("Buyurtmangiz qabul qilindi");
      },
      (error) => {
        alert("Buyurtmangiz qabul qilinmadi");
      }
    );
}
</script>

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
        <form class="form" id="form" ref="message">
          <label for="address">Manzil</label>
          <input id="address" type="text" name="address" />
          <label for="phone">Tel raqam</label>
          <input id="phone" type="phone" name="phone" />
          <label for="count">Soni</label>
          <input id="count" type="number" name="count" />
          <button type="button" @click="sendEmail()">Buyurtma qilish</button>
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
          <a href="tel:+998942150002">+998942150002</a>
        </div>
        <div class="contact">
          <img src="../assets/phone-call.png" alt="" class="icon" />
          <a href="tel:+998934526788">+998934526788</a>
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
