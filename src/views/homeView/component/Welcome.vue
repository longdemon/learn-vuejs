<template>
  <div class="welcome-container position-relative">
    <div
      class="welcome-container__background d-flex justify-content-lg-center justify-content-start align-items-center position-absolute h-100 col-12 col-lg-6 uppercase fw-bold px-5 ps-lg-0"
    >
      <div class="welcome-container__content">
        <p class="text-welcome h4">welcome to</p>
        <p class="welcome-container__name style-text px-1 font-dancing">Annagaseh</p>
        <p class="welcome-container__dess h3">hair and makeup artist</p>
        <button class="mt-1 mt-lg-4">
          <p class="style-text">make appointent</p>
        </button>
      </div>
    </div>
    <div id="myCarousel" class="carousel slide" data-bs-ride="carousel">
      <ol class="carousel-indicators">
        <li data-bs-target="#myCarousel" data-bs-slide-to="0" class="active"></li>
        <li data-bs-target="#myCarousel" data-bs-slide-to="1"></li>
      </ol>
      <div class="carousel-inner">
        <div class="carousel-item active">
          <img class="bgr-img d-block w-100" :src="img1" alt="First slide" />
        </div>
        <div class="carousel-item">
          <img class="bgr-img d-block w-100" :src="img2" alt="Second slide" />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import img1 from "../../../assets/img/img-1.jpg";
import img2 from "../../../assets/img/img-2.jpg";
</script>

<style>
.welcome-container {
  /* min-height: 500px; */
}
.carousel-indicators li {
  border-radius: 50%;
  height: 10px !important;
  width: 10px !important;
}
.carousel-inner {
  max-height: 85vh;
  /* min-height: 500px; */
}
.carousel {
  max-height: 100%;
}
.welcome-container__background {
  background-image: linear-gradient(
    to right,
    var(--background-color) 30%,
    transparent
  );
  z-index: 2;
}
.welcome-container__name {
  font-size: 5rem;
}

@media (max-width: 992px) {
  .welcome-container__name {
    font-size: 3rem;
  }
  .text-welcome{
    font-size: 1rem !important;
  }
  .welcome-container__dess{
    font-size: 1.2rem !important;
  }
}



</style>