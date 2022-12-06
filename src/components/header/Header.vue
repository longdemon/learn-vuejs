<template>
  <div id="header" class="header d-flex align-items-center px-2 py-4 py-2 py-sm-5">
    <div class="row w-100 align-items-center">
      <div class="top-bar__name col-6 font-dancing">
        <p class="style-text px-2 px-sm-5 h1">Annagaseh</p>
      </div>
      <div
        class="col-6 top-bar__link d-none d-lg-flex justify-content-lg-center justify-content-end align-items-center"
      >
        <ul class="d-lg-flex d-none">
          <li class="active py-2 px-3 fw-bold">
            <a>HOME</a>
          </li>
          <li class="py-2 px-3 fw-bold">
            <a>ABOUT</a>
          </li>
          <li class="py-2 px-3 fw-bold">
            <a>SERVICE</a>
          </li>
          <li class="py-2 px-3 fw-bold">
            <a>TESTIMONIALS</a>
          </li>
          <li class="py-2 px-3 fw-bold">
            <a>CONTACT</a>
          </li>
        </ul>
        <button class="ms-4">
          <p class="style-text">APPOINTMENT</p>
        </button>
      </div>
      <div class="col-6 toggle d-block d-lg-none">
        <div class="d-flex justify-content-end">
          <Icon icon="fontisto:nav-icon-a" @click="(isShowSideBar = !isShowSideBar)"></Icon>
        </div>
      </div>

      <div
        class="side-bar d-flex justify-content-between position-fixed top-0 vh-100 w-75"
        :class="{'side-bar__show': isShowSideBar}"
      >
        <div class="mt-2">
          <ul class="d-flex flex-column">
            <li class="active py-4 px-3 fw-bold">
              <a href="#header">HOME</a>
            </li>
            <li class="py-4 px-3 fw-bold">
              <a href="#about">ABOUT</a>
            </li>
            <li class="py-4 px-3 fw-bold">
              <a href="#service">SERVICE</a>
            </li>
            <li class="py-4 px-3 fw-bold">
              <a href="#testimonials">TESTIMONIALS</a>
            </li>
            <li class="py-4 px-3 fw-bold">
              <a href="#contact">CONTACT</a>
            </li>
          </ul>
          <button class="mt-4">
            <p class="style-text">APPOINTMENT</p>
          </button>
        </div>
        <button class="close-btn mt-3">
          <Icon
            icon="material-symbols:close-rounded"
            @click="(isShowSideBar = !isShowSideBar)"
            width="30"
            height="30"
          ></Icon>
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
import { Icon } from "@iconify/vue";
import { ref } from "vue";
const isShowSideBar = ref(false);
</script>

<style>
.header {
  height: 15vh !important;
}
.top-bar__link li {
  font-size: 0.8rem;
  cursor: pointer;
}
.active {
  color: var(--main-color-text);
}
.side-bar {
  background: linear-gradient(
    to right,
    var(--background-color) 30%,
    var(--background-color-50)
  );
  z-index: 100;
  left: -100%;
  transition: 0.5s;
}
.side-bar__show {
  left: 0;
}
.close-btn {
  height: 50px;
  width: 50px;
  background-color: transparent;
}
</style>