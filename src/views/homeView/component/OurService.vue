<template>
  <div id="service" class="service-container d-flex justify-content-center align-items-center flex-column pb-5 mb-5 uppercase">
    <div class="service-container__title style-text font-dancing h1">
      <p>our service</p>
    </div>
    <div class="service-container__content col-lg-6 col-8 text-center">
      <p>stage makeup is used as a mathod in conjunction with stage light to highlight moderate distances.</p>
    </div>
    <div class="list-service col-10 d-flex flex-lg-row flex-column justify-content-between align-items-center position-relative gap-2 py-4">

      <div v-for="(service, index) in listService" :key="index" class="service-item mx-2 p-4 col-10 col-lg-3 d-flex justify-content-center align-items-center flex-column" :class="{'service-item-center': (index === 1)}">
        <div class="service-item__img">
          <img class="rounded-circle" :src="service.image" alt />
        </div>
        <div class="service-item__title font-dancing h3 px-1 style-text">{{service.name}}</div>
        <div
          class="service-item__dess text-lg-justify text-center"
        >{{service.dess}}</div>
        <div class="read-more style-text mt-2 d-flex align-items-center">read more <Icon icon="material-symbols:navigate-next"></Icon></div>
      </div>

      <div class="background d-none d-lg-block"></div>
    </div>
  </div>
</template>

<script setup>
import img5 from "../../../assets/img/img-5.jpg"
import img6 from "../../../assets/img/img-6.jpg"
import img7 from "../../../assets/img/img-7.jpg"
import { Icon } from "@iconify/vue";


const listService = [
  { image: img5,
    name: "makeup hairstyle",
    dess: "the use of special effects techniques enhancing physical features to exhibit well as fantasy makeup"
  }, 
  { image: img6,
    name: "shooting",
    dess: "stage makeup is used as a method in conjunction with stage lighting to highlight the actors faces"
  }, 
  { image: img7,
    name: "event makeup",
    dess: "the use of special effects techniques enhancing physical features to exhibit well as fantasy makeup"
  },
]
</script>

<style>
.background {
    position: absolute;
    height: 280px;
    width: 100%;
    border-radius: 10px;
    background: #fff;
    box-shadow: 2px 2px 10px #fecdcd, -2px -2px 10px #fecdcd;
    bottom: 0;
}
.service-container__title {
  font-size: 5rem;
  padding-left: 3px;
}
.service-container__content {
  color: var(--text-color-bland);
}
.service-item {
  font-size: 0.8rem;
  z-index: 10;
  gap: 10px
}
.service-item-center {
  background-color: var(--background-color-button);
  border-radius: 5px;
  box-shadow: 2px 2px 10px #f1dfdf, -2px -2px 10px #f1dfdf;
}
.service-item__img img {
  width: 150px;
  border-radius: 50%;
  border: 3px solid #fff;
}
.service-item__dess {
  color: var(--text-color-bland);
}
</style>