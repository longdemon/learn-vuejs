<template>
  <div id="contact" class="contact-container d-flex justify-content-center align-items-center flex-column vh-lg-100 vh-50 py-5">
    <div class="contact-title style-text font-dancing h1 px-1">Contact us</div>
    <div
      class="contact-dess col-lg-4 col-10 mb-5 text-center"
    >Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolores rem commodi obcaecati corrupti! Numquam rem cupiditate odit beatae aliquid. Molestias blanditiis sit, eaque error quibusdam molestiae repellendus? Molestiae, fugit deleniti.</div>
    <div class="contact-body d-flex gap-5 col-lg-8 col-10 justify-content-between flex-lg-row flex-column">
      <div class="contact-body__info d-flex flex-lg-column flex-md-row flex-column col-lg-5 gap-4 col-12">
        <div v-for="(contact,index) in listContact" :key="index" class="d-flex gap-2 align-items-center ms-lg-5 ms-0 flex-lg-row flex-column col-12 col-md-4 col-lg-12 justify-content-center justify-content-lg-start">
          <div class="infor__icon__wrapper rounded-circle d-flex justify-content-center align-items-center">
            <Icon class="info__icon" :icon="contact.icon"></Icon>
          </div>
          <div class="info__content">
            <p class="fw-bold uppercase d-flex d-lg-block justify-content-center">{{contact.title}}</p>
            <span>{{contact.dess}}</span>
          </div>
        </div>
      </div>
      <div class="contact-body__form col-lg-7 col-12">
        <div class="contact-body__input gap-2">
          <input type="text" class="form-control py-3" placeholder="First name" />
          <input type="text" class="form-control py-3" placeholder="Last name" />
          <input type="text" class="form-control py-3" placeholder="Email" />
          <input type="text" class="form-control py-3" placeholder="Phone" />
          <input type="text" class="form-control py-3" placeholder="Subject" />
          <input type="text" class="form-control py-3" placeholder="Reason for contact" />
          <textarea name id cols="30" rows="5" class="form-control py-3" placeholder="message"></textarea>
        </div>
        <div class="contact-body__btn text-end text-lg-start">
          <button class="py-lg-2 px-5 py-3 fw-bold text-light mt-2">
            Submit
            <Icon icon="material-symbols:navigate-next" style="color: white;" width="25" height="25"></Icon>
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { Icon } from "@iconify/vue";
const listContact = [
  {
    title: "address",
    dess: "Lugui Cazzavillan, no 20, Bucharest",
    icon: "mdi:address-marker"
  },
  {
    title: "phone",
    dess: "0932193099",
    icon: "material-symbols:phone-enabled"
  },
  {
    title: "email",
    dess: "email@gmail.com",
    icon: "ic:baseline-email"
  },
]
</script>

<style>
.contact-container{
  min-height: 700px;
}
.infor__icon__wrapper {
  min-height: 70px;
  min-width: 70px;
  border: 2px solid #906c41;
}
.info__icon {
  color: #906c41;
  width: 40px;
  height: 40px;
}

.info__content span {
  color: var(--text-color-bland);
  font-size: 0.9rem;
}
.contact-body__input {
  display: grid;
  grid-template-columns: auto auto;
  gap: 5px;
}
.contact-body__input textarea {
  grid-column-start: 1;
  grid-column-end: 3;
  resize: none;
}
.contact-body__btn button {
  background: linear-gradient(
    to right,
    var(--main-color-bland) 0%,
    var(--main-color-bold) 100%
  );
}
</style>