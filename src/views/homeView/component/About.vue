<template>
  <div id="about" class="about-container d-flex justify-content-center align-items-center vh-md-100 p-5 p-lg-0">
    <div class="d-flex flex-lg-row flex-column">
      <div class="about-container__img h-100 d-flex justify-content-center align-items-center col-lg-6 col-12">
        <img class="rounded-circle p-2" :src="img4" alt />
      </div>
      <div class="about-container__content d-flex flex-column align-items-center align-items-lg-start justify-content-center col-lg-6 col-12 gap-4 gap-lg-0">
        <div class="about-container__title style-text font-dancing h1 px-1 pt-4 p-lg-0">
          <p>About us</p>
        </div>
        <div class="about-container__dess col-8 uppercase text-justify">
          <p>
            fashion makeup is used in magazine photography as well as on the
            fashion runway. Avant-garde makeup is also an aoolicable technique
            user for projects that require experimantal themes. Fashion makeup
            is also commonly used in television and film ranging for the natural
            prime look to more sophisticated applications
          </p>
        </div>
        <button class="mt-4">
          <p class="style-text">make appointment</p>
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
import img4 from "../../../assets/img/img-4.png"
</script>

<style>
.about-container{
  min-height: 700px;
}
.about-container__img img {
  width: 450px;
  height: 450px;
  border: 6px solid var(--main-color-bland);
}
.about-container__dess{
    color: var(--text-color-bland)
}
.about-container__content button {
  margin-top: 2rem;
}
</style>