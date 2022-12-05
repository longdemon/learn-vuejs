<template>
  <div id="testimonials" class="testimonials-container d-flex justify-content-center align-items-center flex-column vh-50 vh-lg-100">
    <div class="testimonials-title style-text font-dancing h2 px-1">What Our Customers Say</div>
    <div id="testimonialsCarousel" class="carousel slide" data-bs-ride="carousel">
      <ol class="carousel-indicators carousel-position">
        <li data-bs-target="#testimonialsCarousel" data-bs-slide-to="0" class="active"></li>
        <li data-bs-target="#testimonialsCarousel" data-bs-slide-to="1"></li>
      </ol>
      <div class="carousel-inner">
        <div
          v-for="(cus,index) in listCustomer"
          :key="index"
          class="carousel-item"
          :class="{active: index === 0}"
        >
          <div
            class="testimonials-content m-auto pt-3 pb-5 position-relative d-flex justify-content-center align-items-center flex-column col-10 gap-4"
          >
            <div class="customer-avt">
              <img :src="cus.avt" alt />
            </div>
            <div class="customer-review text-center col-8">
              <p>"{{cus.comment}}"</p>
            </div>
            <div class="customer-name">
              <p class="style-text font-dancing h3">{{cus.name}}</p>
            </div>
            <div class="background col-10">
              <div class="border-in-background"></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import img8 from "../../../assets/img/img-8.jpg";
import img9 from "../../../assets/img/img-9.jpg";

const listCustomer = [
  {
    avt: img8,
    comment:
      "It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout. The point of using Lorem Ipsum is that it has a more-or-less normal distribution of letters, as opposed to using 'Content here, content here', making it look like readable English",
    name: "Nguyen Nhu Ly"
  },

  {
    avt: img9,
    comment:
      "It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout. The point of using Lorem Ipsum is that it has a more-or-less normal distribution of letters, as opposed to using 'Content here, content here', making it look like readable English",
    name: "Pham Thi Minh Phuong"
  }
];
</script>

<style scoped>
.testimonials-container {
  background-color: var(--background-color-button);
  min-height: 700px;
}
.testimonialsCarousel{
  height: 700px;
}
.customer-avt,
.customer-review,
.customer-name {
  z-index: 3;
}
.customer-avt img {
  width: 150px;
  border-radius: 20px;
  border: 5px solid #fff;
}
.customer-review {
  color: var(--text-color-bland);
}
.background {
  position: absolute;
  height: 75%;
  border-radius: 10px;
  background: #fff;
  box-shadow: 2px 2px 10px rgb(166, 166, 166), -2px -2px 10px rgb(166, 166, 166);
  bottom: 10px;
  padding: 20px;
}
.border-in-background {
  height: 100%;
  width: 100%;
  border-radius: 10px;
  border: 2px solid rgb(166, 166, 166);
}
.carousel-position {
  position: absolute;
  bottom: -70px;
}

@media (max-width: 992px) {
  .customer-name p {
    font-size: 1rem !important;
  }
}
</style>