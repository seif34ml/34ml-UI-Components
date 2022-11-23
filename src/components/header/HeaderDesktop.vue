<template>
  <div
    class="relative header-desktop-container px-20 py-2 shadow-md items-center justify-between"
  >
    <LogoContainerImage :logo="getImgSrc" />
    <MenuDesktopContainer :menu="menu" :styleApply="styleApply" />
    <CartContainer :cart="cart" />
    <LocalizationContainer :languages="languages" />
  </div>
</template>

<script>
import MenuDesktopContainer from "./MenuDesktopContainer.vue";
import LogoContainerImage from "./LogoContainerImage.vue";
import CartContainer from "./CartContainer.vue";
import LocalizationContainer from "./LocalizationContainer.vue";
export default {
  name: "HeaderDesktop",
  props: {
    logo: String,
    menu: Array,
    styleApply: Boolean,
    cart: Object,
    languages: Object,
  },
  components: {
    LogoContainerImage,
    MenuDesktopContainer,
    CartContainer,
    LocalizationContainer,
  },
  computed: {
    getImgSrc() {
      return require("../../assets/" + this.logo);
    },
  },
};
</script>

<style></style>
