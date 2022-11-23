<template>
  <div class="relative header-desktop-container-cart">
    <a :href="cart.url">
      <img :src="require('../../assets/' + cart.image)" alt="cart icon" />
    </a>
    <p
      class="text-white rounded-full ltr:font-montserrat-bold rtl:font-tajawal-bold text-center bg-primary absolute -top-1/2 left-full"
    >
      {{ cart.count }}
    </p>
  </div>
</template>

<script>
export default {
  name: "CartContainer",
  props: { cart: Object },
};
</script>

<style></style>
