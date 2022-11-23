<template>
  <div
    class="header-mobile-container justify-between items-center bg-white px-8 py-8 shadow-md relative"
  >
    <MobileMenuContainer
      :menu="menu"
      :burgerIcon="getIconSrc"
      :languages="languages"
    >
      <LogoContainerImage :logo="getImgSrc" />
    </MobileMenuContainer>
    <LogoContainerImage :logo="getImgSrc" />

    <CartContainer :cart="cart" />
  </div>
</template>

<script>
import LogoContainerImage from "./LogoContainerImage.vue";
import MobileMenuContainer from "../MobileMenuContainer.vue";
import CartContainer from "./CartContainer.vue";
export default {
  name: "HeaderMobile",
  components: { LogoContainerImage, MobileMenuContainer, CartContainer },
  props: {
    logo: String,
    menu: Array,
    styleApply: Boolean,
    cart: Object,
    languages: Object,
    burgerIcon: String,
  },
  computed: {
    getImgSrc() {
      return require("../../assets/" + this.logo);
    },
    getIconSrc() {
      return require("../../assets/" + this.burgerIcon);
    },
  },
};
</script>

<style></style>
