<template>
  <div class="footer-container d-flex justify-content-center">
    <div class="col-12 d-flex justify-content-between align-items-center px-5 py-5 flex-lg-row flex-column gap-5">
      <div class="name col-lg-2 col-10 text-center">
        <p class="style-text font-dancing px-1 h2">Annagaseh</p>
      </div>
      <div class="list-menu col-lg-6 col-12 fw-bold px-5 d-flex justify-content-center justify-content-lg-between">
        <ul class="d-flex justify-content-between flex-column flex-md-row w-100 align-items-center">
          <li v-for="(item, index) in listMenu" :key="index">
            <a :href="item.to">{{item.title}}</a>
          </li>
        </ul>
      </div>
      <div class="subscribe-form col-lg-2 uppercase d-flex d-flex d-lg-block justify-content-between align-items-center flex-column flex-md-row">
        <div class="subscribe-form__title fw-bold h5 pe-3 pe-lg-0">subscribe the newsletter</div>
        <div class="subscribe-form__input d-flex">
          <input type="text" class="form-control" placeholder="EMAIL" />
          <button>
            <Icon icon="ph:magnifying-glass-bold" style="color: white;" width="20" height="20"></Icon>
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { Icon } from "@iconify/vue";
const listMenu = [
  { title: "home", to: "#header" },
  { title: "about us", to: "#about" },
  { title: "Testimonials", to: "#testimonials" },
  { title: "service", to: "#service" },
  { title: "contact", to: "#contact" }
];
</script>

<style>
.list-menu ul li {
  list-style: disc !important;
  text-transform: uppercase;
}
.footer-container {
  background-color: var(--background-color-button);
  font-size: 0.9rem;
  cursor: pointer;
}
.subscribe-form__input button {
  background: linear-gradient(
    to bottom,
    var(--main-color-bland) 0%,
    var(--main-color-bold) 100%
  );
  color: white;
  padding: 10px;
  border-radius: 5px;
  box-shadow: none;
}
</style>