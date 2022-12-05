<template>
  <div id="header" class="header d-flex align-items-center px-2 py-4 py-2 py-sm-5">
    <div class="row w-100">
      <div class="top-bar__name col-6 font-dancing">
        <p class="style-text px-2 px-sm-5 h1">Annagaseh</p>
      </div>
      <div class="col-6 top-bar__link d-none d-sm-flex justify-content-lg-center justify-content-end align-items-center">
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
    </div>
  </div>
</template>

<script>
export default {};
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
</style>